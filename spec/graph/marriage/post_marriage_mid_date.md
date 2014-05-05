# POST /graph/marriage/{mid}/date
Update the marriage date.

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
  "original": "",
  "formal": ""
}
````

## Validation

* If Content-Type is not json, `415`
* If Body is missing or malformed, `400`
* If original is missing or [invalid](https://github.com/trepo/ptree/blob/master/spec/date.md), `400`
* If formal is missing or [invalid](https://github.com/trepo/ptree/blob/master/spec/date.md), `400`
* If node does not exist, `404`
* If node is not a marriage node, `404`

## Graph Operations

* Lookup the marriage node
* If a date is already associated, update it
* Else create the date and create and edge from marriage to date

## Response
**Headers**

* Status: 204

**Body**