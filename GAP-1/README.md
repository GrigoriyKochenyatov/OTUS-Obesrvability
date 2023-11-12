** Домашнее задание №1 **
1. Создаем ВМ Hyper-V (ОС Debian)
2. Устанавливаем PHP-FPM, MySQL (MariaDB), NGINX
3. Скачиваем и разворачиваем WordPress
4. Настраиваем подключение WP к СУБД, а также виртуальные хосты NGINX
5. Устанавливаем DOCKER (пришлось повозиться с ca-certificate т.к в Debian12 отсутствует корневой сертификат Amazon_RSA_2048_M01.crt)
   - решение: скачиваем в /usr/local/share/ca-certificates/amazon/Amazon_RSA_2048_M01.crt публичный сертификат Амазона, выполняем update-ca-certificates, профит
6. Пишем композики (отдельно для Прометея, отдельно для Экспортеров написал), делаем конфигурации
7. Запускаем весь комбайн через docker-compose -f docker-compose-prometheus.yml up -d и docker-compose -f docker-compose-exporters.yml up -d
