# GET /graph/gender/{id}
Get the gender associated with a person

## URL Parameters

* `id` - The gender-id.

## Request
**Headers**

`None`

**Query Parameters**

`None`

**Body**

`None`

## Validation

* If gender node does not exist, `404`

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