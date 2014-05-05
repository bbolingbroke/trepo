# GET /graph/person/{id}/marriage
Get the marriage associated with a person

## URL Parameters

* `id` - The person-id.

## Request
**Headers**

`None`

**Query Parameters**

`None`

**Body**

`None`

## Validation

* If person does not exist, `400`
* If person does not have a marriage associated, `404`

## Graph Operations

`None`

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