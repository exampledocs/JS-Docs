## SkyAuth JavaScript Example

##### API 1.0 > Example is using Encryption so Request will be encrypted, and it needs to be decrypted before using.

-----------

##### **Filling SkyAuth Class Constructor**
```js
const SkyAuthApp = new SkyAuth(
    '',      // Application Name
    '',     // Application OwnerId
    '',    // Application Secret
    '1.0' // Application Version
);
```

##### **Initializing Application**
```js
await SkyAuthApp.Initialize();
```
---

##### **General Features**
###### **Login**
```js
await SkyAuthApp.login("<USERNAME>", "<PASSWORD>");
```

###### **Register**
```js
await SkyAuthApp.register("<USERNAME>", "<PASSWORD>", "<LICENSE/KEY>", "<OPTIONAL EMAIL>")
```

###### **Forgot**
```js
await SkyAuthApp.forgot("<USERNAME>", "<EMAIL>");
```

###### **License Login**
```js
await SkyAuthApp.license("<LICENSE/KEY>");
```

###### **Upgrade an Account**
```js
await SkyAuthApp.upgrade("<USERNAME>", "<LICENSE/KEY>");
```
---

##### **Variables**
###### **Get Public Variable**
```js
await SkyAuthApp.var("<VarId>");
```

###### **Get User Variable**
```js
await SkyAuthApp.GetVar("<VarId>");
```

###### **Set User Variable**
```js
await SkyAuthApp.SetVar("<VarId>", "<VarData>");
```
---
##### **Banning Logged in User**
```js
await SkyAuthApp.ban();
```
---

##### **File Downloads**
```js
await SkyAuthApp.file("<FileId>");
```
---
##### **Webhooks**

###### Normal Request with Params
```js
await SkyAuthApp.webhook("<WebId>", "<Params>")
```

###### Webhook Request with Body & Content Type
```js
await SkyAuthApp.webhook("<WebId>", "<Params>", "<Body>", "<Content Type>");
```

###### Discord Webhook Example
```js
await SkyAuthApp.webhook("<WebId>", "", "{\"content\": \"webhook message here\",\"embeds\": null}", "application/json");
```
---
##### **Checks**
###### Check Session Status
```js
await SkyAuthApp.check();
```

##### **Check Blacklist Status**
```js
await SkyAuthApp.checkBlack();
```

##### **Check / Fetch Online Users**
```js
await SkyAuthApp.fetchOnline();
```
---


##### **Chats**
###### Get 20 Latest Chat Messages

```js
await SkyAuthApp.ChatGet();
```

###### Send Chat Message
```js
await SkyAuthApp.ChatSend("<ChannelName>", "<Message>");
```
---

##### **Logs**
```js
await SkyAuthApp.log("<Message>");
```
---

### **Additional / Extra Functions**

##### **Set/Change Console Title**
```js
await SkyAuthApp.setTitle("<NewTitle>");
```

##### **Sleep is ms(s)**
```js
await SkyAuthApp.sleep("<1 sec = 1000ms>")
```
