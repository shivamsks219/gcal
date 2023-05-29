# gcal
This is a django project that fetches the events from google calendar using Outh and django Rest api.
It has two endpoints.
**1. /rest/v1/calendar/init/ -> GoogleCalendarInitView()**
   OAuth. Which will prompt user for his/her credentials
   
**2. /rest/v1/calendar/redirect/ -> GoogleCalendarRedirectView()**
  It will perform two operations
  1. Handle redirect request sent by google with code for token. You need to implement mechanism to get access_token from given code.
  2. Once got the access_token get list of events in users calendar

**Prerequisite :**
Before creating a django app, we are required to create a project in google cloud.
Then create a credential and setup Outh Consent Screen with scopes and user id to test.
Download the json file for client secret file and rename as credentials.json .

**How to use the app**
1. Clone the git repo
2. Create virtual environment 
3. Install the requirements using "pip install -r requirements.txt"
4. Copy the credentials.json in the static folder
5. Run the app using python "manage.py runserver"
