# BR-001 — Страница падает при вводе и удалении текста в поле Subjects

- **Severity:** Critical
- **Priority:** High
- **Окружение:** Windows 11 Pro, Google Chrome (143.0.7499.193)
- **Страница:** Forms - Practice Form

## Preconditions
1. Открыта страница Practice Form

## Steps to Reproduce
1. Кликнуть в поле **Subjects**
2. Ввести любой текст (например: `Math`)
3. Полностью удалить введённый текст

## Actual Result
Страница перестает отображаться, появляется белый экран (white screen).

## Expected Result
Страница должна продолжать корректно работать.
Ввод и удаление текста в поле Subjects не должны приводить к падению страницы.

## Evidence
- Видео: `../../attachments/demoqa/BR-001/DEMOQA - Google Chrome 2026-01-13 13-14-04.mp4`


## Notes
Предположительно проблема связана с JavaScript-обработкой события очистки значения поля Subjects.

