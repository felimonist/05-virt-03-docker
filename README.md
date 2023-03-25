Задание 1.

![slave](https://github.com/felimonist/05-virt-03-docker/blob/main/img/1.JPG)

https://hub.docker.com/r/felimonist/feli/tags
Задание 2.

- Высоконагруженное монолитное java веб-приложение;

> Монолитное веб-приложение вероятно не реализуемо в микропроцессорной архитектуре без изменения кода, а так как приложение высоконагруженное то лучше использовать физический сервер.
- Nodejs веб-приложение;

> Это веб приложение, для таких приложений достаточно докера. В рамках микропроцессрной архитектуры может быть хорошим решением
- Мобильное приложение c версиями для Android и iOS;

> Виртуализация, т.к. docker приложение не имеет UI.
- Шина данных на базе Apache Kafka;

> Это сервис по трансляции данных. Хорошо применить контейнеризацию, так как отсутствуют накладные расходы на виртуализацию, достигается простота масштабирования и управления. 
- Elasticsearch кластер для реализации логирования продуктивного веб-приложения - три ноды elasticsearch, два logstash и две ноды kibana;

> Для прода лучше использовать виртуализация, а отказоустойчивость решается на уровне HA кластера гипервизоров. В тестовой среде возможна реализация в контейнерах (для быстрого разворачивания).
- Мониторинг-стек на базе Prometheus и Grafana;

> системы можно развернуть в docker это бысто и можно масштабировать при необходимости.
- MongoDB, как основное хранилище данных для java-приложения;

> можно использовать виртуальную машину, можно контейнер. Разница вероятно всего в нагруженности сервиса при большой нагрузке лучше использовать виртуальную машину.
- Gitlab сервер для реализации CI/CD процессов и приватный (закрытый) Docker Registry.

> Можно использовать и виртуальную машину и докер контейнер. Докер позволит масштабировать решение, так же удобно обновлять приложение без большого простоя сервиса.
> Использование виртуальной машины позволит удобно администрировать сервис.

Задание 3

![slave](https://github.com/felimonist/05-virt-03-docker/blob/main/img/3.JPG)

![slave](https://github.com/felimonist/05-virt-03-docker/blob/main/img/3.1.JPG)
