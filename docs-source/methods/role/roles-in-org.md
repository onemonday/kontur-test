# Просмотр всех ролей в организации

## Синтаксис запроса {#request}

```
GET https://employee-api.kontur.ru/roles/{OrganizationId}
```

// TODO: уточнить эндпоинт у разработчика

### Параметры пути {#path}

#|
{{ path-params-table-header }}
{{ organization-id }}
|#

\* — обязательный параметр.

## Формат ответа {#response}

### // TODO: уточнить успешный код возврата у разработчика {#200}

Вывод списка всех ролей в организации.

```json
{
    "{RoleType}": "{Person}/{Position}",
    ...
}
```

#|
|| **Свойство** | **Тип** | **Описание** ||
|| `RoleType` | `string` | Тип роли

{% cut "Возможные значения" %}

- `Head` — руководитель;
- `ChiefAccountant` — главный бухгалтер;
- `Sender` — уполномоченный представитель;
- `Ip` — индивидуальный предприниматель.

{% endcut %}
||
|| `Person` | `string` | GUID сотрудника ||
|| `Position` | `string` | Должность сотрудника ||
|#

## Пример {#example}

#### Запрос {#example-request}

```shell
curl -X GET 'https://employee-api.kontur.ru/roles/c59793e3-ab1d-41f9-b229-0777e59b787c' \
     -H 'Content-Type: application/json'
```

#### Ответ {#example-response}

```json
// TODO: уточнить успешный код возврата у разработчика

{
    "Head": "8aeac99b-2580-4e55-8d50-f6a9bd92e1ec/Директор",
    "Sender": "1406f828-1563-4f1b-8cf6-50c9beabf8f5/Специалист"
}
```
