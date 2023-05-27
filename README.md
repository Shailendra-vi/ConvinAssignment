
# Convin Assignment Problem Statement

In this assignment you have to implement google calendar integration using django rest api. You need to use the OAuth2 mechanism to get users calendar access. Below are detail of API endpoint and corresponding views which you need to implement

    /rest/v1/calendar/init/ -> GoogleCalendarInitView()
This view should start step 1 of the OAuth. Which will prompt user for his/her credentials

    /rest/v1/calendar/redirect/ -> GoogleCalendarRedirectView()
This view will do two things
- Handle redirect request sent by google with code for token. You need to implement mechanism to get access_token from given code
- Once got the access_token get list of events in users calendar



## Run

Clone the project

```bash
  git clone https://github.com/Shailendra-vi/ConvinAssignment
```


Generate Credentials
```bash
  Go to console.cloud.google.com
  Add Calendar API from Services
  # Make sure localhost:8080 is added in redirect_uri and also add your testing email id in OAuth consent screen.
  Save credentials.json in base directory
```


Install dependencies
```bash
  pip install -r requirements.txt
```

Start local server
```bash
  python manage.py runserver
```

