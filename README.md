GetResponse API
=============

Super-simple, minimum abstraction GetResponse API v3 wrapper, in PHP.

Requires PHP 5.3 and a pulse.

Installation
------------

You can install the GetResponse using Composer:

```
composer require mizanur/getresponse-api-php
```

Examples
--------

use this on top of your class
```
use GetResponse\jsonRPCClient;
use GetResponse\GetResponse;
```

your API key is available at
https://app.getresponse.com/my_api_key.html
```
$api_key = 'YOUR-API-KEY';
```

API 2.x URL
```
$api_url = 'http://api2.getresponse.com';
```

Initialize JSON-RPC client
```
$client = new jsonRPCClient($api_url);
```

Get all campaigns
```
$client = new jsonRPCClient($api_url);
$campaigns = $client->get_campaigns($api_key);
echo "<pre>";print_r($campaigns);
```

Get campaign by campaign name
````
$campaigns = $client->get_campaigns(
    $api_key,
    [
        'name' => [ 'EQUALS' => 'YOUR-CAMPAIGN-NAME' ]
    ]
);
echo "<pre>";print_r($campaigns);
````

Add contact to the campaign
```
$api = new GetResponse ( $gp_api_key );
$api->addContact ( $list_id, $full_name, $email, 'insert', 0, ['name' => $full_name]);
```

*Note for contributors:* We should HELP each other by contribution.
