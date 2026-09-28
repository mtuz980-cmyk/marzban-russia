# Установщики

Ключи в репозиторий не входят.

`bootstrap.sh.b64` — прежний зашифрованный установщик.

`bootstrap-russia-v3.sh.b64` — текущий скрипт `bootstrap-russia.sh` без изменений, тоже зашифрован.

Скачать и запустить текущий скрипт от root, сохранив его в файл:

```
apt-get update && apt-get install -y curl openssl
curl -fsSL https://raw.githubusercontent.com/mtuz980-cmyk/marzban-russia/main/bootstrap-russia-v3.sh.b64 | openssl enc -d -aes-256-cbc -pbkdf2 -a -pass pass:КЛЮЧ -out /root/bootstrap-russia-v3.sh
bash /root/bootstrap-russia-v3.sh
```