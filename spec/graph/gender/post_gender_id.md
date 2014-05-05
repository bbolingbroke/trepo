# POST /graph/gender/{id}
Update the gender

## URL Parameters
`None`

## Request
**Headers**

* Content-Type: application/json

**Query Parameters**

`None`

**Body**

````javascript
{
  "value": "Male, Female, or Unknown"
}
````

## Validation

* If Content-Type is not json, `415`
* If Body is missing or malformed, `400`
* If value is missing or malformed, `400`
* If gender node is missing, `404`

## Graph Operations

* Set `value` on gender node

## Response
**Headers**

* Status: 204

**Body**

`None`