# [Mass shootings since Sandy Hook](http://interactive.nydailynews.com/map/mass-shootings-since-sandy-hook/)

## Usage

### How to update the json data files

1. Get the latest mass shootings spreadsheet.
    1. From [Gun Violence Archive’s reports page](http://www.gunviolencearchive.org/reports),
    1. click the [Mass Shootings 2018 link](http://www.gunviolencearchive.org/reports/mass-shooting),
    1. then click the Export as CSV button,
    1. and on the resulting page click the Download button.
1. Open the Google Sheets spreadsheet SHOOTINGS (MASS, SCHOOL)
1. Create a new tab, name it after the current date (YYYYMMDD format).
1. Compare the contents of the CSV you downloaded against the previous month's update. Import the CSV you downloaded into Google Sheets using the File --> Import menu command. From there choose the "Upload" tab, upload your CSV, and choose the "Replace current cells" option (or whatever sounds like that).
1. This is janky. You'll need to copy the Incident Date column and paste that into an excel spreadsheet to get the dates formatted the way we format the dates in this project ("13-Mar-18"). Ugh, right? And that's not all:
1. Since once Google Sheets identifies a table cell as containing a date, it obsessively holds onto that cell's formatting. The only way to fix the date formatting to what we want is to kill the original cell. In this case we delete the column.
1. So: Delete the Incident Date column, then create a new column, then paste in that column from excel.
1. Reorder the columns in your new tab. You want the columns in this order: `Incident Date    Address    City Or County    State    killed    injured    lat    long    url    headline`
1. Batch geocode the new records. Add the records lat/long's to the spreadsheet.
1. For the mass shootings we've written about, add the URL and headline.
1. Convert the spreadsheet to JSON.
1. Save the JSON in a new file named after the month it is, ala 201804.json for April 2018 or 201811.json for November 2018.
1. Put that file in the www/data directory and add it to the repo.

### How to add the updated JSON to the interactive map

