САНКТ-ПЕТЕРБУРГСКИЙ НАЦИОНАЛЬНЫЙ ИССЛЕДОВАТЕЛЬСКИЙ УНИВЕРСИТЕТ

ИНФОРМАЦИОННЫХ ТЕХНОЛОГИЙ, МЕХАНИКИ И ОПТИКИ

ФАКУЛЬТЕТ ИНФОКОММУНИКАЦИОННЫХ ТЕХНОЛОГИЙ



Отчет по лабораторной работе №1 по курсу «Информатика »

**Тема: VirtualBox**

***Чан Тхи Лиен***

***К3140***

1. Скачайте и установите VirtualBox
2. Создание виртуальной машины A с Ubuntu
![1](https://github.com/user-attachments/assets/81ced490-7c8a-4714-9796-43bb88fcd00f)
3. Создание виртуальной машины B и C с Ubuntu
![2](https://github.com/user-attachments/assets/30c2f441-e438-4e28-91d9-10c307da6233)
4. Проверка доступа в интернет на:
- Машина А:

![ping A](https://github.com/user-attachments/assets/b58c2404-cf5b-4476-8b9e-2a82a8bb71fd)

- Машина В:

![ping B](https://github.com/user-attachments/assets/83d6ced1-2244-4978-9f4c-a164836976ee)

- Машина С:

![ping C](https://github.com/user-attachments/assets/fb196ec3-853f-4c96-bba8-45a469602bab)

5. Поиска IP - адрес:

- Машина А:

![ip A](https://github.com/user-attachments/assets/3fd02086-d463-4f8c-a5b9-e6ac104d6219)

- Машина В:

![ip B](https://github.com/user-attachments/assets/84335ef3-38e4-41fc-94dd-6888edd3fedb)

- Машина С:

![ip C](https://github.com/user-attachments/assets/2e85b949-91f4-4b0d-af0a-282f8eef7357)

6. Проверка сетевого доступа

- На машины А:

![may A](https://github.com/user-attachments/assets/9892a740-6969-465f-957e-3396cee44056)

- На машины В:

![may B](https://github.com/user-attachments/assets/6ca73dab-c4a9-409f-a5f8-82b659c31059)

- На машины С:

![may C](https://github.com/user-attachments/assets/b1515ed5-9364-420e-b8a0-17f8095848eb)

7. Запрета доступа из B в C:

Выполнит команду на машины В: **sudo iptables -A OUTPUT -d <<IP - адрес С>> -j DROP**

![chan B den C 2](https://github.com/user-attachments/assets/4c63dba5-b9c2-4b27-b56f-cd0bb9a59861)

Или Выполнит команду на машины C: **sudo iptables -A INPUT -s <<IP - адрес B>> -j DROP**

![chan B den C](https://github.com/user-attachments/assets/1b848b77-083b-4a7e-8eb1-7ce6bbe0934e)

9. Результат:

- машина А:

![may A sau](https://github.com/user-attachments/assets/94218666-6945-42bc-8883-d8ec4c4af4e9)

- машина В:

![may B sau](https://github.com/user-attachments/assets/3e4c9c4a-3df0-4f2a-80c2-982d30371777)

- машина С:

![may C sau](https://github.com/user-attachments/assets/3d5c30ff-1e0d-4e9c-b6ba-0ba4a1789e03)

**Вывод**

- Проверка доступа в интернет на машины
- Проверка сетевого доступа из одной машины на другую машину.
- Запрета доступа из одной машины на другую машину.
