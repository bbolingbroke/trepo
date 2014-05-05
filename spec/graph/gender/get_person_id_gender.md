# GET /graph/person/{id}/gender
Get the gender associated with a person

## URL Parameters

* `id` - The person-id.

## Request
**Headers**

* Content-Type: application/json

**Query Parameters**

`None`

**Body**

`None`

## Validation

* If person does not exist, `400`
* If person does not have a gender associated, `404`

## Graph Operations

`None`

## Response
**Headers**

* Status: 200

**Body**
````javascript
{
  "gender_id": "The ID of the created gender node",
  "value" : "The gender value"
}
````