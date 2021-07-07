# Task 2
 
 In this task, you will be creating a Discord bot which responds to commands.
 You should use the project set up in the last task. 
 Commit and push your code after each task is done.
 
 ## 2.1 Create test server and bot
 
 ### 2.1.1 Create test server
 Create a test Discord server for all your testing.
 Assign the a Hasbulla image to the server icon.
 
 ### 2.1.2 Create a bot
 [Create a bot using the Discord Developer panel](https://www.writebots.com/discord-bot-token/). 
 Assign it all "Text Permissions" and keep the token safe for the next step.
 
 ## 3.1 Setup
 
 ### 3.1.1 Import the library using Maven
 In order to setup a Discord bot, [import the JDA library via Maven](https://github.com/DV8FromTheWorld/JDA#download).
 
 ## 4.1 Basics
 For the next tasks you will need to use the JDA documentation. It contains various examples you must adapt in your own code. You should create a Main class with a main method.
 
 ### 4.1.1 Token from program arguments
 In order to create a bot using JDA you need to pass the token generated earlier as the first parameter. 
 However, you should not store the token within your code. Can you think why?
 
 Instead, we need to use program arguments. [Set the program argument in IntelliJ](https://www.youtube.com/watch?v=kAAbdoq1to8) to contain your token.
 
 ### 4.1.2 Connection
 Configure the bot so that when you start up your application your bot shows up as "Online" in your test server.
 
 ### 4.1.3 Status
 Configure the bot so that the status of the bot shows up as "Hanz Dirtyson!"
 
 ### 4.1.4 Commands
 
 #### 4.1.4.1 Hanz command
 Make the bot respond when a user sends a "!hanz" command. 
 The bot should respond with "Kanch".
 
 #### 4.1.4.1 Time command 
 Make the bot respond when a user sends a "!time command. 
 The bot should respond with the current time.
 
 ### 4.1.5 Private mesage
 Make the bot respond when a user sends a private message.
 The bot should respond with "Hello *username here*, you sent me *message content here*".
