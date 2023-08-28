Feeds are a way for you to make announcements and ping a specific role without having to deal with the annoyances and potential abuse from having a mentionable role or manually toggling a role inbetween mentionable and not.

A feed is an association between a role and a channel. When you use the feed announce command, the role will be set to mentionable very briefly, the role will be pinged and your message will be sent in the channel with which the feed is associated, and the role will subsequently be set back to unmentionable.

## Feed Commands

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
[**feed**\|**feeds**]<br><span class="user-permissions">Manage Server</span> | `!feeds`          | Lists all the feeds that have been set up in the server.                      
**feeds create** \<name> \<role><br><span class="user-permissions">Manage Server</span> | `!feeds create got game of thrones` | Creates a feed in the channel the command is used in with a specific name and a specific role that will be mentioned.
**feeds announce** \<name> \<content><br><span class="user-permissions">Manage Server</span> | `!feeds announce got Hey guys, everyone dies` | Makes an announcement to the specified feed.
**feeds** [delete/del/remove] \<name><br><span class="user-permissions">Manage Server</span> | `!feeds del got` | Deletes a feed.                                            
**feeds clear**<br><span class="user-permissions">Manage Server</span>   | `!feeds clear`    | Delets all feeds from the server.                                             
**feeds move** \<name> \<channel><br><span class="user-permissions">Manage Server</span> | `!feeds move got #tv-shows` | Moves a feed to a specified channel.                

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**feeds list**<br><span class="user-permissions">Manage Server</span>    | `/feeds list`     | Lists all the feeds that have been set up in the server.                      
**feeds create** \<name> \<role><br><span class="user-permissions">Manage Server</span> | `/feeds create got @game of thrones` | Creates a feed in the channel the command is used in with a specific name and a specific role that will be mentioned.
**feeds announce** \<name> \<content><br><span class="user-permissions">Manage Server</span> | `/feeds announce got Hey guys, everyone dies` | Makes an announcement to the specified feed.
**feeds delete** \<name><br><span class="user-permissions">Manage Server</span> | `/feeds delete got` | Deletes a feed.                                                      
**feeds clear**<br><span class="user-permissions">Manage Server</span>   | `/feeds clear`    | Delets all feeds from the server.                                             
**feeds move** \<name> \<channel><br><span class="user-permissions">Manage Server</span> | `/feeds move got #tv-shows` | Moves a feed to a specified channel.                

<!-- tabs:end -->


## Autofeeds

Automatic feeds can be seen as group reminders, and they share a lot of functionality with reminders.

?> Timezones suck, use the [Dashboard](https://carl.gg) to create autofeeds with your local timezone.

![Autofeeds](_images/create_autofeed.png ':size=75%')

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
[**autofeed**\|**autofeeds**\|**af**]<br><span class="user-permissions">Manage Server</span> | `!af` | Lists all autofeeds that have been set up in the server.                      
**autofeeds create** \<role> \<time> \<message><br><span class="user-permissions">Manage Server</span> | `!af create "Final Fantasy" 18h The servers have been reset.` | Autofeeds that will ping the role specified each time they run.
**autofeeds silent** \<time> \<message><br><span class="user-permissions">Manage Server</span> | `!af silent 2h Vote for Carl-bot on Top.gg` | Autofeeds that won't ping any role each time they run.
**autofeeds silence** \<id><br><span class="user-permissions">Manage Server</span> | `!af silence 37` | Silences an already existing autofeed.                              
**autofeeds repeat** \<id> \<time><br><span class="user-permissions">Manage Server</span> | `!af repeat 13 24h` | Marks an autofeed to be repeated. This keeps going until you delete the autofeed.
**autofeeds remove** \<id><br><span class="user-permissions">Manage Server</span> | `!af remove 77` | Removes an autofeed.                                                   
**autofeeds clear**<br><span class="user-permissions">Manage Server</span> | `!af clear`     | Removes all autofeeds.                                                        
**autofeeds move** \<id> \<channel><br><span class="user-permissions">Manage Server</span> | `!af move 73 #general` | Moves an autofeed to the specified channel.            

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**autofeeds list**<br><span class="user-permissions">Manage Server</span> | `/autofeeds list` | Lists all autofeeds that have been set up in the server.                      
**autofeeds create** \<role> \<when> \<message><br><span class="user-permissions">Manage Server</span> | `/autofeeds create @FF 18h The servers have been reset.` | Autofeeds that will ping the role specified each time they run. |\
**autofeeds everyone** \<duration><br><span class="user-permissions">Manage Server</span> | `/autofeeds everyone 24h Good morning` | Creates an autofeed that pings @everyone.
**autofeeds here** \<duration><br><span class="user-permissions">Manage Server</span> | `/autofeeds here 24h Good morning` | Creates an autofeed that pings @here.           
**autofeeds silent** \<duration><br><span class="user-permissions">Manage Server</span> | `/autofeeds silent 2h Vote for Carl-bot on Top.gg` | Autofeeds that won't ping any role each time they run.
**autofeeds silence** \<id><br><span class="user-permissions">Manage Server</span> | `/autofeeds silence 37` | Silences an already existing autofeed.                        
**autofeeds repeat** \<id> \<when><br><span class="user-permissions">Manage Server</span> | `/autofeeds repeat 13 24h` | Marks an autofeed to be repeated. This keeps going until you delete the autofeed.
**autofeeds delete** \<id><br><span class="user-permissions">Manage Server</span> | `/autofeeds delete 77` | Removes an autofeed.                                            
**autofeeds clear**<br><span class="user-permissions">Manage Server</span> | `/autofeeds clear` | Removes all autofeeds.                                                     
**autofeeds move** \<id> \<channel><br><span class="user-permissions">Manage Server</span> | `/autofeeds move 73 #general` | Moves an autofeed to the specified channel.     

<!-- tabs:end -->

### Variables
These variables can be used in the message that is sent through an autofeed:
- `{server}` - Server name
- `{channel}` - Channel name
- `{unix}` - Unix time