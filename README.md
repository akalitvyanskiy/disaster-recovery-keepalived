# Домашнее задание к занятию "Disaster recovery и Keepalived" - Калитвянский Александр SYS-27


### Инструкция по выполнению домашнего задания

   1. Сделайте `fork` данного репозитория к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/git-hw или  https://github.com/имя-вашего-репозитория/7-1-ansible-hw).
   2. Выполните клонирование данного репозитория к себе на ПК с помощью команды `git clone`.
   3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
      - впишите вверху название занятия и вашу фамилию и имя
      - в каждом задании добавьте решение в требуемом виде (текст/код/скриншоты/ссылка)
      - для корректного добавления скриншотов воспользуйтесь [инструкцией "Как вставить скриншот в шаблон с решением](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md)
      - при оформлении используйте возможности языка разметки md (коротко об этом можно посмотреть в [инструкции  по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md))
   4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`);
   5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
   6. Любые вопросы по выполнению заданий спрашивайте в чате учебной группы и/или в разделе “Вопросы по заданию” в личном кабинете.
   
Желаем успехов в выполнении домашнего задания!
   
### Дополнительные материалы, которые могут быть полезны для выполнения задания

1. [Руководство по оформлению Markdown файлов](https://gist.github.com/Jekins/2bf2d0638163f1294637#Code)

---

### Задание 1

- Дана [схема](1/hsrp_advanced.pkt) для Cisco Packet Tracer, рассматриваемая в лекции.
- На данной схеме уже настроено отслеживание интерфейсов маршрутизаторов Gi0/1 (для нулевой группы)
- Необходимо аналогично настроить отслеживание состояния интерфейсов Gi0/0 (для первой группы).
- Для проверки корректности настройки, разорвите один из кабелей между одним из маршрутизаторов и Switch0 и запустите ping между PC0 и Server0.
- На проверку отправьте получившуюся схему в формате pkt и скриншот, где виден процесс настройки маршрутизатора.
 
![Скриншот 1](https://github.com/akalitvyanskiy/disaster-recovery-keepalived/blob/main/img/11.png)
![Скриншот 2](https://github.com/akalitvyanskiy/disaster-recovery-keepalived/blob/main/img/12.png)
![Скриншот 3](https://github.com/akalitvyanskiy/disaster-recovery-keepalived/blob/main/img/13.png)

---

### Задание 2

- Запустите две виртуальные машины Linux, установите и настройте сервис Keepalived как в лекции, используя пример конфигурационного [файла](1/keepalived-simple.conf).
- Настройте любой веб-сервер (например, nginx или simple python server) на двух виртуальных машинах
- Напишите Bash-скрипт, который будет проверять доступность порта данного веб-сервера и существование файла index.html в root-директории данного веб-сервера.
- Настройте Keepalived так, чтобы он запускал данный скрипт каждые 3 секунды и переносил виртуальный IP на другой сервер, если bash-скрипт завершался с кодом, отличным от нуля (то есть порт веб-сервера был недоступен или отсутствовал index.html). Используйте для этого секцию vrrp_script
- На проверку отправьте получившейся bash-скрипт и конфигурационный файл keepalived, а также скриншот с демонстрацией переезда плавающего ip на другой сервер в случае недоступности порта или файла index.html

![Скриншот 1](https://github.com/akalitvyanskiy/disaster-recovery-keepalived/blob/main/img/21.png)
![Скриншот 2](https://github.com/akalitvyanskiy/disaster-recovery-keepalived/blob/main/img/22.png)
![Скриншот 3](https://github.com/akalitvyanskiy/disaster-recovery-keepalived/blob/main/img/23.png)
![Скриншот 4](https://github.com/akalitvyanskiy/disaster-recovery-keepalived/blob/main/img/24.png)
![Скриншот 5](https://github.com/akalitvyanskiy/disaster-recovery-keepalived/blob/main/img/25.png)
![Скриншот 6](https://github.com/akalitvyanskiy/disaster-recovery-keepalived/blob/main/img/26.png)
![Скриншот 7](https://github.com/akalitvyanskiy/disaster-recovery-keepalived/blob/main/img/27.png)
![Скриншот 8](https://github.com/akalitvyanskiy/disaster-recovery-keepalived/blob/main/img/28.png)
![Скриншот 9](https://github.com/akalitvyanskiy/disaster-recovery-keepalived/blob/main/img/29.png)
![Скриншот 10](https://github.com/akalitvyanskiy/disaster-recovery-keepalived/blob/main/img/291.png)
![Скриншот 11](https://github.com/akalitvyanskiy/disaster-recovery-keepalived/blob/main/img/292.png)
![Скриншот 12](https://github.com/akalitvyanskiy/disaster-recovery-keepalived/blob/main/img/293.png)
![Скриншот 13](https://github.com/akalitvyanskiy/disaster-recovery-keepalived/blob/main/img/294.png)
![Скриншот 14](https://github.com/akalitvyanskiy/disaster-recovery-keepalived/blob/main/img/295.png)
![Скриншот 15](https://github.com/akalitvyanskiy/disaster-recovery-keepalived/blob/main/img/296.png)

---

