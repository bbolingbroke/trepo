# POST /graph/gender
Create and associate a gender with a person

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
  "person": "Person Identifier",
  "value": "Male, Female, or Unknown"
}
````

## Validation

* If Content-Type is not json, `415`
* If Body is missing or malformed, `400`
* If person or value is missing or malformed, `400`
* If person does not exist, `400`
* If person already has a gender associated, `400`

## Graph Operations

* Create `gender` node
* Set `value` on created node
* Create `gender_ref` edge from person to gender

## Response
**Headers**

* Status: 201

**Body**
````javascript
{
  "gender_id": "The ID of the created gender node"
}
````