# Member dump

!!! info "Flags"
    * `--format/-f` <format> Formatting rules for each member
    * `--desc/-d` Sort descending
    * `--has-roles/-r <roles...>` Show members with any of these roles
    * `--order/-o <by>` Order by name, id, created_at, joined_at or nick
    * `--limit/-l <number>` Only outputs that number of members
    * `--has-all-roles <roles...>` Show members with all these roles
    * `--no-roles` Show members without roles
    * `--enumerate/-e` Enumerate entries
    * `--separator/-s <sep>` Changes what the separator is (newline by default, no idea why anyone would want this)
    * `--dateformat <fmt>` Changes the way dates are represented. See [strftime.org](http://strftime.org/) for these flags.

!!! info "Variables"
	Variables follow `--format` or `-f`

    * `%u` is a full name, example: Carl#0001
    * `%n` is the member's display name (nick if it exists otherwise username)
    * `%i` is their id
    * `%c` is the account creation date
    * `%j` is when they joined the server

**!dump** Is a special command that deserves its own page.

The syntax is **!dump [role] [args]**

If you're not used to using flags this might be confusing, so here are some examples and what they do:

!!! tldr "!dump Patrons --enumerate --order id -f %n %c --dateformat %c --limit 10"
	Dumps the 10 oldest accounts with the patreon role. Output:
	```
	1. evlsmurf Mon Aug 31 22:23:33 2015
	2. Hammy:hamster: Thu Sep 24 23:04:31 2015
	3. iscottnoidea Tue Sep 29 14:35:10 2015
	4. Ahmad Fri Oct  2 14:22:21 2015
	5. Zerxion :coffee: Mon Oct  5 07:36:54 2015
	6. ! Whoozard Tue Oct 20 16:48:57 2015
	7. Iris Tue Oct 27 01:53:04 2015
	8. orangespire Thu Oct 29 06:51:14 2015
	9. aphoenix Mon Nov  9 02:09:03 2015
	10. Terra Fri Dec  4 02:49:17 2015
	```

!!! tldr "!dump -o id --limit 10 --no-roles"
	Dumps the 10 oldest accounts without roles. Output:
	```
	Andy#7194 (23572087872421888)
	macki#9999 (48287434319855616)
	Xaric123#8510 (49188871384072192)
	Blackstar#1425 (49212295229739008)
	Nyte#0001 (49253701973442560)
	Xin#1645 (49548576702861312)
	Fondue#7609 (49663303806357504)
	Ryando#2997 (53163621441605632)
	ZeroMastery#1287 (53695818749706240)
	Tristin#7915 (54374655984668672)
	```

!!! tldr "!dump -o joined_at -d --limit 1 -r Moderator"
	Dumps the moderator who joined most recently

The order of the flags does not matter, below is a more in-depth explanation of how it works.

```
!dump --enumerate -f %u (%i) -o id -d --limit 50
       │          │          │     │
       │          │          │     └── Descending order
       │          │          └── Order by id
       │          └── The format currently used
       └── Prepends each line by the line number, emulating a text editor
```