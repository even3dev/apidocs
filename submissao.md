# 📜 Submissão

## Retorna as modalidades e áreas temáticas de submissão

<mark style="color:blue;">`GET`</mark> `https://www.even3.com.br/api/v1/submission/`

Retorna as modalidades e áreas temáticas do evento

#### Headers

| Name                                                  | Type   | Description                                                  |
| ----------------------------------------------------- | ------ | ------------------------------------------------------------ |
| Authorization-Token<mark style="color:red;">\*</mark> | string | Token de autenticação obtido nas configurações do evento.Re{ |

{% tabs %}
{% tab title="200 " %}
```javascript
  "submission_type": {
    "data": [
      {
        "id_event": 37524,
        "id_submissiontype": 29631,
        "url_roles": "https://even3.blob.core.windows.net/geral/Template-para-Trabalhos-completos-CONINTER-em-18.09.2019.d825047b7c5947b290df.docx",
        "title": "Regras de submissão de Article"
      },
      {
        "id_event": 37524,
        "id_submissiontype": 29635,
        "url_roles": "",
        "title": "Rules for submission of {{name}}"
      }
    ],
    "count": 2
  },
  "topic_area": {
    "data": [
      {
        "id_event": 37524,
        "id_topicarea": 30747,
        "title": "Tecnologías y Servicios de Acceso a la Información y la Comunicación"
      },
      {
        "id_event": 37524,
        "id_topicarea": 30749,
        "title": "Interacción persona máquina"
      },
      {
        "id_event": 37524,
        "id_topicarea": 30750,
        "title": "Teleasistencia y Telecuidado: Prolongación de la vida activa"
      },
      {
        "id_event": 37524,
        "id_topicarea": 30751,
        "title": "Smart City"
      },
      {
        "id_event": 37524,
        "id_topicarea": 30752,
        "title": "Aprendizaje y colaboración accesibles"
      }
    ],
    "count": 5
  },
  "count": 2
}
```
{% endtab %}

{% tab title="404 " %}
```javascript
{
  "Message": "No HTTP resource was found that matches the request URI 'https://www.even3.com.br/api/v1/submission/29631'."
}
```
{% endtab %}
{% endtabs %}

## Retorna detalhes das submissões e apresentações de trabalho do seu evento

<mark style="color:blue;">`GET`</mark> `https://www.even3.com.br/api/v1/submission/list`

Retorna os detalhes das submissões e apresentações de trabalho do evento

#### Headers

| Name                                                  | Type   | Description                                                  |
| ----------------------------------------------------- | ------ | ------------------------------------------------------------ |
| Authorization-Token<mark style="color:red;">\*</mark> | string | Token de autenticação obtido nas configurações do evento.Re{ |

{% tabs %}
{% tab title="200 " %}
```javascript
{
    "submission": {
        "data": [
            {
                "id_event": 1234,
                "id_submission": 567,
                "title": "Teste Submissão",
                "status": "Aprovado",
                "id_submission_type": 123,
                "submission_type": "Resumo",
                "topic_area": "Exemplo de Área Temática",
                "id_topic_area": 456,
                "abstract": "https://static.even3.com/processos/322312bac4a4ad081e2.pdf",
                "proceedings_abstract": "https://static.even3.com/anais/02340.pdf",
                "proceedings_full_paper": "https://static.even3.com/processos/02340.pdf",
                "date": "2026-05-16T10:00:00",
                "start_time": "10:02",
                "end_time": "10:04",
                "location": null,
                "author": [
                    {
                        "id_event": 1234,
                        "id_submission": 567,
                        "name": "João Pedro",
                        "email": "joao@gmail.com",
                        "is_presenter": false,
                        "author_order": 1
                    }
                ]
            }
        ],
        "count": 1
    },
    "count": 1
}
```
{% endtab %}
{% endtabs %}
