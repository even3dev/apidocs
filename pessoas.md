# Pessoas

{% api-method method="get" host="https://www.even3.com.br" path="/api/v1/attendees/:id" %}
{% api-method-summary %}
Retornar participantes
{% endapi-method-summary %}

{% api-method-description %}
Esse método retorna um ou todos os participantes de um evento.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" %}
ID do um participante específico
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
Participante retornado com sucesso
{% endapi-method-response-example-description %}

```javascript
{
    "data": [
        {
            "id_attendees": 9,
            "id_event": 1,
            "checkin_code": 11,
            "name": "Renan José Guedes",
            "bagde_name": "Renan Guedes",
            "email": "renang@hotmail.com",
            "gender": "M",
            "photo": "https://graph.facebook.com/1569985586409400/picture?width=150&height=150",
            "confirmed": false
        },
        {
            "id_attendees": 24,
            "id_event": 1,
            "checkin_code": 25,
            "name": "Luciana Corrêa",
            "bagde_name": "Luciana Corrêa",
            "email": "luciana@gmail.com",
            "gender": "F",
            "photo": " ",
            "confirmed": false
        },
        {
            "id_attendees": 25,
            "id_event": 1,
            "name": "Germana Marques",
            "bagde_name": "Germana Marques",
            "email": "germana@globo.com",
            "gender": "F",
            "photo": " ",
            "confirmed": false
        },
],
    "count": 3
}

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```javascript
{
    "data": [],
    "count": 0
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://www.even3.com.br" path="/api/v1/attendees/create" %}
{% api-method-summary %}
Inserir um participante
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization-Token" type="string" required=true %}
Token de autenticação obtido nas configurações do evento
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="attendee" type="string" required=false %}
Objeto `Atendee`
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### Attendee

```text
{
  "name": "string",
  "bagde_name": "string",
  "email": "string",
  "gender": "string",
  "photo": "string",
  "registration_confirmed": true,
  "registration": {
    "id_ticket_price": 0,
    "price": 0
  }
}
```

{% hint style="info" %}
**`id_ticket_price`**- É a entrada no qual o participante será inscrito, a lista de entradas e seus ids podem ser obtida no endpoint Evento 
{% endhint %}

