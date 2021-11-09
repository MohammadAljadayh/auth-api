# auth-api

### Deployment Test


- [ci/cd GitHub Actions](https://github.com/MohammadAljadayh/auth-api/actions).
- [herokuapp Link Main ](https://authapimohammad.herokuapp.com/).
**I forget to make branch dev at the first push to githup .**
- [PULL_REQUEST ](https://github.com/MohammadAljadayh/auth-api/pull/2).
- [Main Repo link](https://github.com/MohammadAljadayh/auth-api).

**Setup**

`.env` **requirements**

- `PORT` - 3001

- `DATABASE_URL` = Postgres DB

- `SECRET` = JWT 

**Running the app**

- `npm start`

- Endpoint: `/signup`

 ```
 {
    "username": "root",
    "password": "root",
    "role": "admin"
    }

```

- Returns Object

```
{
    "user": {
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6InJvb3QiLCJpYXQiOjE2MzY0OTE5MDB9.hk7MSolXWlrlf-LxsTFkO9BN4KXI0X_KGhZf7kUC58M",
        "capabilities": [
            "read",
            "create",
            "update",
            "delete"
        ],
        "id": 2,
        "username": "root",
        "password": "$2b$10$W12HziuIwdF8UEKYGyZ1WOk3dAGtDqBHNjI5RZmoS/lE3Ys1BJX.C",
        "role": "admin",
        "updatedAt": "2021-11-09T21:05:00.145Z",
        "createdAt": "2021-11-09T21:05:00.145Z"
    },
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6InJvb3QiLCJpYXQiOjE2MzY0OTE5MDB9.hk7MSolXWlrlf-LxsTFkO9BN4KXI0X_KGhZf7kUC58M"
}
```



 

- Endpoint: `/signin`

```
- Username `root`
- Password `root`
``` 
- Returns Object
```
{
    "user": {
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6InJvb3QiLCJpYXQiOjE2MzY0OTE5Nzl9.yHDQBXzy4gVEK37nBXIx1NYR38Zwe54krU2ffLDVPHU",
        "capabilities": [
            "read",
            "create",
            "update",
            "delete"
        ],
        "id": 2,
        "username": "root",
        "password": "$2b$10$W12HziuIwdF8UEKYGyZ1WOk3dAGtDqBHNjI5RZmoS/lE3Ys1BJX.C",
        "role": "admin",
        "createdAt": "2021-11-09T21:05:00.145Z",
        "updatedAt": "2021-11-09T21:05:00.145Z"
    },
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6InJvb3QiLCJpYXQiOjE2MzY0OTE5Nzl9.yHDQBXzy4gVEK37nBXIx1NYR38Zwe54krU2ffLDVPHU"
}
```



- Endpoint: `/users`

> - Token `   `

- Returns Object
[
    "root",
    "root"
]

> - Token `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6InJvb3QiLCJpYXQiOjE2MzY0OTE5Nzl9.yHDQBXzy4gVEK37nBXIx1NYR38Zwe54krU2ffLDVPHUaaaa`

- Returns Object
```
{
    "status": 500,
    "message": "Invalid Login"
}
``` 

- Endpoint: `/secret`

> - Token `  `


- Returns Object
```
Welcome to the secret area!
```

- Endpoint: `/api/v1/food`
- Post : 
```
 {
  "name": "Orange",
        "calories":"1000",
        "type": "fruit"
        }
 ``` 
 ```
  {
  "name": "tomatow",
        "calories":"500",
        "type": "vegetable"
        }
```

- Returns Object (Get)

        [
     {
    "id": 1,
    "name": "Orange",
    "calories": 1000,
    "type": "fruit",
    "updatedAt": "2021-11-09T21:11:21.027Z",
    "createdAt": "2021-11-09T21:11:21.027Z"
},
       {
    "id": 2,
    "name": "tomatow",
    "calories": 500,
    "type": "vegetable",
    "updatedAt": "2021-11-09T21:13:38.585Z",
    "createdAt": "2021-11-09T21:13:38.585Z"
}
        ]


- Endpoint: `/api/v2/clothes`

> - Token `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6InJvb3QiLCJpYXQiOjE2MzY0OTE5Nzl9.yHDQBXzy4gVEK37nBXIx1NYR38Zwe54krU2ffLDVPHU`

- Returns Object
```
[
    {
        "id": 1,
        "name": "TEST",
        "color": "red",
        "size": "xl",
        "createdAt": "2021-11-09T21:16:14.537Z",
        "updatedAt": "2021-11-09T21:16:14.537Z"
    },
    {
        "id": 2,
        "name": "TEST",
        "color": "red",
        "size": "xl",
        "createdAt": "2021-11-09T21:16:16.160Z",
        "updatedAt": "2021-11-09T21:16:16.160Z"
    }
]
``` 
**Tests**

- Unit Tests: `npm run test`
- Lint Tests: `npm run lint`

**UML**

![UML](UML.PNG)
