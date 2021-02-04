---
description: Users Resource
---

# Users

### User Object

| Field | Type | Description |
| :--- | :--- | :--- |
| id | snowflake | the user's id |
| username | string | the user's username |
| discriminator | string | the user's 4-digit tag |
| avatar | ?string | the user's avatar hash |
| flags | array of user flags | the user's flags |

#### Example User

```javascript
{
    "id": "42388375784780768",
    "username": "NamesAreHardOkay?",
    "discriminator": "0001",
    "avatar": "53021917291361dbb71017991aff7f99fd943f71757c2ef764f79445c72eed79"
    "flags": [
        1, // System Account
        10 // Bot Account
    ]
}
```

<table>
  <thead>
    <tr>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Value</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Developer</td>
      <td style="text-align:left">1</td>
      <td style="text-align:left">Developer Account</td>
    </tr>
    <tr>
      <td style="text-align:left">System Account</td>
      <td style="text-align:left">11</td>
      <td style="text-align:left">
        <p>Whether the user is an account managed</p>
        <p>by Saryno</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Bot Account</td>
      <td style="text-align:left">10</td>
      <td style="text-align:left">Whether the user is a bot account</td>
    </tr>
  </tbody>
</table>

{% api-method method="get" host="" path="/users/@me" %}
{% api-method-summary %}
Get Current User
{% endapi-method-summary %}

{% api-method-description %}
Returns the current user object of the requester's account. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "id": "42388375784780768",
    "username": "NamesAreHardOkay?",
    "discriminator": "0001",
    "avatar": "53021917291361dbb71017991aff7f99fd943f71757c2ef764f79445c72eed79"
    "flags": [
        1, // System Account
        10 // Bot Account
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="" path="/users/{user.id}" %}
{% api-method-summary %}
Get User
{% endapi-method-summary %}

{% api-method-description %}
Returns a user object
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="user.id" type="string" required=true %}
the user's id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "id": "42388375784780768",
    "username": "NamesAreHardOkay?",
    "discriminator": "0001",
    "avatar": "53021917291361dbb71017991aff7f99fd943f71757c2ef764f79445c72eed79"
    "flags": [
        1, // System Account
        10 // Bot Account
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="patch" host="" path="/users/@me" %}
{% api-method-summary %}
Modify Current User
{% endapi-method-summary %}

{% api-method-description %}
Modify the requester's user account settings. Returns a user object on success. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="discriminator" type="string" required=false %}
the new discriminator of the user
{% endapi-method-parameter %}

{% api-method-parameter name="username" type="string" required=false %}
the new username of the user
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "id": "42388375784780768",
    "username": "NamesAreHardOkay?",
    "discriminator": "0001",
    "avatar": "53021917291361dbb71017991aff7f99fd943f71757c2ef764f79445c72eed79"
    "flags": [
        1, // System Account
        10 // Bot Account
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="" path="/users/@me/communities" %}
{% api-method-summary %}
Get Current User Communities
{% endapi-method-summary %}

{% api-method-description %}
\[WIP\]
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="delete" host="" path="/users/@me/communities/{community.id}" %}
{% api-method-summary %}
Leave Community
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="" path="/users/@me/channels" %}
{% api-method-summary %}
Get User DMs
{% endapi-method-summary %}

{% api-method-description %}
Returns a list of DM Channel Objects
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
Todo
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="" path="/users/@me/channels" %}
{% api-method-summary %}
Create a DM Channel
{% endapi-method-summary %}

{% api-method-description %}
If the channel was created before, it will simply return that channel
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="recipient\_id" type="string" required=true %}
the recipient's user.id
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="number" required=true %}
2 \(DM Channel\)
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="" path="/users/@me/channels" %}
{% api-method-summary %}
Create a Group DM Channel
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="recipient\_ids" type="array" required=true %}
array of user.ids 
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="number" required=true %}
3 \(Group DM Channel\)
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

