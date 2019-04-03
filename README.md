# medical-data-date-extraction

Goal is to identify all of the different date variants encoded in this medical dataset and to properly normalize and sort the dates. We will be using pandas and regular expressions to extract and normalize date.

Each line in data may or may not contain a date and date could be in any format. Some of the date variants that are encountered in this dataset:

* ###### 04/20/2009; 04/20/09; 4/20/09; 4/3/09
* ###### Mar-20-2009; Mar 20, 2009; March 20, 2009; Mar. 20, 2009; Mar 20 2009;
* ###### 20 Mar 2009; 20 March 2009; 20 Mar. 2009; 20 March, 2009
* ###### Mar 20th, 2009; Mar 21st, 2009; Mar 22nd, 2009
* ###### Feb 2009; Sep 2009; Oct 2010
* ###### 6/2008; 12/2009
* ###### 2009; 2010


**Assumptions**:
* ###### Assume all dates in xx/xx/xx format are mm/dd/yy
* ###### Assume all dates where year is encoded in only two digits are years from the 1900's (e.g. 1/5/89 is January 5th, 1989)
* ###### If the day is missing (e.g. 9/2009), assume it is the first day of the month (e.g. September 1, 2009).
* ###### If the month is missing (e.g. 2010), assume it is the first of January of that year (e.g. January 1, 2010).
* ###### Watch out for potential typos as this is a raw, real-life derived dataset.
