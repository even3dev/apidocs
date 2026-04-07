# 📃 Certificados



## Retornar dados dos certificados do evento

<mark style="color:blue;">`GET`</mark> `https://www.even3.com.br/api/v1/certificates`

Este endpoint retorna todas as informações dos certificados do seu evento

#### Headers

| Name                                                  | Type   | Description                                                  |
| ----------------------------------------------------- | ------ | ------------------------------------------------------------ |
| Authorization-Token<mark style="color:red;">\*</mark> | string | Token de autenticação encontrado nas configurações do evento |

{% tabs %}
{% tab title="200 " %}
```javascript
{
  "certificates": {
    "data": [
      {
        "id_pessoa": 1234,
        "id_event": 123456,
        "name": "João Fictício",
        "email": "joao@exemplo.com",
        "document": "000.000.000-00",
        "certificate_url": "https://www.even3.com/certificados/imprimir?"
      }
    ],
    "count": 1
  },
  "count": 1
}
```
{% endtab %}
{% endtabs %}
