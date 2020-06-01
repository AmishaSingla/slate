---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  # - ruby
  # - python
  # - javascript

toc_footers:
  # - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

# cludes:
#   - errorsin

search: true
---

# Introduction

Welcome to the NotificationTrapper by Decabits! Notification Trapper provides a dedicated environment to send, view and share access to emails & SMSes sent during the testing process. 

Enjoy the functionality of this dedicated playground, which organizes all your emails and SMSes in one place. Bypass spam filters and blacklists, cut down on cumbersome SMS costs and make use of a fully encrypted and secure connection.


# Emails

## Create Email

> To create **emails**, use this code:

<!-- ```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
``` -->

<!-- ```python
import kittn

api = kittn.authorize('meowmeowmeow')
``` -->

```shell
curl --location --request POST 'http://notification-trapper.test.com/api/emails' \
--header 'Authorization: hello_world' \
--header 'Content-Type: application/json' \
--header 'Content-Type: text/plain' \
--data-raw '{
  "account_id": "1",
	"to": "test@gmail.com",
	"from": "test@decabits.com",
	"content": "Hello World",
	"subject": "Hello World",
	"cc": "test@gmail.com",
	"bcc": "test@gmail.com",
  "environment": "staging"
}'
```

<!-- ```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
``` -->

> Make sure to replace `hello_world` with your API key.

NotificationTrapper uses this API key to create emails. 
NotificationTrapper expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: hello_world`

<aside class="notice">
You must replace <code>hello_world</code> with your personal API key.
</aside>

# Text Messages/SMS

## Create Text Message

<!-- ```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get
``` -->

<!-- ```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get()
``` -->

> To create **sms**, use this code:

```shell
curl --location --request POST 'http://notification-trapper.test.com/api/text_message' \
--header 'Authorization: hello_world' \
--header 'Content-Type: application/json' \
--header 'Content-Type: text/plain' \
--data-raw '{
  "account_id": "1",
	"to": "9876543212",
	"from": "9875453631",
	"content": "Hello World",
	"environment": "staging"
}'
```
<!-- 
```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let kittens = api.kittens.get();
``` -->

> Make sure to replace `hello_world` with your API key.

NotificationTrapper uses this API key to create text message/sms.
NotificationTrapper expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: hello_world`

<aside class="notice">
You must replace <code>hello_world</code> with your personal API key.
</aside>

> The above command returns JSON structured like this:

```json
[
 {
    "email": {
        "id": 1,
        "account_id": 1,
        "to": "test@gmail.com",
        "from": "test@decabits.com",
        "content": "Hello World",
        "subject": "Hello World",
        "bcc": "test@gmail.com",
        "cc": "test@gmail.com",
        "environment": "staging"
    }
}
  
```

This endpoints create emails and text messages/sms.

### HTTP Request

`POST http://notification-trapper.test.com/api/emails`

### Query Parameters

Parameter | Add
--------- | ------- 
Authorization| Your_API_Key
Content-Type | application/json

<aside class="success">
Status - 201 Created
</aside>


> The above command returns JSON structured like this:

```json
[
 {
    "text_message": {
        "id": 1,
        "account_id": 1,
        "to": "9876543212",
        "from": "9875453631",
        "content": "Hello World",
        "environment": "staging"
    }
}
  
```

### HTTP Request

`POST http://notification-trapper.test.com/api/emails`

### Query Parameters

Parameter | Add
--------- | ------- 
Authorization| Your_API_Key
Content-Type | application/json

<aside class="success">
Status- 201 Created
</aside>

<!-- ## Get a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.get(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

## Delete a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.delete(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.delete(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -X DELETE
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.delete(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific kitten.

### HTTP Request

`DELETE http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete
 -->
