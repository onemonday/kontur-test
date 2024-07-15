# Редактирование должности

## Синтаксис запроса {#request}

```
PUT https://employee-api.kontur.ru/position/{PersonId}
```

//TODO: PersonId в этом методе не может быть токеном идемпотентности

// TODO: уточнить метод и эндпоинт у разработчика

### Тело запроса {#body}

```json
{
    "Organization": < string >,
    "Title": < string >
}
```

#|
{{ properties-table-header }}
|| `Organization`* | `string` | GUID организации ||
|| `Title` | `string` | Должность сотрудника в организации ||
|#

\* — обязательный параметр.

## Формат ответа {#response}

### // TODO: уточнить успешный код возврата у разработчика

Должность успешно отредактирована.

## Пример {#example}

#### Запрос {#example-request}

```shell
curl -X POST 'https://employee-api.kontur.ru/position/916c064c-ef20-4613-bdfb-9bed9e0333ac' \
     -H 'Content-Type: application/json' \
     -d '{"Organization":"e6e9e527-a3e7-4a9f-a326-373aafc3023e", "Title":"C# Developer"}'
```

#### Ответ {#example-response}

```json
// TODO: уточнить успешный код возврата у разработчика
```
