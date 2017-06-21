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

## GitHub
[Doc](https://developer.github.com/v3/users/#get-the-authenticated-user)
### API
```
https://api.github.com/user
```

Method: `GET`.

Arguments:
* `access_token`: Your OAuth2 Access Token.

### JSON Response Examples
No explicit scope.
```json
{
  "login": "octocat",
  "id": 1,
  "avatar_url": "https://github.com/images/error/octocat_happy.gif",
  "gravatar_id": "",
  "url": "https://api.github.com/users/octocat",
  "html_url": "https://github.com/octocat",
  "followers_url": "https://api.github.com/users/octocat/followers",
  "following_url": "https://api.github.com/users/octocat/following{/other_user}",
  "gists_url": "https://api.github.com/users/octocat/gists{/gist_id}",
  "starred_url": "https://api.github.com/users/octocat/starred{/owner}{/repo}",
  "subscriptions_url": "https://api.github.com/users/octocat/subscriptions",
  "organizations_url": "https://api.github.com/users/octocat/orgs",
  "repos_url": "https://api.github.com/users/octocat/repos",
  "events_url": "https://api.github.com/users/octocat/events{/privacy}",
  "received_events_url": "https://api.github.com/users/octocat/received_events",
  "type": "User",
  "site_admin": false,
  "name": "monalisa octocat",
  "company": "GitHub",
  "blog": "https://github.com/blog",
  "location": "San Francisco",
  "email": "octocat@github.com",
  "hireable": false,
  "bio": "There once was...",
  "public_repos": 2,
  "public_gists": 1,
  "followers": 20,
  "following": 0,
  "created_at": "2008-01-14T04:33:35Z",
  "updated_at": "2008-01-14T04:33:35Z"
}
```

Scope = `user`:
```json
{
  "login": "octocat",
  "id": 1,
  "avatar_url": "https://github.com/images/error/octocat_happy.gif",
  "gravatar_id": "",
  "url": "https://api.github.com/users/octocat",
  "html_url": "https://github.com/octocat",
  "followers_url": "https://api.github.com/users/octocat/followers",
  "following_url": "https://api.github.com/users/octocat/following{/other_user}",
  "gists_url": "https://api.github.com/users/octocat/gists{/gist_id}",
  "starred_url": "https://api.github.com/users/octocat/starred{/owner}{/repo}",
  "subscriptions_url": "https://api.github.com/users/octocat/subscriptions",
  "organizations_url": "https://api.github.com/users/octocat/orgs",
  "repos_url": "https://api.github.com/users/octocat/repos",
  "events_url": "https://api.github.com/users/octocat/events{/privacy}",
  "received_events_url": "https://api.github.com/users/octocat/received_events",
  "type": "User",
  "site_admin": false,
  "name": "monalisa octocat",
  "company": "GitHub",
  "blog": "https://github.com/blog",
  "location": "San Francisco",
  "email": "octocat@github.com",
  "hireable": false,
  "bio": "There once was...",
  "public_repos": 2,
  "public_gists": 1,
  "followers": 20,
  "following": 0,
  "created_at": "2008-01-14T04:33:35Z",
  "updated_at": "2008-01-14T04:33:35Z",
  "total_private_repos": 100,
  "owned_private_repos": 100,
  "private_gists": 81,
  "disk_usage": 10000,
  "collaborators": 8,
  "two_factor_authentication": true,
  "plan": {
    "name": "Medium",
    "space": 400,
    "private_repos": 20,
    "collaborators": 0
  }
}
```
