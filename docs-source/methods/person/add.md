# Создание сотрудника

## Синтаксис запроса {#request}

```
PUT https://employee-api.kontur.ru/person/{PersonId}
```

### Параметры пути {#path}

#|
{{ path-params-table-header }}
{{ person-id }}
|#

\* — обязательный параметр.

### Тело запроса {#body}

#|
|| **Свойство** | **Тип** | **Описание** ||
|| `FullName`* | `object` | [ФИО](#full-name) ||
|| `Innfl` | `string` | ИНН физического лица ||
|| `Gender` | `string` | Пол

{% cut "Возможные значения" %}

// TODO: спросить у разработчика

{% endcut %}

||
|| `Citizenship` | `string` | Гражданство ||
|| `BirthDate` | `string <date-time>` | Дата рождения ||
|| `BirthPlace` | `string` | Место рождения ||
|| `RegistrationAddress` | `object` | [Адрес регистрации](#registration-address) ||
|| `IdentityCard` | `object` | [Удостоверение личности](#identity-card) ||
|| `ForeignAddress` | `object` | Зарубежный адрес ||
|#

\* — обязательное свойство.

##### ФИО `FullName` {#full-name}

{% include notitle [Объект ФИО](../../_includes/full-name.md) %}

\* — обязательное свойство.

##### Адрес регистрации `RegistrationAddress` {#registration-address}

// TODO: спросить у разработчика

##### Удостоверения личности `IdentityCard` {#identity-card}

{% include notitle [Объект удостоверения личности](../../_includes/identity-card.md) %}

## Формат ответа {#response}

### 201: Created {#201}

Сотрудник успешно создан или сотрудник с таким PersonId уже есть.

```json
{
    "Guid": < string >
}
```

#|
{{ properties-table-header }}
|| `Guid` | `string` | GUID сотрудника ||
|#

## Пример {#example}

#### Запрос {#example-request}

```shell
curl -X PUT 'https://employee-api.kontur.ru/person/916c064c-ef20-4613-bdfb-9bed9e0333ac' \
     -H 'Content-Type: application/json' \
     -d '{"FullName": {"FirstName":"Кирилл", "LastName":"Дрешпак", "MiddleName":"Александрович"}}'
```

#### Ответ {#example-response}

```json
201: Created

{
    "Guid": "916c064c-ef20-4613-bdfb-9bed9e0333ac"
}
```
