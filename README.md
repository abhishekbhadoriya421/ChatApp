### Chat bot
> It's a web application which allow it's user to chat with random other user's

## File and Folder

**Client Folder** : This Folder Contain's file and folder for front-end code or React Code

**Server Folder** : This Folder Contain's file and folder for back-end code Like Nodejs express js mongodb etc.

## Used Tool's
>Front-End
```
React.js
React-Router-Dom
axios
emoji-picker-react
react-toastify
socket.io-client
```
>Back-End
```
Nodejs
Express.js
Mongodb
cors
bcrypt
socket.io
```

## DataBase Schema
> User Schema
```js
    const userSchema = new mongoose.Schema({
    username: {
        type: String,
        required: true,
        min: 3,
        max: 20,
        unique: true,
    },
    email: {
        type: String,
        required: true,
        unique: true,
        max: 50,
    },
    password: {
        type: String,
        required: true,
        min: 8,
    },
    isAvatarImageSet: {
        type: Boolean,
        default: false,
    },
    avatarImage: {
        type: String,
        default: "",
    },
    });
```

> Message Schema

```js

const MessageSchema = mongoose.Schema(
  {
    message: {
      text: { type: String, required: true },
    },
    users: Array,
    sender: {
      type: mongoose.Schema.Types.ObjectId,
      ref: "User",
      required: true,
    },
  },
  {
    timestamps: true,
  }
);
```

