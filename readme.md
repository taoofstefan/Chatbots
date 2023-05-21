# About the Chatbot
This chatbot is based on the Microsoft Bot Framework SDK. I mainly build it using the Bot Framework Composer. The bot is _intelligent_, meaning it's using NLP (here specificially the Microsoft Languag Understanding Cognitive Services).

This means you need a LUIS account to traing and use the specific NLP phrases used within the bot.

The bot is a hotel assisstant. You can ask specific questions about the fictious hotel located in London, UK. Questions like is ther parking? Are pets allowed? I tried to add whatever meaningful and potential question could be raised by a customer. The main part of the chatbot is the possibility to book a room in this ficticious hotel. Once you are part of the room booking logic, you will be guided through all the important questions (Name, booking address, arrival date, which room, and extras like breakfast or pickup service).
Lastly, there will be a booking overview provided, with all the relevant details.

This bot isn't linked to any database, hence none of the information is stored anywhere as far as I am aware.

This was my first bot. It works well, but it is  far from being perfect. I added some logical tests (like you have to leave later than you arrive), but there might be problems.
Feel free to raise any problems.

## Installation Guide
To test the bot either via the integrated Web Chat or the emulator the following SDKs and programs need to be installed:

• Bot Framework Composer (required): https://docs.microsoft.com/en-us/composer/install-composer?tabs=windows

• .NET Core 3.1 SDK (required): https://dotnet.microsoft.com/en-us/download/dotnet/3.1

• Bot Framework Emulator (optional): https://github.com/microsoft/BotFramework-Emulator


## Starting The Chatbot
Once all the programs are installed, the chatbot can be loaded. To load the files please locate the BigBen.sln
The bot has been loaded.

## Link LUIS
Now we need to link it to the trained LUIS application.
Please click on “Configure” -> “Development resources” and enter the following parameters:

• Bot Name

• Your LUIS Authoring KEY


# Troubleshooting
In case the LUIS key is missing, and the bot is loaded, the following errors will appear in the Bot Framework Console:
*:luisKey Missing LUIS key*

Once the LUIS key has been entered, the error messages will disappear.

The Bot Framework Composer on some occasions takes longer until all the builds are loaded. This throws a LUIS error while starting the bot:
*Sorry, something went wrong with publishing. Try again or exit out of this task.*
*Luis build failed: Cannot read property 'error' of undefinded*

This will be resolved by simply re-starting the bot again. It might take up to 5 times until the LUIS build was successful (based on personal experience). So far there was no reliable way to either fix the problem or consistently reproduce it.
