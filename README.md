# bdfd-purge-command# bdfd-purge-command

This project implements the purge command for BDFD (Bot Designer for Discord).

# ## Usage

This command is used to quickly delete messages from a Discord channel.

##




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

$endif
