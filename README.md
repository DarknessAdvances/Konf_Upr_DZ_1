# Readme.md для программы эмулятора оболочки

## Обзор
Эмулятор оболочки — это программа, которая имитирует базовые команды оболочки для взаимодействия с виртуальной файловой системой. Она позволяет пользователям перемещаться по директориям, изменять права доступа, удалять файлы и отображать содержимое файлов.

## Возможности
- **Список файлов**: Используйте команду `ls` для отображения файлов в текущей директории.
- **Смена директории**: Перемещайтесь по директориям с помощью команды `cd`.
- **Изменение прав доступа**: Изменяйте права доступа к файлам с помощью команды `chmod`.
- **Удаление файлов/каталогов**: Удаляйте файлы или каталоги рекурсивно с помощью команды `rm`.
- **Отображение содержимого файла**: Просматривайте содержимое файлов с помощью команды `cat`.

## Установка
1. Убедитесь, что у вас установлен Python.
2. Скачайте исходный код из репозитория.
3. Установите необходимые зависимости (если применимо).

## Использование
Для запуска эмулятора оболочки используйте следующую команду:

```bash
python emulator.py <путь_к_tar_архиву>
```

Замените `<путь_к_tar_архиву>` на путь к вашему tar-архиву, содержащему виртуальную файловую систему.

## Команды
### Доступные команды
- `ls`: Выводит файлы в текущей директории.
- `cd <директория>`: Переход в указанную директорию.
- `chmod <права> <имя_файла>`: Изменяет права доступа к файлу.
- `rm <имя_файла>`: Удаляет файл или директорию.
- `cat <имя_файла>`: Отображает содержимое файла.
- `exit`: Выход из эмулятора.

### Пример использования
```bash
emulator:/home$ ls
documents
music
emulator:/home$ cd documents
emulator:/home/documents$ ls
file1.txt
file2.txt
emulator:/home/documents$ cat file1.txt
```

## Обработка ошибок
Эмулятор предоставляет обратную связь по различным условиям ошибок, включая:
- Неизвестные команды.
- Директория не найдена или недоступна из-за проблем с правами.
- Файл не найден при попытке чтения или удаления.
