---
title: Stockage sécurisé des secrets d’application en phase de développement
description: Architecture de microservices .NET pour les applications .NET en conteneur | Stockage sécurisé des secrets d’application en phase de développement
author: mjrousos
ms.author: wiwagn
ms.date: 05/26/2017
ms.openlocfilehash: 560120db35ae190bdef1f95d72ac1e5de697124e
ms.sourcegitcommit: 979597cd8055534b63d2c6ee8322938a27d0c87b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2018
ms.locfileid: "37105944"
---
# <a name="storing-application-secrets-safely-during-development"></a><span data-ttu-id="2f804-103">Stockage sécurisé des secrets d’application en phase de développement</span><span class="sxs-lookup"><span data-stu-id="2f804-103">Storing application secrets safely during development</span></span>

<span data-ttu-id="2f804-104">Pour se connecter à des ressources protégées et à d’autres services, les applications ASP.NET Core doivent généralement utiliser des chaînes de connexion, des mots de passe ou d’autres informations d’identification qui contiennent des informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="2f804-104">To connect with protected resources and other services, ASP.NET Core applications typically need to use connection strings, passwords, or other credentials that contain sensitive information.</span></span> <span data-ttu-id="2f804-105">Ces informations sensibles sont appelées *secrets*.</span><span class="sxs-lookup"><span data-stu-id="2f804-105">These sensitive pieces of information are called *secrets*.</span></span> <span data-ttu-id="2f804-106">La bonne pratique consiste à ne pas inclure les secrets dans le code source et certainement pas de les stocker dans le contrôle de code source.</span><span class="sxs-lookup"><span data-stu-id="2f804-106">It is a best practice to not include secrets in source code and certainly not to store secrets in source control.</span></span> <span data-ttu-id="2f804-107">Au lieu de cela, vous devez utiliser le modèle de configuration ASP.NET Core pour lire les secrets à partir d’emplacements plus sécurisés.</span><span class="sxs-lookup"><span data-stu-id="2f804-107">Instead, you should use the ASP.NET Core configuration model to read the secrets from more secure locations.</span></span>

<span data-ttu-id="2f804-108">Vous devez distinguer les secrets destinés à accéder aux ressources de développement et de préproduction de ceux utilisés pour accéder aux ressources de production, car ce ne sont pas les mêmes personnes qui ont besoin d’accéder à ces différents jeux de secrets.</span><span class="sxs-lookup"><span data-stu-id="2f804-108">You should separate the secrets for accessing development and staging resources from those used for accessing production resources, because different individuals will need access to those different sets of secrets.</span></span> <span data-ttu-id="2f804-109">Dans la pratique, les secrets utilisés en phase de développement sont généralement stockés dans des variables d’environnement ou avec l’outil Secret Manager d’ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="2f804-109">To store secrets used during development, common approaches are to either store secrets in environment variables or by using the ASP.NET Core Secret Manager tool.</span></span> <span data-ttu-id="2f804-110">Pour un stockage plus sécurisé dans les environnements de production, les microservices peuvent stocker les secrets dans Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="2f804-110">For more secure storage in production environments, microservices can store secrets in an Azure Key Vault.</span></span>

## <a name="storing-secrets-in-environment-variables"></a><span data-ttu-id="2f804-111">Stockage des secrets dans des variables d’environnement</span><span class="sxs-lookup"><span data-stu-id="2f804-111">Storing secrets in environment variables</span></span>

<span data-ttu-id="2f804-112">Pour les développeurs, l’un des moyens de maintenir les secrets en dehors du code source est de définir des secrets basés sur des chaînes prenant la forme de [variables d’environnement](https://docs.microsoft.com/aspnet/core/security/app-secrets#environment-variables) sur leurs machines de développement.</span><span class="sxs-lookup"><span data-stu-id="2f804-112">One way to keep secrets out of source code is for developers to set string-based secrets as [environment variables](https://docs.microsoft.com/aspnet/core/security/app-secrets#environment-variables) on their development machines.</span></span> <span data-ttu-id="2f804-113">Quand vous utilisez des variables d’environnement pour stocker les secrets avec des noms hiérarchisés (ceux imbriqués dans les sections de configuration), attribuez un nom aux variables d’environnement qui inclut la hiérarchie complète du nom du secret en les séparant de deux-points (:).</span><span class="sxs-lookup"><span data-stu-id="2f804-113">When you use environment variables to store secrets with hierarchical names (those nested in configuration sections), create a name for the environment variables that includes the full hierarchy of the secret’s name, delimited with colons (:).</span></span>

<span data-ttu-id="2f804-114">Par exemple, le fait de définir une variable d’environnement Logging:LogLevel:Default sur Debug équivaudrait à une valeur de configuration du fichier JSON suivant :</span><span class="sxs-lookup"><span data-stu-id="2f804-114">For example, setting an environment variable Logging:LogLevel:Default to Debug would be equivalent to a configuration value from the following JSON file:</span></span>

```json
{
    "Logging": {
        "LogLevel": {
            "Default": "Debug"
        }
    }
}
```

<span data-ttu-id="2f804-115">Pour accéder à ces valeurs de variables d’environnement, l’application doit simplement appeler AddEnvironmentVariables sur son ConfigurationBuilder pendant la construction d’un objet IConfigurationRoot.</span><span class="sxs-lookup"><span data-stu-id="2f804-115">To access these values from environment variables, the application just needs to call AddEnvironmentVariables on its ConfigurationBuilder when constructing an IConfigurationRoot object.</span></span>

<span data-ttu-id="2f804-116">Notez que les variables d’environnement sont généralement stockées en texte clair. Par conséquent, si la machine ou le processus comprenant les variables d’environnement est compromis, les valeurs des variables d’environnement sont visibles.</span><span class="sxs-lookup"><span data-stu-id="2f804-116">Note that environment variables are generally stored as plain text, so if the machine or process with the environment variables is compromised, the environment variable values will be visible.</span></span>

## <a name="storing-secrets-using-the-aspnet-core-secret-manager"></a><span data-ttu-id="2f804-117">Stockage des secrets à l’aide de l’outil Secret Manager d’ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="2f804-117">Storing secrets using the ASP.NET Core Secret Manager</span></span>

<span data-ttu-id="2f804-118">L’outil [Secret Manager](https://docs.microsoft.com/aspnet/core/security/app-secrets#secret-manager) d’ASP.NET Core offre un autre moyen de maintenir les secrets en dehors du code source.</span><span class="sxs-lookup"><span data-stu-id="2f804-118">The ASP.NET Core [Secret Manager](https://docs.microsoft.com/aspnet/core/security/app-secrets#secret-manager) tool provides another method of keeping secrets out of source code.</span></span> <span data-ttu-id="2f804-119">Pour utiliser l’outil Secret Manager, incluez une référence de l’outil (DotNetCliToolReference) au package Microsoft.Extensions.SecretManager.Tools de votre fichier projet.</span><span class="sxs-lookup"><span data-stu-id="2f804-119">To use the Secret Manager tool, include a tools reference (DotNetCliToolReference) to the Microsoft.Extensions.SecretManager.Tools package in your project file.</span></span> <span data-ttu-id="2f804-120">Une fois cette dépendance présente et restaurée, la commande dotnet user-secrets peut être utilisée pour définir la valeur des secrets à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="2f804-120">Once that dependency is present and has been restored, the dotnet user-secrets command can be used to set the value of secrets from the command line.</span></span> <span data-ttu-id="2f804-121">Ces secrets sont alors stockés dans un fichier JSON dans le répertoire du profil de l’utilisateur (les détails varient selon le système d’exploitation), à l’écart du code source.</span><span class="sxs-lookup"><span data-stu-id="2f804-121">These secrets will be stored in a JSON file in the user’s profile directory (details vary by OS), away from source code.</span></span>

<span data-ttu-id="2f804-122">Les secrets définis par l’outil Secret Manager sont organisés par la propriété UserSecretsId du projet qui utilise les secrets.</span><span class="sxs-lookup"><span data-stu-id="2f804-122">Secrets set by the Secret Manager tool are organized by the UserSecretsId property of the project that is using the secrets.</span></span> <span data-ttu-id="2f804-123">Par conséquent, veillez à définir la propriété UserSecretsId dans votre fichier projet (comme indiqué dans l’extrait de code ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="2f804-123">Therefore, you must be sure to set the UserSecretsId property in your project file (as shown in the snippet below).</span></span> <span data-ttu-id="2f804-124">Vous pouvez utiliser n’importe quelle chaîne en guise d’ID du moment qu’elle est unique dans le projet.</span><span class="sxs-lookup"><span data-stu-id="2f804-124">The actual string used as the ID is not important as long as it is unique in the project.</span></span>

```xml
<PropertyGroup>
    <UserSecretsId>UniqueIdentifyingString</UserSecretsId>
</PropertyGroup>
```

<span data-ttu-id="2f804-125">Pour utiliser les secrets stockés avec Secret Manager dans une application, AddUserSecrets&lt;T&gt; est appelé au niveau de l’instance ConfigurationBuilder. Les secrets de l’application sont alors inclus dans sa configuration.</span><span class="sxs-lookup"><span data-stu-id="2f804-125">Using secrets stored with Secret Manager in an application is accomplished by calling AddUserSecrets&lt;T&gt; on the ConfigurationBuilder instance to include secrets for the application in its configuration.</span></span> <span data-ttu-id="2f804-126">Le paramètre générique T doit être un type de l’assembly auquel UserSecretId a été appliqué.</span><span class="sxs-lookup"><span data-stu-id="2f804-126">The generic parameter T should be a type from the assembly that the UserSecretId was applied to.</span></span> <span data-ttu-id="2f804-127">En règle générale, l’utilisation d’AddUserSecrets&lt;Startup&gt; convient.</span><span class="sxs-lookup"><span data-stu-id="2f804-127">Usually using AddUserSecrets&lt;Startup&gt; is fine.</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="2f804-128">[Précédent](authorization-net-microservices-web-applications.md)
[Suivant](azure-key-vault-protects-secrets.md)</span><span class="sxs-lookup"><span data-stu-id="2f804-128">[Previous](authorization-net-microservices-web-applications.md)
[Next](azure-key-vault-protects-secrets.md)</span></span>
