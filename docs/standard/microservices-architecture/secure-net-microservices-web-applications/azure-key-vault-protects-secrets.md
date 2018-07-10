---
title: Utilisation d’Azure Key Vault pour protéger les secrets au moment de la production
description: Architecture de microservices .NET pour les applications .NET en conteneur | Utilisation d’Azure Key Vault pour protéger les secrets au moment de la production
author: mjrousos
ms.author: wiwagn
ms.date: 05/26/2017
ms.openlocfilehash: 171d9120e4817065ddafc9dfa9caa362694ddeb3
ms.sourcegitcommit: 979597cd8055534b63d2c6ee8322938a27d0c87b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2018
ms.locfileid: "37105282"
---
# <a name="using-azure-key-vault-to-protect-secrets-at-production-time"></a>Utilisation d’Azure Key Vault pour protéger les secrets au moment de la production

Les secrets stockés comme variables d’environnement ou au moyen de l’outil Secret Manager sont toujours stockés localement sur l’ordinateur et non chiffrés. [Azure Key Vault](https://azure.microsoft.com/services/key-vault/) constitue une option de stockage des secrets plus sûre, offrant un emplacement centralisé et sécurisé pour le stockage des clés et des secrets.

Le package Microsoft.Extensions.Configuration.AzureKeyVault permet à une application ASP.NET Core de lire les informations de configuration d’Azure Key Vault. Pour commencer à utiliser des secrets à partir d’Azure Key Valut, procédez comme suit :

En premier lieu, inscrivez votre application en tant qu’application Azure AD. (L’accès aux coffres de clés est géré par Azure AD.) Vous pouvez faire cela sur le portail de gestion Azure.

Si vous préférez que votre application s’authentifie avec un certificat plutôt qu’un mot de passe ou une clé secrète client, vous pouvez utiliser l’applet de commande PowerShell [New-AzureRmADApplication](https://docs.microsoft.com/powershell/resourcemanager/azurerm.resources/v3.3.0/new-azurermadapplication). Le certificat que vous inscrivez auprès d’Azure Key Vault n’a besoin que de votre clé publique. (Votre application utilisera la clé privée.)

En second lieu, accordez à l’application inscrite un accès au coffre de clés en créant un principal de service. Pour cela, vous pouvez utiliser les commandes PowerShell suivantes :

```powershell
$sp = New-AzureRmADServicePrincipal -ApplicationId "<Application ID guid>"
Set-AzureRmKeyVaultAccessPolicy -VaultName "<VaultName>" -ServicePrincipalName $sp.ServicePrincipalNames[0] -PermissionsToSecrets all -ResourceGroupName "<KeyVault Resource Group>"
```

En troisième lieu, ajoutez le coffre de clés comme source de configuration dans votre application en appelant la méthode d’extension IConfigurationBuilder.AddAzureKeyVault au moment de créer une instance d’IConfigurationRoot. Notez que l’appel d’AddAzureKeyVault nécessite l’ID de l’application qui a été inscrite et qui a obtenu l’accès au coffre de clés aux étapes précédentes.

  Pour l’heure, .NET Standard et .NET Core permettent d’obtenir des informations de configuration auprès d’Azure Key Vault à l’aide d’un ID client et d’une clé secrète client. Les applications .NET Framework peuvent utiliser une surcharge d’IConfigurationBuilder.AddAzureKeyVault qui prend un certificat à la place de la clé secrète client. À ce jour, le travail est [en cours d’exécution](https://github.com/aspnet/Configuration/issues/605) pour rendre cette surcharge disponible dans .NET Standard Edition et .NET Core. Tant que la surcharge AddAzureKeyVault qui accepte un certificat n’est pas disponible, les applications ASP.NET Core peuvent accéder à Azure Key Vault avec une authentification basée sur un certificat en créant explicitement un objet KeyVaultClient, comme dans l’exemple suivant :

```csharp
// Configure Key Vault client
var kvClient = new KeyVaultClient(new KeyVaultClient.AuthenticationCallback(async
    (authority, resource, scope) =>
    {
        var cert = // Get certificate from local store/file/key vault etc. as needed
        // From the Microsoft.IdentityModel.Clients.ActiveDirectory pacakge
        var authContext = new AuthenticationContext(authority,
            TokenCache.DefaultShared);
        var result = await authContext.AcquireTokenAsync(resource,
            // From the Microsoft.Rest.ClientRuntime.Azure.Authentication pacakge
            new ClientAssertionCertificate("{Application ID}", cert));
        return result.AccessToken;
    }));

    // Get configuration values from Key Vault
    var builder = new ConfigurationBuilder()
        .SetBasePath(env.ContentRootPath)
        // Other configuration providers go here.
        .AddAzureKeyVault("{KeyValueUri}", kvClient,
        new DefaultKeyVaultSecretManager());
```

Dans cet exemple, l’appel à AddAzureKeyVault est émis à la fin de l’inscription du fournisseur de configuration. Une bonne pratique consiste à inscrire Azure Key Vault comme dernier fournisseur de configuration. Il pourra ainsi remplacer les valeurs de configuration des fournisseurs précédents et aucune valeur de configuration issue d’autres sources ne remplacera celles du coffre de clés.

## <a name="additional-resources"></a>Ressources supplémentaires

-   **Utilisation d’Azure Key Vault pour protéger les secrets d’application**
    [*https://docs.microsoft.com/azure/guidance/guidance-multitenant-identity-keyvault*](https://docs.microsoft.com/azure/guidance/guidance-multitenant-identity-keyvault)

-   **Stockage sécurisé des secrets d’application en cours de développement**
    [*https://docs.microsoft.com/aspnet/core/security/app-secrets*](https://docs.microsoft.com/aspnet/core/security/app-secrets)

-   **Configuration de la protection des données**
    [*https://docs.microsoft.com/aspnet/core/security/data-protection/configuration/overview*](https://docs.microsoft.com/aspnet/core/security/data-protection/configuration/overview)

-   **Gestion et durée de vie des clés**
    [*https://docs.microsoft.com/aspnet/core/security/data-protection/configuration/default-settings\#data-protection-default-settings*](https://docs.microsoft.com/aspnet/core/security/data-protection/configuration/default-settings#data-protection-default-settings)

-   **Microsoft.Extensions.Configuration.DockerSecrets.** Dépôt GitHub
    [*https://github.com/aspnet/Configuration/tree/dev/src/Microsoft.Extensions.Configuration.DockerSecrets*](https://github.com/aspnet/Configuration/tree/dev/src/Microsoft.Extensions.Configuration.DockerSecrets)

>[!div class="step-by-step"]
[Précédent](developer-app-secrets-storage.md)
[Suivant](../key-takeaways.md)
