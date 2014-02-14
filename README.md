### Purpose

A CSV file that maps bill codes to popular nicknames and keywords.

If you run a service that allows people to search for bills, this would be a great dataset to integrate into your search.


### Design

This dataset is designed to be responsive to user searches, so it's not always a literal match between a bill and its keyword. If someone searches for "SOPA", this should match on both SOPA and PIPA, because many people don't know the difference, and the two are often confused or referred to as a single entity.

Similarly, "Obamacare" should match on both the [Patient Protection and Affordable Care Act](https://en.wikipedia.org/wiki/Patient_Protection_and_Affordable_Care_Act) and the associated [Health Care and Education Reconciliation Act](https://en.wikipedia.org/wiki/Health_Care_and_Education_Reconciliation_Act_of_2010), which were passed as a package deal and both collectively define what people think of as "Obamacare".

One possible way to have both precision and flexibility would be to add another column that has a relationship flag, to distinguish between terms that refer to a bill exactly, or terms that are less directly related. [Open an issue](https://github.com/unitedstates/bill-nicknames/issues) if you want to talk about that.


### How it works

The CSV has 5 columns.

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

**term** - The term or phrase that should be associated with this bill. All lower case.

**comment** - Any comment to describe why this bill should be linked to this keyword.


### Contributing

If you want to add entries, fork it, add away, and send a pull request. I'm inclined to take an inclusive approach, since false positives don't seem as bad as simply missing out on finding the bill someone was searching for altogether.


## Public domain

This project is [dedicated to the public domain](LICENSE). As spelled out in [CONTRIBUTING](CONTRIBUTING.md):

> The project is in the public domain within the United States, and copyright and related rights in the work worldwide are waived through the [CC0 1.0 Universal public domain dedication](http://creativecommons.org/publicdomain/zero/1.0/).

> All contributions to this project will be released under the CC0 dedication. By submitting a pull request, you are agreeing to comply with this waiver of copyright interest.

**However**, if you split this off somewhere else and add your own expertise to it, our request is you keep it public. Most ideally, keep it within Github, so that your additions can easily be seen and retrieved.