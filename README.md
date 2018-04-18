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
1. Compare the contents of the CSV you downloaded against the previous month's update. Copy and paste the records that are new into the new tab you just created.
1. Reorder the columns in your new tab. You want the columns in this order: `Incident Date    Address    City Or County    State    killed    injured    lat    long    url    headline`
1. Batch geocode the new records. Add the records lat/long's to the spreadsheet.
1. For the mass shootings we've written about, add the URL and headline.
1. Convert the spreadsheet to JSON.
1. Save the JSON in a new file named after the month it is, ala 201804.json for April 2018 or 201811.json for November 2018.
1. Put that file in the www/data directory and add it to the repo.
