# Сотрудник (Person)

Person — сущность, описывающая сведения о сотруднике.

## Свойства {#properties}

#|
|| **Свойство** | **Тип** | **Описание** ||
|| `guid`* | `Guid` | GUID сотрудника ||
|| `fullName`* | `FullName` | [ФИО](#full-name) ||
|| `innFl` | `string` | ИНН физического лица ||
|| `gender` | `Gender? (enum)` | Пол

{% cut "Возможные значения" %}

// TODO: спросить у разработчика

{% endcut %}

||
|| `citizenship` | `string` | Гражданство ||
|| `birthDate` | `DateTime?` | Дата рождения ||
|| `birthPlace` | `string` | Место рождения ||
|| `registrationAddress` | `ExtendedAddress` | [Адрес регистрации](#registration-address) ||
|| `identityCard` | `IdentityCard` | [Объект удостоверения личности](#identity-card) ||
|| `foreignAddress` | `ForeignAddress` | Зарубежный адрес ||
|#

\* — обязательное свойство.

#### ФИО (FullName) {#full-name}

#|
|| **Свойство** | **Тип** | **Описание** ||
|| `firstName`* | `string` | Имя ||"
|| `lastName`* | `string` | Фамилия ||"
|| `middleName` | `string` | Отчество ||"
|#

\* — обязательное свойство.

#### Адрес регистрации (registrationAddress) {#registration-address}

// TODO: спросить у разработчика

#### Удостоверение личности (IdentityCard) {#identity-card}

#|
|| **Свойство** | **Тип** | **Описание** ||
|| `documentType` | `string` | Тип документа ||"
|| `series` | `string` | Серия ||"
|| `number` | `string` | Номер ||"
|| `issuer` | `string` | Кем выдан ||"
|| `issuanceDate` | `DateTime?` | Дата выдачи ||"
|| `issuanceDate` | `string <date-time>` | Дата выдачи ||"
|| `issuerCode` | `string` | Код подразделения ||"
|#
