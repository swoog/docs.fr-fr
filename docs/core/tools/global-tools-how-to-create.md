---
title: Créer un Outil global .NET Core
description: Décrit comment créer un Outil global. Un Outil global est une application console qui est installée via la CLI .NET Core.
author: Thraka
ms.author: adegeo
ms.date: 08/22/2018
ms.openlocfilehash: e544ab51920015e0f1ea48ad83ba9b637d98aa0c
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53144577"
---
# <a name="create-a-net-core-global-tool-using-the-net-core-cli"></a><span data-ttu-id="36144-104">Créer un Outil global .NET Core avec la CLI .NET Core</span><span class="sxs-lookup"><span data-stu-id="36144-104">Create a .NET Core Global Tool using the .NET Core CLI</span></span>

<span data-ttu-id="36144-105">Cet article vous explique comment créer et empaqueter un Outil global .NET Core.</span><span class="sxs-lookup"><span data-stu-id="36144-105">This article teaches you how to create and package a .NET Core Global Tool.</span></span> <span data-ttu-id="36144-106">La CLI .NET Core vous permet de créer une application console comme un Outil global, que d’autres utilisateurs peuvent facilement installer et exécuter.</span><span class="sxs-lookup"><span data-stu-id="36144-106">The .NET Core CLI allows you to create a console application as a Global Tool, which others can easily install and run.</span></span> <span data-ttu-id="36144-107">Les Outils globaux .NET Core sont des packages NuGet qui sont installés à partir de la CLI .NET Core.</span><span class="sxs-lookup"><span data-stu-id="36144-107">.NET Core Global Tools are NuGet packages that are installed from the .NET Core CLI.</span></span> <span data-ttu-id="36144-108">Pour plus d’informations sur les Outils globaux, consultez [Vue d’ensemble des outils globaux .NET Core][global-tool-info].</span><span class="sxs-lookup"><span data-stu-id="36144-108">For more information about Global Tools, see [.NET Core Global Tools overview][global-tool-info].</span></span>

[!INCLUDE [topic-appliesto-net-core-21plus.md](../../../includes/topic-appliesto-net-core-21plus.md)]

## <a name="create-a-project"></a><span data-ttu-id="36144-109">Créer un projet</span><span class="sxs-lookup"><span data-stu-id="36144-109">Create a project</span></span>

<span data-ttu-id="36144-110">Cet article utilise la CLI .NET Core pour créer et gérer un projet.</span><span class="sxs-lookup"><span data-stu-id="36144-110">This article uses the .NET Core CLI to create and manage a project.</span></span>

<span data-ttu-id="36144-111">Notre exemple d’outil est une application console qui génère un bot ASCII et imprime un message.</span><span class="sxs-lookup"><span data-stu-id="36144-111">Our example tool will be a console application that generates an ASCII bot and prints a message.</span></span> <span data-ttu-id="36144-112">Pour commencer, créez une application console .NET Core.</span><span class="sxs-lookup"><span data-stu-id="36144-112">First, create a new .NET Core Console Application.</span></span>

```console
dotnet new console -o botsay
```

<span data-ttu-id="36144-113">Accédez au répertoire `botsay` créé par la commande précédente.</span><span class="sxs-lookup"><span data-stu-id="36144-113">Navigate to the `botsay` directory created by the previous command.</span></span>

## <a name="add-the-code"></a><span data-ttu-id="36144-114">Ajoutez le code</span><span class="sxs-lookup"><span data-stu-id="36144-114">Add the code</span></span>

<span data-ttu-id="36144-115">Ouvrez le fichier `Program.cs` avec votre éditeur de texte préféré, tel que `vim` ou [Visual Studio Code](https://code.visualstudio.com/).</span><span class="sxs-lookup"><span data-stu-id="36144-115">Open the `Program.cs` file with your favorite text editor, such as `vim` or [Visual Studio Code](https://code.visualstudio.com/).</span></span>

<span data-ttu-id="36144-116">Ajoutez la directive `using` suivante au début du fichier. Cela permet de raccourcir le code pour afficher les informations de version de l’application.</span><span class="sxs-lookup"><span data-stu-id="36144-116">Add the following `using` directive to the top of the file, this helps shorten the code to display the version information of the application.</span></span>

```csharp
using System.Reflection;
```

<span data-ttu-id="36144-117">Ensuite, passez à la méthode `Main`.</span><span class="sxs-lookup"><span data-stu-id="36144-117">Next, move down to the `Main` method.</span></span> <span data-ttu-id="36144-118">Remplacez la méthode par le code suivant afin de traiter les arguments de ligne de commande pour votre application.</span><span class="sxs-lookup"><span data-stu-id="36144-118">Replace the method with the following code to process the command-line arguments for your application.</span></span> <span data-ttu-id="36144-119">Si aucun argument n’a été passé, un court message d’aide s’affiche.</span><span class="sxs-lookup"><span data-stu-id="36144-119">If no arguments were passed, a short help message is displayed.</span></span> <span data-ttu-id="36144-120">Dans le cas contraire, tous ces arguments sont transformés en une chaîne et imprimés avec le robot.</span><span class="sxs-lookup"><span data-stu-id="36144-120">Otherwise, all of those arguments are transformed into a string and printed with the bot.</span></span>

```csharp
static void Main(string[] args)
{
    if (args.Length == 0)
    {
        var versionString = Assembly.GetEntryAssembly()
                                .GetCustomAttribute<AssemblyInformationalVersionAttribute>()
                                .InformationalVersion
                                .ToString();
                                
        Console.WriteLine($"botsay v{versionString}");
        Console.WriteLine("-------------");
        Console.WriteLine("\nUsage:");
        Console.WriteLine("  botsay <message>");
        return;
    }

    ShowBot(string.Join(' ', args));
}
```

### <a name="create-the-bot"></a><span data-ttu-id="36144-121">Créer le bot</span><span class="sxs-lookup"><span data-stu-id="36144-121">Create the bot</span></span>

<span data-ttu-id="36144-122">Ensuite, ajoutez une nouvelle méthode nommée `ShowBot` qui accepte un paramètre de chaîne.</span><span class="sxs-lookup"><span data-stu-id="36144-122">Next, add a new method named `ShowBot` that takes a string parameter.</span></span> <span data-ttu-id="36144-123">Cette méthode imprime le message et le bot ASCII.</span><span class="sxs-lookup"><span data-stu-id="36144-123">This method prints out the message and the ASCII bot.</span></span> <span data-ttu-id="36144-124">Le code de bot ASCII a été pris dans l’exemple [dotnetbot](https://github.com/dotnet/core/blob/master/samples/dotnetsay/Program.cs).</span><span class="sxs-lookup"><span data-stu-id="36144-124">The ASCII bot code was taken from the [dotnetbot](https://github.com/dotnet/core/blob/master/samples/dotnetsay/Program.cs) sample.</span></span>

```csharp
static void ShowBot(string message)
{
    string bot = $"\n        {message}";
    bot += @"
    __________________
                      \
                       \
                          ....
                          ....'
                           ....
                        ..........
                    .............'..'..
                 ................'..'.....
               .......'..........'..'..'....
              ........'..........'..'..'.....
             .'....'..'..........'..'.......'.
             .'..................'...   ......
             .  ......'.........         .....
             .    _            __        ......
            ..    #            ##        ......
           ....       .                 .......
           ......  .......          ............
            ................  ......................
            ........................'................
           ......................'..'......    .......
        .........................'..'.....       .......
     ........    ..'.............'..'....      ..........
   ..'..'...      ...............'.......      ..........
  ...'......     ...... ..........  ......         .......
 ...........   .......              ........        ......
.......        '...'.'.              '.'.'.'         ....
.......       .....'..               ..'.....
   ..       ..........               ..'........
          ............               ..............
         .............               '..............
        ...........'..              .'.'............
       ...............              .'.'.............
      .............'..               ..'..'...........
      ...............                 .'..............
       .........                        ..............
        .....
";
    Console.WriteLine(bot);
}
```

### <a name="test-the-tool"></a><span data-ttu-id="36144-125">Tester l’outil</span><span class="sxs-lookup"><span data-stu-id="36144-125">Test the tool</span></span>

<span data-ttu-id="36144-126">Exécutez le projet et observez le résultat.</span><span class="sxs-lookup"><span data-stu-id="36144-126">Run the project and see the output.</span></span> <span data-ttu-id="36144-127">Essayez ces variations de la ligne de commande pour obtenir des résultats différents :</span><span class="sxs-lookup"><span data-stu-id="36144-127">Try these variations of the command-line to see different results:</span></span>

```csharp
dotnet run
dotnet run -- "Hello from the bot"
dotnet run -- hello from the bot
```

<span data-ttu-id="36144-128">Tous les arguments après le délimiteur `--` sont passés à votre application.</span><span class="sxs-lookup"><span data-stu-id="36144-128">All arguments after the `--` delimiter are passed to your application.</span></span>

## <a name="setup-the-global-tool"></a><span data-ttu-id="36144-129">Configurer l’outil global</span><span class="sxs-lookup"><span data-stu-id="36144-129">Setup the global tool</span></span>

<span data-ttu-id="36144-130">Avant de pouvoir compresser et distribuer l’application en tant qu’outil global, vous devez modifier le fichier projet.</span><span class="sxs-lookup"><span data-stu-id="36144-130">Before you can pack and distribute the application as a Global Tool, you need to modify the project file.</span></span> <span data-ttu-id="36144-131">Ouvrez le fichier `botsay.csproj`, puis ajoutez trois nouveaux nœuds XML au nœud `<Project><PropertyGroup>` :</span><span class="sxs-lookup"><span data-stu-id="36144-131">Open the `botsay.csproj` file and add three new XML nodes to the `<Project><PropertyGroup>` node:</span></span>

- `<PackAsTool>`  
<span data-ttu-id="36144-132">[OBLIGATOIRE] Indique que l’application est empaquetée pour une installation en tant qu’outil global.</span><span class="sxs-lookup"><span data-stu-id="36144-132">[REQUIRED] Indicates that the application will be packaged for install as a Global Tool.</span></span>

- `<ToolCommandName>`  
<span data-ttu-id="36144-133">[FACULTATIF] Autre nom de l’outil, sinon le nom de commande de l’outil sera nommé après le fichier projet.</span><span class="sxs-lookup"><span data-stu-id="36144-133">[OPTIONAL] An alternative name for the tool, otherwise the command name for the tool will be named after the project file.</span></span> <span data-ttu-id="36144-134">Vous pouvez avoir plusieurs outils dans un package et choisir un nom unique et convivial vous aide à différencier les outils dans un même package.</span><span class="sxs-lookup"><span data-stu-id="36144-134">You can have multiple tools in a package, choosing a unique and friendly name helps differentiate from other tools in the same package.</span></span>

- `<PackageOutputPath>`  
<span data-ttu-id="36144-135">[FACULTATIF] Emplacement où le package NuGet sera produit.</span><span class="sxs-lookup"><span data-stu-id="36144-135">[OPTIONAL] Where the NuGet package will be produced.</span></span> <span data-ttu-id="36144-136">Le package NuGet est utilisé par les Outils globaux CLI .NET Core pour installer votre outil.</span><span class="sxs-lookup"><span data-stu-id="36144-136">The NuGet package is what the .NET Core CLI Global Tools uses to install your tool.</span></span>

```xml
<Project Sdk="Microsoft.NET.Sdk">

  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp2.1</TargetFramework>

    <PackAsTool>true</PackAsTool>
    <ToolCommandName>botsay</ToolCommandName>
    <PackageOutputPath>./nupkg</PackageOutputPath>

  </PropertyGroup>

</Project>
```

<span data-ttu-id="36144-137">Bien que `<PackageOutputPath>` soit facultatif, utilisez-le dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="36144-137">Even though `<PackageOutputPath>` is optional, use it in this example.</span></span> <span data-ttu-id="36144-138">Veillez à le définir sur : `<PackageOutputPath>./nupkg</PackageOutputPath>`.</span><span class="sxs-lookup"><span data-stu-id="36144-138">Make sure you set it: `<PackageOutputPath>./nupkg</PackageOutputPath>`.</span></span>

<span data-ttu-id="36144-139">Ensuite, créez un package NuGet pour votre application.</span><span class="sxs-lookup"><span data-stu-id="36144-139">Next, create a NuGet package for your application.</span></span>

```console
dotnet pack
```

<span data-ttu-id="36144-140">Le fichier `botsay.1.0.0.nupkg` est créé dans le dossier identifié par la valeur XML `<PackageOutputPath>` à partir du fichier `botsay.csproj`, qui dans cet exemple est le dossier `./nupkg`.</span><span class="sxs-lookup"><span data-stu-id="36144-140">The `botsay.1.0.0.nupkg` file is created in the folder identified by the `<PackageOutputPath>` XML value from the `botsay.csproj` file, which in this example is the `./nupkg` folder.</span></span> <span data-ttu-id="36144-141">Cela facilite l’installation et le test.</span><span class="sxs-lookup"><span data-stu-id="36144-141">This makes it easy to install and test.</span></span> <span data-ttu-id="36144-142">Lorsque vous souhaitez distribuer un outil publiquement, chargez-le dans [https://www.nuget.org](https://www.nuget.org). Une fois l’outil disponible sur NuGet, les développeurs peuvent l’installer à l’échelle de l’utilisateur en utilisant l’option `--global` de la commande [dotnet tool install](dotnet-tool-install.md).</span><span class="sxs-lookup"><span data-stu-id="36144-142">When you want to release a tool publicly, upload it to [https://www.nuget.org](https://www.nuget.org). Once the tool is available on NuGet, developers can perform a user-wide installation of the tool using the `--global` option of the [dotnet tool install](dotnet-tool-install.md) command.</span></span>

<span data-ttu-id="36144-143">Maintenant que vous avez un package, installez l’outil à partir de ce package :</span><span class="sxs-lookup"><span data-stu-id="36144-143">Now that you have a package, install the tool from that package:</span></span> 

```console
dotnet tool install --global --add-source ./nupkg botsay
```

<span data-ttu-id="36144-144">Le paramètre `--add-source` indique à la CLI .NET Core d’utiliser temporairement le dossier `./nupkg` (notre dossier `<PackageOutputPath>`) comme source supplémentaire de flux pour les packages NuGet.</span><span class="sxs-lookup"><span data-stu-id="36144-144">The `--add-source` parameter tells the .NET Core CLI to temporarily use the `./nupkg` folder (our `<PackageOutputPath>` folder) as an additional source feed for NuGet packages.</span></span> <span data-ttu-id="36144-145">Pour plus d’informations sur l’installation des Outils globaux, consultez [Vue d’ensemble des outils globaux .NET Core][global-tool-info].</span><span class="sxs-lookup"><span data-stu-id="36144-145">For more information about installing Global Tools, see [.NET Core Global Tools overview][global-tool-info].</span></span>

<span data-ttu-id="36144-146">Si l’installation réussit, un message s’affiche indiquant la commande utilisée pour appeler l’outil et la version installée, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="36144-146">If installation is successful, a message is displayed showing the command used to call the tool and the version installed, similar to the following example:</span></span>

```
You can invoke the tool using the following command: botsay
Tool 'botsay' (version '1.0.0') was successfully installed.
```

<span data-ttu-id="36144-147">Vous devez maintenant pouvoir taper `botsay` et obtenir une réponse à partir de l’outil.</span><span class="sxs-lookup"><span data-stu-id="36144-147">You should now be able to type `botsay` and get a response from the tool.</span></span>

> [!NOTE]
> <span data-ttu-id="36144-148">Si l’installation a réussi, mais que vous ne pouvez pas utiliser la commande `botsay`, vous devrez peut-être ouvrir un nouveau terminal pour actualiser le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="36144-148">If the install was successful, but you cannot use the `botsay` command, you may need to open a new terminal to refresh the PATH.</span></span>

## <a name="remove-the-tool"></a><span data-ttu-id="36144-149">Supprimer l’outil</span><span class="sxs-lookup"><span data-stu-id="36144-149">Remove the tool</span></span>

<span data-ttu-id="36144-150">Une fois que vous avez fini de tester l’outil, vous pouvez le supprimer avec la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="36144-150">Once you're done experimenting with the tool, you can remove it with the following commnand:</span></span>

```console
dotnet tool uninstall -g botsay
```

[global-tool-info]: global-tools.md
