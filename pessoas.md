# Pessoas

{% swagger baseUrl="https://www.even3.com.br" path="/api/v1/attendees/:id" method="get" summary="Retornar participantes" %}
{% swagger-description %}
Esse método retorna um ou todos os participantes de um evento.
{% endswagger-description %}

{% swagger-parameter name="id" type="string" in="path" %}
ID do um participante específico
{% endswagger-parameter %}

{% swagger-parameter name="Authorization-Token" type="string" required="true" in="header" %}
Token de autenticação obtido nas configurações do evento.
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
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
            "document": "000.000.000-00",
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
            "document": "000.000.000-00",
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
            "document": "123456789",
            "confirmed": false
        },
],
    "count": 3
}

```
{% endswagger-response %}

{% swagger-response status="404" description="" %}
```javascript
{
    "data": [],
    "count": 0
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://www.even3.com.br" path="/api/v1/attendees/create" method="post" summary="Inserir um participante" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter name="Authorization-Token" type="string" required="true" in="header" %}
Token de autenticação obtido nas configurações do evento
{% endswagger-parameter %}

{% swagger-parameter name="attendee" type="string" required="false" in="body" %}
Objeto `Atendee`
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
```
{% endswagger-response %}
{% endswagger %}

### Attendee

```
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
**`id_ticket_price`**- É a entrada no qual o participante será inscrito. A lista de entradas e seus ids podem ser obtidas no endpoint Evento
{% endhint %}
