# BR-001 — Страница падает при вводе и удалении текста в поле Subjects (также в Date of Birth)

- **Severity:** Critical
- **Priority:** High
- **Окружение:** Windows 11 Pro, Google Chrome (143.0.7499.193)
- **Страница:** Forms - Practice Form

## Preconditions
1. Открыта страница Practice Form

## Steps to Reproduce

### Вариант 1 — Subjects
1. Кликнуть в поле **Subjects**
2. Ввести любой текст (например: `Math`)
3. Полностью удалить введённый текст

### Вариант 2 — Date of Birth
1. Кликнуть в поле **Date of Birth**
2. Ввести дату вручную или выбрать дату в календаре
3. Полностью удалить значение в поле (Backspace)

## Actual Result
Страница перестает отображаться, появляется белый экран (white screen).

## Expected Result
Страница должна продолжать корректно работать.
Ввод и удаление значения в полях **Subjects** и **Date of Birth** не должны приводить к падению страницы.

## Evidence
- Видео: `../../attachments/demoqa/BR-001/DEMOQA - Google Chrome 2026-01-13 13-14-04.mp4`

## Notes
Предположительно проблема связана с JavaScript-обработкой события очистки значения поля (возможная ошибка обработки пустого значения).
