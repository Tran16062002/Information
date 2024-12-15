САНКТ-ПЕТЕРБУРГСКИЙ НАЦИОНАЛЬНЫЙ ИССЛЕДОВАТЕЛЬСКИЙ УНИВЕРСИТЕТ

ИНФОРМАЦИОННЫХ ТЕХНОЛОГИЙ, МЕХАНИКИ И ОПТИКИ

ФАКУЛЬТЕТ ИНФОКОММУНИКАЦИОННЫХ ТЕХНОЛОГИЙ



Отчет по лабораторной работе №1 по курсу «Информатика »

**Тема: Git Hooks и Git Flow**

***Чан Тхи Лиен***

***К3140***

**Содержание отчета**

**1.	Задание 1 - Автоматизация проверки формата файлов при коммите**

**2.	Задание 2 - Использование Git Flow в проекте**

**Вывод**

## Задание 1 - Автоматизация проверки формата файлов при коммите

*Для выполнения этой задачи, можно использовать **Git Hook**.*

1. Создать папку **.git/hooks**.

 ```bash
   mkdir -p .git/hooks
   ```
![1 1](https://github.com/user-attachments/assets/bc19f7f0-fc66-4fba-9b85-ac0a20861e8a)

2. В папке **.git/hooks** создать файл **pre-commit**.

```bash
   nano pre-commit
   ```
![1 2](https://github.com/user-attachments/assets/46f1f618-3f8e-4a77-81e6-1f5a3a7857d5)

3. Вставить в этот файл следующий код.

![1 3](https://github.com/user-attachments/assets/6be9c68c-1034-4c1b-8cde-3054286da484)

4. Сделать файл исполнимым.

 ```bash
   chmod +x pre-commit
   ```
![1 4](https://github.com/user-attachments/assets/5281d331-2047-425b-acc2-ded75847934a)

5. Создать файл тескта **example.txt**.

```bash
   touch example.txt
   nano example.txt
   ```
![1 5](https://github.com/user-attachments/assets/247ba1b0-8d94-4092-a23f-3907a76dd076)

![1 5-1](https://github.com/user-attachments/assets/c09716b1-7443-4d5c-8d48-d3d97b009422)

6. Если в файле нет подписи автора.

![1 6](https://github.com/user-attachments/assets/d1511c23-901d-4d53-8aa9-345cdcad8eba)

Результат: 

![1 7](https://github.com/user-attachments/assets/82765ce3-c529-4d1c-bc63-29b0a0504559)

7. Если в файле есть подпись автора.

![1 8](https://github.com/user-attachments/assets/620bc717-99e8-4d3a-a707-03b1e9f67c95)

Результат:

![1 9](https://github.com/user-attachments/assets/944cc1e4-90ea-4890-9e40-22716af90e78)

## Задание 2 - Использование Git Flow в проекте

1. Проверка Git Flow.

 ```bash
   git flow version
   ```
![2 1](https://github.com/user-attachments/assets/769fdcd4-2248-4ac0-b1f7-218ae6819ca7)

2. В корне репозитория выполнить инициализацию Git Flow.

 ```bash
   git flow init
   ```
![2 2](https://github.com/user-attachments/assets/1f04bb97-7590-4ab8-8391-e91fe47b2dbd)

3. Создать ветку для новой функциональности.

 ```bash
   git flow feature start task-management
   ```
![2 3](https://github.com/user-attachments/assets/60e2048f-5f38-44ae-b84d-8ba363baafed)

4. Создать файл **task_manager.py**.

```bash
   nano task_manager.py
   ```
![2 4](https://github.com/user-attachments/assets/45ae9342-86ba-42ef-af6d-a0a974550b71)

Содержение:

![2 5](https://github.com/user-attachments/assets/5d373678-5479-4fde-9b91-c3f94b9f7179)

5. Добавить и выполнить коммит файла.

```bash
   git add task_manager.py
   git commit -m "Добавлен функционал управления задачами"
   ```
![2 6](https://github.com/user-attachments/assets/9055d223-c085-4b90-b0c3-f64536d671e5)

6. После завершения разработки функции.

```bash
   git flow feature finish task-management
   ```
![2 7](https://github.com/user-attachments/assets/fbc850ac-9a06-4285-8ba9-7d0cb197032d)

7. Создать ветку для новой функциональности.

```bash
   git flow release start v1.0.0
   ```
![2 8](https://github.com/user-attachments/assets/1bc839a4-ef4f-4227-9420-2f0974049eac)

8. Создать файл текста **version.txt**.

```bash
   nano version.txt
   ```
![2 9(0)](https://github.com/user-attachments/assets/b5385f5a-da9b-47a1-8c7b-227eda435857)

![2 9](https://github.com/user-attachments/assets/e028f19f-1f92-4567-8243-25ce6021fdc3)

9. Добавить и выполнить коммит файла.

```bash
   git add version.txt
   git commit -m "Обновлена версия для релиза v1.0.0"
   ```
![2 10](https://github.com/user-attachments/assets/4ea7a853-d670-4786-b213-5b25f3637bf7)

10. Завершить релиз и объединить его с ветками "develop" и "main".

```bash
   git flow release finish v1.0.0
   ```
![2 11](https://github.com/user-attachments/assets/7602a1e5-1f15-46d4-bd4a-61ffa7c7fb58)

11. Создать **hotfix** (у нас конечно же ошибки никакой не возникнет, но hotfix все равно создаем).

```bash
   git flow hotfix start hotfix-1.0.1
   ```
![2 12](https://github.com/user-attachments/assets/7b80b4ae-d7cf-4c58-9077-32c582ce389e)

12. Создать файл **file_with_error.py**.

![2 13](https://github.com/user-attachments/assets/c0bcd4d3-133b-4fd7-822e-5eb0c76b7549)

Например:

![2 14](https://github.com/user-attachments/assets/ee508bf8-6c18-4f2f-a543-8490942dd526)

13. Добавить и выполнить коммит файла.

```bash
   git add file_with_error.py
   git commit -m "Исправлена критическая ошибка"
   ```
![2 15](https://github.com/user-attachments/assets/1621c8ed-a586-48fd-aac4-3204ac8cfd42)

14. Завершить hotfix и объединить его с ветками "develop" и "main":

```bash
   git flow hotfix finish hotfix-1.0.1
   ```
![2 16](https://github.com/user-attachments/assets/0530d2da-b9d5-4c0a-899b-7eb1528c4a99)

15. Завершение работы и отправка изменений на удаленный репозиторий.

```bash
   git push origin develop
   git push origin main
   ```

![2 17](https://github.com/user-attachments/assets/ef7d62e3-8e7e-4672-b878-84e1ebc79852)

![2 18](https://github.com/user-attachments/assets/71c23d32-8d3a-4d84-adcc-1ad7ca4d3eeb)

## Вывод

- Работа с ветками
- Работа с удаленным репозиторием
- Моделирование конфликта
- Разрешение конфликта
