# ✅ Credenciamento

{% swagger baseUrl="https://www.even3.com.br" path="/api/v1/checkin/attendees" method="post" summary="Credenciamento dos participantes no evento" %}
{% swagger-description %}
Realiza credenciamento dos participantes no evento
{% endswagger-description %}

{% swagger-parameter name="Authorization-Token" type="string" required="true" in="header" %}
Token de autenticação obtido nas configurações do evento.
{% endswagger-parameter %}

{% swagger-parameter name="attendees" type="array" required="true" in="body" %}
Lista de CheckinAttendees (Ver Models)
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
"OK"
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://www.even3.com.br" path="/api/v1/checkin/sessions" method="post" summary="" %}
{% swagger-description %}
Realiza credenciamento dos participantes em atividades
{% endswagger-description %}

{% swagger-parameter name="Authorization-Token" type="string" required="true" in="header" %}
Token de autenticação obtido nas configurações do evento.
{% endswagger-parameter %}

{% swagger-parameter name="sessions" type="array" required="true" in="body" %}
Lista de CheckinSessions (Ver Models)
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
"OK"
```
{% endswagger-response %}
{% endswagger %}
