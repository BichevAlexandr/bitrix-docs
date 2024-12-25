# Дата и время
##	Получить разницу в днях и записать в свойство
```php
$difference = round(strtotime($arItems['PROPERTY_DATE']) - strtotime(date(Y-m-d)));
$interval = round($difference / (3600 * 24));
$res = \CIBlockElement::SetPropertyValueEx($nElementID, $nIBlockID, ['NOSTALOS_DNEY' => $interval]);
```
