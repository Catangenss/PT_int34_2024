Тестовое задание Int-4 №1 для стажировки PT-START-2024.2

Сценарий Ansible выполнялся на debian-11.11.0-amd64

Для корректного выполнения необходимо соответствие одному из двух условий:
1. На хосте Debian присутствует пользователь, для которого в /etc/sudoers прописаны права "ALL=(ALL:ALL) NOPASSWD:ALL" 
Имя и пароль пользователя, ip debian устанавливаются в inventory для хоста `debian_ansible`
2. На хосте Debian присутствует пользователь с правами применения sudo. Сценраий создаст пользователя ansible и продолжит работу от него.
Имя и пароль пользователя, ip debian устанавливаются в inventory для хоста `debian_sudo`

Выполняются следующие действия:
1. Обновление зависимостей и пакетов
2. Устанавливается часовой пояс Europe/Moscow
3. Создается пара ssh ключей, запрещается аутентификация по паролю, осуществляется подключение по ключам.
4. Устанавливается и включается UFW, открываются порты для SSH и postgresql
5. Конфигурируется sysctl
6. Устанавливается Postgresql 16, разрешается подключение с любого ip
7. Редактируется пользователь postgres, БД наполяется тестовыми данными
8. Последним таском выводятся тестовые данные из postgresql
