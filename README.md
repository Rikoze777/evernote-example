# evernote-example
Упражнение на чтение кода. Взаимодействие с API Evernote.

## Как установить
  Для начала работы вам необходимо получить `Consumer Key` и `Consumer Secret` [здесь](https://dev.evernote.com/doc/). 
А также `API token` [здесь](https://dev.evernote.com/get-token/)

Далее в корне папки необходимо создать пустой `.env` файл и записать туда следующие переменные

*EVERNOTE_CONSUMER_KEY=`Consumer Key`

*EVERNOTE_CONSUMER_SECRET=`Consumer Secret`

*EVERNOTE_PERSONAL_TOKEN=`API Token`

*JOURNAL_TEMPLATE_NOTE_GUID= GUID вашего шаблона

*JOURNAL_NOTEBOOK_GUID=GUID записи для создания заметок

*INBOX_NOTEBOOK_GUID=GUID записи для получения заметок

Python3 должен быть уже установлен. Затем используйте pip (или pip3, есть конфликт с Python2) для установки зависимостей:

`pip install -r requirements.txt`

## Запуск

### config
Файл, для хранения личных данных для работы с заметками.

### list_notebooks.py

Команда `python3 list_notebooks.py` - вывдет `id` заметок и их название. Полученные данные можно подставить `JOURNAL_NOTEBOOK_GUID` и `INBOX_NOTEBOOK_GUID`

Пример успешного запуска (id в примере выдуман):
`5e22324b-723c-4f232-a123b-2123156085 - Первый блокнот` 

### dump_inbox
Команда `python3 dump_inbox` - выводит содержимое заметок с ее `id`.

Пример успешного запуска:
```
--------- 1 ---------


213123123

--------- 2 ---------


11
```

### add_note2journal.py

Команда `python3 add_note2journal.py` создает заметку сегодняшней датой.

Пример успешного запуска:
```
Title Context is:
{
    "date": "2022-12-23",
    "dow": "пятница"
}
Done
```
