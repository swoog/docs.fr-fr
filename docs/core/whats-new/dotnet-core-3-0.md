---
title: Nouveautés de .NET Core 3.0
description: Découvrez les nouvelles fonctionnalités de .NET Core 3.0.
dev_langs:
- csharp
- vb
author: thraka
ms.author: adegeo
ms.date: 12/04/2018
ms.openlocfilehash: 3ca833031eb8bb0f43a334f833f2e0075842d57d
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53156667"
---
# <a name="whats-new-in-net-core-30-preview-1"></a>Nouveautés de .NET Core 3.0 (préversion 1)

Cet article décrit les nouveautés de .NET Core 3.0 (préversion 1). Une des principales améliorations est la prise en charge des applications de bureau Windows (Windows uniquement). En utilisant un composant .NET Core 3.0 appelé Bureau Windows, vous pouvez porter vos applications Windows Forms Windows Presentation Foundation (WPF). Pour être clair, le composant Bureau Windows est uniquement pris en charge sous Windows. Pour plus d'informations, consultez la section [Bureau Windows](#windows-desktop) ci-dessous.

.NET Core 3.0 prend en charge C# 8.0.

[Téléchargez et commencez à utiliser .NET Core 3 Préversion 1](https://aka.ms/netcore3download) dès maintenant sous Windows, Mac et Linux. Vous pouvez consulter les détails complets de la version dans les [notes de publication de .NET Core 3 Préversion 1](https://aka.ms/netcore3releasenotes).

Pour plus d’informations, consultez l’[annonce de .NET Core 3.0 Préversion 1](https://blogs.msdn.microsoft.com/dotnet/2018/12/04/announcing-net-core-3-preview-1-and-open-sourcing-windows-desktop-frameworks/).

## <a name="net-standard-21"></a>.NET Standard 2.1

.NET Core 3.0 implémente également .NET Standard 2.1.

## <a name="default-executables"></a>Exécutables par défaut

.NET Core permet désormais de générer des exécutables par défaut. Il s’agit d’une nouvelle fonctionnalité pour les applications qui utilisent une version .NET Core installée de façon globale. Jusqu'à présent, seuls les [déploiements autonomes](../deploying/index.md#self-contained-deployments-scd) avaient des exécutables.

Lors de l’étape `dotnet build` ou `dotnet publish`, un exécutable est créé s’il correspond à l’environnement et à la plateforme du Kit de développement que vous utilisez. Vous pouvez obtenir le même résultat avec ces exécutables, comme vous le feriez avec d’autres exécutables natifs comme :

* Vous pouvez double-cliquer sur l’exécutable.
* Vous pouvez lancer l’application directement à partir d’une invite de commandes, par exemple `myapp.exe` sous Windows, et `./myapp` sous Linux et macOS.

> [!NOTE]
> La spécification d’un runtime avec des arguments `dotnet publish -r` ou `dotnet build -r` pour d’autres environnements de runtime n’est pas prise en charge.

## <a name="build-copies-dependencies"></a>Dépendances de copies de build

`dotnet build` copie maintenant les dépendances NuGet pour votre application à partir du cache NuGet vers le dossier de sortie de build. Auparavant, les dépendances étaient copiées uniquement dans le cadre de `dotnet publish`. 

Certaines opérations, par exemple la liaison et la publication d’une page de type Razor, nécessiteront toujours une publication.


## <a name="local-dotnet-tools"></a>Outils dotnet locaux

Alors que .NET Core 2.1 prenant en charge des outils globaux, .NET Core 3.0 dispose maintenant d’outils locaux. Les outils locaux sont similaires aux outils globales mais ils sont associés à un emplacement particulier sur le disque. Cela permet une utilisation par projet et par référentiel. Un outil installé localement n’est pas disponible de façon globale.

Les outils locaux s’appuient sur un nom de fichier manifeste `dotnet-tools.json` dans votre répertoire actuel. Ce fichier manifeste définit les outils qui doivent être disponibles. En créant ce fichier manifeste à la racine de votre référentiel, vous garantissez que toute personne qui clone votre code pourra restaurer et utiliser les outils nécessaires pour fonctionner correctement avec votre code.

Lorsque le fichier manifeste des outils locaux est disponible, utilisez la commande suivante pour automatiquement télécharger et installer localement ces outils :

```console
dotnet tool restore
```

Exécutez l’outil local avec la commande suivante :

```console
dotnet tool run <tool-command-name>
```

Lorsqu’un outil local est appelé, dotnet recherche un manifeste dans la structure de répertoire. Si le fichier manifeste d’un outil est trouvé, la commande recherche l’outil demandé. Si elle trouve l’outil, elle inclut les informations nécessaires pour trouver l’outil à l’emplacement des packages globaux NuGet. 

Si l’outil se trouve dans le manifeste mais pas dans le cache, l’utilisateur reçoit une erreur. Le message sera amélioré après la préversion 1 pour demander à l’utilisateur d’exécuter `dotnet tool restore`.

Pour ajouter des outils locaux à un répertoire, vous devez d’abord créer le fichier manifeste de l’outil. Après la préversion 1, nous proposerons un mécanisme pour la création des fichiers manifeste, notamment un nouveau modèle dotnet. Pour la préversion 1, vous devez créer le fichier `dotnet-tools.json` avec le contenu suivant :

```json
{
  "version": 1,
  "isRoot": true,
  "tools": {}
}
```

Une fois le manifeste créé, vous pouvez ajouter des outils locaux à l’aide de la commande :

```console
dotnet tool install <toolPackageId>
```

Cette commande installe la dernière version de l’outil, sauf si une autre version est spécifiée.  Même si la version la plus récente a été automatiquement choisie, la version de l’outil est inscrite dans le fichier manifeste de l’outil pour permettre la restauration ou l’exécution de la version correcte de l’outil.

Le fichier manifeste de l’outil est conçu pour permettre des modifications manuelles et ainsi mettre à jour la version requise pour une utilisation avec le référentiel.

Voici un exemple de fichier `dotnet-tools.json` :

```json
{
  "version": 1,
  "isRoot": true,
  "tools": {
    "dotnetsay": {
      "version": "2.1.4",
      "commands": [
        "dotnetsay"
      ]
    },
    "t-rex": {
      "version": "1.0.103",
      "commands": [
        "t-rex"
      ]
    }
  }
}
```

Pour supprimer un outil du fichier manifeste, exécutez la commande suivante :

```console
dotnet tool uninstall <toolPackageId>
```

Pour les outils locaux et globaux, une version compatible du runtime est requise. De nombreux outils actuellement sur NuGet.org ciblent le runtime .NET Core 2.1. Pour installer ces outils de façon locale ou globale, vous devez toujours installer le [runtime NET Core 2.1](https://dotnet.microsoft.com/download/dotnet-core/2.1).

Pour plus d’informations, consultez [Local Tools Early Preview Documentation](https://github.com/dotnet/cli/issues/10288).

## <a name="windows-desktop"></a>Bureau Windows

À compter de .NET Core 3.0 Préversion 1, vous pouvez créer des applications de bureau Windows à l’aide des outils WPF et Windows Forms. Ces infrastructures prennent également en charge l’utilisation de contrôles modernes et le style Fluent à partir de la bibliothèque XAML de l’interface utilisateur Windows (WinUI) via des [îles XAML](/windows/uwp/xaml-platform/xaml-host-controls).

Le composant Bureau Windows fait partie du SDK .NET Core 3.0 Windows.

Vous pouvez créer une nouvelle application WPF ou Windows Forms à l’aide des commandes `dotnet` suivantes :

```console
dotnet new wpf
dotnet new winforms
```

Vous pouvez également ouvrir, lancer et déboguer des projets .NET Core 3.0 WPF et Windows Forms dans Visual Studio 2019 Préversion 1. Il est actuellement possible d’ouvrir ces projets dans 15.9 de 2017 Visual Studio, mais ce n’est pas un scénario pris en charge (et vous devez [activer les préversions](https://blogs.msdn.microsoft.com/dotnet/2018/11/13/net-core-tooling-update-for-visual-studio-2017-version-15-9/)).

Les nouveaux projets sont identiques aux projets .NET Core existants, avec quelques ajouts. Voici une comparaison entre le projet de console .NET Core de base et un projet Windows Forms et WPF de base.

Dans un projet de console .NET Core, le projet utilise le SDK `Microsoft.NET.Sdk` et déclare une dépendance sur .NET Core 3.0 via l’infrastructure cible `netcoreapp3.0`. Pour créer une application Bureau Windows, utilisez le SDK `Microsoft.NET.Sdk.WindowsDesktop` et choisissez l’infrastructure d’interface utilisateur à utiliser :

```diff
-<Project Sdk="Microsoft.NET.Sdk">
+<Project Sdk="Microsoft.NET.Sdk.WindowsDesktop">
  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp3.0</TargetFramework>
+   <UseWPF>true</UseWPF>
  </PropertyGroup>
</Project>
```

Pour choisir Windows Forms plutôt que WPF, définissez `UseWindowsForms` au lieu de `UseWPF` :

```diff
<Project Sdk="Microsoft.NET.Sdk.WindowsDesktop">
  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp3.0</TargetFramework>
-   <UseWPF>true</UseWPF>
+   <UseWindowsForms>true</UseWindowsForms>
  </PropertyGroup>
</Project>
```

`UseWPF` et `UseWindowsForms` peuvent être définies sur `true` si l’application utilise les deux infrastructures, par exemple lorsqu’une boîte de dialogue Windows Forms héberge un contrôle WPF.

Partagez vos commentaires sur les référentiels [dotnet/winforms](https://github.com/dotnet/winforms/issues), [dotnet/wpf](https://github.com/dotnet/wpf/issues) et [dotnet/core](https://github.com/dotnet/core/issues).

## <a name="fast-built-in-json-support"></a>Prise en charge JSON intégrée rapide

`System.Text.Json.Utf8JsonReader` est un lecteur hautes performances et à faible allocation de type forward-only pour le texte JSON codé au format UTF-8 et lu à partir de `ReadOnlySpan<byte>`. `Utf8JsonReader` est un type fondamental de bas niveau, permettant de générer des analyseurs et des désérialiseurs personnalisés. La lecture d’une charge utile JSON à l’aide du nouveau `Utf8JsonReader` est 2 fois plus rapide qu’avec le lecteur proposé par [Json.NET](https://www.newtonsoft.com/json). Ce lecteur n’alloue aucune ressource tant que vous n’avez pas besoin d’actualiser des jetons JSON sous forme de chaînes (UTF-16).

Cette nouvelle API inclura les composants suivants :

* Préversion 1 : lecteur JSON (accès séquentiel)
* Prochainement : enregistreur JSON, DOM (accès aléatoire), sérialiseur poco, désérialiseur poco

Voici la boucle de lecteur de base pour le `Utf8JsonReader`, utilisable comme point de départ :

```csharp
using System.Text.Json;

public static void Utf8JsonReaderLoop(ReadOnlySpan<byte> dataUtf8)
{
    var json = new Utf8JsonReader(dataUtf8, isFinalBlock: true, state: default);

    while (json.Read())
    {
        JsonTokenType tokenType = json.TokenType;
        ReadOnlySpan<byte> valueSpan = json.ValueSpan;
        switch (tokenType)
        {
            case JsonTokenType.StartObject:
            case JsonTokenType.EndObject:
                break;
            case JsonTokenType.StartArray:
            case JsonTokenType.EndArray:
                break;
            case JsonTokenType.PropertyName:
                break;
            case JsonTokenType.String:
                string valueString = json.GetStringValue();
                break;
            case JsonTokenType.Number:
                if (!json.TryGetInt32Value(out int valueInteger))
                {
                    throw new FormatException();
                }
                break;
            case JsonTokenType.True:
            case JsonTokenType.False:
                bool valueBool = json.GetBooleanValue();
                break;
            case JsonTokenType.Null:
                break;
            default:
                throw new ArgumentException();
        }
    }

    dataUtf8 = dataUtf8.Slice((int)json.BytesConsumed);
    JsonReaderState state = json.CurrentState;
}
```

L’écosystème .NET s’appuyaient sur [Json.NET](https://www.newtonsoft.com/json) et d’autres bibliothèques JSON populaires, qui restent des solutions efficaces. JSON.NET utilise des chaînes .NET comme type de données de base, au format UTF-16. 

Dans .NET Core 2.1 et 3.0, nous avons ajouté de nouvelles API permettant d’écrire des API JSON (notamment `Utf8JsonReader`) qui nécessitent beaucoup moins de mémoire, s’appuient sur l’utilisation de `Span<T>` et de chaînes UTF-8, et répondent mieux aux besoins des applications à débit élevé comme Kestrel ou le serveur web ASP.NET Core.

## <a name="ranges-and-indices"></a>Plages et index

Le nouveau type `Index` peut être utilisé pour l’indexation. Vous pouvez en créer un à partir d’un `int` qui compte à partir du début, ou avec un opérateur (C#) `^` préfixé qui compte à partir de la fin :

```csharp
Index i1 = 3;  // number 3 from beginning
Index i2 = ^4; // number 4 from end
int[] a = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
Console.WriteLine($"{a[i1]}, {a[i2]}"); // "3, 6"
```

Il existe également un type `Range`, composé de deux `Index` valeurs, une pour le début et une pour la fin, et qui peut être écrit avec une expression de plage (C#) `x..y`. Vous pouvez indexer ensuite avec un `Range` afin de produire une tranche :

```csharp
var slice = a[i1..i2]; // { 3, 4, 5 }
```

> [!NOTE]
> Seul [C# 8.0](https://blogs.msdn.microsoft.com/dotnet/2018/11/12/building-c-8-0/) prend en charge la syntaxe pour `Range` et `Index`.

## <a name="async-streams"></a>Flux asynchrones

Le type `IAsyncEnumerable<T>` est une nouvelle version asynchrone de `IEnumerable<T>`. Le langage vous permet d’appliquer une opération `await foreach` sur ces objets pour consommer leurs éléments, et une opération `yield return` pour produire les éléments.

L’exemple suivant montre la production et la consommation de flux de données asynchrones. L’instruction `foreach` est asynchrone et utilise elle-même `yield return` afin de produire un flux asynchrone pour les appelants. Ce modèle (qui utilise `yield return`) est le modèle recommandé pour produire des flux de données asynchrones.

```csharp
async IAsyncEnumerable<int> GetBigResultsAsync()
{
    await foreach (var result in GetResultsAsync())
    {
        if (result > 20) yield return result; 
    }
}
```

> [!WARNING]
> .NET core 3.0 Préversion 1 contient actuellement un bogue au niveau de `await foreach`. Utilisez plutôt `GetEnumerator` et `MoveNext` pour traiter les éléments. Pour plus d'informations, consultez [roslyn/#31268](https://github.com/dotnet/roslyn/issues/31268).

Outre la possibilité d’effectuer une opération `await foreach`, vous pouvez également créer des itérateurs asynchrones, par exemple un itérateur qui retourne un objet `IAsyncEnumerable/IAsyncEnumerator` auquel vous pouvez à la fois appliquer des opérations `await` et `yield`. Pour les objets qui doivent être supprimés, vous pouvez utiliser `IAsyncDisposable`, qui implémentent différents types BCL, notamment `Stream` et `Timer`.

> [!NOTE]
> Seul [C# 8.0](https://blogs.msdn.microsoft.com/dotnet/2018/11/12/building-c-8-0/) prend en charge la syntaxe `await foreach`

## <a name="type-sequencereader"></a>Type : SequenceReader

Dans .NET Core 3.0, `System.Buffers.SequenceReader` a été ajouté et peut servir de lecteur pour `ReadOnlySequence<T>`. Cela permet une analyse facile, hautes performances et à faible allocation des données `System.IO.Pipelines`, capable de couvrir plusieurs mémoires tampon de stockage. 

L’exemple suivant segmente une entrée `Sequence` en plusieurs lignes délimitées `CR/LF` valides :

```csharp
private static ReadOnlySpan<byte> CRLF => new byte[] { (byte)'\r', (byte)'\n' };

public static void ReadLines(ReadOnlySequence<byte> sequence)
{
    SequenceReader<byte> reader = new SequenceReader<byte>(sequence);

    while (!reader.End)
    {
        if (!reader.TryReadToAny(out ReadOnlySpan<byte> line, CRLF, advancePastDelimiter:false))
        {
            // Couldn't find another delimiter
            // ...
        }

        if (!reader.IsNext(CRLF, advancePast: true))
        {
            // Not a good CR/LF pair
            // ...
        }

        // line is valid, process
        ProcessLine(line);
    }
}
```

## <a name="type-metadataloadcontext"></a>Type : MetadataLoadContext

Le type `MetadataLoadContext` a été ajouté et permet la lecture des métadonnées de l'assembly sans affecter le domaine d’application de l’appelant. Les assemblys sont lus comme des données, y compris ceux générés pour des architectures et plateformes différentes de l’environnement d’exécution actuel. `MetadataLoadContext` se superpose à <xref:System.Reflection.Assembly.ReflectionOnlyLoad*>, qui est uniquement disponible dans .NET Framework.

`MetdataLoadContext` est disponible dans le [package System.Reflection.MetadataLoadContext](https://www.nuget.org/packages/System.Reflection.MetadataLoadContext). Il s’agit d’un package .NET Standard 2.0.

`MetadataLoadContext` expose les API semblables au type <xref:System.Runtime.Loader.AssemblyLoadContext>, mais il n’est pas basé sur ce type. Tout comme <xref:System.Runtime.Loader.AssemblyLoadContext>, `MetadataLoadContext` permet le chargement d’assemblys dans un univers de chargement d’assemblys isolé. Les API `MetdataLoadContext` retournent des objets <xref:System.Reflection.Assembly>, permettant l’utilisation des API de réflexion courantes. Les API orientées exécution, par exemple [MethodBase.Invoke](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/src/System/Reflection/TypeLoading/Methods/RoMethod.cs#L127), ne sont pas autorisées et renverront une exception InvalidOperationException.

L’exemple suivant montre comment rechercher des types concrets dans un assembly qui implémente une interface donnée :

```csharp
var paths = new string[] {@"C:\myapp\mscorlib.dll", @"C:\myapp\myapp.dll"};
var resolver = new PathAssemblyResolver(paths);
using (var lc = new MetadataLoadContext(resolver))
{
    Assembly a = lc.LoadFromAssemblyName("myapp");
    Type myInterface = a.GetType("MyApp.IPluginInterface");
    foreach (Type t in a.GetTypes())
    {
        if (t.IsClass && myInterface.IsAssignableFrom(t))
            Console.WriteLine($"Class {t.FullName} implements IPluginInterface");
    }
}
```

Les scénarios pour `MetadataLoadContext` incluent des fonctionnalités et des outils au moment de la conception, ainsi que des fonctionnalités de runtime qui doivent inspecter un ensemble d’assemblys en tant que données et dont l’intégralité des verrous appliqués aux fichiers et à la mémoire doivent être supprimés une l’inspection terminée.

`MetadataLoadContext` contient une classe de résolution passée à son constructeur. La tâche du programme de résolution consiste à charger un `Assembly` en fonction de son `AssemblyName`. La classe de résolution est dérivée de la classe abstraite `MetadataAssemblyResolver`. Une implémentation du programme de résolution pour des scénarios basés sur le chemin d’accès est fournie avec `PathAssemblyResolver`.

Les [tests MetadataLoadContext](https://github.com/dotnet/corefx/tree/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests) illustrent de nombreux cas d’usage. Les [tests Assembly](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests/Assembly/AssemblyTests.cs) constituent un bon point de départ.

## <a name="tls-13--openssl-111-on-linux"></a>TLS 1.3 et OpenSSL 1.1.1 sous Linux

.NET Core tire désormais parti de la [prise en charge de TLS 1.3 dans OpenSSL 1.1.1](https://www.openssl.org/blog/blog/2018/09/11/release111/), si disponible dans un environnement donné. Selon l’[équipe OpenSSL](https://www.openssl.org/blog/blog/2018/09/11/release111/), TLS 1.3 présentent plusieurs avantages :

* Délais de connexion améliorés grâce à une réduction du nombre d’allers-retours requis entre le client et le serveur.

* Sécurité améliorée grâce à la suppression de différents algorithmes de chiffrement obsolètes et non sécurisés et à un chiffrement plus complet de la négociation de connexion.

.NET Core 3.0 Préversion 1 est capable d’utiliser **OpenSSL 1.1.1**, **OpenSSL 1.1.0** ou **OpenSSL 1.0.2** (soit la meilleure version trouvée, sur un système Linux).  Si **OpenSSL 1.1.1** est disponible, les types SslStream et HttpClient utiliseront **TLS 1.3** avec `SslProtocols.None` (protocoles système par défaut), en supposant que le client et le serveur prennent en charge **TLS 1.3**.

L’exemple suivant montre comment .NET Core 3.0 Préversion 1 sous Ubuntu 18.10 se connecte à <https://www.cloudflare.com> :

```csharp
using System;
using System.Net.Security;
using System.Net.Sockets;
using System.Threading.Tasks;

namespace tlstest
{
    class Program
    {
        static async Task Main()
        {
            using (TcpClient tcpClient = new TcpClient())
            {
                string targetHost = "www.cloudflare.com";

                await tcpClient.ConnectAsync(targetHost, 443);

                using (SslStream sslStream = new SslStream(tcpClient.GetStream()))
                {
                    await sslStream.AuthenticateAsClientAsync(targetHost);
                    await Console.Out.WriteLineAsync($"Connected to {targetHost} with {sslStream.SslProtocol}");
                }
            }
        }
    }
}
```

```console
user@comp-ubuntu1810:~/tlstest$ dotnet run
Connected to www.cloudflare.com with Tls13
user@comp-ubuntu1810:~/tlstest$ openssl version
OpenSSL 1.1.1  11 Sep 2018
```

>[!IMPORTANT]
>Windows et macOS ne prennent pas encore en charge **TLS 1.3**. .NET Core 3.0 prendra en charge **TLS 1.3** sur ces systèmes d’exploitation dès que de la prise en charge sera disponible.

## <a name="cryptography"></a>Chiffrement

La prise en charge a été ajoutée pour les chiffrements **AES-GCM** et **AES-CCM**, avec une implémentation via `System.Security.Cryptography.AesGcm` et `System.Security.Cryptography.AesCcm`. Ces algorithmes sont de type [Authenticated Encryption with Association Data (AEAD)](https://en.wikipedia.org/wiki/Authenticated_encryption), et les premiers algorithmes Authenticated Encryption (AE) ont été ajoutés à .NET Core.

Le code suivant montre l’utilisation du chiffrement **AesGcm** pour chiffrer et déchiffrer des données aléatoires.

Le code pour **AesCcm** sera presque identique (seuls les noms des variables de classe seraient différents).

```csharp
// key should be: pre-known, derived, or transported via another channel, such as RSA encryption
byte[] key = new byte[16];
RandomNumberGenerator.Fill(key);

byte[] nonce = new byte[12];
RandomNumberGenerator.Fill(nonce);

// normally this would be your data
byte[] dataToEncrypt = new byte[1234];
byte[] associatedData = new byte[333];
RandomNumberGenerator.Fill(dataToEncrypt);
RandomNumberGenerator.Fill(associatedData);

// these will be filled during the encryption
byte[] tag = new byte[16];
byte[] ciphertext = new byte[dataToEncrypt.Length];

using (AesGcm aesGcm = new AesGcm(key))
{
    aesGcm.Encrypt(nonce, dataToEncrypt, ciphertext, tag, associatedData);
}

// tag, nonce, ciphertext, associatedData should be sent to the other part

byte[] decryptedData = new byte[ciphertext.Length];

using (AesGcm aesGcm = new AesGcm(key))
{
    aesGcm.Decrypt(nonce, ciphertext, tag, decryptedData, associatedData);
}

// do something with the data
// this should always print that data is the same
Console.WriteLine($"AES-GCM: Decrypted data is{(dataToEncrypt.SequenceEqual(decryptedData) ? "the same as" : "different than")} original data.");
```

## <a name="cryptographic-key-importexport"></a>Importation/exportation d’une clé de chiffrement

.NET Core 3.0 Préversion 1 prend en charge l’importation et l’exportation de clés publiques et privées asymétriques aux formats standard, sans avoir à utiliser un certificat X.509.

Tous les types de clés (RSA, DSA, ECDsa, ECDiffieHellman) prennent en charge le format **X.509 SubjectPublicKeyInfo** pour les clés publiques, et les formats **PKCS #8 PrivateKeyInfo** et **PKCS #8 EncryptedPrivateKeyInfo** pour les clés privées. Le chiffrement RSA prend également en charge **PKCS #1 RSAPublicKey** et **PKCS #1 RSAPrivateKey**. Les méthodes d’exportation produisent toutes des données binaires encodées au format DER, tout comme les méthodes d’importation. Si une clé est stockée au format PEM compatible avec le texte, l’appelant devra décoder le contenu au format base64 avant d’appeler une méthode d’importation.

```csharp
using System;
using System.IO;
using System.Security.Cryptography;

namespace rsakeyprint
{
    class Program
    {
        static void Main(string[] args)
        {
            using (RSA rsa = RSA.Create())
            {
                byte[] keyBytes = File.ReadAllBytes(args[0]);
                rsa.ImportRSAPrivateKey(keyBytes, out int bytesRead);
 
                Console.WriteLine($"Read {bytesRead} bytes, {keyBytes.Length-bytesRead} extra byte(s) in file.");
                RSAParameters rsaParameters = rsa.ExportParameters(true);
                Console.WriteLine(BitConverter.ToString(rsaParameters.D));
            }
        }
    }
}
```

```console
user@comp-ubuntu1810:~/rsakeyprint$ echo Making a small key to save on screen space.
Making a small key to save on screen space.
user@comp-ubuntu1810:~/rsakeyprint$ openssl genrsa 768 | openssl rsa -outform der -out rsa.key
Generating RSA private key, 768 bit long modulus (2 primes)
..+++++++
........+++++++
e is 65537 (0x010001)
writing RSA key
user@comp-ubuntu1810:~/rsakeyprint$ dotnet run rsa.key
Read 461 bytes, 0 extra byte(s) in file.
0F-D0-82-34-F8-13-38-4A-7F-C7-52-4A-F6-93-F8-FB-6D-98-7A-6A-04-3B-BC-35-8C-7D-AC-A5-A3-6E-AD-C1-66-30-81-2C-2A-DE-DA-60-03-6A-2C-D9-76-15-7F-61-97-57-
79-E1-6E-45-62-C3-83-04-97-CB-32-EF-C5-17-5F-99-60-92-AE-B6-34-6F-30-06-03-AC-BF-15-24-43-84-EB-83-60-EF-4D-3B-BD-D9-5D-56-26-F0-51-CE-F1
user@comp-ubuntu1810:~/rsakeyprint$ openssl rsa -in rsa.key -inform der -text -noout | grep -A7 private
privateExponent:
    0f:d0:82:34:f8:13:38:4a:7f:c7:52:4a:f6:93:f8:
    fb:6d:98:7a:6a:04:3b:bc:35:8c:7d:ac:a5:a3:6e:
    ad:c1:66:30:81:2c:2a:de:da:60:03:6a:2c:d9:76:
    15:7f:61:97:57:79:e1:6e:45:62:c3:83:04:97:cb:
    32:ef:c5:17:5f:99:60:92:ae:b6:34:6f:30:06:03:
    ac:bf:15:24:43:84:eb:83:60:ef:4d:3b:bd:d9:5d:
    56:26:f0:51:ce:f1
```

Les fichiers PKCS #8 peuvent être inspectés avec la classe `System.Security.Cryptography.Pkcs.Pkcs8PrivateKeyInfo`.

Les fichiers PFX/PKCS#12 peuvent être inspectés et manipulés avec `System.Security.Cryptography.Pkcs.Pkcs12Info` et `System.Security.Cryptography.Pkcs.Pkcs12Builder`, respectivement.

## <a name="serialport-for-linux"></a>SerialPort pour Linux

.NET Core 3.0 prend désormais en charge <xref:System.IO.Ports.SerialPort?displayProperty=nameWithType> sous Linux.

Auparavant, .NET Core était uniquement pris en charge grâce au type `SerialPort` sous Windows.

## <a name="more-bcl-improvements"></a>Plusieurs améliorations BCL

Les types `Span<T>`, `Memory<T>` et autres types associés qui avaient été introduits dans .NET Core 2.1 ont été optimisées dans .NET Core 3.0. Les opérations courantes comme la construction de type span, le découpage, l’analyse et la mise en forme sont maintenant plus performantes. 

En outre, les types comme `String` ont bénéficié d’améliorations en arrière-plan pour les rendre plus efficaces lorsqu’ils sont utilisés comme des clés avec `Dictionary<TKey, TValue>` et d’autres collections. Aucune modification de code n’est nécessaire pour tirer parti de ces améliorations.

Les améliorations suivantes sont également des nouveautés dans .NET Core 3 Préversion 1 :

* Prise en charge de Brotli intégrée à HttpClient
* ThreadPool.UnsafeQueueWorkItem(IThreadPoolWorkItem)
* Unsafe.Unbox
* CancellationToken.Unregister
* Opérateurs arithmétiques complexes
* API de socket pour TCP keep alive
* StringBuilder.GetChunks
* Analyse IPEndPoint
* RandomNumberGenerator.GetInt32

## <a name="tiered-compilation"></a>Compilation hiérarchisée

La [compilation hiérarchisée](https://blogs.msdn.microsoft.com/dotnet/2018/08/02/tiered-compilation-preview-in-net-core-2-1/) est activée par défaut avec .NET Core 3.0. Cette fonctionnalité permet au runtime d’utiliser de manière plus adaptative le compilateur juste-à-temps (Just-In-Time ou JIT) pour obtenir de meilleures performances, à la fois au démarrage et pour optimiser le débit.

Cette fonctionnalité avait été ajoutée en option dans [.NET Core 2.1](https://blogs.msdn.microsoft.com/dotnet/2018/05/30/announcing-net-core-2-1/) et était activée par défaut dans [.NET Core 2.2 Préversion 2](https://blogs.msdn.microsoft.com/dotnet/2018/09/12/announcing-net-core-2-2-preview-2/). Elle est ensuite redevenue une option dans la version .NET Core 2.2.

## <a name="arm64-linux-support"></a>Support ARM64 Linux

Nous ajoutons la prise en charge de ARM64 sous Linux dans cette version. Pour le contexte, nous avons ajouté la prise en charge d’ARM32 sous Linux avec .NET Core 2.1, et sous Windows avec .NET Core 2.2. Actuellement, ARM64 est principallement utilisé dans des scénarios IoT.

Des [images Docker Alpine, Debian et Ubuntu sont disponibles avec .NET Core pour ARM64](https://hub.docker.com/r/microsoft/dotnet/).

Consultez [État de .NET Core ARM64](https://github.com/dotnet/announcements/issues/82) pour plus d’informations.

>[!NOTE]
> La prise en charge d’**ARM64** sous Windows n’est pas encore disponible.
