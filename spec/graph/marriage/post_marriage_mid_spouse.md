# POST /graph/marriage/{mid}/spouse
Associate a spouse with this marriage.

## URL Parameters

* `mid` - The marriage-id.

## Request

**Headers**

* Content-Type: application/json

**Query Parameters**

`None`

**Body**

````javascript
{
  "person_id": ""
}
````

## Validation

* If Content-Type is not json, `415`
* If Body is missing or malformed, `400`
* If person_id is missing or malformed, `400`
* If specified marriage does not exist, `400`
* If specified person does not exist, `400`
* If there is more than one spouse currently associated, `400`
* If the specified person is already associated, `400`

## Graph Operations

* Create a spouse edge from person to marriage

## Response
**Headers**

* Status: 204

**Body**

`None`