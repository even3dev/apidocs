# 💙 Evento



## Retornar dados do evento

<mark style="color:blue;">`GET`</mark> `https://www.even3.com.br/api/v1/event`

Este endpoint retorna todas as informações sobre o seu evento

#### Headers

| Name                                                  | Type   | Description                                                  |
| ----------------------------------------------------- | ------ | ------------------------------------------------------------ |
| Authorization-Token<mark style="color:red;">\*</mark> | string | Token de autenticação encontrado nas configurações do evento |

{% tabs %}
{% tab title="200 " %}
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
                    "registration_quantity": 4
                    "prices": [
                        {
                            "id_ticket": 2,
                            "id_ticket_price": 2,
                            "price": 370,
                            "start_date": "2014-01-09T00:00:00",
                            "due_date": "2014-01-10T00:00:00",
                            "registration_quantity_price": 1
                        },
                        {
                            "id_ticket": 2,
                            "id_ticket_price": 3,
                            "price": 390,
                            "start_date": "2014-01-10T00:00:00",
                            "due_date": "2014-01-16T00:00:00",
                            "registration_quantity_price": 1
                        },
                        {
                            "id_ticket": 2,
                            "id_ticket_price": 4,
                            "price": 400,
                            "start_date": "2014-03-01T00:00:00",
                            "due_date": "2014-03-01T00:00:00",
                            "registration_quantity_price": 1
                        },
                        {
                            "id_ticket": 2,
                            "id_ticket_price": 5,
                            "price": 420,
                            "start_date": "2014-04-03T00:00:00",
                            "due_date": "2014-04-03T00:00:00",
                            "registration_quantity_price": 1
                        }
                    ]
                },
                {
                    "title": "Estudante de Graduação",
                    "registration_quantity": 1
                    "prices": [
                        {
                            "id_ticket": 3,
                            "id_ticket_price": 6,
                            "price": 160,
                            "start_date": "2013-12-15T00:00:00",
                            "due_date": "2013-12-16T00:00:00",
                            "registration_quantity_price": 1
                        },
                        {
                            "id_ticket": 3,
                            "id_ticket_price": 7,
                            "price": 190,
                            "start_date": "2014-01-16T00:00:00",
                            "due_date": "2014-01-16T00:00:00",
                            "registration_quantity_price": 0
                        },
                        {
                            "id_ticket": 3,
                            "id_ticket_price": 8,
                            "price": 230,
                            "start_date": "2014-03-01T00:00:00",
                            "due_date": "2014-03-01T00:00:00",
                            "registration_quantity_price": 0
                        },
                        {
                            "id_ticket": 3,
                            "id_ticket_price": 9,
                            "price": 260,
                            "start_date": "2014-04-03T00:00:00",
                            "due_date": "2014-04-03T00:00:00",
                            "registration_quantity_price": 0
                        }
                    ]
                },
                {
                    "title": "Profissional (Autor)",
                    "registration_quantity": 0
                    "prices": [
                        {
                            "id_ticket": 4,
                            "id_ticket_price": 11,
                            "price": 370,
                            "start_date": "2014-01-16T00:00:00",
                            "due_date": "2013-12-16T00:00:00",
                            "registration_quantity_price": 0
                        },
                        {
                            "id_ticket": 4,
                            "id_ticket_price": 12,
                            "price": 370,
                            "start_date": "2014-01-16T00:00:00",
                            "due_date": "2014-01-16T00:00:00",
                            "registration_quantity_price": 0
                        },
                        {
                            "id_ticket": 4,
                            "id_ticket_price": 13,
                            "price": 370,
                            "start_date": "2014-03-01T00:00:00",
                            "due_date": "2014-03-01T00:00:00",
                            "registration_quantity_price": 0
                        },
                        {
                            "id_ticket": 4,
                            "id_ticket_price": 10,
                            "price": 370,
                            "start_date": "2013-08-27T00:00:00",
                            "due_date": "2014-04-03T00:00:00",
                            "registration_quantity_price": 0
                        }
                    ]
                },
                {
                    "title": "Estudante de Graduação (Autor)",
                    "registration_quantity": 2
                    "prices": [
                        {
                            "id_ticket": 5,
                            "id_ticket_price": 14,
                            "price": 160,
                            "start_date": "2014-01-12T00:00:00",
                            "due_date": "2013-12-16T00:00:00",
                            "registration_quantity_price": 1
                        },
                        {
                            "id_ticket": 5,
                            "id_ticket_price": 15,
                            "price": 160,
                            "start_date": "2014-01-14T00:00:00",
                            "due_date": "2014-01-16T00:00:00",
                            "registration_quantity_price": 1
                        },
                        {
                            "id_ticket": 5,
                            "id_ticket_price": 16,
                            "price": 160,
                            "start_date": "2014-01-03T00:00:00",
                            "due_date": "2014-03-01T00:00:00",
                            "registration_quantity_price": 0
                        },
                        {
                            "id_ticket": 5,
                            "id_ticket_price": 17,
                            "price": 160,
                            "start_date": "2014-04-03T00:00:00",
                            "due_date": "2014-04-03T00:00:00",
                            "registration_quantity_price": 0
                        }
                    ]
                }
            ]
        }
    ],
    "count": 1
}
```
{% endtab %}

{% tab title="404 " %}
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
{% endtab %}
{% endtabs %}
