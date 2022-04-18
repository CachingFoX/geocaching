
##
GET https://www.geocaching.com/play/search/typeahead-complete?query=Herzogenaurach

[{"id":28021,"indexName":"Herzogenaurach, Bavaria","displayName":"Herzogenaurach, Bavaria","originTreatment":3},{"id":-1,"indexName":"Herzogenaurach","displayName":"Herzogenaurach","originTreatment":0}]
[{"id":136,"indexName":"Bayern, Germany","displayName":"Bayern","originTreatment":1},{"id":-1,"indexName":"Bayern","displayName":"Bayern","originTreatment":0}]
[{"id":79,"indexName":"Germany","displayName":"Germany","originTreatment":2},{"id":-1,"indexName":"Germany","displayName":"Germany","originTreatment":0}]


##
`GET https://www.geocaching.com/play/search/matching-usernames?input={name}&count={value}`
```
[
  {
    "Id":3217216,
    "Username":"Geoca Nick",
    "AvatarUrl":"https://www.geocaching.com/images/default_avatar.png"
  }
]
```
Maximal 10 names

## Check if a name is available
URL: '‘’https://www.geocaching.com/account/join/usernameavailable
POST
authentifcation: not necessary
Formulardaten:
Username: ????
__RequestVerificationToken: from the web page

antwort: false - bei unerlaubten zeichen oder schon vergebenen namen
true wenn der namen noch frei ist

