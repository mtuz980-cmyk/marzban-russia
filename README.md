# Установка панели

`bootstrap.sh.b64` — зашифрованный установщик чистого сервера Ubuntu.

Ключ в этот репозиторий не входит. Команду с ключом храните отдельно.

```
bash <(curl -fsSL https://raw.githubusercontent.com/mtuz980-cmyk/marzban-russia/main/bootstrap.sh.b64 | openssl enc -d -aes-256-cbc -pbkdf2 -a -pass pass:КЛЮЧ)
```

Запускать от root на новой машине, где домен уже указывает на её белый IP. Нужны curl и openssl.

Скрипт для зарубежных машин здесь не лежит. Его создаёт установленная панель и отдаёт по адресу `https://ДОМЕН/join-node.sh`. На ноде спрашивается только короткое имя.