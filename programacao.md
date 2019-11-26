# Programação

{% api-method method="get" host="https://www.even3.com.br" path="/api/v1/session/:id" %}
{% api-method-summary %}
Retorna as atividades do evento
{% endapi-method-summary %}

{% api-method-description %}
Retorne a lista de atividades do evento ou uma única atividade
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" %}
ID de uma atividade específica \(opcional\)
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization-Token" type="string" required=true %}
Token de autenticação obtido nas configurações do evento.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Atividade retornada com sucesso.
{% endapi-method-response-example-description %}

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
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Erro ao retornar a atividade.
{% endapi-method-response-example-description %}

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
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://www.even3.com.br" path="/api/v1/speaker/:id" %}
{% api-method-summary %}
Retorna os palestrantes do evento
{% endapi-method-summary %}

{% api-method-description %}
Retornar todos os pale
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}
ID de um palestrantes específico \(opcional\)
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization-Token" type="string" required=true %}
Token de autenticação obtido nas configurações do evento
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

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
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

