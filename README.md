[![SensioLabs Insight](https://insight.sensiolabs.com/projects/dba9eb6e-83de-43f4-80c6-04d273178f37/small.png)](https://insight.sensiolabs.com/projects/dba9eb6e-83de-43f4-80c6-04d273178f37)
[![Code Climate](https://codeclimate.com/github/kitsunet/Flowpack.SimpleSearch/badges/gpa.svg)](https://codeclimate.com/github/kitsunet/Flowpack.SimpleSearch)

Flowpack.SimpleSearch
=====================

A simple php search engine based on sqlite. Performance is acceptable but decreases quickly with the amount of entries.
Depending on the queries you want to perform a sane upper limit is somewhere around 50000 entries.

This package has no hard dependencies on anything so could be used in any project.

Code and API are still pretty rough. I just implemented the minimum version. A higher level query API will follow (see the ContentRepositoryAdaptor for the direction).

If you look at the code the sqlite storage of properties looks pretty strange but with SQlite3 the actual storage type is determined per row, so a column can contain different datatypes in each row. That should make all those empty rows more or less acceptable. We are trying to mimic a document database here after all.
