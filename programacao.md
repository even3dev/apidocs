# Programação

{% swagger baseUrl="https://www.even3.com.br" path="/api/v1/session/:id" method="get" summary="Retorna as atividades" %}
{% swagger-description %}
Retorne a lista de atividades do evento ou uma única atividade
{% endswagger-description %}

{% swagger-parameter name="id" type="string" in="path" %}
ID de uma atividade específica (opcional)
{% endswagger-parameter %}

{% swagger-parameter name="Authorization-Token" type="string" required="true" in="header" %}
Token de autenticação obtido nas configurações do evento.
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
{
  "data": [
    {
      "id_session": 155553,
      "id_event": 37524,
      "title": "Accessibility Management In Large Companies",
      "description": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus feugiat blandit lectus. In placerat purus tellus. Proin eros dui, condimentum at imperdiet vel, pretium vel ipsum. Nunc varius lectus eu mi tempor, ut luctus est ultricies. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Proin imperdiet nisi et risus gravida pharetra sit amet a odio. Nam laoreet sem vitae finibus laoreet. Nulla eget lectus at sem consectetur volutpat. Duis scelerisque tellus id vestibulum aliquam.",
      "credit_hour": "1",
      "capacity": 50,
      "ticket_price": 10.0000,
      "type": "Conferência",
      "venue": "AUDITORIUM 1",
      "tags": "Accessibility, Enterprise",
      "speakers": [
        {
          "id_event": 37524,
          "id_speaker": 117452,
          "id_session": 155553,
          "name": "Katherine Martin",
          "photo": "https://images.even3.com.br/4Ru_0labb33RLwLB8BABoTSc38k=/150x150/smart/even3.blob.core.windows.net/geral/1.f8ee65f357fe420ead67.jpeg",
          "resume": "Sed convallis quam vel mi porta rutrum. Sed non egestas ipsum",
          "facebook": "",
          "linkedin": "https://www.google.com.br/",
          "email": "",
          "lattes": "https://www.google.com.br/",
          "twitter": "",
          "site": ""
        },
        {
          "id_event": 37524,
          "id_speaker": 117453,
          "id_session": 155553,
          "name": "José Antonio",
          "photo": "https://images.even3.com.br/pfHDCxbvC3rxTpEmlhwYtEh5ess=/150x150/smart/even3.blob.core.windows.net/geral/image.e75181cc624d4cd49b6b.jpeg",
          "resume": "Sed convallis quam vel mi porta rutrum. Sed non egestas ipsum",
          "facebook": "https://www.google.com.br/",
          "linkedin": "https://www.google.com.br/",
          "email": "",
          "lattes": "https://www.google.com.br/",
          "twitter": "https://www.google.com.br/",
          "site": ""
        }
      ],
      "times": [
        {
          "id_event": 37524,
          "id_session": 155553,
          "id_time": 534771,
          "date": "2020-01-01T00:00:00",
          "start_time": "10:00",
          "end_time": "11:00"
        }
      ]
    }
  ]
}
```
{% endswagger-response %}

{% swagger-response status="404" description="" %}
```
{
  "message": "Something bad happened :(",
  "erros": [
    {
      "code": 204,
      "description": "Internal server error"
    }
  ],
  "count_erros": 1
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://www.even3.com.br" path="/api/v1/speaker/:id" method="get" summary="Retorna o palestrante" %}
{% swagger-description %}
Retornar o palestrante
{% endswagger-description %}

{% swagger-parameter name="" type="string" required="false" in="path" %}
ID de um palestrantes específico (opcional)
{% endswagger-parameter %}

{% swagger-parameter name="Authorization-Token" type="string" required="true" in="header" %}
Token de autenticação obtido nas configurações do evento
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
{
  "data": [
    {
      "id_event": 37524,
      "id_speaker": 117452,
      "name": "Katherine Martin",
      "photo": "https://images.even3.com.br/4Ru_0labb33RLwLB8BABoTSc38k=/150x150/smart/even3.blob.core.windows.net/geral/1.f8ee65f357fe420ead67.jpeg",
      "resume": "Sed convallis quam vel mi porta rutrum. Sed non egestas ipsum",
      "facebook": "",
      "linkedin": "https://www.google.com.br/",
      "email": "",
      "lattes": "https://www.google.com.br/",
      "twitter": "",
      "site": ""
    }
  ]
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://www.even3.com.br" path="/api/v1/session/getschedule" method="get" summary="Retorna a programação por dia" %}
{% swagger-description %}
Retornar a programação para facilitar a criação de uma grade de programação
{% endswagger-description %}

{% swagger-parameter name="Authorization-Token" type="string" required="false" in="path" %}
Token de autenticação obtido nas configurações do evento
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
{
  "data": [
    {
      "id_schedule": "01012020",
      "date": "2020-01-01T00:00:00.0000000",
      "day": "quarta-feira",
      "sessions": [
        {
          "id_session": 155553,
          "title": "Accessibility Management In Large Companies",
          "title_schedule": "Atividades",
          "venue": "AUDITORIUM 1",
          "description": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus feugiat blandit lectus. In placerat purus tellus. Proin eros dui, condimentum at imperdiet vel, pretium vel ipsum. Nunc varius lectus eu mi tempor, ut luctus est ultricies. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Proin imperdiet nisi et risus gravida pharetra sit amet a odio. Nam laoreet sem vitae finibus laoreet. Nulla eget lectus at sem consectetur volutpat. Duis scelerisque tellus id vestibulum aliquam.",
          "tags": "Accessibility, Enterprise",
          "date": "01/01/2020",
          "date_UTC": "2020-01-01T00:00:00.0000000",
          "start_time": "10:00",
          "end_time": "11:00",
          "speakers": [
            {
              "id_speaker": 117452,
              "name": "Katherine Martin",
              "photo": "https://images.even3.com.br/4Ru_0labb33RLwLB8BABoTSc38k=/150x150/smart/even3.blob.core.windows.net/geral/1.f8ee65f357fe420ead67.jpeg",
              "resume": "Sed convallis quam vel mi porta rutrum. Sed non egestas ipsum",
              "facebook": "",
              "linkedin": "https://www.google.com.br/",
              "email": "",
              "lattes": "https://www.google.com.br/",
              "twitter": "",
              "site": ""
            },
            {
              "id_speaker": 117453,
              "name": "José Antonio",
              "photo": "https://images.even3.com.br/pfHDCxbvC3rxTpEmlhwYtEh5ess=/150x150/smart/even3.blob.core.windows.net/geral/image.e75181cc624d4cd49b6b.jpeg",
              "resume": "Sed convallis quam vel mi porta rutrum. Sed non egestas ipsum",
              "facebook": "https://www.google.com.br/",
              "linkedin": "https://www.google.com.br/",
              "email": "",
              "lattes": "https://www.google.com.br/",
              "twitter": "https://www.google.com.br/",
              "site": ""
            }
          ],
          "all_dates": [
            {
              "date": "2020-01-01T00:00:00",
              "day": "quarta-feira",
              "start_time": "10:00",
              "end_time": "11:00"
            }
          ]
        },
        {
          "id_session": 155554,
          "title": "Inaugural Speech",
          "title_schedule": "Atividades",
          "venue": "AUDITORIUM 1",
          "description": " ",
          "tags": null,
          "date": "01/01/2020",
          "date_UTC": "2020-01-01T00:00:00.0000000",
          "start_time": "11:00",
          "end_time": "12:00",
          "speakers": [
            {
              "id_speaker": 117452,
              "name": "Katherine Martin",
              "photo": "https://images.even3.com.br/4Ru_0labb33RLwLB8BABoTSc38k=/150x150/smart/even3.blob.core.windows.net/geral/1.f8ee65f357fe420ead67.jpeg",
              "resume": "Sed convallis quam vel mi porta rutrum. Sed non egestas ipsum",
              "facebook": "",
              "linkedin": "https://www.google.com.br/",
              "email": "",
              "lattes": "https://www.google.com.br/",
              "twitter": "",
              "site": ""
            },
            {
              "id_speaker": 117453,
              "name": "José Antonio",
              "photo": "https://images.even3.com.br/pfHDCxbvC3rxTpEmlhwYtEh5ess=/150x150/smart/even3.blob.core.windows.net/geral/image.e75181cc624d4cd49b6b.jpeg",
              "resume": "Sed convallis quam vel mi porta rutrum. Sed non egestas ipsum",
              "facebook": "https://www.google.com.br/",
              "linkedin": "https://www.google.com.br/",
              "email": "",
              "lattes": "https://www.google.com.br/",
              "twitter": "https://www.google.com.br/",
              "site": ""
            }
          ],
          "all_dates": [
            {
              "date": "2020-01-01T00:00:00",
              "day": "quarta-feira",
              "start_time": "11:00",
              "end_time": "12:00"
            }
          ]
        },
        {
          "id_session": 155555,
          "title": "Coffee Break",
          "title_schedule": "Atividades",
          "venue": null,
          "description": " ",
          "tags": null,
          "date": "01/01/2020",
          "date_UTC": "2020-01-01T00:00:00.0000000",
          "start_time": "12:00",
          "end_time": "13:00",
          "speakers": [],
          "all_dates": [
            {
              "date": "2020-01-01T00:00:00",
              "day": "quarta-feira",
              "start_time": "12:00",
              "end_time": "13:00"
            }
          ]
        },
        {
          "id_session": 155560,
          "title": "Accessibility In Mice (Meetings, Incentives, Conferencing And Exhibitions)",
          "title_schedule": "Atividades",
          "venue": "AUDITORIUM 1",
          "description": " ",
          "tags": null,
          "date": "01/01/2020",
          "date_UTC": "2020-01-01T00:00:00.0000000",
          "start_time": "13:00",
          "end_time": "15:00",
          "speakers": [
            {
              "id_speaker": 117452,
              "name": "Katherine Martin",
              "photo": "https://images.even3.com.br/4Ru_0labb33RLwLB8BABoTSc38k=/150x150/smart/even3.blob.core.windows.net/geral/1.f8ee65f357fe420ead67.jpeg",
              "resume": "Sed convallis quam vel mi porta rutrum. Sed non egestas ipsum",
              "facebook": "",
              "linkedin": "https://www.google.com.br/",
              "email": "",
              "lattes": "https://www.google.com.br/",
              "twitter": "",
              "site": ""
            },
            {
              "id_speaker": 117462,
              "name": "Philip Lang",
              "photo": "https://images.even3.com.br/xxZs9DB481SVpgo3bcKu_9AHRKo=/150x150/smart/even3.blob.core.windows.net/geral/image3.df2be705053d42149231.jpeg",
              "resume": null,
              "facebook": "",
              "linkedin": "",
              "email": "",
              "lattes": "",
              "twitter": "",
              "site": ""
            }
          ],
          "all_dates": [
            {
              "date": "2020-01-01T00:00:00",
              "day": "quarta-feira",
              "start_time": "13:00",
              "end_time": "15:00"
            }
          ]
        },
        {
          "id_session": 155561,
          "title": "Accessibility in International",
          "title_schedule": "Atividades",
          "venue": "AUDITORIUM 1",
          "description": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus feugiat blandit lectus. In placerat purus tellus. Proin eros dui, condimentum at imperdiet vel, pretium vel ipsum. Nunc varius lectus eu mi tempor, ut luctus est ultricies. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Proin imperdiet nisi et risus gravida pharetra sit amet a odio. Nam laoreet sem vitae finibus laoreet. Nulla eget lectus at sem consectetur volutpat. Duis scelerisque tellus id vestibulum aliquam.",
          "tags": null,
          "date": "01/01/2020",
          "date_UTC": "2020-01-01T00:00:00.0000000",
          "start_time": "15:00",
          "end_time": "17:00",
          "speakers": [
            {
              "id_speaker": 117452,
              "name": "Katherine Martin",
              "photo": "https://images.even3.com.br/4Ru_0labb33RLwLB8BABoTSc38k=/150x150/smart/even3.blob.core.windows.net/geral/1.f8ee65f357fe420ead67.jpeg",
              "resume": "Sed convallis quam vel mi porta rutrum. Sed non egestas ipsum",
              "facebook": "",
              "linkedin": "https://www.google.com.br/",
              "email": "",
              "lattes": "https://www.google.com.br/",
              "twitter": "",
              "site": ""
            }
          ],
          "all_dates": [
            {
              "date": "2020-01-01T00:00:00",
              "day": "quarta-feira",
              "start_time": "15:00",
              "end_time": "17:00"
            }
          ]
        },
        {
          "id_session": 155571,
          "title": "Current Training Model: University and Professional",
          "title_schedule": "Atividades",
          "venue": null,
          "description": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus feugiat blandit lectus. In placerat purus tellus. Proin eros dui, condimentum at imperdiet vel, pretium vel ipsum. Nunc varius lectus eu mi tempor, ut luctus est ultricies. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Proin imperdiet nisi et risus gravida pharetra sit amet a odio. Nam laoreet sem vitae finibus laoreet. Nulla eget lectus at sem consectetur volutpat. Duis scelerisque tellus id vestibulum aliquam",
          "tags": null,
          "date": "01/01/2020",
          "date_UTC": "2020-01-01T00:00:00.0000000",
          "start_time": "17:00",
          "end_time": "18:00",
          "speakers": [
            {
              "id_speaker": 117464,
              "name": "Joana Johnson",
              "photo": "https://images.even3.com.br/c7-XGsFsPdMcL-HgZiSRraiBaCM=/150x150/smart/even3.blob.core.windows.net/geral/image2.565b9a549e4544ccb27c.jpeg",
              "resume": "Sed accumsan lacus vitae dictum malesuada. Praesent varius massa tristique elementum bibendum",
              "facebook": "",
              "linkedin": "https://www.google.com.br/",
              "email": "",
              "lattes": "",
              "twitter": "https://www.google.com.br/",
              "site": ""
            }
          ],
          "all_dates": [
            {
              "date": "2020-01-01T00:00:00",
              "day": "quarta-feira",
              "start_time": "17:00",
              "end_time": "18:00"
            },
            {
              "date": "2020-01-02T00:00:00",
              "day": "quinta-feira",
              "start_time": "17:00",
              "end_time": "18:00"
            }
          ]
        }
      ]
    },
    {
      "id_schedule": "02012020",
      "date": "2020-01-02T00:00:00.0000000",
      "day": "quinta-feira",
      "sessions": [
        {
          "id_session": 155567,
          "title": "Inclusion in Emergency Management",
          "title_schedule": "Atividades",
          "venue": null,
          "description": " ",
          "tags": null,
          "date": "02/01/2020",
          "date_UTC": "2020-01-02T00:00:00.0000000",
          "start_time": "10:00",
          "end_time": "11:00",
          "speakers": [
            {
              "id_speaker": 117462,
              "name": "Philip Lang",
              "photo": "https://images.even3.com.br/xxZs9DB481SVpgo3bcKu_9AHRKo=/150x150/smart/even3.blob.core.windows.net/geral/image3.df2be705053d42149231.jpeg",
              "resume": null,
              "facebook": "",
              "linkedin": "",
              "email": "",
              "lattes": "",
              "twitter": "",
              "site": ""
            }
          ],
          "all_dates": [
            {
              "date": "2020-01-02T00:00:00",
              "day": "quinta-feira",
              "start_time": "10:00",
              "end_time": "11:00"
            }
          ]
        },
        {
          "id_session": 155568,
          "title": "Accessibility in Smart Cities",
          "title_schedule": "Atividades",
          "venue": null,
          "description": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus feugiat blandit lectus. In placerat purus tellus. Proin eros dui, condimentum at imperdiet vel, pretium vel ipsum. Nunc varius lectus eu mi tempor, ut luctus est ultricies. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Proin imperdiet nisi et risus gravida pharetra sit amet a odio. Nam laoreet sem vitae finibus laoreet. Nulla eget lectus at sem consectetur volutpat. Duis scelerisque tellus id vestibulum aliquam",
          "tags": null,
          "date": "02/01/2020",
          "date_UTC": "2020-01-02T00:00:00.0000000",
          "start_time": "11:00",
          "end_time": "12:00",
          "speakers": [
            {
              "id_speaker": 117453,
              "name": "José Antonio",
              "photo": "https://images.even3.com.br/pfHDCxbvC3rxTpEmlhwYtEh5ess=/150x150/smart/even3.blob.core.windows.net/geral/image.e75181cc624d4cd49b6b.jpeg",
              "resume": "Sed convallis quam vel mi porta rutrum. Sed non egestas ipsum",
              "facebook": "https://www.google.com.br/",
              "linkedin": "https://www.google.com.br/",
              "email": "",
              "lattes": "https://www.google.com.br/",
              "twitter": "https://www.google.com.br/",
              "site": ""
            }
          ],
          "all_dates": [
            {
              "date": "2020-01-02T00:00:00",
              "day": "quinta-feira",
              "start_time": "11:00",
              "end_time": "12:00"
            }
          ]
        },
        {
          "id_session": 155569,
          "title": "Coffee Break",
          "title_schedule": "Atividades",
          "venue": null,
          "description": " ",
          "tags": null,
          "date": "02/01/2020",
          "date_UTC": "2020-01-02T00:00:00.0000000",
          "start_time": "12:00",
          "end_time": "13:00",
          "speakers": [],
          "all_dates": [
            {
              "date": "2020-01-02T00:00:00",
              "day": "quinta-feira",
              "start_time": "12:00",
              "end_time": "13:00"
            }
          ]
        },
        {
          "id_session": 155570,
          "title": "Access to Cultural Contents",
          "title_schedule": "Atividades",
          "venue": null,
          "description": " ",
          "tags": null,
          "date": "02/01/2020",
          "date_UTC": "2020-01-02T00:00:00.0000000",
          "start_time": "13:00",
          "end_time": "17:00",
          "speakers": [
            {
              "id_speaker": 117452,
              "name": "Katherine Martin",
              "photo": "https://images.even3.com.br/4Ru_0labb33RLwLB8BABoTSc38k=/150x150/smart/even3.blob.core.windows.net/geral/1.f8ee65f357fe420ead67.jpeg",
              "resume": "Sed convallis quam vel mi porta rutrum. Sed non egestas ipsum",
              "facebook": "",
              "linkedin": "https://www.google.com.br/",
              "email": "",
              "lattes": "https://www.google.com.br/",
              "twitter": "",
              "site": ""
            }
          ],
          "all_dates": [
            {
              "date": "2020-01-02T00:00:00",
              "day": "quinta-feira",
              "start_time": "13:00",
              "end_time": "17:00"
            }
          ]
        },
        {
          "id_session": 155571,
          "title": "Current Training Model: University and Professional",
          "title_schedule": "Atividades",
          "venue": null,
          "description": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus feugiat blandit lectus. In placerat purus tellus. Proin eros dui, condimentum at imperdiet vel, pretium vel ipsum. Nunc varius lectus eu mi tempor, ut luctus est ultricies. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Proin imperdiet nisi et risus gravida pharetra sit amet a odio. Nam laoreet sem vitae finibus laoreet. Nulla eget lectus at sem consectetur volutpat. Duis scelerisque tellus id vestibulum aliquam",
          "tags": null,
          "date": "02/01/2020",
          "date_UTC": "2020-01-02T00:00:00.0000000",
          "start_time": "17:00",
          "end_time": "18:00",
          "speakers": [
            {
              "id_speaker": 117464,
              "name": "Joana Johnson",
              "photo": "https://images.even3.com.br/c7-XGsFsPdMcL-HgZiSRraiBaCM=/150x150/smart/even3.blob.core.windows.net/geral/image2.565b9a549e4544ccb27c.jpeg",
              "resume": "Sed accumsan lacus vitae dictum malesuada. Praesent varius massa tristique elementum bibendum",
              "facebook": "",
              "linkedin": "https://www.google.com.br/",
              "email": "",
              "lattes": "",
              "twitter": "https://www.google.com.br/",
              "site": ""
            }
          ],
          "all_dates": [
            {
              "date": "2020-01-01T00:00:00",
              "day": "quarta-feira",
              "start_time": "17:00",
              "end_time": "18:00"
            },
            {
              "date": "2020-01-02T00:00:00",
              "day": "quinta-feira",
              "start_time": "17:00",
              "end_time": "18:00"
            }
          ]
        }
      ]
    }
  ],
  "count": 2
}
```
{% endswagger-response %}
{% endswagger %}
