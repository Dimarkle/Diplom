#  Дипломная работа по профессии «Системный администратор»  Рогачев Дмитрий

## Задача
Ключевая задача — разработать отказоустойчивую инфраструктуру для сайта, включающую мониторинг, сбор логов и резервное копирование основных данных. Инфраструктура должна размещаться в [Yandex Cloud](https://cloud.yandex.com/). Задание расположено по [ссылке](https://github.com/netology-code/sys-diplom/blob/main/README.md).
## Инфраструктура
Для развёртки инфраструктуры использовал  [Terraform](https://github.com/Dimarkle/Diplom/tree/main/terraform) и [Ansible](https://github.com/Dimarkle/Diplom/tree/main/ansible).

### Terraform
* Поднял инфраструктуру в Яндекс Облаке с помощью [Terraform](https://github.com/Dimarkle/Diplom/tree/main/terraform)

![default-—-Дашборд-каталога-Yandex-Cloud](https://github.com/Dimarkle/Diplom/assets/118626944/d64b0178-614c-43b8-ad86-d405d80efe66)
___
![Виртуальные-машины-Yandex-Compute-Cloud](https://github.com/Dimarkle/Diplom/assets/118626944/ade2ac42-837e-47e6-89ce-e75dd376c927)
___
* Также с помощью Terraform создал  резервное копирование (snapshot) дисков всех ВМ

![Снимки-дисков-Yandex-Compute-Cloud](https://github.com/Dimarkle/Diplom/assets/118626944/d364e17a-0176-445f-a3bb-fe5bca539127)
___
![Обзор](https://github.com/Dimarkle/Diplom/assets/118626944/0e199655-38de-4b4e-b88e-4d829bd93702)
___
* Получаем выходные параметры: 
___
![Снимок экрана от 2023-05-21 14-15-13](https://github.com/Dimarkle/Diplom/assets/118626944/bb408c20-1f5b-4c61-83f1-d9902ffd35b9)
___
* Сгенерирован  [hosts.ini](https://github.com/Dimarkle/Diplom/blob/main/ansible/inventory/hosts.ini) ansible.
___
### Ansible
* С помощью [Ansible](https://github.com/Dimarkle/Diplom/tree/main/ansible) установил необходимые сервисы на виртуальных машинах:
* [elasticsearch-playbook.yml](https://github.com/Dimarkle/Diplom/blob/main/ansible/elasticsearch-playbook.yml)


![Снимок экрана от 2023-05-21 14-15-50](https://github.com/Dimarkle/Diplom/assets/118626944/10ad7cec-6f4e-4e54-a443-0845b6b2b33e)
___

* [grafana-playbook.yml](https://github.com/Dimarkle/Diplom/blob/main/ansible/grafana-playbook.yml) Создал user (Admin) и пароль (12345) 
![Снимок экрана от 2023-05-21 14-16-55](https://github.com/Dimarkle/Diplom/assets/118626944/df44d346-3c26-44cd-92cf-c80a67adeb3c)
___
* [prometheus-playbook.yml](https://github.com/Dimarkle/Diplom/blob/main/ansible/prometheus-playbook.yml)
![Снимок экрана от 2023-05-21 14-16-33](https://github.com/Dimarkle/Diplom/assets/118626944/5a4f74dc-e482-44d7-ace2-37638e791a89)
___
* [kibana-playbook.yml](https://github.com/Dimarkle/Diplom/blob/main/ansible/kibana-playbook.yml)
![Снимок экрана от 2023-05-21 14-16-17](https://github.com/Dimarkle/Diplom/assets/118626944/2cb9d977-1731-4399-b9f2-be97477165ed)
___

* [servers-playbook.yml](https://github.com/Dimarkle/Diplom/blob/main/ansible/servers-playbook.yml)
![Без имени](https://github.com/Dimarkle/Diplom/assets/118626944/0162cbfd-475f-4062-8abc-8c388578035c)
___
## Итоги:
* Сайт доступен по андресу: http://51.250.23.14/

![Снимок экрана от 2023-05-21 14-23-39](https://github.com/Dimarkle/Diplom/assets/118626944/7d508eb6-23a5-4a78-9523-24262adf6fae)
___
* Kibana доступна по адресу: http://158.160.65.138:5601/app/home#/
![1](https://github.com/Dimarkle/Diplom/assets/118626944/abbf9f59-c066-4a1a-94de-15ce0cdce398)
___
![2](https://github.com/Dimarkle/Diplom/assets/118626944/531780fe-0bc8-414c-85c0-ada1cfd33c23)
___
![3](https://github.com/Dimarkle/Diplom/assets/118626944/5e081dea-945e-4270-9bef-64d7fb7f87c2)
___

