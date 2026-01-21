GET /api/v1/partner/stores

JSON schema:
{
  "type": "object",
  "required": ["stores"],
  "properties": {
    "stores": {
      "items": {
        "type": "object",
        "required": ["name", "image", "delivery", "external_link"],
        "properties": {
          "name": { "type": "string" },
          "image": { "type": "string"},
          "delivery": { "type": "string" },
          "external_link": { "type": "string", "format": "uri" }
        }
      }
    }
  }
}

JSON:
{
  "stores": [
    {
      "name": "METRO",
      "image": "https://cdn.petrushka.ru/metro.png",
      "delivery": "сегодня 21:00-23:00",
      "external_link": "https://metro.ru/?from=petrushka"
    },
    {
      "name": "Ашан",
      "image": "https://cdn.petrushka.ru/auchan.png", 
      "delivery": "сегодня 18:00-20:00",
      "external_link": "https://auchan.ru/?from=petrushka"
    },
    {
      "name": "ВкусВилл",
      "image": "https://cdn.petrushka.ru/vkusvill.png", 
      "delivery": "от 20 до 60 минут",
      "external_link": "https://vkusvill.ru/?from=petrushka"
    },
    {
      "name": "Виктория",
      "image": "https://cdn.petrushka.ru/victoria-group.png", 
      "delivery": "сегодня 17:00-19:00",
      "external_link": "https://victoria-group.ru/?from=petrushka"
    }
  ]
}


Ошибки, обработку которых нужно учесть:
1) 400 BAD REQUEST;
2) 401 UNAUTHORIZED;
2) 403 FORBIDDEN;
3) 404 NOT FOUND;
4) 500 INTERNAL SERVER ERROR;
5) 503 SERVICE UNAVAILABLE;