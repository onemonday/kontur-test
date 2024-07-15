# Удаление сотрудника

## Синтаксис запроса {#request}

```
DELETE https://employee-api.kontur.ru/person/{PersonId}
```

### Параметры пути {#path}

#|
{{ path-params-table-header }}
{{ person-id }}
|#

\* — обязательный параметр.

## Формат ответа {#response}

### // TODO: уточнить успешный код возврата у разработчика

Сотрудник успешно удален.

## Пример {#example}

#### Запрос {#example-request}

```shell
curl -X DELETE 'https://employee-api.kontur.ru/person/916c064c-ef20-4613-bdfb-9bed9e0333ac' \
     -H 'Content-Type: application/json'
```

#### Ответ {#example-response}

```json
// TODO: уточнить успешный код возврата у разработчика
```
