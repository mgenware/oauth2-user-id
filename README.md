# oauth2-user-id
Obtain user ID via OAuth2 on different sites

## Google

API:
```
https://www.googleapis.com/oauth2/v1/userinfo
```

Arguments:
* `alt`: `"json"`.
* `access_token`: Your OAuth2 Access Token.


Sample JSON:
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
