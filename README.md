social-media-app/
│
├── cmd/
| |── app/
| │ └── app.go
│ └── main.go
├── internals/
| |── config/
| │ └── config.go
| |── constants/
| │ └── constants.go
| |── server/
| │ └── server.go
| │ └── handlers.go
| │ └── middleware.go
| |── database/
| │ └── db.go
| |── cache/
| │ └── cache.go
├── controllers/
│ └── users.go
│ └── posts.go
│ └── friendship.go
├── models/
│ └── user.go
│ └── post.go
├── routes/
│ └── routes.go
├── services/
│ └── user_service.go
│ └── post_service.go
└── utils/
| └── utils.go
└── go.mod
└── go.sum
└── makefile

1. Notification store to keep track of users and their channels
2. New user added -> add entry in the notification store.
3. New user added -> start listening on the notifications channel in a go routine.
4. New Post added -> Start notifying all friends
5. Get Notification!!!
