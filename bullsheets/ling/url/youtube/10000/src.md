10000 lines 

generated with php code:






```php 
<?php


use BullSheet\Generator\LingBullSheetGenerator;

require_once "bigbang.php"; // start the local universe

require_once __DIR__ . "/../vendor/autoload.php";


// Call set_include_path() as needed to point to your client library.
require_once 'Google/Client.php';
require_once 'Google/Service/YouTube.php';

/*
 * Set $DEVELOPER_KEY to the "API key" value from the "Access" tab of the
 * Google Developers Console <https://console.developers.google.com/>
 * Please ensure that you have enabled the YouTube Data API for your project.
 */
$DEVELOPER_KEY = 'myAPIKEY';

$client = new Google_Client();
$client->setDeveloperKey($DEVELOPER_KEY);

// Define an object that will be used to make all API requests.
$youtube = new Google_Service_YouTube($client);
$gen = LingBullSheetGenerator::create()->setDir("/path/to/my/bullsheets");


try {
    $htmlBody = '';
    // Call the search.list method to retrieve results matching the specified
    // query term.


    for ($i = 0; $i < 200; $i++) {


        $searchResponse = $youtube->search->listSearch('id', array(
            'q' => $gen->getPureData("word"),
            'maxResults' => 50,
            'type' => 'video',
        ));
        $items = $searchResponse->getItems();

        foreach ($items as $info) {
            echo 'https://www.youtube.com/watch?v=' . $info['id']['videoId'];
            echo '<br>';
        }
    }


} catch (Google_Service_Exception $e) {

    $htmlBody .= sprintf('<p>A service error occurred: <code>%s</code></p>',
        htmlspecialchars($e->getMessage()));


} catch (Google_Exception $e) {
    $htmlBody .= sprintf('<p>An client error occurred: <code>%s</code></p>',
        htmlspecialchars($e->getMessage()));
}

echo $htmlBody;
```