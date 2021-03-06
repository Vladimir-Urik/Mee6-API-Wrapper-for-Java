[download]: https://github.com/Miic/Mee6-API-Wrapper-for-Java/releases/latest

# MEE6 API Wrapper for Java

Java 8 API Wrapper for the MEE6 Discord Bot

## What is it?
MEE6 is a Discord bot that lets you easily add your own commands to your server
through a user-friendly dashboard, but it is a little known fact is that MEE6 has an API which other applications can call information from.

While building a bot with JDA around Mee6 player statistics, I found that there was no public wrappers for Mee6, so I built one. I thought I would share this with the community in case someone else needed it.



![Jason](https://i.gyazo.com/53d14bf4550f2efd4f835f3bd4563292.png)

**Using Mee6API Object**:
```java
public class Example
{
    public static void main(String[] args)
    {
    	//Step 1: Build a corresponding JDA with the Guild's ID
        Mee6API mee = new Mee6API("222123744959660032");
        
        //Grab a player by ID (will output null if player does not exist in this leaderboard)
        Players player = mee.getPlayer("157692073699573761");
        
        //An example of displaying this data
        System.out.println(player.getUsername() + " : " + player.getLevel());
    }
}
```

**Output**
```
Micc : 21
//Note: the level may change by the time you attempt to use this
```


## Frequently Asked Questions and Issues

**How do I find a Guild ID / Player ID?**
```
Step 1: Enable developer mode on your Discord Client. 
You can find this option in User Settings >  Apperance > Advanced > Developer Mode.

Step 2: Right click any Guild or Player and click Copy ID

Step 3: Profit
```

**I'm making modifications to the data in my program but the changes aren't being reflected on the server. Help?**

```
All returned objects are immutable. This API only allows for querying and not for sending data back to Mee6.
```


## Download
Latest Stable Version: [GitHub Release](https://github.com/Miic/Mee6-API-Wrapper-for-Java/releases/latest)

Latest Version: [download]

**Maven**
```xml
<dependency>
    <groupId>com.github.Miic</groupId>
    <artifactId>Mee6-API-Wrapper-for-Java</artifactId>
    <version>LATEST</version>
</dependency>
```
```xml
<repository>
    <id>jitpack.io</id>
    <url>https://jitpack.io</url>
</repository>

```
