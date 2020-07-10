# Credenciamento

{% api-method method="post" host="https://www.even3.com.br" path="/api/v1/checkin/attendees" %}
{% api-method-summary %}
Credenciamento dos participantes no evento
{% endapi-method-summary %}

{% api-method-description %}
Realiza credenciamento dos participantes no evento
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization-Token" type="string" required=true %}
Token de autenticação obtido nas configurações do evento.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="attendees" type="array" required=true %}
Lista de CheckinAttendees \(Ver Models\)
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Credenciamento realizado
{% endapi-method-response-example-description %}

```
"OK"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://www.even3.com.br" path="/api/v1/checkin/sessions" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}
Realiza credenciamento dos participantes em atividades
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization-Token" type="string" required=true %}
Token de autenticação obtido nas configurações do evento.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="sessions" type="array" required=true %}
Lista de CheckinSessions \(Ver Models\)
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Credenciamento realizado
{% endapi-method-response-example-description %}

```
"OK"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



