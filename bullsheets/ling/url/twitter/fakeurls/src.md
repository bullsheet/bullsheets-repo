1999 lines


generated with code like this:


```php
$gen = LingBullSheetGenerator::create()->setDir($bullsheetsDir);
for ($i = 0; $i < 2000; $i++) {
    $firstName = $gen->firstName();
    $lastName = $gen->lastName();
    echo 'https://www.twitter.com/' . CaseTool::toSnake($firstName . '_' . $lastName) . "<br>";
}
```