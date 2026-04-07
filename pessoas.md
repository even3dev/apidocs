# 🧑‍🤝‍🧑 Pessoas

## Retornar participantes

<mark style="color:blue;">`GET`</mark> `https://www.even3.com.br/api/v1/attendees/:id`

Esse método retorna todos os participantes de um evento.

**Path Parameters**

| **Name** | **Type** | **Description**    |
| -------- | -------- | ------------------ |
| id       | string   | ID do participante |

#### Headers

| Name                                                  | Type   | Description                                               |
| ----------------------------------------------------- | ------ | --------------------------------------------------------- |
| Authorization-Token<mark style="color:red;">\*</mark> | string | Token de autenticação obtido nas configurações do evento. |

{% tabs %}
{% tab title="200 " %}
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
            "confirmed": false,
            "registration_category": "",
            "registration_date": "",
            "registration_hour": ""
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
            "confirmed": false,
            "registration_category": "",
            "registration_date": "",
            "registration_hour": ""
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
            "confirmed": false,
            "registration_category": "Geral",
            "registration_date": "20/08/2022",
            "registration_hour": "11:50"
        },
],
    "count": 3
}

```
{% endtab %}

{% tab title="404 " %}
```javascript
{
    "data": [],
    "count": 0
}
```
{% endtab %}
{% endtabs %}

## Inserir um participante

<mark style="color:green;">`POST`</mark> `https://www.even3.com.br/api/v1/attendees/create`

#### Headers

| Name                                                  | Type   | Description                                              |
| ----------------------------------------------------- | ------ | -------------------------------------------------------- |
| Authorization-Token<mark style="color:red;">\*</mark> | string | Token de autenticação obtido nas configurações do evento |

#### Request Body

| Name     | Type   | Description      |
| -------- | ------ | ---------------- |
| attendee | string | Objeto `Atendee` |

{% tabs %}
{% tab title="200 " %}
```json
"Data entered successfully."
```
{% endtab %}
{% endtabs %}

### Attendee

```javascript
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
