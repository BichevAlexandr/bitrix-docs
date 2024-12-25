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
