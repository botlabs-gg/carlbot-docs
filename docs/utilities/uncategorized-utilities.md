# Uncategorized utilities



<table>
  <thead>
    <tr>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Example</th>
      <th style="text-align:left">Usage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">poll &lt;question&gt;</td>
      <td style="text-align:left">!poll should I sleep?</td>
      <td style="text-align:left">Creates a yes/no poll where you vote with reactions</td>
    </tr>
    <tr>
      <td style="text-align:left">quickpoll &lt;question | answers...&gt;</td>
      <td style="text-align:left">!quickpoll best game?| wow | overwatch | only losers play games</td>
      <td
      style="text-align:left">Use pipes <code>|</code> or commas to separate the questions and answers.
        The first arg is the question, all after that are individual answers. You
        can&apos;t mix pipes and commas, pipes are intended for polls where you
        want commas in the question or answer.</td>
    </tr>
    <tr>
      <td style="text-align:left">[d|define] &lt;word&gt;</td>
      <td style="text-align:left">!define well</td>
      <td style="text-align:left">Shows the oxford dictionary&apos;s definition for the word. Note: due
        to the length of some definitions it might be a good idea to restrict this
        command to prevent abuse.</td>
    </tr>
    <tr>
      <td style="text-align:left">wolfram</td>
      <td style="text-align:left">!wa e ^ (pi * i) + 1</td>
      <td style="text-align:left">This is similar to going to wolframalpha and entering the text yourself.
        Doesn&apos;t support complicated answers.</td>
    </tr>
    <tr>
      <td style="text-align:left">[pick|choice|select] &lt;choices&gt;</td>
      <td style="text-align:left">!choose go to sleep, play overwatch</td>
      <td style="text-align:left">Picks one of your specified arguments. Use commas for multiple words.</td>
    </tr>
    <tr>
      <td style="text-align:left">activity [day/week/month/year]</td>
      <td style="text-align:left">!activity week</td>
      <td style="text-align:left">Defaults to month, shows the 25 most active members by postcount for the
        specified timespan (that the bot has seen)</td>
    </tr>
    <tr>
      <td style="text-align:left">youngest</td>
      <td style="text-align:left">!youngest</td>
      <td style="text-align:left">Ranks members by account creation - Requires Manage Messages</td>
    </tr>
    <tr>
      <td style="text-align:left">oldest</td>
      <td style="text-align:left">!oldest</td>
      <td style="text-align:left">Ranks members by account creation - Requires Manage Messages</td>
    </tr>
    <tr>
      <td style="text-align:left">[ud|urbandictionary] &lt;word&gt;</td>
      <td style="text-align:left">!ud cleveland steamer</td>
      <td style="text-align:left">Returns the urbandictionary definition for your word. @everyone proof.
        (looking at you, b1nzy)</td>
    </tr>
    <tr>
      <td style="text-align:left">[i|info] [@member]</td>
      <td style="text-align:left">!i @Carl#0080</td>
      <td style="text-align:left">Returns Name, last 5 nicknames, id, postcount (that the bot has seen),
        creation date, server join date and some cool information related to these</td>
    </tr>
    <tr>
      <td style="text-align:left">[weather|temp] [location]</td>
      <td style="text-align:left">!weather stockholm</td>
      <td style="text-align:left">If no city is specified, it will give you info for your set home. If used
        for the first time, that city will be set as your home. Since countries
        don&apos;t have weather (think about it) you have to be more specific.</td>
    </tr>
    <tr>
      <td style="text-align:left">temp home &lt;location&gt;</td>
      <td style="text-align:left">!temp home tampa</td>
      <td style="text-align:left">Lets you set a city as your home for !temp to default to.</td>
    </tr>
    <tr>
      <td style="text-align:left">[nicks|nicknames] [@user]</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">Shows you your nicknames history, duplicates are moved to the end of the
        list. The names are ordered from oldest to newest.</td>
    </tr>
    <tr>
      <td style="text-align:left">setnick &lt;member&gt; &lt;name&gt;</td>
      <td style="text-align:left">!setnick @Carl#0080 Do not ping</td>
      <td style="text-align:left">Changes the user&apos;s nickname.</td>
    </tr>
    <tr>
      <td style="text-align:left">dice [sides] [rolls]</td>
      <td style="text-align:left">!dice 6</td>
      <td style="text-align:left">Rolls a [sides] sided die [rolls] times. Defaults to 6 sides and 1 roll.</td>
    </tr>
    <tr>
      <td style="text-align:left">roll [lower-[upper]]</td>
      <td style="text-align:left">!roll 100-1100</td>
      <td style="text-align:left">Works just like in wow, defaults to 1 to 100. Changing just one number
        will change the upper bound.</td>
    </tr>
    <tr>
      <td style="text-align:left">[flip|coin]</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">Flips a coin</td>
    </tr>
    <tr>
      <td style="text-align:left">avatar &lt;member/ID&gt;</td>
      <td style="text-align:left">!avatar</td>
      <td style="text-align:left">Shows the avatar of a mentioned user or yourself if you don&apos;t. Works
        even if the user doesn&apos;t share a server with the bot. Also works in
        dms, you creeps.</td>
    </tr>
    <tr>
      <td style="text-align:left">serverinfo</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">Displays server information.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p><b>spacemychannel</b>
        </p>
        <p><b>&lt;channel&gt;</b>
        </p>
      </td>
      <td style="text-align:left">!spacemychannel #test-channel</td>
      <td style="text-align:left">Removes the - and _ in channel names replacing with a space.</td>
    </tr>
  </tbody>
</table>

