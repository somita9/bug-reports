# BR-001 — Страница падает (white screen) при очистке поля Subjects и Date of Birth

- **Severity:** Critical
- **Priority:** High
- **Окружение:** Windows 11 Pro, Google Chrome (143.0.7499.193)
- **Страница:** [Forms → Practice Form](https://demoqa.com/automation-practice-form)

## Preconditions
1. Открыта страница Practice Form

## Steps to Reproduce

### Вариант 1 — Subjects
1. Кликнуть в поле **Subjects**
2. Ввести любой текст (например: `Math`)
3. Полностью удалить введённый текст (Backspace / выделить и удалить)

### Вариант 2 — Date of Birth
1. Кликнуть в поле **Date of Birth**
2. Ввести дату вручную или выбрать дату в календаре
3. Полностью удалить значение в поле (Backspace / выделить и удалить)

## Actual Result
Страница перестает отображаться, появляется белый экран (white screen).

## Expected Result
Страница должна продолжать корректно работать.
Очистка значения в полях **Subjects** и **Date of Birth** не должна приводить к падению страницы.

## Evidence
- Скриншот (DevTools/Console): [BR-001.png](https://github.com/somita9/attachments/blob/main/demoqa/BR-001/BR-001.png)
- Видео: [DEMOQA - Google Chrome 2026-01-13 13-14-04.mp4](https://github.com/somita9/attachments/blob/main/demoqa/BR-001/DEMOQA%20-%20Google%20Chrome%202026-01-13%2013-14-04.mp4)

## Console
- TypeError: Cannot read properties of null (reading 'getMonth') (bundle.js:63 / bundle.js:95)

## Notes
Вероятно, при очистке значения отсутствует проверка перед обращением к `getMonth()`, что приводит к падению страницы.
