# PatternMVP_simplest

#### Преимущества использования паттерна MVP (по сравнению с написанием кода в кнопках форм):
* Лёгкая замена форм. Достаточно реализовать интерфейс IView и можно подключить хоть консоль.
* Бывает, что в источнике данных и в GUI форматы данных не совпадают. В случае MVP, конвертация данных ложиться на presenter. Соответственно, при замене view, придётся менять меньше кода(что и отобразил в этом примере).
* C применением MVP, формы перестают отвечать за порождение источников данных и содержать логику работы программы, а становятся именно средством реализации графического интерфейса.
* Говорят, что с MVP проще тестировать GUI, ведь вместо формы можно подставить mock-объект.

#### Отличия от классической реализации MVP:
В википедии https://ru.wikipedia.org/wiki/Model-View-Presenter сказано:
«Обычно экземпляр Представления создаёт экземпляр Presenterʼа, передавая ему ссылку на себя.»
Но я сделал, чтобы view, как и model, просто предоставлял публичные события и методы. Таким образом, view не нужно создавать  presenter, и хранить/получать ссылки на источник данных. И использование view перестаёт ограничивается лишь presenter'ом.

#### Описание работы программы:
Можно регистрировать ники пользователей.
Если вводится ник, который уже зарегистрирован, то выдаётся сообщение, что такой ник уже занят.
