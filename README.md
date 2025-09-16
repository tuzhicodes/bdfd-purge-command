# 🧹 BDFD Purge Command  

A clean & professional **purge/clear command** for Discord bots made with **[Bot Designer for Discord (BDFD)](https://botdesignerdiscord.com/)**.  

This repository contains an easy-to-use purge command that lets admins quickly delete bulk messages while keeping your server clean and organized.  

---

## ✨ Features
- 🔒 **Admin Only** → Runs only if the user has `ADMIN` permissions  
- 🧹 **Bulk Delete** → Removes multiple messages in one go  
- ⚠️ **Error Handling** → Detects old messages that cannot be deleted  
- ⏳ **Auto Cleanup** → Deletes bot’s response messages after 10 seconds  
- 🛠️ **Beginner-Friendly** → Just copy-paste into BDFD and use  

---

## 📜 Usage
In your Discord server, type:

➡️ This will delete the last **10 messages** from the channel.  

---

## 💻 The Code
Copy this into your BDFD command:

```bdfd
$nomention
$onlyPerms[admin;<a:TuZhi_Warn:1411694998797287497> **| $displayName**, you need admin perm to use this command!]
$onlyIf[$message[1]!=;❌ **| $displayName** Use like **`T!purge 10`**]

$try
$clear 
$deletecommand
<a:TuZhi_Warn:1411694998797287497> **| $displayName** **`$message[1]`** messages have been deleted successfully!
$catch
⚠️ **| $displayName** This message is too old and cannot be deleted!
$deleteIn[10s]
$endtry
