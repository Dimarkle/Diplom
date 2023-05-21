#  Дипломная работа по профессии «Системный администратор»  Рогачев Дмитрий

## Задача
Ключевая задача — разработать отказоустойчивую инфраструктуру для сайта, включающую мониторинг, сбор логов и резервное копирование основных данных. Инфраструктура должна размещаться в [Yandex Cloud](https://cloud.yandex.com/). Задание расположено по [ссылке](https://github.com/netology-code/sys-diplom/blob/main/README.md).
## Инфраструктура
Для развёртки инфраструктуры использовал  [Terraform](https://github.com/Dimarkle/Diplom/tree/main/terraform) и [Ansible](https://github.com/Dimarkle/Diplom/tree/main/ansible).

### Terraform
* Поднял инфраструктуру в Яндекс Облаке с помощью [Terraform](https://github.com/Dimarkle/Diplom/tree/main/terraform)

![default-—-Дашборд-каталога-Yandex-Cloud](https://github.com/Dimarkle/Diplom/assets/118626944/d64b0178-614c-43b8-ad86-d405d80efe66)

![Виртуальные-машины-Yandex-Compute-Cloud](https://github.com/Dimarkle/Diplom/assets/118626944/ade2ac42-837e-47e6-89ce-e75dd376c927)
* Также с помощью Terraform создал  резервное копирование (snapshot) дисков всех ВМ

![Снимки-дисков-Yandex-Compute-Cloud](https://github.com/Dimarkle/Diplom/assets/118626944/d364e17a-0176-445f-a3bb-fe5bca539127)

![Обзор](https://github.com/Dimarkle/Diplom/assets/118626944/0e199655-38de-4b4e-b88e-4d829bd93702)

* Получаем выходные параметры: 

![Снимок экрана от 2023-05-21 14-15-13](https://github.com/Dimarkle/Diplom/assets/118626944/bb408c20-1f5b-4c61-83f1-d9902ffd35b9)

* Сгенерирован  [hosts.ini](https://github.com/Dimarkle/Diplom/blob/main/ansible/inventory/hosts.ini)
___
