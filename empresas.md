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
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{    "name": "Cake's name",    "recipe": "Cake's recipe name",    "cake": "Binary cake"}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```
{    "message": "Ain't no cake like that."}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



