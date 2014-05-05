# GET /graph/marriage/{mid}/place
Get the place associated with a marriage.

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

* If node does not exist, `404`
* If node is not a marriage node, `404`
* If there is no place associated, `404`

## Graph Operations

* Get the specified node and verify it is a marriage
* Follow the place edge and get the Place node

## Response

**Headers**

* Status: 200

**Body**
````javascript
{
  "name": "place name"
}
````