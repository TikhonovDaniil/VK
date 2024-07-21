# VK
Из-за ошибки авторизации 
"Не указан обязательный параметр client_id"
неудалось выполнить запрос. Ввиду наличия ошибки, вместо кода, высылаю набор тест-кейсов:

**Тест кейс 1**

Получение ошибки 403 с пустыми полями авторизации\
Выполнить POST запрос с пустым полем авторизации\
Проверить, что status code = 403

**Тест кейс 2**

Получение ошибки 403 неверный пароль\
Выполнить POST запрос с неверным паролем \
Проверить, что status code = 403

**Параметризированный Тест кейс 3**

Получение ошибки 400 не указан обязательный параметр [group_id, counterTypes]\
Выполнить POST запрос без обязательных параметров\
Проверить, что status code = 400

**Параметризированный тест кейс 4**

Получение счетчиков группы [themes, photo_albums, members videos, presents, links, moderators, join_requests, black_list, maybe, photos, всех счетчиков]

counterTypes = [themes, photo_albums, members videos, presents, links, moderators, join_requests, black_list, maybe, photos, всех счетчиков]

Выполнить POST запрос с counterTypes = [counterTypes[i]]\
Проверить, что status code = 200\
Проверить, что <counterTypes> в теле ответа не пустой
