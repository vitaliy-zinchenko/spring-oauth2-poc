Google app:

{
   "web":{
      "client_id":"312024895404-ogq6mcc7dcvhhi3pm7kaa04bj68ehai3.apps.googleusercontent.com",
      "project_id":"oauth2learn",
      "auth_uri":"https://accounts.google.com/o/oauth2/auth",
      "token_uri":"https://accounts.google.com/o/oauth2/token",
      "auth_provider_x509_cert_url":"https://www.googleapis.com/oauth2/v1/certs",
      "client_secret":"gIdHKPO-wXjpo-ONqjo4rIxm",
      "redirect_uris":[
         "http://localhost:8080"
      ]
   }
}

base64(client_id:client_secret) = MzEyMDI0ODk1NDA0LW9ncTZtY2M3ZGN2aGhpM3BtN2thYTA0Ymo2OGVoYWkzLmFwcHMuZ29vZ2xldXNlcmNvbnRlbnQuY29tOmdJZEhLUE8td1hqcG8tT05xam80ckl4bQ==

Authorization Code Grant:

Flow - Part 1 - Get authorization code:

Request:
https://accounts.google.com/o/oauth2/auth?response_type=code&client_id=312024895404-ogq6mcc7dcvhhi3pm7kaa04bj68ehai3.apps.googleusercontent.com&redirect_uri=http://localhost:8080&scope=https://www.googleapis.com/auth/drive
Response:
http://localhost:8080/?code=4/4EIy9oOE2ZwEkHpw2RYiSKu-xdTQcmiYZ-aBwK7ajpg#

Flow - Part 2 - Get token:

---------------------------------
POST /o/oauth2/token HTTP/1.1
Host: accounts.google.com
Authorization: Basic MzEyMDI0ODk1NDA0LW9ncTZtY2M3ZGN2aGhpM3BtN2thYTA0Ymo2OGVoYWkzLmFwcHMuZ29vZ2xldXNlcmNvbnRlbnQuY29tOmdJZEhLUE8td1hqcG8tT05xam80ckl4bQ==
Content-Type: application/x-www-form-urlencoded
Cache-Control: no-cache
Postman-Token: c3c2d211-724c-d173-3795-91a45ce80b10

grant_type=authorization_code&code=4/8yUjKOxn7g5RVPUxPhfXr5kMQqT3wd5BAfhLAhTerzc#&redirect_uri=http://localhost:8080
---------------------------------
