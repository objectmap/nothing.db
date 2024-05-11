<img alt="." src="./assets/nothing-banner.png">

# Nothing.db
Nothing unusual, just a multifunctional local database.

# Installation
```console
npm install nothing.db
```

# Methods
- .add(Name, Number)
- .all()
- .delete(Name)
- .get(Name)
- .length()
- .push(Name, Value)
- .resetDatabase()
- .startsWith(Name)
- .set(Name, Value)
- .subtract(Name, Number)

# Example code
```js
const { Database } = require("nothing.db")

const db = new Database({
	file: "nothing.json", // (String) not required
	language: "en",  // (String) not required
	formating: true,  // (Boolean) not required
	logger: false  // (Boolean) not required
})

db.set("nothing", "is cool simple local database!")

db.on(db.evenst.Set, (data) => {
	console.log(data)
})
```

# Usage
## .add(Name, Data)
```js
// Adds a number to the data.
<Database>.add("money", 1488)
// ooutput: { ID: "money", data: 1488 }
```
## .all()
```js
// Return all data.
<Database>.all()
// output: [{ ID: "mooney", data: 1488 },{ ID: "objectmap", data: "hot developer" },{ ID: "somename", data: "somedata" }]
```
## .delete(Name)
```js
// Delete data.
<Database>.delete("objectmap")
// output: true
```
## .get(Name)
```js
// Get data with data name.
<Database>.get("objectmap")
// output: hot developer
```
## ..length()
```js
// Return size database
<Database>.length()
// output: 2
```
## .push(Name, Data)
```js
// Push data into Array[].
<Database>.push("users", "Steve")
// output: [{ ID: "users", data: ["Steve"] }]
<Database>.push("users", "Alex")
// output: [{ ID: "users", data: ["Steve", "Alex"] }]
```
## .resetDatabase()
```js
// Reset all database.js
<Database>.resetDatabase()
// output: true
```
## .startsWith(Name)
```js
// Returns all data starting with "Specified Name" in database
<Database>.startsWith("user.")
//output:
// [
// { ID: "user.Steve", data: 0 },
// { ID: "user.Alex", data: 1 },
// ]
```
## .set(Name, Data)
```js
// Set data.
<Database>.set("objectmap", "hot")
// output: { ID: "objectmap", data: "hot developer" }
```
## .subtract(Name, Data)
```js
// Adds a number to the data.
<Database>.subtract("money", 100)
// output: { ID: "money", data: 1388 }
```

# Events
- Add
- CreateDatabase
- Delete
- Push
- ResetDatabase
- Set
- Subtract

# Suppoted languages
| Language | Code |
| ------------- | ------------- |
| English (default) | en  |
| Russian  | ru  |
| Ukrainian  | ua  |
| Arabic  | ar  |
| German  | de  |

## Thank you for using (or just watching) my project, rate it with a star on the github homepage! 💜
