# springboot-oauth2-mysql
In this project you will learn oauth2 example with mysql in springboot.

You can create DB manually or it can be created automatically.

### Get access token request.
```
URL: http://localhost:8081/oauth/token
Method: POST
Authorization: Basic Auth/username(ClientId)/password(secret)
Content-Type: application/x-www-form-urlencoded
Body:
  username: <username>
  password: <password>
  grant_type: password
  
 Response:
  {
    "access_token": "43c76f19-724e-40d8-8929-2a01a458e5a3",
    "token_type": "bearer",
    "refresh_token": "ab3df451-b068-44fb-942f-af62cbe290a2",
    "expires_in": 899,
    "scope": "read"
}
```


### Get access token using refresh_token request.
```
URL: http://localhost:8081/oauth/token
Method: POST
Authorization: Basic Auth/username(ClientId)/password(secret)
Content-Type: application/x-www-form-urlencoded
Body:
  grant_type: refresh_token
  refresh_token: <Enter refresh token>
  
 Response:
{
    "access_token": "fdd123a0-9e65-48e7-8a90-59d5e1d081cc",
    "token_type": "bearer",
    "refresh_token": "af3dd145-ae30-403a-afcb-ae20f944789d",
    "expires_in": 899,
    "scope": "read"
}
```

# Thank you!
