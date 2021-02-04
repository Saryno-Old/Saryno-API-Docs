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
|  |  |  |
|  |  |  |

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

{% api-method method="get" host="https://api.saryno.com/v1" path="/users/@me" %}
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

{% api-method method="get" host="https://api.saryno.com/v1" path="/users/{user.id}" %}
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

