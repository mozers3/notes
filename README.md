# Starred Files — PWA для Google Drive

Это PWA-оболочка для веб-приложения на Google Apps Script, показывающего "помеченные" файлы.

## 🔧 Настройка

1. **В Google Apps Script**:
   - Убедитесь, что ваша функция `doGet()` возвращает **JSON** через `ContentService`.
   - Пример:
     ```javascript
     function doGet() {
       const files = [...]; // ваши файлы: { id, name, url }
       return ContentService
         .createTextOutput(JSON.stringify(files))
         .setMimeType(ContentService.MimeType.JSON);
     }
     ```
   - Разверните как Web App → скопируйте URL вида `.../exec`.

2. **В `index.html`**:
   - Замените `YOUR_DEPLOYMENT_ID` на ваш реальный ID из URL.

3. **Добавьте иконку**:
   - Положите ваш `umbrella.gif` в папку `images/`.

## 🚀 Публикация на GitHub Pages

1. Создайте репозиторий на GitHub с названием: `вашлогин.github.io`
2. Загрузите все файлы в корень репозитория.
3. Подождите 1–2 минуты.
4. Откройте: `https://вашлогин.github.io`

## 📲 Установка как PWA

- На Android: Chrome → меню → «Установить приложение»
- На iOS: Safari → «Поделиться» → «На экран «Домой»»
- На Desktop: Chrome → значок «+» в адресной строке