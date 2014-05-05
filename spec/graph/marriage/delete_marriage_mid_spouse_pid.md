# DELETE /graph/marriage/{mid}/spouse/{pid}
Remove a marriage.

## URL Parameters

* `mid` - The marriage-id.
* `pid` - The spouses person-id.

## Request

**Headers**

`None`

**Query Parameters**

`None`

**Body**

`None`

## Validation

* If `mid` node does not exist, `400`
* If `mid` node is not a marriage node, `400`
* If `pid` node does not exist, `400`
* If `pid` node is not a person node, `400`
* If `pid` node is not associated with `pid` node as a spouse, `400`

## Graph Operations

* Get the specified `mid` node and verify it is a marriage
* Get the specified `pid` node and verify it is a person and assocaited (via spouse) to the marriage
* Remove the spouse edge between the person node and the marriage node

## Response

**Headers**

* Status: 204

**Body**

`None`