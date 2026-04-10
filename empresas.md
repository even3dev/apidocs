# 🏦 Empresas

## Retorna lista de eventos da empresa

<mark style="color:blue;">`GET`</mark> `https://www.even3.com.br/api/v1/customclient/events`

Retorna a lista de eventos do plano empresarial. É necessário solicitar as informações de autenticação ao suporte

#### Headers

| Name                                                  | Type   | Description          |
| ----------------------------------------------------- | ------ | -------------------- |
| Authorization-Token<mark style="color:red;">\*</mark> | string | Solicitar ao suporte |
| Authorization-App<mark style="color:red;">\*</mark>   | string | Solicitar ao suporte |

{% tabs %}
{% tab title="200 " %}
```javascript
{
  "data": [
    {
      "id": 1,
      "titulo": "Evento teste 1",
      "url": "urleventoTeste",
      "token": "123456789",
      "email_organizador": "apiempresas@even3.com",
      "start_date": "2024-01-01",
      "start_time": "19:00",
      "end_date": "2024-02-01",
      "end_time": "21:30",
      "local": "Centro de Convenções de Pernambuco",
      "city":"Recife",
      "state":"Pernambuco",
      "country":"Brasil",
      "publicated": true,
      "privacy": {
        "data": [
          {
            "id": 2,
            "type": "Privado - com link de acessso"
          }
        ]
      }
     }
  ]
}
```
{% endtab %}
{% endtabs %}
