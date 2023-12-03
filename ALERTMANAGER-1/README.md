Поднят ALERTMANAGER
Вынесены правила нотификации Prometheus в alert_rules.yml
Сконфигурированы два маршрута ALERTMANAGER

Для теста:
amtool --alertmanager.url=http://localhost:9093/ alert add alertname="test123" severity="test-telegram" job="test-alert" instance="localhost" exporter="none" cluster="test"
