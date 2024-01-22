# Empresas

{% swagger baseUrl="https://www.even3.com.br" path="/api/v1/customclient/events" method="get" summary="Retorna lista de eventos da empresa" %}
{% swagger-description %}
Retorna a lista de eventos do plano empresarial. É necessário solicitar as informações de autenticação ao suporte
{% endswagger-description %}

{% swagger-parameter name="Authorization-Token" type="string" required="true" in="header" %}
Solicitar ao suporte
{% endswagger-parameter %}

{% swagger-parameter name="Authorization-App" type="string" required="true" in="header" %}
Solicitar ao suporte
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
{
  "data": [
    {
      "id": 1,
      "titulo": "Evento teste 1",
      "url": "urleventoTeste",
      "token": "123456789",
      "email_organizador": "apiempresas@even3.com",
      "start_date": "2024-01-01",
      "start_time": "19:00",
      "end_date": "2024-02-01",
      "end_time": "21:30"
     }
  ]
}
```
{% endswagger-response %}
{% endswagger %}
