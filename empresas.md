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
      "id": 1
      "titulo": "Evento teste 1",
      "url": "urleventoTeste",
      "token": "123456789",
      "start_date": "2014-04-13T00:00:00",
      "start_time": "09:00",
      "end_date": "2014-06-03T00:00:00",
      "end_time": "18:00",
     }
  ]
}
```
{% endswagger-response %}
{% endswagger %}
