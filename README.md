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

**Screenshots**<br><br>

![Screenshot (257)](https://github.com/shivamsks219/gcal/assets/68140446/e34bc2ec-6810-465a-9b3e-eda696a5d728)
<br>**Index Page**<br><br>
![Screenshot (258)](https://github.com/shivamsks219/gcal/assets/68140446/b8cadd71-ddf6-4a31-9d86-bd507643cec7)
<br>**Outh Login**<br><br>
![Screenshot (259)](https://github.com/shivamsks219/gcal/assets/68140446/9627f6f0-afd7-42c5-8ba9-27e2c2a21ea6)
<br>**Taking permission for calendar details**<br><br>
![Screenshot (260)](https://github.com/shivamsks219/gcal/assets/68140446/cd025e12-0490-4549-be9f-7afa387be037)
<br>**Returning the Events from google Calendar**
