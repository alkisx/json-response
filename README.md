# json-response
A simple class that returns a properly formatted json response with HTTP status

## Installation

composer require alkisx/json-response

### Usage

```php

require_once __DIR__ . "/vendor/autoload.php";


use alearn\ResponseClass\JsonResponse;


$student = [

    'name' => 'John Doe',
    'course' => 'Software Engineering',
    'level' => '200',
    'collections' => ['books'=>'Intro to UML', 'music'=>'rap']

];


new JsonResponse('unauthorized', '', $student);

```


### Param 1 (Required)
1. success or ok - 200 http status
2. unauthorized - 401 http status
3. exception - 500 http status (interval server error)

### Param 2 (Optional)
string - the return message, use empty quote if not available

### Param 3 (Optional)
Array - Array of Data