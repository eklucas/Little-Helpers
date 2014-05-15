<h1>What is a CSV?</h1>
*<h6>by Travis Hartman and Liz Lucas</h6>*

Is it a drug store?  Some kind of tropical disease?  No, no, it’s a data format: a type of **text file**.

A quick word about text files: in the world of data formats, a text file does not refer to a `.doc` or `.pdf`, but rather a `.txt` or `.csv`. A text file contains _machine-readable_ text, not necessarily _human-readable_ text.

CSV stands for ***Comma-Separated Values***, and is also sometimes referred to as Character-Separated Values, because the separator (or “delimiter”) does not have to be a comma. It is a format that almost all programs (e.g. Excel, Microsoft Access, MySQL) can understand and import. It also has the advantage of being somewhat **understandable to humans** at a glance. You may not be able to make perfect sense of what’s in there, but you can eyeball it quickly in a text editor to see if it’s what you expected, which is nice. 

It will look something like this:
```
SSN,"LNAME","FNAME","MNAME","DEATHMON","DEATHDAY","DEATHYR","BIRTHMON","BIRTHDAY","BIRTHYR"
86056266,"LANDSMAN","ABE","","12","00","1969","09","15","1894"
86056268,"KILLIAN","LORETTA","","01","00","1984","04","24","1900"
86056269,"SHEAR","MICHAEL","","11","00","1970","05","20","1884"
86056272,"FICARRA","JOSEPH","","01","00","1980","03","17","1914"
86056274,"DIMEOLA","MARJORIE","","09","00","1989","02","18","1903"
```
This is a small snapshot of the [Social Security Administration's Death Master File](http://ire.org/nicar/database-library/databases/social-security-administration-death-master-file/), the most complete list of dead people currently available. 

You'll notice that the first row looks a little different than the other rows: it's called the **header row**, and contains the names of each field in the data. The first value is "SSN", so the first column of data will be the social security numbers for the people who've died. _Don't worry, these are public records._

The commas separate the values for each column in a row. The first row of data below the header row contains 10 values, all separated by commas, because there are 10 columns in this data snapshot. 

Notice too that most values are surrounded by double quotes: `"LANDSMAN"` The double quote is a **text qualifier**, which helps programs identify text fields as opposed to number or date fields. 

Most programs will have an import wizard to help you import a CSV file, and the wizard will ask you for some information about your file: What is the delimiter? What is the text qualifier? What data type is each field? 

Most CSVs have a comma as a delimiter, but there are a number of other options, too:
  * pipe `|` 
  * tab
  * space
  * tilde `~`

The text qualifier is often either double quotes `"` or single quotes `'`.

As for data types, refer to the **record layout**.
