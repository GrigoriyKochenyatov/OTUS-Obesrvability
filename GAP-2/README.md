**Домашнее задание**

**Цель:**
*Научиться устанавливать и работать с хранилищем метрик.
В данном дз вы можете воспользоваться наработками из предыдущего.*


*Описание/Пошаговая инструкция выполнения домашнего задания:
Для Prometheus необходимо установить отдельно хранилище метрик (Victoria Metrics, Grafana Mimir, Thanos, etc.)
Во время записи метрики в хранилище Prometheus должен дополнительно добавлять лейбл site: prod
Дополнительные параметры хранилища:
Metrics retention - 2 weeks
В качестве результата дз принимаются - файл конфигурации системы хранения, файл конфигурации Prometheus*

1. Используем ранее созданное окружение ВМ Hyper-V (ОС Debian)
2. Создаем compose для VictoriaMetrics
3. Создаем директорию для хранения volume
4. Настраиваем retention period = 14d в конфигурации VM
5. Настраиваем remote_write для VM в prometheus
6. Запускаем весь комбайн через docker-compose -f docker-compose-prometheus.yml up -d и docker-compose -f docker-compose-victoria.yml up -d
