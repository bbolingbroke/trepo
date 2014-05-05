# DELETE /graph/marriage/{mid}/date
Remove a marriage date.

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
* If there is no date associated with the marriage, `400`

## Graph Operations

* Get the specified node and verify it is a marriage
* Remove the date node and the edge from marriage to date

## Response

**Headers**

* Status: 204

**Body**

`None`