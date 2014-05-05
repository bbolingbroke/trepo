# GET /graph/marriage/{mid}
Get a marriage.

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

## Graph Operations

* Get the specified node and verify it is a marriage

## Response

**Headers**

* Status: 200

**Body**
````javascript
{
  "marriage_id": "The ID of the marriage node",
  "spouses": [
    {"person_id": ""},
    {"person_id": ""}
  ],
  "place": {
    "name": "place name"
  },
  "date": {
    "original": "",
    "formal": ""
  }
}
````