# Структура хранилища

Employee хранит данные о сущностях в документоориентированной NoSQL базе данных:

#|
|| **Таблица** | **Описание** | **Ключ** | **Значение** ||
|| `employee.persons` | Хранит сведения о сотрудниках. |
```json
{
    "Guid": < string > 
}
```
|
```json
{
    "Guid": < string >,
    "FullName": {
        "FirstName": < string >,
        "LastName": < string >,
        "MiddleName": < string >
    },
    "InnFl": < string >,
    "Gender": < string >,
    "Citizenship": < string >,
    "BirthDate": < string >,
    "BirthPlace": < string >,
    "Phone": < string >,
    "Email": < string >,
    "RegistrationAddress": {
        // TODO: спросить у разработчика
    },
    "IdentityCard": {
        "DocumentType": < string >,
        "Series": < string >,
        "Number": < string >,
        "Issuer": < string >,
        "IssuanceDate": < string >,
        "IssuerCode": < string >
    },
    "ForeignAddress": < string >
}
```
||
|| `employee.positions` | Хранит должность сотрудника в организации. |
```json
{
    "Guid1": < string >, // guid сотрудника
    "Guid2": < string > // guid организации
}
```
|
```json
{
    "Title": < string > // Должность
}
```
||
|| `employee.roles` | Связывает сотрудника и его место работы с его ролями в организациях.

Значения полей `guid2` и `PersonOrganization` могут совпадать.

|
```json
{
    "Guid2": < string >, // guid организации
    "RoleType": < string > // Тип роли
}
```
|
```json
{
    "Person": < string >, // guid сотрудника, который
                          // исполняет роль в организации из ключа

    "PositionOrganization": <string> // guid организации,
                                     // в которой работает сотрудник

}
```
||
|#