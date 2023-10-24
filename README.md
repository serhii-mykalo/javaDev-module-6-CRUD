# Module 6 [CRUD, міграції баз даних]

## Завдання №1 - використай міграції
Візьми проєкт з попереднього ДЗ. Цей проєкт завантажує та виконує 2 файли - `sql/init_db.sql` та \```sql/populate_db.sql\```.

Підключи фреймворк для міграцій flyway, та напиши 2 міграції - V1__init_db.sql та V2__populate_db.sql відповідно. Прибери з проєкту старий код, який завантажував та виконував SQL файли - тепер це має робити движок міграцій flyway.

Запусти проєкт та переконайсь, що flyway коректно налаштований та виконує обидві міграції. В логах ти маєш побачити, що обидві міграції виконались.

## Завдання №2 - напиши сервіс для CRUD операцій для сутності client
Напиши клас з назвою ClientService. Цей клас призначений для CRUD операцій з клієнтами. Мають бути наступні методи:

long create(String name) - додає нового клієнта з іменем name. Повертає ідентифікатор щойно створеного клієнта.
String getById(long id) - повертає назву клієнта з ідентифікатором id
void setName(long id, String name) - встановлює нове ім'я name для клієнта з ідентифікатором id
void deleteById(long id) - видаляє клієнта з ідентифікатором id
List<Client> listAll() - повертає всіх клієнтів з БД у вигляді колекції об'єктів типу Client (цей клас створи сам, у ньому має бути 2 поля - id та name)
Передбач валідацію вхідних даних в методах класу ClientService. Якщо якісь вхідні дані некоректні (наприклад, ми намагаємось створити клієнта з занадто коротким чи довгим іменем) - відповідний метод має викидати Exception.

Завдання №3 - залий код на github
Створи новий репозиторій на GitHub. Додай туди всі необхідні файли твого проєкту. Переконайсь, що в репозиторії немає зайвих файлів.

Результат виконання ДЗ - GitHub репозиторій зі всіма файлами.
