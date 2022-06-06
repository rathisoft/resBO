# Multilanguage QnA Bot

This Bot was created using the [Bot Framework v4](https://dev.botframework.com), an AI based cognitive service, to implement simple Question and Answer conversational patterns, and can answer questions in more than 60 languages. The Bot uses the [QnA Maker](https://www.qnamaker.ai) as well as the [Text Translator API](https://azure.microsoft.com/en-us/services/cognitive-services/translator-text-api/).
The [QnA Maker Service](https://www.qnamaker.ai) enables you to build, train and publish a simple question and answer bot based on FAQ URLs, structured documents or editorial content in minutes. In this sample, I demonstrate how to use the QnA Maker service in combination with the Text Translator to answer questions asked in more than 60 languages.

## Prerequisites

The solution was written in [.NET Core SDK](https://dotnet.microsoft.com/download) version 2.1.
You can check your installed version the following way:

```bash
# determine dotnet version
dotnet --version
```
## Run the Multilanguage QnA Bot

### Clone the repository

```bash
git clone https://github.com/marvinbuss/MultilanguageQnABot.git
```

- If you downloaded the repository as zip-File, then please unzip the archive.
- In a terminal, navigate to the project folder.

### Update `appsettings.json`

Your Bot has to connect to the deployed services to function properly. Therefore you have to update the `appsettings.json`.

- `MicrosoftAppId`: For local testing not required.
- `MicrosoftAppPassword`: For local testing not required.
- `QnAKnowledgebaseId`: Base ID of your published Knowledge Base
- `QnAAuthKey`: Authentication Key of your published Knowledge Base
- `QnAEndpointHostName`: Endpoint of your QnA service
- `QnAThreshold`: Threshold/Accuracy of accepted answers (e.g. 0.6 or 0.7)
- `TranslatorTextSubscriptionKey`: Subscription Key of your Text Translator API
- `TranslatorTextEndpoint`: Endpoint of your Text Translator service (e.g. https://api.cognitive.microsofttranslator.com/translate?api-version=3.0)
- `TranslatorTextRoute`: Should not be changed

### Run the Bot
- Run the bot from a terminal or from Visual Studio, choose option A or B.

#### A) From a terminal

```bash
# run the bot
dotnet run
```

#### B) From Visual Studio

- Launch Visual Studio
- File -> Open -> Project/Solution
- Navigate to the project folder.
- Select `MultilanguageQnABot.csproj` file
- Press `F5` to run the project

## Testing the Multilanguage QnA Bot using Bot Framework Emulator

[Bot Framework Emulator](https://github.com/microsoft/botframework-emulator) is a desktop application that allows bot developers to test and debug their bots on localhost or running remotely through a tunnel.
Follow [this](https://github.com/Microsoft/BotFramework-Emulator/releases) link to install the Bot Framework Emulator version 4.3.0 or greater.

### Connect to the bot using Bot Framework Emulator

- Launch Bot Framework Emulator
- File -> Open Bot
- Enter a Bot URL of `http://localhost:3978/api/messages`
