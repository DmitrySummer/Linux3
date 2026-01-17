Ошибка возникает из-за того, что вы пытаетесь установить очень старую версию Tor (0.3.2.10 из 2018 года) на современную версию Ubuntu (вероятно, 22.04 или 24.04), где необходимые ей библиотеки (libssl1.1 и libevent-2.1-6) заменены на более новые версии или удалены из стандартных репозиториев.

Установить через apt последнюю версию 
sudo apt update
sudo apt install tor

Если нужен именно пакет tor_0.3.2.10: 
wget http://security.ubuntu.com/ubuntu/pool/main/o/openssl/libssl1.1_1.1.1f-1ubuntu2.22_amd64.deb
sudo dpkg -i libssl1.1_1.1.1f-1ubuntu2.22_amd64.deb

либо sudo apt install libevent-2.1-7  # Попробуйте установить актуальную версию, иногда срабатывает совместимость
# Если не помогло:
sudo apt install libevent-2.1-64
Потом исправить зависимости 
sudo apt install -f

