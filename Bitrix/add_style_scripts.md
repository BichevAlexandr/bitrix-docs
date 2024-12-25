## Подключение стилей и скриптов
### Для чего подключать скрипты и js через API
Это нужно для правильной оптимизации сайта. CMS Битрикс, умеет самостоятельно объединять и сжимать подключаемые файлы стилей и js файлы.

Старый способ подключения стилей с скриптов
```html
Для стилей
<link href="/file.css">
Для js файлов
<script src="/file.js">
```
###  Подключение стилей и скриптов с D7
```php
use Bitrix\Main\Page\Asset;
// Для подключения css
Asset::getInstance()->addCss("/bitrix/css/main/bootstrap.min.css");
// Для подключения скриптов
Asset::getInstance()->addJs(SITE_TEMPLATE_PATH . "/js/myscripts.js");
// Подключение мета тегов или сторонних файлов
// Подключение мета тегов или сторонних файлов
Asset::getInstance()->addString("<link rel='shortcut icon' href='/local/images/favicon.ico' />");
```
### Подключение стилей и js в шаблонах компонентов
```php
$this->addExternalCss("/local/styles.css");
$this->addExternalJS("/local/liba.js");
```