---
layout: default
title: DomIRC - Cloaks
---

# CLOAKS

A **cloak** is an alternative name for a **vHost** (virtual host).  
On DomIRC, you can find three types of vHosts: the [user](#user-cloaks) cloaks, the [group](#group-cloaks) cloaks and the [gateway](#gateway-cloaks) cloaks.  
To request a cloak, please ask in **#domirc** or see the `/msg HelpServ help request` command if you prefer the private way.  
Each cloak you can see on the network is unique, so you can safely use them to target only one person.  
Bot cloaks are considered as **user cloaks** or **group cloaks**.  


## User Cloaks

By default, when you connect to DomIRC, your [hostname](https://en.wikipedia.org/wiki/Hostname) is publicly displayed whenever someone performs a `/whois` on you.  
It can also be seen when you join/part a channel or quit the network, and IRC bots are usually keeping it for various reasons.  
If you have an account (see [registering an account](/registration/#registering-an-account)), you can request a **user cloak** to change your displayed hostname.  
Your account name **must only** contain letters, numbers and hyphens. Special characters are not allowed.  

A **user cloak** has the appearance of `user/<account name>`, where **\<account name\>** is replaced with the user's account name.  
A **bot cloak** has the appearance of `user/<account name>/bot/<bot account name>` and needs to be on a separate account.  
You can request a **bot cloak** only if yourself are already cloaked.

Please note that you **will not** be able to change your account name after being cloaked, so choose it carefully.  
If you want to change your account name before getting a cloak, see the `/msg NickServ help set accountname` command.  

You should also read the [security considerations](#security-considerations) before requesting a cloak, as they **do not** guarantee your privacy.  


## Group Cloaks

A **group cloak** is a cloak that can only be requested by the founders of an **approved channels**.  
An **approved channel** has the **HOLD** flag, see `/msg ChanServ help info` to know how to check it.  

A **group cloak** has the appearance of `<channel>/<whatever>`, where **\<channel\>** is replaced with  
the channel name, except for **topical channels** which are prefixed by the `about/` indication, and  
**\<whatever\>** is replaced with whatever is requested by the founder as long as the cloak remains unique.  

A **bot cloak** has no specific appearance and must also be requested by the founders.  

Please note that you **will not** be able to change your account name only if it is contained in your cloak.  


## Gateway Cloaks

A **gateway cloak** is a cloak prefixed by the `gateway/` indication.  
Those are automatically applied when you connect from a [registered provider](/about/#registered-providers).  
You can override a **gateway cloak** if you use a cloaked account.  

A **nat cloak** is considered as a **gateway cloak** and has the same properties.  
Those are automatically applied when you connect from some places with an extended connection limit.


## Security Considerations

A **cloak**, no matter the one we are talking about, will **never** protect nor hide your IP address properly.  
Anyone with enough knowledge about IRC knows (or should know) that, and some people know how to pretty easily  
get your IP (you can find tutorials yourself) as a `/whois` is not the only means to get someone's informations.  

So, having a **cloak** on DomIRC only allows you to display something else in **whois requests**  
and not having your IP address in everyone's logs, as some channels might publish them.  

Those are useful to target a single user, especially in bans or various bots' access lists.  
Beside that, a **group cloak** is also meant to show your affiliation with a specific group.  
