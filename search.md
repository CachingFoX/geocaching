# Index
* e - Active Status
* f - Found Status
* fb - Found by user
* kw? - Keyword
* note
* ot - Origin Type


# ???
radius=16km&g=-1&ot=4&kw=burgruine&o=2

# --------
# Keyword
kw=<string>
Name or tokens of the name starts with

# Radius
radius=<value><unit>
value
unit= km or mi

Note: nur wirksam mit option = ?

# Ownership
o=<value>
0 
1 I own the cache   => owner[0]=<username> -> führt zu o=1
2 I don't own the cache => o=2

ot=4&g=-1&

Example
ot=4&owner[0]=CachingFoX&o=1
Option erzeugt bei der Suche: radius=16km&g=-1&ot=4&o=2
Note
* Option ot=4 required

owner[0]=<username>&o=2 -> owner[0]=<username>&o=1 (o parameter will be ignored)


# Owner
owner[0]=<username> or owner=<username>
See also Ownership




# -------- 

# Origin Type
ot=
0
1
2
3
4 - Home location

# Found Status
f=
0 ...
1 found by current user
2 not found by current user

Note: f=2 generates nfb[0]=<username>


# Found by a user
fb=<username>

username is typical not the current user

# Not found by users
nfb[<index>]=<username>
Only shows caches which are not found by the given users. If f=2 given nfb[0] is set to the current user.

index from 0 to 4 
Maximum five?


# Archive
a=<value>
0 all
1 only active caches
2 only archived caches

# Solved Coordinates
cc=<value>
0 All
1 Solved coordinats only
2 Oriiginal coordinates only


# Sorting

## Sorting by Column
sort=<value>
FoundDateOfFoundByUser - referenced to current user - außer wenn options fb genutzt wird

## Sorting Order 
asc=
False
True

