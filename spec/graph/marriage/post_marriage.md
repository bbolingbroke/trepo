# POST /graph/marriage
Create a marriage.

## URL Parameters

`None`

## Request

**Headers**

* Content-Type: application/json

**Query Parameters**

`None`

**Body**

````javascript
{
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

## Validation

* If Content-Type is not json, `415`
* If Body is missing or malformed, `400`
* If spouses is missing or is not an array, `400`
* If there are more than two spouses, `400`
* If both spouses have the same id, `400`
* If a specified person does not exist, `400`
* If place is missing or [invalid](https://github.com/trepo/ptree/blob/master/spec/place.md), `400`
* If date is missing or [invalid](https://github.com/trepo/ptree/blob/master/spec/date.md), `400`

## Graph Operations

* Create a marriage node
* If there are spouses, create an edge from marriage to each person
* If there is a place, create the place node and create an edge from marriage to place.
* If there is a date, create the date node and create an edge from marriage to date.

## Response
**Headers**

* Status: 204

**Body**