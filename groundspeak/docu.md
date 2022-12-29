# Groundspeak's Geocaching Search API

Website

`GET https://www.geocaching.com/play/search?<parameters>`

Data

`GET https://www.geocaching.com/play/search/more-results?<parameters>`

## Results
The result is splitted in chunks of 20 items. First pages is returned as HTML page. The results of the next page are return in JSON format. The JSON structure stores results in pre-rendered HTML format strings.

## Limits
Groundspeak only shows 1000 geocaches at a time.

## Parameters

| Parameter        | Function           | Values  |
| ------------- |-------------| -----|
| a | Archive | Number/TriState | 0 includes archived
| c | Country | |
| cc | Corrected Coordinates | |
| d | Difficulty |
| e | Cache Status | |
| f | Found Status | |
| fav | Favorite Points | |
| g |
| kw | Keyword | |
| lat | Latitude
| lng | Longitude | |
| m | D/T combinations | |
| nfb | Not found by | |
| note | Cache has personal note | |
| o | Cache Owner | |
| origin | | 
| ot | | 
| owner | Hidden by | |
| p | Membership Type | |
| pe | Exclude past events | TriState |
| r | region
| radius | | Number postfix km/mi
| sc | | Boolean
| sizes | Container sizes |
| sort | |
| t | Terrain | |
| types | Caceh type |
| 

### Parameter Types
* string
* string-arrays
* comma-sperated values
* range
* string-based boolean
* tri-state

## Select Parameters
Selects the caches based on characteristics of the caches.

### Parameter Cache Status
`e=<value>`
* 0: both
* 1: Enabled caches
* 2: Disabled caches

### Parameter Membership Type
`p=<value>`
* 0 both
* 1 Premium
* 2 Basic

### Cache Owner
`o=<value>`
* 0: both
* 1: Caches I own
* 2: Caches I don't own 

## XXX Parameters
Selects the caches based on user-based characteristics of the caches.

### Found Status
f=
0: both
1: Found
2: Not found -> nfb[0]=<currentuser>

### Corrected Coordinates
cc=
* 0: both
* 1: Updated coordinates only
* 2: Original coordinates only

### Personal Note
note=
* 0: with and without personal note
* 1: without personal note
* 2: with personal note


## Sort Parameters 
There are two parameters which defines the sorting order of the results:
* `sort` - a string specifies the sorted field
* `asc`- a string specifies the sort order

### Parameter `sort`
Parameter `sort` is a string based parameter specifies the sorting field/column.

Valid fields/columns:
* ContainerSize
* DateLastVisited
* Difficulty
* Distance
* FavoritePoint
* FoundDateOfFoundByUser
* GeocacheName
* PlaceDate
* Terrain

### Parameter `asc`
`asc` is a string-based boolean parameter with value `False` or `True`

* `False` - descending sorting order (default value)
* `True` - ascending sorting order

## Unknown/documented parameters
There is a list of parameters with a unknown function:

* `ot=4` 0,1,2,3,4 (Location)
* owner[0]=CachingFoX&f=1&o=1&e=1&p=2&cc=1
* utr=true/false
* sc=False
* startIndex=50
* selectAll=false
* m
* Cache attributes


--------------------

### Attributes

### Container size
`sizes={values}`
A comma seperated list of values
```
2: Micro
8: Small
3: Regular
4: Large
6: Other
```

### Terrain and Difficulty
`t=1.5-5`
`d=1-4.5`

### Favorite Points
`fav=42`

### Keyword
`kw=cache`

### Caches types
types=6,4,13,453,1304,3653,3774,4738,7005&c=76

### Exclude past events
&pe=1

### Country
c=76

### Region
r=??

### Hidden By
`owner[0]={name}`
Waldkauz1977

### Not found by
`nfb[0]={name}&nfb[1]={name}`
index 0 to 4

### 
lat=49.59099&lng=11.00783&origin=Erlangen&ot=3&g=29736
lat=50.74718&lng=14.33328&origin=Erlangen&ot=3&g=19736

### Radius
`radius={value}km`

## Archived
a=
0: active and archived
1: archived
2: active

# Found by User
fb=<usernane>
  

# Placed Date






-----

# Groundspeak's Geocaching API

## Request URL
Limit 1000

```
GET https://www.geocaching.com/play/search?<parameter>
```
Answer comes as HTML

## Request more results

```
https://www.geocaching.com/play/search/more-results?ot=4&tr=18&utr=true&startIndex=50&selectAll=false
```
startIndex - 0...999

### Answer
Answer comes as JSON.

Fields:
* HtmlString - includes the result as HTML string
* ShowLoadMore - 


The request have to be include login data.

## Answer
The answer of the reqeust is a HTML web page, includes the complete page. Number of results 50

### Number of total results
```
<div class="controls-wrapper">
   <h1 class="controls-header">297,791 results</h1>
```

### Results
Table of results
```
<table class="search-results-table" id="searchResultsTable">
```

#### Results
```
<tbody id="geocaches">
```

#### Result
For each result is a single row with all data.
```
<tr data-rownumber="0" data-id="GC8XTJ4" data-name="Zapfen-Drilling">
```





## Parameters






## Values

### Boolean Parameters


### Missing
Cache has personal note


### Unknown Parameter
`ot=4`

###
owner[0]=CachingFoX&f=1&o=1&e=1&p=2&cc=1

### Cache Status
e=
* 1: Enabled caches
* 2: Disabled caches

### Membership Type
p=
* 2 Basic
* 1 Premium
### Cache Owner
o=
* 1: Caches I own
* 2: Caches I don't own 

### Found Status
f=
1: Found
2: Not found

### Corrected Coordinates
cc=
* 1: Updated coordinates only
* : Original coordinates only

### Container size
`sizes={values}`
A comma seperated list of values
```
2: Micro
8: Small
3: Regular
4: Large
6: Other
```

### Terrain and Difficulty
`t=1.5-5`
`d=1-4.5`

### Favorite Points
`fav=42`

### Keyword
`kw=cache`

### Caches types
types=6,4,13,453,1304,3653,3774,4738,7005

### Exclude past events
&pe=1

### Country
c=76

### Region
r=??

### Hidden By
`owner[0]={name}`
Waldkauz1977

### Not found by
`nfb[0]={name}&nfb[1]={name}`
index 0 to 4

###
lat=49.59099&lng=11.00783&origin=Erlangen&ot=3&g=29736
lat=50.74718&lng=14.33328&origin=Erlangen&ot=3&g=19736

### Radius
`radius={value}km` or 
`radius={value}mi`

### Personal Note
Cache has personal note
```note=1/2```

* 1: has personal note
* 2: hasn't personal note

### Attributes

### World Wonders
tr=
modern 11,...17
antic 18,...,24
