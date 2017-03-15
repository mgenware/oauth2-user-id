# OAuth2 User ID
Obtain User ID via OAuth2 AccessToken on different sites.

## Google

### API
```
https://www.googleapis.com/oauth2/v1/userinfo
```

Method: `GET`.

Arguments:
* `alt`: `json`.
* `access_token`: Your OAuth2 Access Token.

### JSON Response Examples
OAuth Scope = `profile`:
```json
{
 "id": "11421324<...Secret...>",
 "name": "Ryan Liu",
 "given_name": "Ryan",
 "family_name": "Liu",
 "picture": "https://lh4.googleusercontent.com/-inpJebsD9oE/AAAAAAAAAAI/AAAAAAAAAAs/rfzWSJk5zEI/photo.jpg",
 "locale": "en"
}
```

OAuth Scope = `email`:
```json
{
 "id": "1142132<...Secret...>",
 "email": "<...Your Email...>",
 "verified_email": true,
 "name": "",
 "given_name": "",
 "family_name": "",
 "picture": "https://lh4.googleusercontent.com/-inpJebsD9oE/AAAAAAAAAAI/AAAAAAAAAAs/rfzWSJk5zEI/photo.jpg"
}
```

OAuth Scope = `openid`:
```json
{
 "id": "1142132<...Secret...>",
 "name": "",
 "given_name": "",
 "family_name": "",
 "picture": "https://lh4.googleusercontent.com/-inpJebsD9oE/AAAAAAAAAAI/AAAAAAAAAAs/rfzWSJk5zEI/photo.jpg"
}
```

## Facebook
### API
```
https://graph.facebook.com/me
```

Method: `GET`.

Arguments:
* `access_token`: Your OAuth2 Access Token.

### JSON Response Examples
Default Scope: `public_profile`:
```json
{
  "name":"Ryan Liu",
  "id":"170879<...Secret...>"
}
```
