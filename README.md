# sky-api
Steps to connect Google Workspace with Blackbaud SKY API using Google Apps Script

## 1. Create 3 Accounts:
#### Blackbaud Account (with BB ID) and Security in Education Management
#### Google "Service" account to store Google Scripts
#### SKY API Developer account at developer.blackbaud.com
## 2. Create a new Application in the developer account (SKY Extract)
#### Get the application ID after it is created
## 3. BB Environment Administrator needs to:
#### Install Sky API Console from the BB Marketplace in the school environment
#### Connect the SKY Extract application to the envirnoment (get Application ID from #2 above)
####  go to this URL https://app.blackbaud.com/marketplace/manage
###### Click Manage at the top of the screen
###### Click Connect App (blue button)
###### for the application ID, copy and paste the ID below
###### click Connect
## 4. Create a new Google Apps Script to be a Library Script (BSKY Library)
#### Create a new script
#### Add the OAUTH2 library (ID = 1B7FSrk5Zi6L1rSxxTDgDEUsPzlukDsi4KGuTMorsTQHhGBzBkMun4iDF From https://github.com/googleworkspace/apps-script-oauth2
#### Insert Code in attached file
###### Sky Subscription is code from SKY API Console	
###### Client ID & Client Secret are from new application under #2 Above
###### Subscription is from Developer subscriptions at https://developer.blackbaud.com/subscriptions/
## 5. Run the BSKY Library script to set up the OAUTH connection
#### Run showRD to create a redirect URI (requires authorization)
#### Return to the Blackbaud app (#2).  Paste in the Redirect URI to the app created
## 5. Authorize the BSKY Library script connection between Google App Script and Developer account
#### Return to the BSKY Library script
#### Deploy it as a web app
#### Execute the web app, authorize access to the Blackbaud account from #1 above
#### The BSKY Library is now a Google Apps Script Library which can be used in other Google Scripts
## Sample Script for a Google Sheet
#### Create google spreadsheet, add Apps Script
#### Add library key to script above in the sheet script
#### Sample code will pull an Advanced List from Blackbaud Education Managment into a Google Sheet
