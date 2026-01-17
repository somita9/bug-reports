# BR-003 - Web Tables: пробелы в First Name/Last Name проходят валидацию как валидные значения

- **Severity:** Medium
- **Priority:** Medium
- **Окружение:** Windows 11 Pro, Google Chrome (143.0.7499.193)
- **Страница:** Elements > Web Tables

## Preconditions
1. Открыта страница Web Tables

## Steps to Reproduce
1. Нажать кнопку **Add**
2. В поле **First Name** ввести только пробелы (например: `␠␠␠`)
3. В поле **Last Name** ввести только пробелы (например: `␠␠␠`)
4. Кликнуть вне поля (чтобы сработала валидация)

## Actual Result
Поля с пробелами отображаются как валидные (зелёная рамка и галочка).

## Expected Result
Значения, состоящие только из пробелов, должны считаться пустыми и отображаться как невалидные / обязательные к заполнению.

## Evidence
- Скриншот: [BR-003.png](https://github.com/somita9/attachments/blob/main/demoqa/BR-003/BR-003.png)

