# Инфорблоки. Элементы. Свойства

##	Получение всех вариантов значений свойства типа список
```php
$obj = CIBlockProperty::GetPropertyEnum(
	$propertyID,
	[],
	[
		'IBLOCK_ID' => $arResult['IBLOCK_ID']
	]
);
while ($arValuesPropEnum = $obj->Fetch()) {
	p($arValuesPropEnum);
}
```

##	Получение ID свойства элемента инфоблока по символьному коду
```php
$objProp = CIBlockProperty::GetList(
	[],
	[
		'ACTIVE' => 'Y',
		'IBLOCK_ID' => $arResult['IBLOCK_ID'],
		'CODE' => 'STATUS_USER'
	]
);
if ($arResProp = $objProp->Fetch()) {
	p($arResProp['ID']);
}
```
