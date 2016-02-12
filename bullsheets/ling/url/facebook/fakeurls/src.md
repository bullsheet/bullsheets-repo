1558 lines


generated with code like this:


```php
$gen = LingBullSheetGenerator::create()->setDir($bullsheetsDir);
for ($i = 0; $i < 10000; $i++) {
    $firstName = $gen->firstName();
    $lastName = $gen->lastName();
    echo 'https://www.facebook.com/' . CaseTool::toFlea($firstName . '.' . $lastName) . "<br>";
}
```