# HangoutBot Official Documentation
### User Join/Leave Messages
HangoutBot has the ability to send a message into a predesignated channel when a user joins or leaves a server. 
This particular channel is chosen using the `mb/set` command, and only people with administrative control over the bot
can change this particular channel.

To help make welcome/leave messages more personal, we've allowed for a number of variables which can be used in Welcome Leave Messages.
When a user is configuring these messages, they must just surround the name of the variable with 
curly brackets (eg `{mention_user}`) and the text will be replaced with the appropriate value at runtime.

### **Variables**
The following can all be used as variables, and will each have their respective values beside them.

#### Mention

``{mention_user}`` will mention the user who is joining or leaving the server.
* *Note: On occasion, and especially on lower memory devices - this might not work correctly, and the user will just see `@<284930823095835320984>` instead of the user's handle. This happens if the users device has not yet cached the user who is joining/leaving.*

Use Case:
```
    Welcome, @thatmaxplayle to our server.
```
The person who is leaving/joining **will** receive a ping (red notification against the channel) in the channel in which they are welcomed by the bot. Please note that individuals who are leaving the server will __not__ receive a notification because they will have left the server by the time the message has been sent.

#### Username

``{username}`` will be replaced with the username (but not the discriminator) of the person who is joining or leaving the server.
* *Note: Unlike the previous example, this will work 100% of the time, because the bot will always have cached the target user, and therefore will have the username of said user to display in a plain text message.*

Use Case:
```
    Welcome, thatmaxplayle to our server.
```
The person who is leaving/joining will *not* receive a ping (red notification against the channel) in the channel in which they are welcomed by the bot. Please note that individuals who are leaving the server will __not__ receive a notification because they will have left the server by the time the message has been sent.

#### Username with Discriminator 

``{username_with_discim}`` will be replaced with the username and the discriminator of the person who is joining or leaving the server.
* *The same note applies as the previous entry.*

Use Case:
```
    Welcome, thatmaxplayle#8811 to our server.
```
The person who is leaving/joining will *not* receive a ping (red notification against the channel) in the channel in which they are welcomed by the bot. Please note that individuals who are leaving the server will __not__ receive a notification because they will have left the server by the time the message has been sent.


#### Guild Name

``{guild_name}`` will be replaced with the name of the guild the user is joining or leaving.

Use Case:
```
    Welcome, thatmaxplayle#8811 to Max's Hangout.
```

#### Member Count

``{member_count}`` will be replaced with the total amount of users in the Discord Server.

Use Case:
```
    Welcome, @thatmaxplayle to Max's Hangout. You are member 400!
```

#### Member Count (excluding bots)

``{member_count!bots}`` will be replaced with the total amount of users in the Discord Server, exlcuding bots.

Use Case:
```
    Welcome, @thatmaxplayle to Max's Hangout. There are now 395 humans in the server!
```
