---
layout: default
title: registration
---

# REGISTRATION


## Registering a nickname  
Registering your nickname prevents other people to use it / steal it from you.  
It will also allow you to register a channel in order to manage it.

To register a nickname, you will need to type the following command in your IRC client:  
> /msg NickServ REGISTER \<password\> \<email\>

Replace `<password>` by your own secret password and `<email>` by a valid email address.

You will receive an email confirmation containing a command like that:  
> /msg NickServ VERIFY REGISTER \<code\>

Just copy & paste it in your IRC client and that's all, your nick is now registered!

To login, you will need to configure SASL or type the following command each time you connect to the network:  
> /msg NickServ IDENTIFY \<password\>

Of course, replace `<password>` by the password you used to register.  
If you are not using your registered nickname, please specify it before the password.

You can have multiple nicks under your account.  
To add another nickname to your account, take it then use the following command:  
> /msg NickServ GROUP

You must be connected to your account for this command to work.

For more information about NickServ's commands:  
> /msg NickServ HELP


## Registering a channel

Before registering any channel, you must have registered your nickname (see [Registering a nickname](#registering-a-nickname)).  
Trying to register a channel with an unregistered nickname or without being identified to services **will** fail.

### Domain name channels
In order to register a channel matching your domain name (*e.g.* #domain.tld) you have to set a TXT record as `DomIRC <nick>` (case unsensitive).  
You will need to replace `<nick>` by the nickname you use on DomIRC in order to prove your domain name ownership.

If your nickname doesn't match the one in the record or the record is otherwise invalid, channel registration will fail.  
We advise you remove the TXT record once your channel is registered in order to prevent channel theft if your nickname is dropped.  
Once your channel is registered, you may register a channel for any section of your website (*e.g.* #domain.tld/staff) without needing verification.

### Group channels
Any channel whose name begins with a single sharp without matching a domain name (*e.g.* #group)is considered a group channel.  
To register such a channel, you must be able to prove that you are a representative of that group, which will be checked manually by the network staff.  
Once you have a group channel registered to your name, you may register any channel whose name begins with the channel name's followed by a dash (*e.g.* #group-dev) without needing verification.

### Standard channels
Any channel whose name begins with a double sharp (*e.g.* ##channel) may be registered without any restriction.

### Command
To register a channel, you will need to type the following command in your IRC client:  
> /msg ChanServ REGISTER \<channel\>

Replace `<channel>` by the name of the channel you wish to register.  
If you are allowed to register the channel, you will be granted its foundership.  
You may register multiple channels under the same nickname.

For more information about ChanServ's commands:  
> /msg ChanServ HELP