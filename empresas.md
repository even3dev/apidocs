# Empresas

{% api-method method="get" host="https://www.even3.com.br" path="/api/v1/customclient/events" %}
{% api-method-summary %}
Retorna lista de eventos da empresa
{% endapi-method-summary %}

{% api-method-description %}
Retorna a lista de eventos do plano empresarial. É necessário solicitar as informações de autenticação ao suporte
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization-Token" type="string" required=true %}
Solicitar ao suporte
{% endapi-method-parameter %}

{% api-method-parameter name="Authorization-App" type="string" required=true %}
Solicitar ao suporte
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Lista de eventos
{% endapi-method-response-example-description %}

```
{
  "data": [
    {
      "id": 1
      "titulo": "Evento teste 1",
      "url": "urleventoTeste",
      "token": "123456789"
       }
  ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



