# RSNA Measurement Crowd Sourcing tool
Based on crowdQuant


### Setup and Run
- git clone https://github.com/QTIM-Lab/rsnaCrowdQuant
- npm install
- npm start

This will start a local server that communicates with a live Couch DB. 

### DB 
http://rsnacrowdquant.cloudapp.net:5984/_utils/

### Build Views in the DB
https://github.com/pieper/Chronicle/blob/master/design/views.py



### TODO

- tag (with collection-tag (by anatomy e.g. liver, lung)) images on upload to database - Jayashree
- build view per collection-tag by enhancing views.py - Jayashree
- select next image with tag and fewest measurements - Steve to make query function
- (bug) logging in as existing user starts with series index 0 again (already measured cases) - Steve to provide query function to suggest next case that is least reviewed and not already reviewed by this user
- investigate how "U" showed up a annotator in DB ?
- consolidate databases? - probably not needed for now
- investigate 2 finger scrolling for mobile - Rob
- add kiosk mode as query parameter
-- don't the username
-- login times out after 2 minute
- improve the registration form with a few big buttons for the categories
- statistics page - Steve to make stubs, Jayashree to create infovis
- continuous replication to a backed up disk - operational plan TBD with RSNA docent
- about box with acknowledgements
- tutorial info
- auto window/level to get lung window/liver ? - Rob
- address "Uncaught Error: image has not been loaded yet"
- Android (maybe ios?) Can make 2 Length Measurements on the same image
- Potentially change least measured to be an array of all "least measured" and select one at random
- log skipped cases
- annotator is hardcoded -fix that
- skip case does not work
- make getNextSeriesForAnnotator call parallel

### DONE
- include seriesUID with measurements (still need to see if this is the right way)
- (bug) in a session: first case sends 1 measurement, second sends 2, third 3, etc.
- need to record position of start/end of line drawn lengths.data[0].handles.end.y near line 40 commands.js
- include slice index with measurements
- change browser tab title from "lightweight viewer" to "RSNA CrowdQuant"
- (bug) save in hamburger does not record annotator (removed instead)
- remove hamburger
- remember username in localStorage for easier re-login
- include slice UID with measurement
- investigate why scrolling is not working on iPad - works with 3 finger scrolling
- livereload is timing out on the real site: Fix or Remove
- see if we can save a screenshot with measurement document - Steve
- add ability to skip the case (e.g. when there is no tumor)
