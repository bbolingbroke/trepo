# POST /graph/marriage/{mid}/place
Update the marriage place.

## URL Parameters

* `mid` - The marriage-id.

## Request

**Headers**

* Content-Type: application/json

**Query Parameters**

`None`

**Body**

````javascript
{
  "name": "place name"
}
````

## Validation

* If Content-Type is not json, `415`
* If Body is missing or malformed, `400`
* If name is missing or invalid, `400`
* If node does not exist, `404`
* If node is not a marriage node, `404`

## Graph Operations

* Lookup the marriage node
* If a place is already associated, update it
* Else create the place and create and edge from marriage to place

## Response
**Headers**

* Status: 204

**Body**