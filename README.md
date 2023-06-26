# Rocket.Chat_ES_Lucas_Paz_Suarez
Test Rocket.chat
## 1. Create new user:

Request:

```bash
curl -X POST -H "X-Auth-Token: cfPmA24o96NWXTCwHV8oMOMeQ0LRQCLDxruV1qKpiXJ" -H "X-User-Id: nRjLrqMF9cbQjrtiw" -H "Content-type:application/json" \
     http://localhost:3000/api/v1/users.create \
     -d '{"name": "name", "email": "lucaspazsuarez17@gmail.com", "password": "anypassyouwant", "username": "uniqueusername"}'
```

```json
{"user":{"_id":"f2mvYck7LC5zHGHwe","createdAt":"2023-06-26T01:19:32.279Z","username":"uniqueusername","emails":[{"address":"lucaspazsuarez17@gmail.com","verified":false}],"type":"user","status":"offline","active":true,"__rooms":["GENERAL"],"_updatedAt":"2023-06-26T01:19:32.536Z","roles":["user"],"name":"name","settings":{}},"success":true}% 
```

Result:
![image](https://user-images.githubusercontent.com/696982/248603881-2a6a692c-103d-44c4-a7b8-25363ce8d411.png)

## 2. Get a room info:

```bash
curl -H "X-Auth-Token: cfPmA24o96NWXTCwHV8oMOMeQ0LRQCLDxruV1qKpiXJ" -H "X-User-Id: nRjLrqMF9cbQjrtiw" -H "Content-type:application/json" http://localhost:3000/api/v1/rooms.info\?roomId=GENERAL
```

Result:
```json
{"room":{"_id":"GENERAL","ts":"2023-06-26T01:10:33.124Z","t":"c","name":"general","usernames":[],"msgs":2,"usersCount":2,"default":true,"_updatedAt":"2023-06-26T01:19:32.316Z"},"success":true}%
```

## 3. Get all user roles

Request: 

```bash
curl -H "X-Auth-Token: cfPmA24o96NWXTCwHV8oMOMeQ0LRQCLDxruV1qKpiXJ" -H "X-User-Id: nRjLrqMF9cbQjrtiw" -H "Content-type:application/json"  http://localhost:3000/api/v1/roles.list
```

Result:

```json
{
	"roles": [
		{
			"_id": "admin",
			"scope": "Users",
			"description": "Admin",
			"mandatory2fa": false,
			"name": "admin",
			"protected": true
		},
		{
			"_id": "moderator",
			"scope": "Subscriptions",
			"description": "Moderator",
			"mandatory2fa": false,
			"name": "moderator",
			"protected": true
		},
		{
			"_id": "leader",
			"scope": "Subscriptions",
			"description": "Leader",
			"mandatory2fa": false,
			"name": "leader",
			"protected": true
		},
		{
			"_id": "owner",
			"scope": "Subscriptions",
			"description": "Owner",
			"mandatory2fa": false,
			"name": "owner",
			"protected": true
		},
		{
			"_id": "user",
			"scope": "Users",
			"description": "",
			"mandatory2fa": false,
			"name": "user",
			"protected": true
		},
		{
			"_id": "bot",
			"scope": "Users",
			"description": "",
			"mandatory2fa": false,
			"name": "bot",
			"protected": true
		},
		{
			"_id": "app",
			"scope": "Users",
			"description": "",
			"mandatory2fa": false,
			"name": "app",
			"protected": true
		},
		{
			"_id": "guest",
			"scope": "Users",
			"description": "",
			"mandatory2fa": false,
			"name": "guest",
			"protected": true
		},
		{
			"_id": "anonymous",
			"scope": "Users",
			"description": "",
			"mandatory2fa": false,
			"name": "anonymous",
			"protected": true
		},
		{
			"_id": "livechat-agent",
			"scope": "Users",
			"description": "Livechat Agent",
			"mandatory2fa": false,
			"name": "livechat-agent",
			"protected": true
		},
		{
			"_id": "livechat-manager",
			"scope": "Users",
			"description": "Livechat Manager",
			"mandatory2fa": false,
			"name": "livechat-manager",
			"protected": true
		}
	],
	"success": true
}
```
