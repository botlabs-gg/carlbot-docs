?> It is highly recommended to use the **[Dashboard](https://carl.gg)** for setting up automod.

![Automod](_images/automod.png ':size=75%')

## General Settings

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
[**am**\|**automod**]<br><span class="user-permissions">Manage Server</span> | `!am`             | Shows an overview of the current automod settings.                            
**automod drama** \<channel><br><span class="user-permissions">Manage Server</span> | `!automod drama #drama` | This is a [Premium](https://www.patreon.com/carlbot) command.<br>Set the channel where mods can make decisions on rule breakers through reactions.
**automod log** \<channel><br><span class="user-permissions">Manage Server</span> | `!automod log #automod` | Set the channel where the logs for automatic moderation actions go.
**automod** [media\|mo] <channels...><br><span class="user-permissions">Manage Server</span> | `!am mo #show-off` | Set the channel(s) where only posting images/links is allowed.
**automod** [unmedia\|umo\|unmo] <channels...><br><span class="user-permissions">Manage Server</span> | `!am umo #show-off` | Removes the media-only restriction from one or more channels.
**automod** [whitelist\|wl] <roles/channels><br><span class="user-permissions">Manage Server</span> | `!am wl mods #admin-chat` | Whitelists roles and/or channels so that the automod ignores messages posted in/by them.
**automod** [unwhitelist\|unwl] <roles/channels><br><span class="user-permissions">Manage Server</span> | `!automod unwl mods #admin-chat` | Removes roles and/or channels from the automod whitelist.
**deletefiles**<br><span class="user-permissions">Manage Server</span>   | `!deletefiles`    | Toggles deleting unsafe files. Safe formats include png, jpg, jpeg, gif, svg, bmp, tif, webp, webm, mp4, mov, pdf, txt, mp3, flac and wav.

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**automod server**<br><span class="user-permissions">Manage Server</span> | `/automod server` | Shows an overview of the current automod settings.                            
**automod drama** \<channel><br><span class="user-permissions">Manage Server</span> | `/automod drama #drama` | This is a [Premium](https://www.patreon.com/carlbot) command.<br>Set the channel where mods can make decisions on rule breakers through reactions.
**automod log** \<channel><br><span class="user-permissions">Manage Server</span> | `/automod log #automod` | Set the channel where the logs for automatic moderation actions go.
**automod media** <channels...><br><span class="user-permissions">Manage Server</span> | `/automod mo #show-off` | Set the channel(s) where only posting images/links is allowed.
**automod unmedia** <channels...><br><span class="user-permissions">Manage Server</span> | `/automod umo #show-off` | Removes the media-only restriction from one or more channels.
**automod whitelist** [add\|remove] <roles/channels><br><span class="user-permissions">Manage Server</span> | `!automod whitelist add mods #admin-chat` | Add or remove roles and/or channels from the automod whitelist.
**deletefiles**<br><span class="user-permissions">Manage Server</span>   | `/deletefiles`    | Toggles deleting unsafe files. Safe formats include png, jpg, jpeg, gif, svg, bmp, tif, webp, webm, mp4, mov, pdf, txt, mp3, flac and wav.

<!-- tabs:end -->


### Punishments
The punishments available are:
- **delete** - Deletes the message.
- **warn** - Warns the offender.
- **tempmute <duration>** - Temporarily mutes for the duration specified.
- **mute** - Mute for indefinite duration.
- **timeout** - Timeout the offender.
- **kick** - Kicks the offender.
- **tempban <duration>** - Temporarily bans the offender for the duration specified.
- **ban** - Bans the offender.
- **defer** - Sends the context to the drama channel and lets the mods vote on it.
- **message** - Sends a message to the channel warning the member.
- **dm/pm** - Sends a private message to the offender.

?> Input the duration in this format `3h42m`. 

?>You can add more than one punishment by separating them with commas.


## Warn Threshold
Warns do not automatically expire. Managing warns is detailed on the [Moderation](moderation) page. The warn threshold determines how Carl-bot reacts when a user receives a new warning and their total number of warnings exceeds a limit. Unless a user's warnings are reset or reduced manually, this punishment will trigger each time a user receives new warning while their total number of warnings is above your server's set limit. Set it to 0 to turn it off.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**automod** [warn\|threshold] \<limit><br><span class="user-permissions">Manage Server</span> | `!am warn 5`             | Sets the warn threshold for a punishment to be made.
**automod** [warnpunish\|wp] <punishments...><br><span class="user-permissions">Manage Server</span> | `!am wp kick` | Sets the punishment for hitting the threshold.        

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**automod threshold** \<limit><br><span class="user-permissions">Manage Server</span> | `/automod threshold 5`             | Sets the warn threshold for a punishment to be made.
**automod warnpunish** <punishments...><br><span class="user-permissions">Manage Server</span> | `/automod warnpunish kick` | Sets the punishment for hitting the threshold.

<!-- tabs:end -->


## Spam Settings

<!-- tabs:start -->

<!-- tab:Message -->
Message spam will not be active without setting a rate limit of at least 1+ messages in 1+ seconds first.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
[**slowmode**\|**sm**] [rate] [per]<br><span class="user-permissions">Manage Server</span> | `!slowmode 5 25` | Rate is the number of messages you can send per timeframe. Per is the timeframe. If you only supply one value, it sets that value as the per. (1/x)
**slowmode** [punishment\|punish\|p] <punishments...><br><span class="user-permissions">Manage Server</span> | `!sm p delete, tempmute 20m` | Sets the punishment(s) for hitting the rate limit.

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**slowmode set** \<rate><br><span class="user-permissions">Manage Server</span> | `/slowmode set 5 25` | Sets slowmode in the current channel. If you want the rate to be X messages in Y time then input `x y`. If only one value is supplied then it sets it as 1 message every supplied value.
**slowmode disable**<br><span class="user-permissions">Manage Server</span> | `/slowmode disable` | Disables slowmode in the current channel.                                
**slowmode punishment** <punishments...><br><span class="user-permissions">Manage Server</span> | `/slowmode punishment delete, tempmute 20m` | Sets the punishment(s) for hitting the rate limit.

<!-- tabs:end -->

<!-- tab:Attachments -->
Attachmentspam will not be active without setting a rate limit of at least 1+ files in 1+ seconds first.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**attachmentspam** [rate] [per=1]<br><span class="user-permissions">Manage Server</span> | `!attachmentspam 3 5` | Rate limits the number of attachments a member can post in a specific timeframe.
**attachmentspam punishment** <punishments...><br><span class="user-permissions">Manage Server</span> | `!attachmentspam p mute, defer` | Sets the punishment(s) for hitting the rate limit.

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**attachmentspam set** \<rate><br><span class="user-permissions">Manage Server</span> | `/attachmentspam set 3 5` | Rate limits the number of attachments a member can post in a specific timeframe.
**attachmentspam disable**<br><span class="user-permissions">Manage Server</span> | `/attachmentspam disable` | Disables attachmentspam in the current channel.             
**attachmentspam punishment** <punishments...><br><span class="user-permissions">Manage Server</span> | `/attachmentspam punishment mute, defer` | Sets the punishment(s) for hitting the rate limit.

<!-- tabs:end -->

<!-- tab:Mentions -->
Mentionspam will not be active without setting a rate limit of at least 1+ mentions in 1+ seconds first.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**mentionspam** [rate] [per=1]<br><span class="user-permissions">Manage Server</span> | `!mentionspam 25 5` | Enables the bot to automatically punish the mentionspammers.
**mentionspam punishment** <punishments...=mute><br><span class="user-permissions">Manage Server</span> | `!mentionspam p tempban 24h` | Sets the punishment(s) for hitting the rate limit.

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**mentionspam set** \<rate><br><span class="user-permissions">Manage Server</span> | `/mentionspam set 25 5` | Enables the bot to automatically punish the mentionspammers.
**mentionspam disable**<br><span class="user-permissions">Manage Server</span> | `/mentionspam disable` | Disables mentionspam in the current channel.                       
**mentionspam punishment** <punishments...=mute><br><span class="user-permissions">Manage Server</span> | `/mentionspam punishment tempban 24h` | Sets the punishment(s) for hitting the rate limit.

<!-- tabs:end -->

<!-- tab:Links -->
Linkspam will not be active without setting a rate limit of at least 1+ links in 1+ seconds first.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**linkspam**<br><span class="user-permissions">Manage Server</span>      | `!linkspam`       | Shows the current settings.                                                   
**linkspam** \<rate> [per=1]<br><span class="user-permissions">Manage Server</span> | `!linkspam 1 1` | Sets the link rate limit. Use the example command to block all links.
**linkspam punishment** <punishments...><br><span class="user-permissions">Manage Server</span> | `!linkspam p delte, mute, defer` | Sets the punishment(s) for hitting the rate limit.
**linkspam bl** <links...><br><span class="user-permissions">Manage Server</span> | `!linkspam bl reddit.com twitter.com` | Blacklists one or more links.                   
**linkspam wl** <links...><br><span class="user-permissions">Manage Server</span> | `!linkspam wl reddit.com twitter.com` | Whitelists one or more links.                   
**linkspam unbl** <links...><br><span class="user-permissions">Manage Server</span> | `!linkspam unbl reddit.com twitter.com` | Removes one or more links from the blacklist.
**linkspam unwl** <links...><br><span class="user-permissions">Manage Server</span> | `!linkspam unwl reddit.com twitter.com` | Removes one or more links from the whitelist.
**linkspam clearbl**<br><span class="user-permissions">Manage Server</span> | `!linkspam clearbl` | Clears the blacklist.                                                    
**linkspam clearwl**<br><span class="user-permissions">Manage Server</span> | `!linkspam clearwl` | Clears the whitelist.                                                    
**linkspam block**<br><span class="user-permissions">Manage Server</span> | `!linkspam block` | Punish all non-whitelisted links.                                             
**linkspam off**<br><span class="user-permissions">Manage Server</span>  | `!linkspam off`   | Punish only blacklisted links.                                                
**linkspam norole**<br><span class="user-permissions">Manage Server</span> | `!linkspam norole` | Punish only those without roles.                                           



<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**linkspam server**<br><span class="user-permissions">Manage Server</span> | `/linkspam server` | Shows the linkspam settings.                                               
**linkspam rate** \<rate><br><span class="user-permissions">Manage Server</span> | `/linkspam rate 1 1` | Sets the link rate limit. Use the example command to block all links.
**linkspam punishment** <punishments...><br><span class="user-permissions">Manage Server</span> | `/linkspam punishment delte, mute, defer` | Sets the punishment(s) for hitting the rate limit.
**linkspam blacklist** [add\|remove] <links...><br><span class="user-permissions">Manage Server</span> | `/linkspam blacklist add reddit.com twitter.com` | Adds or removes link(s) to/from the linkspam blacklist.
**linkspam whitelist** [add\|remove] <links...><br><span class="user-permissions">Manage Server</span> | `/linkspam whitelist remove reddit.com twitter.com` | Adds or removes link(s) to/from the linkspam whitelist.
**linkspam clear** [blacklist\|whitelist]<br><span class="user-permissions">Manage Server</span> | `/linkspam clear blacklist` | Clears the blacklist or the whitelist.
**linkspam block**<br><span class="user-permissions">Manage Server</span> | `/linkspam block` | Punish all non-whitelisted links.                                             
**linkspam off**<br><span class="user-permissions">Manage Server</span>  | `/linkspam off`   | Punish only blacklisted links.                                                
**linkspam norole**<br><span class="user-permissions">Manage Server</span> | `/linkspam norole` | Punish only those without roles.                                           

<!-- tabs:end -->

<!-- tab:Invites -->
Invitespam will not be active without setting a rate limit of at least 1+ invites in 1+ seconds first.

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**invitespam**<br><span class="user-permissions">Manage Server</span>    | `!invitespam`     | Shows the invitespam settings.                                               
**invitespam** \<rate> [per=1]<br><span class="user-permissions">Manage Server</span> | `!invitespam 1 1` | Sets the invite rate limit. Use the example command to block all invites.
**invitespam punishment** <punishments...><br><span class="user-permissions">Manage Server</span> | `!invitespam p delte, mute, defer, message` | Sets the punishment(s) for hitting the rate limit.
**invitespam bl** <links...><br><span class="user-permissions">Manage Server</span> | `!invitespam bl discord.gg/fredboat` | Adds the server that the invite goes to, to the blacklist.
**invitespam wl** <links...><br><span class="user-permissions">Manage Server</span> | `!invitespam wl discord.gg/fredboat` | Adds the server that the invite goes to, to the whitelist.
**invitespam unbl** <links...><br><span class="user-permissions">Manage Server</span> | `!invitespam unbl discord.gg/fredboat` | Removes one or more servers from the blacklist.
**invitespam unwl** <links...><br><span class="user-permissions">Manage Server</span> | `!invitespam unwl discord.gg/fredboat` | Removes one or more servers from the whitelist.
**invitespam clearbl**<br><span class="user-permissions">Manage Server</span> | `!invitespam clearbl` | Clears the blacklist.                                                    
**invitespam clearwl**<br><span class="user-permissions">Manage Server</span> | `!invitespam clearwl` | Clears the whitelist.                                                    
**invitespam** [on\|block]<br><span class="user-permissions">Manage Server</span> | `!invitespam on` | Punish all non-whitelisted invites.                                    
**invitespam off**<br><span class="user-permissions">Manage Server</span> | `!invitespam off` | Punish only blacklisted invites.                                              
**invitespam norole**<br><span class="user-permissions">Manage Server</span> | `!invitespam norole` | Punish only those without roles.                                       

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**invitespam server**<br><span class="user-permissions">Manage Server</span> | `/invitespam server` | Shows the invitespam settings.                                         
**invitespam punishment** <punishments...><br><span class="user-permissions">Manage Server</span> | `/invitespam punishment delte, mute, defer, message` | Sets the punishment(s) for hitting the rate limit.
**invitespam norole**<br><span class="user-permissions">Manage Server</span> | `/invitespam norole` | Punish only those without roles.                                       

<!-- tabs:end -->

<!-- tab:Bad Words -->
Bad words detection is case insensitive, looks for substrings and ignores punctuation. Censoring `boat` would cause Carl-bot to punish any user that said `fredboat`.

?> **Limit**<br>50 Entries

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**censor** <words...><br><span class="user-permissions">Manage Server</span> | `!censor boat`| Adds one or more words to the list of blacklisted words.                     
**censor add** <words...><br><span class="user-permissions">Manage Server</span> | `!censor add boat` | Same as above.                                                       
**censor remove** <words...><br><span class="user-permissions">Manage Server</span> | `!censor remove boat` | Removes a word from the blacklist.                             
**censor list**<br><span class="user-permissions">Manage Server</span>   | `!censor list`    | Lists all censored words.                                                     
**censor clear**<br><span class="user-permissions">Manage Server</span>  | `!censor clear`   | Clears all censored words.                                                    
**censor punishment** <punishments...=delete, defer><br><span class="user-permissions">Manage Server</span> | `!censor p mute, delete, defer` |  Sets the punishment(s) for bad words.

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**censor server**<br><span class="user-permissions">Manage Server</span> | `/censor server`  | View censor settings for server.                                              
**censor words** [add\|remove] <words...><br><span class="user-permissions">Manage Server</span> | `/censor words add boat`| Adds or removes one or more words to/from the list of blacklisted words.
**censor display**<br><span class="user-permissions">Manage Server</span> | `/censor display` | Lists all censored words.                                                     
**censor clear**<br><span class="user-permissions">Manage Server</span>  | `/censor clear`   | Clears all censored words.                                                    
**censor punishment** <punishments...=delete, defer><br><span class="user-permissions">Manage Server</span> | `/censor punishment mute, delete, defer` |  Sets the punishment(s) for bad words.

<!-- tabs:end -->

<!-- tab:Caps Limit -->

<!-- tabs:start -->

<!-- tab:Prefix Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**capslimit** \<percentage><br><span class="user-permissions">Manage Server</span> | `!capslimit 70` | Punishes messages with the % of its characters being uppercase. The message has to be at least 6 characters long.
[**capspunish**\|**capsp**\|**capspunishment**] <punishments...><br><span class="user-permissions">Manage Server</span> | `!capsp delete, warn` | Sets the punishment(s) for sending a message which hits the threshold.

<!-- tab:Slash Commands -->
Name              | Example           | Usage                                                                         
 ---------------- | ----------------- | ----------------------------------------------------------------------------- 
**caps limit** \<percentage><br><span class="user-permissions">Manage Server</span> | `/caps limit 70` | Punishes messages with the % of its characters being uppercase. The message has to be at least 6 characters long.
**caps punishment** <punishments...><br><span class="user-permissions">Manage Server</span> | `/caps punishment delete, warn` | Sets the punishment(s) for sending a message which hits the threshold.

<!-- tabs:end -->

<!-- tabs:end -->