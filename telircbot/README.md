This is a small Telegram/IRC bot that listens to IRC channels and notifies the user on Telegram 
whenever his name is mentioned. It is also possible to chat in an IRC using Telegram, or to listen
to IRC channels. 

Every telegram message from the 'owner' that starts with a comma is interpreted as a command. The
following commands are available:

* ,join [channel]       joins channel
* ,part [channel]       leaves channel 
* ,listen               turns on listening mode on all channels(in listening mode, all irc messages are redirected to TG)
* ,nolisten             turns off listening mode on all channels (only messages containing IRC_OWNER_NICKS are redirected)
* ,addlisten [channel]  adds [channel] to the channels you are listening to
* ,remlisten [channel]  stops listening to [channel]
* ,channel [channel]    Sets the channel the bot is currently writing to to channel
* ,[message]            Sends a message to the currently set channel
* ,ping                 Prints a short info about the bot's status
* ,reconnect            Reconnects to IRC. Use this when the IRC listener is dead.

Make sure all constants are set to proper values.
Also, this bot logs your irc messages. Logs are stored in irclogs/, make sure that directory exists (or
turn off logging by commenting the corresponding lines in the source).

This bot requires PyTg by luckydonald. It can be found on github: 
https://github.com/luckydonald/pytg
Make sure PyTg and all its dependencies are installed. I recommend to run telegram-cli at least
once before using this script, and register a phone number. Otherwise, things might break.
It is possible to use your own phone number and set the bot to send messages to itself. However, this
won't trigger a telegram notification which kind of defeats the purpose.

Author: Alinea
