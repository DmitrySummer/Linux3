чтобы удалить не только саму библиотеку, но и её конфигурационные файлы:
sudo apt purge libjs-jquery-jush

Чтобы удалить пакеты, которые были установлены автоматически вместе с libjs-jquery-jush и больше не нужны:
sudo apt autoremove --purge
