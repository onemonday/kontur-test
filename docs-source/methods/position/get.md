# Просмотр должности сотрудника

## Синтаксис запроса {#request}

```
GET https://employee-api.kontur.ru/position/{PersonId}/{OrganizationId}
```

// TODO: уточнить эндпоинт у разработчика

### Параметры пути {#path}

#|
{{ path-params-table-header }}
{{ person-id }}
{{ organization-id }}
|#

\* — обязательный параметр.

## Формат ответа {#response}

### 200: OK {#200}

Вывод должности сотрудника.

```json
{
    "O{OrganizationId}<->P{PersonId}": "{Title}"
}
```

#|
{{ properties-table-header }}
|| `OrganizationId` | `string` | GUID организации ||
|| `PersonId` | `string` | GUID сотрудника ||
|| `Title` | `string` | Должность сотрудника в организации ||
|#

## Пример {#example}

#### Запрос {#example-request}

```shell
curl -X GET 'https://employee-api.kontur.ru/position/916c064c-ef20-4613-bdfb-9bed9e0333ac/b840a338-cd73-4097-bdf9-519281873213' \
     -H 'Content-Type: application/json'
```

#### Ответ {#example-response}

```json
200: OK

{
    "Оb840a338-cd73-4097-bdf9-519281873213<->P916c064c-ef20-4613-bdfb-9bed9e0333ac": "C# Developer"
}
```
