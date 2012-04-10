### Purpose

A CSV file that maps bill codes to popular nicknames and keywords.

If you run a service that allows people to search for bills, this would be a great dataset to integrate into your search.


### How it works

The CSV has 4 columns.

**bill_type** - The bill's type. One of:

* "hr" - Bills originating in the House (often seen as "H.R.")
* "hres" - Resolutions originating in the House (often seen as "H.Res")
* "hjres" - Joint resolutions originating in the House (often seen as "H.J.Res")
* "hconres" - Concurrent resolutions originating in the House (often seen as "H.Con.Res")
* "s" - Bills originating in the Senate (often seen as "S.")
* "sres" - Resolutions originating in the Senate (often seen as "S.Res")
* "sjres" - Joint resolutions originating in the Senate (often seen as "S.J.Res")
* "sconres" - Concurrent resolutions originating in the Senate (often seen as "S.Con.Res")

**bill_number** - The bill's number. (e.g. for "H.R. 3590", this would be "3590")

**congress** - The number of the Congress this bill was introduced in. (e.g. for the 111th Congress, this would be "111")

**term** - The term or phrase that should be associated with this bill. Case insensitive, all lower case.


### Contributing

If you want to add entries, fork it, add away, and send a pull request. I'm inclined to take an inclusive approach, since false positives don't seem as bad as simply missing out on finding the bill someone was searching for altogether.


### License

Public domain information, no restrictions whatsoever. 

Project initiated by Eric Mill at the [Sunlight Foundation](http://sunlightfoundation.com).
