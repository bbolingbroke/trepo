# DELETE /graph/marriage/{mid}
Remove a marriage.

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

## Graph Operations

* Get the specified node and verify it is a marriage
* If there are spouse edges, remove them
* If there is a place, remove the place and the place edge.
* If there is a date, remove the date and the date edge.
* Remove the marriage Node.

## Response

**Headers**

* Status: 204

**Body**

`None`