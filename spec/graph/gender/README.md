# Gender
A Representation of a person's gender. See the [pTree Spec](https://github.com/genealogysystems/ptree/blob/master/spec/gender.md).

# Root Endpoints

* [POST /graph/gender](post_gender.md) - Create and associate a gender with a person
* [GET /graph/gender/{id}](get_gender_id.md) - Get a Gender
* [POST /graph/gender/{id}](post_gender_id.md) - Update a Gender
* [DELETE /graph/gender/{id}](delete_gender_id.md) - Remove the gender associated with a person

# Person Endpoints

* [GET /graph/person/{id}/gender](get_person_id_gender.md) - Get the gender associated with the person id