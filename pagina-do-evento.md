# 💻 Página do evento

{% swagger baseUrl="https://www.even3.com.br" path="/api/v1/hotsite/" method="get" summary="Retorna a lista de áreas cadastradas" %}
{% swagger-description %}
Retorna as áreas cadastradas na página do evento
{% endswagger-description %}

{% swagger-parameter name="Authorization-Token" type="string" required="true" in="header" %}
Token de autenticação obtido nas configurações do evento.
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
{
  "capa": null,
  "areasSite": [
    {
      "idAreaSite": null,
      "titulo": "Sobre o evento",
      "subtitulo": "",
      "ordem": 1,
      "jsonObj": [],
      "template": "<p>sadasdasdasdas</p>"
    },
    {
      "idAreaSite": 1,
      "titulo": "Inscrições",
      "subtitulo": null,
      "ordem": 2,
      "jsonObj": [],
      "template": ""
    },
    {
      "idAreaSite": 2,
      "titulo": "Atividades",
      "subtitulo": null,
      "ordem": 3,
      "jsonObj": [],
      "template": ""
    },
    {
      "idAreaSite": 3,
      "titulo": "Palestrantes",
      "subtitulo": null,
      "ordem": 4,
      "jsonObj": [],
      "template": ""
    },
    {
      "idAreaSite": 4,
      "titulo": "Submissões",
      "subtitulo": null,
      "ordem": 5,
      "jsonObj": [],
      "template": ""
    },
    {
      "idAreaSite": 5,
      "titulo": "Local do Evento",
      "subtitulo": null,
      "ordem": 6,
      "jsonObj": [],
      "template": ""
    },
    {
      "idAreaSite": 9,
      "titulo": "Patrocinadores",
      "subtitulo": "",
      "ordem": 7,
      "jsonObj": [
        {
          "titulo": "teste",
          "urlImagem": "https://even3.blob.core.windows.net/pagina-evento/2.94f0dfae23fb4a0ca11d.PNG",
          "link": "globo.com.br",
          "id": 1
        }
      ],
      "template": ""
    },
    {
      "idAreaSite": null,
      "titulo": "Teste avulso",
      "subtitulo": "",
      "ordem": 8,
      "jsonObj": [],
      "template": "<p>asdasdasdas</p>"
    }
  ]
}
```
{% endswagger-response %}
{% endswagger %}
