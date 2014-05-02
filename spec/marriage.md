# Marriage Endpoints

POST /marriage -> 404? can you make a marriage not associated with a person?

GET /marriage/id

DELETE /marriage/id

GET /marriage/id/spouse -> return a list of spouses?

GET /marriage/id/spouse/id

POST /marriage/id/spouse/id

DELETE /marriage/id/spouse/id -> delete using edge id or spouse id?

GET /marriage/id/place -> returns place because max of 1 place can be returned

POST /marriage/id/place

DELETE /marriage/id/place -> deleted ref only

GET /marriage/id/date -> returns date because max of 1 place can be returned

POST /marriage/id/date

DELETE /marriage/id/date -> deletes ref and date

# Person convinience functions

GET /person/id/marriage -> return all marriages for this person

POST /person/id/marriage -> convinience to create marriage and associate with person

# Place convinience functions

GET /place/id/marriage -> return all marriages associatedwith this place