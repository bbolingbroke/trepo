# GET /graph/marriage/{mid}/date
Get the date associated with a marriage.

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
* If there is no date associated, `404`

## Graph Operations

* Get the specified node and verify it is a marriage
* Follow the date edge and get the date node

## Response

**Headers**

* Status: 200

**Body**
````javascript
{
  "original": "",
  "formal": ""
}
````