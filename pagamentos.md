# 💰 Pagamentos

## Retornar dados de pagamentos do evento

<mark style="color:blue;">`GET`</mark> `https://www.even3.com.br/api/v1/payments`

Este endpoint retorna todas as informações dos pagamentos do seu evento

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
            "id_event": 123456,
            "id_payment": 00001,
            "reference_payment": "0101010101",
            "buyer": "Empresa Geral",
            "email_buyer": "empresageral@teste.com.br",
            "country_buyer": "Brazil",
            "document_buyer": "00000000000",
            "description_payment": "1 ingresso(s);",
            "date_payment": "28/11/2023",
            "hour_payment": "17:21",
            "type_payment": "Mastercard",
            "method_payment": "Cartão de Crédito",
            "amount_payment": 10.00,
            "amount_receive_payment": 7.50,
            "status_payment": "Pago",
            "cupom_payment": "",
            "note_payment": " "
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



## Retornar detalhes de um pagamento

<mark style="color:blue;">`GET`</mark> `https://www.even3.com.br/api/v1/payments/details`

Este endpoint retorna todas as informações de um pagamento do evento

#### Headers

| Name                                                  | Type   | Description                                                  |
| ----------------------------------------------------- | ------ | ------------------------------------------------------------ |
| Authorization-Token<mark style="color:red;">\*</mark> | string | Token de autenticação encontrado nas configurações do evento |

#### Request Body

| Name                                        | Type   | Description |
| ------------------------------------------- | ------ | ----------- |
| reference<mark style="color:red;">\*</mark> | string | 12345678    |

{% tabs %}
{% tab title="200: OK " %}


```javascript
{
    "data": [
        {
           "id_event": 123456,
            "id_payment": 00001,
            "reference_payment": "0101010101",
            "attendee": "Maria Silva",
            "email_attendee": "mariasilva@teste.com.br",
            "document_attendee": "",
            "phone_attende": "11111111111",
            "description": "Ingresso",
            "item": "Estudantes",
            "amount": 10.00
        }
    ],
    "count": 1
}
```
{% endtab %}

{% tab title="404: Not Found " %}
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
