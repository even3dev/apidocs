# Submissão

{% api-method method="get" host="https://www.even3.com.br" path="/api/v1/submission/" %}
{% api-method-summary %}
Retorna as modalidades e áreas temáticas de submissão
{% endapi-method-summary %}

{% api-method-description %}
Retorna as modalidades e áreas temáticas do evento
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization-Token" type="string" required=true %}
Token de autenticação obtido nas configurações do evento.Re{
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
  "submission_type": {
    "data": [
      {
        "id_event": 37524,
        "id_submissiontype": 29631,
        "url_roles": "https://even3.blob.core.windows.net/geral/Template-para-Trabalhos-completos-CONINTER-em-18.09.2019.d825047b7c5947b290df.docx",
        "title": "Regras de submissão de Article"
      },
      {
        "id_event": 37524,
        "id_submissiontype": 29635,
        "url_roles": "",
        "title": "Rules for submission of {{name}}"
      }
    ],
    "count": 2
  },
  "topic_area": {
    "data": [
      {
        "id_event": 37524,
        "id_topicarea": 30747,
        "title": "Tecnologías y Servicios de Acceso a la Información y la Comunicación"
      },
      {
        "id_event": 37524,
        "id_topicarea": 30749,
        "title": "Interacción persona máquina"
      },
      {
        "id_event": 37524,
        "id_topicarea": 30750,
        "title": "Teleasistencia y Telecuidado: Prolongación de la vida activa"
      },
      {
        "id_event": 37524,
        "id_topicarea": 30751,
        "title": "Smart City"
      },
      {
        "id_event": 37524,
        "id_topicarea": 30752,
        "title": "Aprendizaje y colaboración accesibles"
      }
    ],
    "count": 5
  },
  "count": 2
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "Message": "No HTTP resource was found that matches the request URI 'https://www.even3.com.br/api/v1/submission/29631'."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



