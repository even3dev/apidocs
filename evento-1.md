# Pagamentos

{% swagger baseUrl="https://www.even3.com.br" path="/api/v1/payments" method="get" summary="Retornar dados de pagamentos do evento" %}
{% swagger-description %}
Este endpoint retorna todas as informações dos pagamentos do seu evento
{% endswagger-description %}

{% swagger-parameter name="Authorization-Token" type="string" required="true" in="header" %}
Token de autenticação encontrado nas configurações do evento
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```javascript
{
    "data": [
        {
            "id_event": 123456,
            "id_payment": 00001,
            "reference_payment": "0101010101",
            "buyer": "Empresa Geral",
            "email_buyer": "empresageral@teste.com.br",
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
{% endswagger-response %}

{% swagger-response status="404" description="" %}
```json
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
{% endswagger-response %}
{% endswagger %}



{% swagger method="get" path="/api/v1/payments/details" baseUrl="https://www.even3.com.br" summary="Retornar detalhes de um pagamento" %}
{% swagger-description %}
Este endpoint retorna todas as informações de um pagamento do evento
{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization-Token" type="string" required="true" %}
Token de autenticação encontrado nas configurações do evento
{% endswagger-parameter %}

{% swagger-parameter in="body" name="reference" type="string" required="true" %}
12345678
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}


```json
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
{% endswagger-response %}

{% swagger-response status="404: Not Found" description="" %}
```json
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
{% endswagger-response %}
{% endswagger %}
