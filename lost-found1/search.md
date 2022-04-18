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

| Parameter        | Function           | Values  |
| ------------- |-------------| -----|
| c | Country | |
| cc | Corrected Coordinates | |
| d | Difficulty |
| e      | Cache Status | |
| f | Found Status | |
| fav | Favorite Points | |
| g |
| kw | Keyword | |
| lat | Latitude
| lng | Longitude | |
| m | D/T combinations | |
| nfb | Not found by | |
| note | Cache has personal note | |
| o | Cache Owner | |
| origin | | 
| ot | | 
| owner | Hidden by | |
| p | Membership Type | |
| pe | Exclude past events | |
| r | region
| radius | |
| sizes | Container sizes |
| t | Terrain | |
| types | Caceh type |
| 





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
