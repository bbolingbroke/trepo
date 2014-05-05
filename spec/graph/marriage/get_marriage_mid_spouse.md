# GET /graph/marriage/{mid}/spouse
Get a list of spouses associated with this marriage.

## URL Parameters

* `mid` - The marriage-id.

## Request

**Headers**

`None`

**Query Parameters**

`None`

**Body**

`None`

## Validation

* If `mid` node does not exist, `404`
* If `mid` node is not a marriage node, `404`

## Graph Operations

* Get the specified node and verify it is a marriage
* Get the ids of all associated spouse persons

## Response

**Headers**

* Status: 200

**Body**
````javascript
[
  {"person_id": ""},
  {"person_id": ""}
]
````