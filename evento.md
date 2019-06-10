# Evento

{% api-method method="get" host="https://www.even3.com.br" path="/api/v1/event" %}
{% api-method-summary %}
Retornar dados do evento
{% endapi-method-summary %}

{% api-method-description %}
Este endpoint retorna todas as informações sobre o seu evento
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization-Token" type="string" required=true %}
Token de autenticação encontrado nas configurações do evento
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
   {
    "data": [
        {
            "id_event": 1,
            "title": "XV Congresso de Ciência do Desporto e Educação Física dos Países de Língua Portuguesa",
            "url": "cdef2014",
            "start_date": "2014-04-13T00:00:00",
            "end_date": "2014-06-03T00:00:00",
            "start_date_registration": "28/11/2013",
            "end_date_registration": "31/03/2014",
            "summary": "O XV Congresso de Educação Física e Ciência do Desporto dos Países de Língua Portuguesa é um evento internacional de âmbito científico e acadêmico. Esta edição tem como Tema: O Desporto e a bola do mundo: Sociedade, Inovação e Tecnologia.",
            "description": null,
            "url_image": "https://images.even3.com.br/P8AIZhrnXjYyZbzpMl_YguQPDnM=/fit-in/250x250/smart/https://even3.blob.core.windows.net/idvisual/cdef.png",
            "credit_hour": 0,
            "country": "Brasil",
            "state": "Pernambuco",
            "city": "Recife",
            "venue": "Mar Hotel",
            "latitude": "-8.0475622",
            "longitude": "-34.8769643",
            "banner": null,
            "tickets": [
                {
                    "title": "Profissional",
                    "prices": [
                        {
                            "id_ticket": 2,
                            "id_ticket_price": 2,
                            "price": 370,
                            "due_date": "2013-12-16T00:00:00"
                        },
                        {
                            "id_ticket": 2,
                            "id_ticket_price": 3,
                            "price": 390,
                            "due_date": "2014-01-16T00:00:00"
                        },
                        {
                            "id_ticket": 2,
                            "id_ticket_price": 4,
                            "price": 400,
                            "due_date": "2014-03-01T00:00:00"
                        },
                        {
                            "id_ticket": 2,
                            "id_ticket_price": 5,
                            "price": 420,
                            "due_date": "2014-04-03T00:00:00"
                        }
                    ]
                },
                {
                    "title": "Estudante de Graduação",
                    "prices": [
                        {
                            "id_ticket": 3,
                            "id_ticket_price": 6,
                            "price": 160,
                            "due_date": "2013-12-16T00:00:00"
                        },
                        {
                            "id_ticket": 3,
                            "id_ticket_price": 7,
                            "price": 190,
                            "due_date": "2014-01-16T00:00:00"
                        },
                        {
                            "id_ticket": 3,
                            "id_ticket_price": 8,
                            "price": 230,
                            "due_date": "2014-03-01T00:00:00"
                        },
                        {
                            "id_ticket": 3,
                            "id_ticket_price": 9,
                            "price": 260,
                            "due_date": "2014-04-03T00:00:00"
                        }
                    ]
                },
                {
                    "title": "Profissional (Autor)",
                    "prices": [
                        {
                            "id_ticket": 4,
                            "id_ticket_price": 11,
                            "price": 370,
                            "due_date": "2013-12-16T00:00:00"
                        },
                        {
                            "id_ticket": 4,
                            "id_ticket_price": 12,
                            "price": 370,
                            "due_date": "2014-01-16T00:00:00"
                        },
                        {
                            "id_ticket": 4,
                            "id_ticket_price": 13,
                            "price": 370,
                            "due_date": "2014-03-01T00:00:00"
                        },
                        {
                            "id_ticket": 4,
                            "id_ticket_price": 10,
                            "price": 370,
                            "due_date": "2014-04-03T00:00:00"
                        }
                    ]
                },
                {
                    "title": "Estudante de Graduação (Autor)",
                    "prices": [
                        {
                            "id_ticket": 5,
                            "id_ticket_price": 14,
                            "price": 160,
                            "due_date": "2013-12-16T00:00:00"
                        },
                        {
                            "id_ticket": 5,
                            "id_ticket_price": 15,
                            "price": 160,
                            "due_date": "2014-01-16T00:00:00"
                        },
                        {
                            "id_ticket": 5,
                            "id_ticket_price": 16,
                            "price": 160,
                            "due_date": "2014-03-01T00:00:00"
                        },
                        {
                            "id_ticket": 5,
                            "id_ticket_price": 17,
                            "price": 160,
                            "due_date": "2014-04-03T00:00:00"
                        }
                    ]
                }
            ]
        }
    ],
    "count": 1
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Não foi possível encontrar os dados do evento
{% endapi-method-response-example-description %}

```javascript
{   
    "message": "string",
    "erros": [
        {
            "code": int,
            "description": "string"
        }
    ],
    "count_erros": 1
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



