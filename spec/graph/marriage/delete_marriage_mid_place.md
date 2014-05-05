# DELETE /graph/marriage/{mid}/place
Remove a marriage place.

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

* If node does not exist, `400`
* If node is not a marriage node, `400`
* If there is no place associated with the marriage, `400`

## Graph Operations

* Get the specified node and verify it is a marriage
* Remove the place node and the edge from marriage to place

## Response

**Headers**

* Status: 204

**Body**

`None`