---
hidden: true
---

# API FGV

### 1. Autenticação

Todas as requisições exigem a passagem de tokens de segurança no cabeçalho (Header).

| **Header**            | **Tipo** | **Obrigatório** | **Descrição**                                             |
| --------------------- | -------- | --------------- | --------------------------------------------------------- |
| `Authorization-Token` | String   | Sim             | Token obtido nas configurações do evento (FGV ou UNICAP). |
| `Authorization-App`   | String   | Sim             | Token fixo de identificação da aplicação autorizada.      |

***

### 2. Endpoints

#### 2.1. Retornar dados customizados (Geral)

Retorna uma estrutura completa com dados de eventos, participantes e logs de LGPD.

* URL: `/api/v1/custom/getdata`
* Método: `POST`

**Parâmetros do Corpo (JSON)**

| **Campo**    | **Tipo**     | **Descrição**                                     |
| ------------ | ------------ | ------------------------------------------------- |
| `dataInicio` | String (ISO) | Data inicial (AAAA-MM-DD). Padrão: 30 dias atrás. |
| `dataFim`    | String (ISO) | Data final (AAAA-MM-DD). Padrão: Amanhã.          |

**Exemplo de Resposta (200 OK)**

```
{
  "data": [
    {
      "evento.id": 1,
      "evento.titulo_evento": "Nome do Evento",
      "evento.data": "2024-12-22T00:00:00",
      "evento.hora_inicio": "08:00:00",
      "evento.hora_fim": "18:00:00",
      "evento.link_do_evento": "https://www.even3.com.br/exemplo",
      "evento.unidade_do_evento": "Unidade Exemplo",
      "evento.sistema_origem": "EVEN3",
      "evento.tipo_evento": "COD_TIPO",
      "evento.classificacao_evento": "COD_CLASS",
      "evento.quantidade_webminars": "5",
      "participantes": [
        {
          "participante.nome": "Nome do Participante",
          "participante.email": "email@provedor.com",
          "participante.cpf": "000.000.000-00",
          "participante.telefone.ddi": "+55",
          "participante.telefone.ddd": "",
          "participante.telefone.numero": "999999999",
          "participante.estado": "Pernambuco",
          "participante.cidade": "Recife",
          "participante.cargo_profissao": "Analista",
          "participante.data_de_nascimento": "1990-01-01T00:00:00",
          "participante.genero": "M",
          "participante.area_de_atuacao": "Tecnologia",
          "inscricao.data_inscricao": "2024-12-20T14:30:00",
          "inscricao.entrada": "Ingresso VIP",
          "lgpd.ip": "189.0.0.1",
          "lgpd.data_hora_envio": "2024-12-20T14:30:05",
          "lgpd.aceite_termos_divulgacoes": true,
          "lgpd.desejo_receber_informacoes_abaixo": [
            {
              "titulo": "Cursos de Extensão",
              "codigo": "0",
              "aceite": 1
            }
          ],
          "lgpd.como_gostaria_receber_informacoes": [
            {
              "titulo": "E-mail",
              "codigo": "0",
              "aceite": 1
            }
          ]
        }
      ]
    }
  ]
}
```

***

#### 2.2. Retornar participantes inscritos

Retorna uma lista simplificada focada no status da inscrição e contatos básicos.

* URL: `/api/v1/custom/getdatasubscribed`
* Método: `POST`

**Parâmetros do Corpo (JSON)**

| **Campo**    | **Tipo**     | **Descrição**                                  |
| ------------ | ------------ | ---------------------------------------------- |
| `dataInicio` | String (ISO) | Início do período de confirmação da inscrição. |
| `dataFim`    | String (ISO) | Fim do período de confirmação da inscrição.    |

**Exemplo de Resposta (200 OK)**

```
{
  "data": [
    {
      "evento.id": 1,
      "evento.titulo_evento": "Nome do Evento",
      "evento.data": "2024-12-22T00:00:00",
      "evento.hora_inicio": "08:00:00",
      "evento.data_fim": "2024-12-23T00:00:00",
      "evento.hora_fim": "18:00:00",
      "evento.link_do_evento": "https://www.even3.com.br/exemplo",
      "evento.comissao.organizadora.nome": "Nome do Organizador",
      "evento.comissao.organizadora.email": "contato@evento.com",
      "participantes": [
        {
          "participante.id": 99,
          "participante.nome": "Nome do Participante",
          "participante.email": "email@provedor.com",
          "participante.genero": "F",
          "participante.data_de_nascimento": "1995-05-10T00:00:00",
          "participante.estado": "São Paulo",
          "participante.cidade": "São Paulo",
          "participante.cargo_profissao": "Estudante",
          "participante.area_de_atuacao": "Direito",
          "inscricao.numero": 12345,
          "inscricao.data_inscricao": "2024-12-21T09:00:00"
        }
      ]
    }
  ]
}
```

***

### 3. Tabela de Erros

A API retorna os seguintes erros baseados no status HTTP:

| **Status** | **Código do Erro**          | **Descrição**                                                            |
| ---------- | --------------------------- | ------------------------------------------------------------------------ |
| 401        | `InvalidAuthorizationApp`   | O header `Authorization-App` é inválido ou nulo.                         |
| 401        | `InvalidAuthorizationToken` | O token do cliente é inválido ou não autorizado para esta rota.          |
| 502        | `InvalidParameter`          | Corpo da requisição vazio ou intervalo de datas inválido (Regra UNICAP). |
| 500        | `InternalServerError`       | Erro inesperado no servidor ou na execução da função SQL.                |

***

> Nota: Datas devem seguir preferencialmente o formato `YYYY-MM-DD`. O sistema realiza o cast interno para `00:00:00` no início e `23:59:59` no fim do período.
