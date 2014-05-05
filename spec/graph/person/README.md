# Person
A Person. See the [pTree Spec](https://github.com/genealogysystems/ptree/blob/master/spec/person.md).

# Root Endpoints

* [POST /graph/person](post_person.md) - Create a person
* [GET /graph/person/{id}](get_person_id.md) - Get a person
* [POST /graph/person/{id}](post_person_id.md) - Update a person
* [DELETE /graph/person/{id}](delete_person_id.md) - Remove the person

Generally, most conclusions expose convenience getter functions in the form of `graph/person/{id}/<conclusion-type>`


You can get a list of conclusions by  
[GET /graph/person/{id}/_conclusions](get_person_id_conclusions.md) // TODO move to /query?

You can get a list of whys by hitting 
[GET /graph/person/{id}/_why](get_person_id_conclusions.md) // TODO move to /query?