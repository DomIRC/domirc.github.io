---
layout: default
title: DomIRC - About
---

# CLOAKS

A **cloak** is an alternative name for a **vHost** (virtual host).  
On DomIRC, you can find three types of vHosts: the [user](#user-cloaks) cloaks, the [group](#group-cloaks) cloaks and the [gateway](#gateway-cloaks) cloaks.  
Each cloak you can see on the network is unique, so you can safely use them to target only one person.
Bot cloaks are considered as  **user cloaks** or **group cloaks**.


## User Cloaks

By default, when you connect to DomIRC, your [hostname](https://en.wikipedia.org/wiki/Hostname) is publicly visible and displayed when someone performs a `/whois` on you.  
If you have an account (see [registering an account](/registration/#registering-an-account)), you can request a **user cloak** to change your displayed hostname.  
Your account name **must only** contain letters, numbers and hyphens. Special characters are not allowed.  

A **user cloak** has the appearance of `user/<account name>`, where **<account name>** is replaced by the user's account name.  
A **bot cloak** has the appearance of `user/<account name>/bot/<bot account name>` and needs to be on a separate account.  
You can request a **bot cloak** only if yourself are already cloaked.

Please note that you **will not** be able to change your account name after being cloaked, so choose it carefully.  
If you want to change your account name before getting a cloak, see the `/msg NickServ help set accountname` command.  

You should also read the [security considerations](#security-considerations) before requesting a cloak, as they **do not** guarantee your privacy.  


## Group Cloaks

A **group cloak** is a cloak that can only be requested by the founders of an **approved channels**.  
An **approved channel** has the **HOLD** flag, see `/msg ChanServ help info` to know how to check it.  

A **group cloak** has the appearance of `<channel>/<whatever>`, where **<channel>** is replaced by  
the channel name, except for **topical channels** which are prefixed by the `about/` indication, and  
**<whatever>** is replaced by whatever is requested by the founder as long as the cloak remains unique.  

A **bot cloak** has no specific appearance and must also be requested by the founders.  

Please note that you **will not** be able to change your account name only if it is contained in your cloak.  


## Gateway Cloaks

A **gateway cloak** is a cloak prefixed by the `gateway/` indication.  
Those are automatically applied when you connect from a [registered provider](/about/#registered-providers).  
You can override a **gateway cloak** if you use a cloaked account.  

A **nat cloak** is considered as a **gateway cloak** and has the same properties.  
Those are automatically applied when you connect from some places with an extended connection limit.