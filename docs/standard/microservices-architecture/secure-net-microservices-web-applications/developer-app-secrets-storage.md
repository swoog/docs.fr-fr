---
title: Stockage sécurisé des secrets d’application en phase de développement
description: Architecture de microservices .NET pour les applications .NET en conteneur | Stockage sécurisé des secrets d’application en phase de développement
author: mjrousos
ms.author: wiwagn
ms.date: 05/26/2017
ms.openlocfilehash: d8dd2da07104d6461d4eec0cb3fccd61c4db71c1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33580112"
---
# <a name="storing-application-secrets-safely-during-development"></a>Stockage sécurisé des secrets d’application en phase de développement

Pour se connecter à des ressources protégées et à d’autres services, les applications ASP.NET Core doivent généralement utiliser des chaînes de connexion, des mots de passe ou d’autres informations d’identification qui contiennent des informations sensibles. Ces informations sensibles sont appelées *secrets*. La bonne pratique consiste à ne pas inclure les secrets dans le code source et certainement pas de les stocker dans le contrôle de code source. Au lieu de cela, vous devez utiliser le modèle de configuration ASP.NET Core pour lire les secrets à partir d’emplacements plus sécurisés.

Vous devez distinguer les secrets destinés à accéder aux ressources de développement et de préproduction de ceux utilisés pour accéder aux ressources de production, car ce ne sont pas les mêmes personnes qui ont besoin d’accéder à ces différents jeux de secrets. Dans la pratique, les secrets utilisés en phase de développement sont généralement stockés dans des variables d’environnement ou avec l’outil Secret Manager d’ASP.NET Core. Pour un stockage plus sécurisé dans les environnements de production, les microservices peuvent stocker les secrets dans Azure Key Vault.

## <a name="storing-secrets-in-environment-variables"></a>Stockage des secrets dans des variables d’environnement

Pour les développeurs, l’un des moyens de maintenir les secrets en dehors du code source est de définir des secrets basés sur des chaînes prenant la forme de [variables d’environnement](https://docs.microsoft.com/aspnet/core/security/app-secrets#environment-variables) sur leurs machines de développement. Quand vous utilisez des variables d’environnement pour stocker les secrets avec des noms hiérarchisés (ceux imbriqués dans les sections de configuration), attribuez un nom aux variables d’environnement qui inclut la hiérarchie complète du nom du secret en les séparant de deux-points (:).

Par exemple, le fait de définir une variable d’environnement Logging:LogLevel:Default sur Debug équivaudrait à une valeur de configuration du fichier JSON suivant :

```json
{
    "Logging": {
        "LogLevel": {
            "Default": "Debug"
        }
    }
}
```

Pour accéder à ces valeurs de variables d’environnement, l’application doit simplement appeler AddEnvironmentVariables sur son ConfigurationBuilder pendant la construction d’un objet IConfigurationRoot.

Notez que les variables d’environnement sont généralement stockées en texte clair. Par conséquent, si la machine ou le processus comprenant les variables d’environnement est compromis, les valeurs des variables d’environnement sont visibles.

## <a name="storing-secrets-using-the-aspnet-core-secret-manager"></a>Stockage des secrets à l’aide de l’outil Secret Manager d’ASP.NET Core

L’outil [Secret Manager](https://docs.microsoft.com/aspnet/core/security/app-secrets#secret-manager) d’ASP.NET Core offre un autre moyen de maintenir les secrets en dehors du code source. Pour utiliser l’outil Secret Manager, incluez une référence de l’outil (DotNetCliToolReference) au package Microsoft.Extensions.SecretManager.Tools de votre fichier projet. Une fois cette dépendance présente et restaurée, la commande dotnet user-secrets peut être utilisée pour définir la valeur des secrets à partir de la ligne de commande. Ces secrets sont alors stockés dans un fichier JSON dans le répertoire du profil de l’utilisateur (les détails varient selon le système d’exploitation), à l’écart du code source.

Les secrets définis par l’outil Secret Manager sont organisés par la propriété UserSecretsId du projet qui utilise les secrets. Par conséquent, veillez à définir la propriété UserSecretsId dans votre fichier projet (comme indiqué dans l’extrait de code ci-dessous). Vous pouvez utiliser n’importe quelle chaîne en guise d’ID du moment qu’elle est unique dans le projet.

```xml
<PropertyGroup>
    <UserSecretsId>UniqueIdentifyingString</UserSecretsId>
</PropertyGroup>
```

Pour utiliser les secrets stockés avec Secret Manager dans une application, AddUserSecrets&lt;T&gt; est appelé au niveau de l’instance ConfigurationBuilder. Les secrets de l’application sont alors inclus dans sa configuration. Le paramètre générique T doit être un type de l’assembly auquel UserSecretId a été appliqué. En règle générale, l’utilisation d’AddUserSecrets&lt;Startup&gt; convient.


>[!div class="step-by-step"]
[Précédent] (authorization-net-microservices-web-applications.md) [Suivant] (azure-key-vault-protects-secrets.md)
