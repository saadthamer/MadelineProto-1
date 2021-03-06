---
title: contacts.exportCard
description: contacts.exportCard parameters, return type and example
---
## Method: contacts.exportCard  
[Back to methods index](index.md)




### Return type: [Vector\_of\_int](../types/int.md)

### Can bots use this method: **NO**


### Example:


```
$MadelineProto = new \danog\MadelineProto\API();
$MadelineProto->session = 'mySession.madeline';
if (isset($number)) { // Login as a user
    $MadelineProto->phone_login($number);
    $code = readline('Enter the code you received: '); // Or do this in two separate steps in an HTTP API
    $MadelineProto->complete_phone_login($code);
}

$Vector_of_int = $MadelineProto->contacts->exportCard();
```

Or, if you're using the [PWRTelegram HTTP API](https://pwrtelegram.xyz):



### As a user:

POST/GET to `https://api.pwrtelegram.xyz/userTOKEN/contacts.exportCard`

Parameters:




Or, if you're into Lua:

```
Vector_of_int = contacts.exportCard({})
```

