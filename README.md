# blackcode-api
<a href="https://web.blackcodetr.cf/dc" target="_blank"><img src="https://img.devsforum.net/tr/img/h1Z2X3.png" alt="Join our discord" width="256"></a><br>
**Support:** [https://web.blackcodetr.cf/dc](https://web.blackcodetr.cf/dc) <br>
**NPM:** [npmjs.com/package/blackcode-api](https://www.npmjs.com/package/blackcode-api)<br>

# Announcemenets / Duyurular


## Installation
*If you have trouble with the installation, please feel free to visit our [discord](https://web.blackcodetr.cf/dc) address.*
- `npm i blackcode-api`

## Getting Started
- `Base URL: https://web.blackcodetr.cf/api/`
- `const black = require("blackcode-api")`

# Has Voted
```json
{
 "user": "",
 "hasvote": "false/true"
}
```
```js
let a = await black.hasVoted(botID, userID);
if(a.error) {
console.log("Error: "+a.message)
} else {
if(!a) { 
console.log("vote pls")
} else {
console.log("your voted")
}
}
```


# Bot Information
```json
{
 "tags": [""],
 "coowners": [""],
 "votes": "",
 "botID": "",
 "ownerID": "",
 "ownerName": "",
 "username": "",
 "discrim": "",
 "avatar": "",
 "longDesc": "",
 "shortDesc": "",
 "prefix": "",
 "certificate": "",
 "premium": "",
 "status": ""
}
```
```js
let b = await black.info(botID);
if(b.error) {
console.log("Error: "+b.message)
} else {
console.log(`
{
 "tags": [${b.tags}],
 "coowners": [${b.coowners}],
 "votes": ${b.votes},
 "botID": ${b.botID},
 "ownerID": ${b.ownerID}
}
`)
}
```

# Bot Search
```json
{
  "botID": "",
  "votes": "",
  "owner": "",
  "ownerID": "",
  "coowners": []
}
```
```js
let b = await black.search(value);
  if(b.error) {
  console.log(`
  "error": true,
  "message": "${b.message}",
  "errorcode": ${b.errorcode}
  `)  
  } else {
  console.log(`
  "botID": "${b.botID}",
  "votes": "${b.votes}",
  "owner": "${b.owner}",
  "ownerID": "${b.ownerID}",
  "coowners": [${b.coowners}]
  `)
  }
```
