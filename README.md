# Commonwealth of Australia Hansard

These are Hansard XML files downloaded from the [Parliament of Australia website](http://parlinfo.aph.gov.au/parlInfo/search/summary/summary.w3p;adv%3Dyes;orderBy%3D_fragment_number,doc_date-rev;query%3DDataset%3Ahansardr,hansardr80;resCount%3DDefault) by [Tim Sherratt](http://timsherratt.org).

## Harvesting history

- The original harvest was run in 2016.
- A complete reharvest was undertaken in April 2019
- A harvest of 1998 to 2005 was added in 2020. 
- A reharvest of 1998 to 2005 was run in August 2023.
- A reharvest of 1901 to 1980 was run in May 2024.
- A complete reharvest using a modified method and including 1981 to 1997 was run in October 2024

Note that file names can change between harvests and some files have been modified, split, added, and deleted over time.

The files are made available on the Parliament website under a [CC-BY-NC-ND licence](http://www.aph.gov.au/Help/Disclaimer_Privacy_Copyright#c).

Currently this repository includes files for the House of Representatives and the Senate from 1901 to 2005. Open Australia provides access to [Hansard XML files from 2006 onwards](http://data.openaustralia.org.au/).

Browse the files or [download a zip file](https://github.com/wragge/hansard-xml/archive/master.zip) of the lot.

## October 2024 note

Thanks to information from the Department of Parliamentary Services, I've finally been able to access XML (or actually SGML) Hansard files for the period 1981 to 1997. I've also modified my harvesting method, making use of the [dataset of sitting days](https://handbook.aph.gov.au/StatisticalInformation/SittingPattern) in the Parliamentary Handbook. As a result, I've been able to run a complete harvest from 1901 to 2005 for the first time. There are, however, some things to note.

First of all, the format of files from 1981 to 1997 is different to those of other years. The tags are all in uppercase but, most importantly, some of the tags themselves are different. For example `<interject>` is used instead of `<interjection>` and `<debate.sub1>` instead of `<subdebate.1>`. I'll be documenting this further as I work on an update of Historic Hansard.

Second, when I checked the harvest results against the dataset of sitting days, I found a few discrepencies – some sitting days either don't return any Hansard search results, or don't have links to XML files. The reason for this is being investigated. Here's a summary of what I found.

**Sitting dates that don't return any search results in ParlInfo:**

- hofreps, 1927-11-18
- hofreps, 1985-05-13
- hofreps, 1991-05-13
- hofreps, 1996-05-30
- hofreps, 1996-11-20
- senate, 1928-03-15
- senate, 1934-08-02
- senate, 1996-11-28
- senate, 2001-08-07
- senate, 2005-09-05
- senate, 2005-11-07

**Sitting dates that return search results in Parlinfo, but don't have links to PDFs or XML files:**

- hofreps, 2000-10-12

**Sitting dates that return search results in Parlinfo and have PDF links, but don't have links XML files:**

- senate, 2000-10-12
- senate, 2004-02-10

**Sitting dates between 1981 and 1997 that return search results in ParlInfo but don't seem to have XML/SGML files:**

- hofreps, 1985-08-23
- hofreps, 1992-09-10
- hofreps, 1996-12-13
- senate, 1988-12-12
- senate, 1988-12-13
- senate, 1988-12-14
- senate, 1988-12-15
- senate, 1988-12-16
- senate, 1988-12-19
- senate, 1988-12-20
- senate, 1988-12-21
- senate, 1993-02-08
- senate, 1994-03-15
- senate, 1994-12-09
- senate, 1995-12-01

The `missing.csv` file contains some more information about these discrepencies.

## May 2024 note

A reharvest of 1901 to 1980 was run in May 2024. Most if not all of the file names seem to have changed with version flags now added, eg `_v4`. Unfortunately the new versioned urls don't redirect to the old forms. The addition of the version flags seem to indicate that corrections and improvements are being made to the xml. I've noticed, for example, some changes to the internal xml structure of files, as well as standardisation of things like quotation marks. This process seems to be ongoing ­– some urls changed as I was in the process of harvesting them! This means that this repository might not reflect the current state of Hansard, but I'll try to reharvest at more regular intervals from now on to pick up these sorts of changes.

## More info

* [GLAM Workbench: Commonwealth Hansard](https://glam-workbench.net/hansard/) – Jupyter notebooks to harvest and explore XML formatted versions of Hansard.
* [Historic Hansard](http://historichansard.net/) – my own version of Hansard, optimised for easy browsing.
* [Documentation](http://timsherratt.org/digital-heritage-handbook/docs/historic-hansard/) of the Historic Hansard site.
