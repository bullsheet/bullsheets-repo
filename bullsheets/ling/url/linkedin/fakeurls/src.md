2000 lines


generated with code like this:


```php
$gen = LingBullSheetGenerator::create()->setDir($bullsheetsDir);
for ($i = 0; $i < 2000; $i++) {
    $firstName = $gen->firstName();
    $lastName = $gen->lastName();
    echo 'https://www.linkedin.com/in/' . urlencode(CaseTool::toDog($firstName . '-' . $lastName) . "-". strtolower($gen->alphaNumericChars(9))) . '<br>';
}
```