# DELETE /graph/gender/{id}
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

* Remove gender node and edge from person to gender

## Response
**Headers**

* Status: 204

**Body**

`None`