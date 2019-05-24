# DBeeKeeper.net

The official DBeeKeeper library, supporting .NET Standard 1.2+, .NET Core 1.0+, and .NET Framework 4.5+

This API allows consumers to interact with DBeeKeeper without using the website - for automated agent deployment/configuration, consuming/responding to webhooks, retrieving database backups or querying object status.

## Documentation

See the [.NET API docs](https://www.dbeekeeper.com/wiki).

## Installation

### Install DBeeKeeper.net via NuGet

From the command line:

	nuget install DBeeKeeper.net

From Package Manager:

	PM> Install-Package DBeeKeeper.net

From within Visual Studio:

1. Open the Solution Explorer.
2. Right-click on a project within your solution.
3. Click on *Manage NuGet Packages...*
4. Click on the *Browse* tab and search for "DBeeKeeper.net".
5. Click on the DBeeKeeper.net package, select the appropriate version in the right-tab and click *Install*.

### Set the API Key for your project

You can configure the DBeeKeeper.net package to use your secret API key in one of two ways:

a) In your application initialization, set your API key (only once once during startup):

```csharp
DBeeKeeperConfiguration.SetApiKey("[your api key here]");
```

b) Pass the API key to [RequestOptions](#requestoptions):

```csharp
var agentService = new AgentService();
agentService.Get(*agentId*, new RequestOptions { ApiKey = "[your api key here]" });
```
