# Marriage
A Representation of a marriage. See the [pTree Spec](https://github.com/genealogysystems/ptree/blob/master/spec/marriage.md).

# Root Endpoints

* [POST /graph/marriage](post_marriage.md) - Create a marriage
* [GET /graph/marriage/{mid}](get_marriage_mid.md) - Get a marriage
* [DELETE /graph/marriage/{mid}](delete_marriage_id.md) - Remove a marriage

* [GET /graph/marriage/{mid}/spouse](get_marriage_mid_spouse.md) - Get a marriage
* [POST /graph/marriage/{mid}/spouse](post_marriage_mid_spouse.md) - Associate a spouse
* [DELETE /graph/marriage/{mid}/spouse/{sid}](delete_marriage_mid_spouse_sid.md) - Disassociate a spouse

* [GET /graph/marriage/{mid}/place](get_marriage_mid_place.md) - Get the marriage place
* [POST /graph/marriage/{mid}/place](post_marriage_mid_place.md) - Add or Update the marriage place?
* [DELETE /graph/marriage/{mid}/place](delete_marriage_mid_place.md) - Remove the marriage place

* [GET /graph/marriage/{mid}/date](get_marriage_mid_date.md) - Get the marriage date
* [POST /graph/marriage/{mid}/date](post_marriage_mid_date.md) - Add or Update the marriage date?
* [DELETE /graph/marriage/{mid}/date](delete_marriage_mid_date.md) - Remove the marriage date

# Person Endpoints

* [GET /graph/person/{id}/marriage](get_person_id_marriage.md) - Get a list of marriages associated with a person