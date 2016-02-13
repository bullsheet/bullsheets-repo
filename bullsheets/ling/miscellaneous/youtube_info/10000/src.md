9992 lines


Generated with following code:


```php
ini_set('max_execution_time', '0');
$f = "/path/to/my/bullsheets/ling/url/youtube/10000/data.txt";

$startAt = 0;
$video = YouTubeVideo::create()
    ->setOnNoResultCb(function(){}) // disable visual output
    ->setApiKey("{myYoutubeApiKeyHere}");
$gen = FileSystemTool::fileGenerator($f);
$sep = '§';
$n = 0;
$failed = [];
foreach ($gen() as $v) {
    if ($n >= $startAt) {
        try {
            $id = substr($v, -11);
            $video->setVideoId($id);
            $info = [
                'id' => $id,
                'duration' => $video->getDuration(),
                'name' => $video->getTitle(),
                'thumbnail' => $video->getThumbnail(),
                'description' => $video->getDescription(),
            ];


            echo implode($sep, $info) . '<br>';
        } catch (\Exception $e) {
            InstantLog::log($e);
        }
    }
    $n++;
}


echo '---------------------';
foreach($failed as $fail){
    echo "$fail<br>";
}


az();
```