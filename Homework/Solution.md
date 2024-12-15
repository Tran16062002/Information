САНКТ-ПЕТЕРБУРГСКИЙ НАЦИОНАЛЬНЫЙ ИССЛЕДОВАТЕЛЬСКИЙ УНИВЕРСИТЕТ

ИНФОРМАЦИОННЫХ ТЕХНОЛОГИЙ, МЕХАНИКИ И ОПТИКИ

ФАКУЛЬТЕТ ИНФОКОММУНИКАЦИОННЫХ ТЕХНОЛОГИЙ



Отчет по лабораторной работе по курсу «Информатика »

**Тема: Grep**

***Чан Тхи Лиен***

***К3140***

1. Поиск без учета регистра.

- Создать файл `text1.txt`.

Например: ФИО студентов и их оценки.

![1 0](https://github.com/user-attachments/assets/4b2051ef-8fcc-400e-a6ca-155ec4bc2a6d)

- Использовать **grep -i "$" text1.txt** ($ - это слово (цифр) без регистра, которое нужно найти).

![1 1](https://github.com/user-attachments/assets/98396150-da0c-475d-8bda-aad8132e915b)

![1 2](https://github.com/user-attachments/assets/f2172abc-72e5-4bb9-9410-cf9df5822a84)

- Если имеет много строк, содержающих слово, возвращает все строки.

![1 5](https://github.com/user-attachments/assets/67eb2a3e-6f0f-44e7-bfa7-9208b993d5a3)

2. Поиск в нескольких файлах.
 - Создать файл `text2.txt` и `text3.txt`.

![2 0](https://github.com/user-attachments/assets/fec474f5-a3c1-4e25-82e1-2a7549d8348e)

![2 1](https://github.com/user-attachments/assets/88ad70a1-ec96-4a32-a940-2f26734beb0f)

- Использовать **grep "$" text1.txt text 2.txt text3.txt** для возвращения всех строк, содержающих слово, в файлов *text1.txt text 2.txt text3.txt*.

![2 2](https://github.com/user-attachments/assets/0669a3dd-5e0b-42df-bfae-018acf71f113)

![2 3](https://github.com/user-attachments/assets/825414c1-7b17-42c9-b467-c5a2f069bc72)

3. Поиск номера строк.

-  Использовать **grep -n "$" text1.txt** для поиска номер строк, содержающих слово.

![3 1](https://github.com/user-attachments/assets/1b495f7d-5bf7-44ba-9da5-3203eaeff863)

В файле **text1.txt** студент, фамилия которого - *Попов* появляет в восьмой строке.

![3 2](https://github.com/user-attachments/assets/85c876b1-6fdd-4f98-a2d2-6de01bdb342b)

Можно найти номер строк в многих файлах.

4. Подсчёт количества строк.

- Использовать **grep -c "$" text1.txt** для подчёта количества строк.

![4 1](https://github.com/user-attachments/assets/fb4cfb38-2cd0-4db7-9006-d5d9350f4c45)

Посчитать количество студентов, которые имеют 10 баллов.

![4 2](https://github.com/user-attachments/assets/d9e648b9-8c65-434a-b5ff-a4a7b5937f51)

Посчитать количество студентов, которые имеют отчество - Алексеевна.

5. Поиск по регулярным выражениям.

- Использовать **grep -E "^$" text1.txt** для поиска строк, начинающихся с любой буквой ($ - это буква).

![5 1](https://github.com/user-attachments/assets/1f41b8d0-3d6e-4f20-bcec-bb819ac9557c)

![5 2](https://github.com/user-attachments/assets/49bffdd2-987b-40fc-b26f-79b1d7320810)

Можно найти строки, начинающихся с любыми буквами.

6. Использование команды **grep** с логическими операторами.

- Использовать **grep -E "$1|$2" text1.txt** для поиска строк, содержающих слово $1 или $2 ($1, $2 - это слово или цифр).

![6 1](https://github.com/user-attachments/assets/10564550-3401-4c34-b513-716f1974e44d)

![6 2](https://github.com/user-attachments/assets/7ed948a0-307f-4763-b8d5-3582ce9f820c)

7.  Инвертированный поиск.

- Использовать **grep -v "$2" text1.txt** для поиска строк, не содержающих слово (цифр).

![7 1](https://github.com/user-attachments/assets/a0cc5a52-4562-47f7-afee-6bb044acfa4a)

![7 2](https://github.com/user-attachments/assets/04cc2ad7-d0f7-4a25-a53b-d0b35839b5df)

8. Рекурсивный поиск.

- Если нужно найти строки в многих файлах, создать папку, содержающую все файлы.

- Использовать **grep -r "$2" practice** для поиска строки в папке **practice**.

![8 1](https://github.com/user-attachments/assets/405064ed-111b-4704-a047-5a7ac748d809)

![8 2](https://github.com/user-attachments/assets/b50c7912-fee5-4bf8-9944-00eccecce4df)


***Вывод**:

- Знакомство с команду **grep**.
- Изучение и использование метода с командой **grep** для поиска информации в файле и папке.
