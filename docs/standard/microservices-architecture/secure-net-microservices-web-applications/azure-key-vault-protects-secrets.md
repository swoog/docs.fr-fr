---
title: Utilisation d’Azure Key Vault pour protéger les secrets au moment de la production
description: Architecture de microservices .NET pour les applications .NET en conteneur | Utilisation d’Azure Key Vault pour protéger les secrets au moment de la production
author: mjrousos
ms.author: wiwagn
ms.date: 05/26/2017
ms.openlocfilehash: 5738b81c90c886aff48451742881807dc09a9ff9
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43863985"
---
# <a name="using-azure-key-vault-to-protect-secrets-at-production-time"></a><span data-ttu-id="2e8e5-103">Utilisation d’Azure Key Vault pour protéger les secrets au moment de la production</span><span class="sxs-lookup"><span data-stu-id="2e8e5-103">Using Azure Key Vault to protect secrets at production time</span></span>

<span data-ttu-id="2e8e5-104">Les secrets stockés comme variables d’environnement ou au moyen de l’outil Secret Manager sont toujours stockés localement sur l’ordinateur et non chiffrés.</span><span class="sxs-lookup"><span data-stu-id="2e8e5-104">Secrets stored as environment variables or stored by the Secret Manager tool are still stored locally and unencrypted on the machine.</span></span> <span data-ttu-id="2e8e5-105">[Azure Key Vault](https://azure.microsoft.com/services/key-vault/) constitue une option de stockage des secrets plus sûre, offrant un emplacement centralisé et sécurisé pour le stockage des clés et des secrets.</span><span class="sxs-lookup"><span data-stu-id="2e8e5-105">A more secure option for storing secrets is [Azure Key Vault](https://azure.microsoft.com/services/key-vault/), which provides a secure, central location for storing keys and secrets.</span></span>

<span data-ttu-id="2e8e5-106">Le package Microsoft.Extensions.Configuration.AzureKeyVault permet à une application ASP.NET Core de lire les informations de configuration d’Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="2e8e5-106">The Microsoft.Extensions.Configuration.AzureKeyVault package allows an ASP.NET Core application to read configuration information from Azure Key Vault.</span></span> <span data-ttu-id="2e8e5-107">Pour commencer à utiliser des secrets à partir d’Azure Key Valut, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="2e8e5-107">To start using secrets from an Azure Key Vault, you follow these steps:</span></span>

<span data-ttu-id="2e8e5-108">En premier lieu, inscrivez votre application en tant qu’application Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2e8e5-108">First, register your application as an Azure AD application.</span></span> <span data-ttu-id="2e8e5-109">(L’accès aux coffres de clés est géré par Azure AD.) Vous pouvez faire cela sur le portail de gestion Azure.</span><span class="sxs-lookup"><span data-stu-id="2e8e5-109">(Access to key vaults is managed by Azure AD.) This can be done through the Azure management portal.</span></span>

<span data-ttu-id="2e8e5-110">Si vous préférez que votre application s’authentifie avec un certificat plutôt qu’un mot de passe ou une clé secrète client, vous pouvez utiliser l’applet de commande PowerShell [New-AzureRmADApplication](https://docs.microsoft.com/powershell/module/azurerm.resources/new-azurermadapplication).</span><span class="sxs-lookup"><span data-stu-id="2e8e5-110">Alternatively, if you want your application to authenticate using a certificate instead of a password or client secret, you can use the [New-AzureRmADApplication](https://docs.microsoft.com/powershell/module/azurerm.resources/new-azurermadapplication) PowerShell cmdlet.</span></span> <span data-ttu-id="2e8e5-111">Le certificat que vous inscrivez auprès d’Azure Key Vault n’a besoin que de votre clé publique.</span><span class="sxs-lookup"><span data-stu-id="2e8e5-111">The certificate that you register with Azure Key Vault needs only your public key.</span></span> <span data-ttu-id="2e8e5-112">(Votre application utilisera la clé privée.)</span><span class="sxs-lookup"><span data-stu-id="2e8e5-112">(Your application will use the private key.)</span></span>

<span data-ttu-id="2e8e5-113">En second lieu, accordez à l’application inscrite un accès au coffre de clés en créant un principal de service.</span><span class="sxs-lookup"><span data-stu-id="2e8e5-113">Second, give the registered application access to the key vault by creating a new service principal.</span></span> <span data-ttu-id="2e8e5-114">Pour cela, vous pouvez utiliser les commandes PowerShell suivantes :</span><span class="sxs-lookup"><span data-stu-id="2e8e5-114">You can do this using the following PowerShell commands:</span></span>

```powershell
$sp = New-AzureRmADServicePrincipal -ApplicationId "<Application ID guid>"
Set-AzureRmKeyVaultAccessPolicy -VaultName "<VaultName>" -ServicePrincipalName $sp.ServicePrincipalNames[0] -PermissionsToSecrets all -ResourceGroupName "<KeyVault Resource Group>"
```

<span data-ttu-id="2e8e5-115">En troisième lieu, ajoutez le coffre de clés comme source de configuration dans votre application en appelant la méthode d’extension IConfigurationBuilder.AddAzureKeyVault au moment de créer une instance d’IConfigurationRoot.</span><span class="sxs-lookup"><span data-stu-id="2e8e5-115">Third, include the key vault as a configuration source in your application by calling the IConfigurationBuilder.AddAzureKeyVault extension method when you create an IConfigurationRoot instance.</span></span> <span data-ttu-id="2e8e5-116">Notez que l’appel d’AddAzureKeyVault nécessite l’ID de l’application qui a été inscrite et qui a obtenu l’accès au coffre de clés aux étapes précédentes.</span><span class="sxs-lookup"><span data-stu-id="2e8e5-116">Note that calling AddAzureKeyVault will require the application ID that was registered and given access to the key vault in the previous steps.</span></span>

  <span data-ttu-id="2e8e5-117">Pour l’heure, .NET Standard et .NET Core permettent d’obtenir des informations de configuration auprès d’Azure Key Vault à l’aide d’un ID client et d’une clé secrète client.</span><span class="sxs-lookup"><span data-stu-id="2e8e5-117">Currently, .NET Standard and .NET Core support getting configuration information from an Azure Key Vault using a client ID and client secret.</span></span> <span data-ttu-id="2e8e5-118">Les applications .NET Framework peuvent utiliser une surcharge d’IConfigurationBuilder.AddAzureKeyVault qui prend un certificat à la place de la clé secrète client.</span><span class="sxs-lookup"><span data-stu-id="2e8e5-118">.NET Framework applications can use an overload of IConfigurationBuilder.AddAzureKeyVault that takes a certificate in place of the client secret.</span></span> <span data-ttu-id="2e8e5-119">À ce jour, le travail est [en cours d’exécution](https://github.com/aspnet/Configuration/issues/605) pour rendre cette surcharge disponible dans .NET Standard Edition et .NET Core.</span><span class="sxs-lookup"><span data-stu-id="2e8e5-119">As of this writing, work is [in progress](https://github.com/aspnet/Configuration/issues/605) to make that overload available in .NET Standard and .NET Core.</span></span> <span data-ttu-id="2e8e5-120">Tant que la surcharge AddAzureKeyVault qui accepte un certificat n’est pas disponible, les applications ASP.NET Core peuvent accéder à Azure Key Vault avec une authentification basée sur un certificat en créant explicitement un objet KeyVaultClient, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="2e8e5-120">Until the AddAzureKeyVault overload that accepts a certificate is available, ASP.NET Core applications can access an Azure Key Vault with certificate-based authentication by explicitly creating a KeyVaultClient object, as shown in the following example:</span></span>

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

<span data-ttu-id="2e8e5-121">Dans cet exemple, l’appel à AddAzureKeyVault est émis à la fin de l’inscription du fournisseur de configuration.</span><span class="sxs-lookup"><span data-stu-id="2e8e5-121">In this example, the call to AddAzureKeyVault comes at the end of configuration provider registration.</span></span> <span data-ttu-id="2e8e5-122">Une bonne pratique consiste à inscrire Azure Key Vault comme dernier fournisseur de configuration. Il pourra ainsi remplacer les valeurs de configuration des fournisseurs précédents et aucune valeur de configuration issue d’autres sources ne remplacera celles du coffre de clés.</span><span class="sxs-lookup"><span data-stu-id="2e8e5-122">It is a best practice to register Azure Key Vault as the last configuration provider so that it has an opportunity to override configuration values from previous providers, and so that no configuration values from other sources override those from the key vault.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2e8e5-123">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="2e8e5-123">Additional resources</span></span>

-   <span data-ttu-id="2e8e5-124">**Utilisation d’Azure Key Vault pour protéger les secrets d’application**
    [*https://docs.microsoft.com/azure/guidance/guidance-multitenant-identity-keyvault*](https://docs.microsoft.com/azure/guidance/guidance-multitenant-identity-keyvault)</span><span class="sxs-lookup"><span data-stu-id="2e8e5-124">**Using Azure Key Vault to protect application secrets**
[*https://docs.microsoft.com/azure/guidance/guidance-multitenant-identity-keyvault*](https://docs.microsoft.com/azure/guidance/guidance-multitenant-identity-keyvault)</span></span>

-   <span data-ttu-id="2e8e5-125">**Stockage sécurisé des secrets d’application en cours de développement**
    [*https://docs.microsoft.com/aspnet/core/security/app-secrets*](https://docs.microsoft.com/aspnet/core/security/app-secrets)</span><span class="sxs-lookup"><span data-stu-id="2e8e5-125">**Safe storage of app secrets during development**
[*https://docs.microsoft.com/aspnet/core/security/app-secrets*](https://docs.microsoft.com/aspnet/core/security/app-secrets)</span></span>

-   <span data-ttu-id="2e8e5-126">**Configuration de la protection des données**
    [*https://docs.microsoft.com/aspnet/core/security/data-protection/configuration/overview*](https://docs.microsoft.com/aspnet/core/security/data-protection/configuration/overview)</span><span class="sxs-lookup"><span data-stu-id="2e8e5-126">**Configuring data protection**
[*https://docs.microsoft.com/aspnet/core/security/data-protection/configuration/overview*](https://docs.microsoft.com/aspnet/core/security/data-protection/configuration/overview)</span></span>

-   <span data-ttu-id="2e8e5-127">**Gestion et durée de vie des clés**
    [*https://docs.microsoft.com/aspnet/core/security/data-protection/configuration/default-settings\#data-protection-default-settings*](https://docs.microsoft.com/aspnet/core/security/data-protection/configuration/default-settings#data-protection-default-settings)</span><span class="sxs-lookup"><span data-stu-id="2e8e5-127">**Key management and lifetime**
[*https://docs.microsoft.com/aspnet/core/security/data-protection/configuration/default-settings\#data-protection-default-settings*](https://docs.microsoft.com/aspnet/core/security/data-protection/configuration/default-settings#data-protection-default-settings)</span></span>

-   <span data-ttu-id="2e8e5-128">Dépôt GitHub **Microsoft.Extensions.Configuration.KeyPerFile**.</span><span class="sxs-lookup"><span data-stu-id="2e8e5-128">**Microsoft.Extensions.Configuration.KeyPerFile** GitHub repo.</span></span>
    [*https://github.com/aspnet/Configuration/tree/master/src/Config.KeyPerFile*](https://github.com/aspnet/Configuration/tree/master/src/Config.KeyPerFile)

>[!div class="step-by-step"]
<span data-ttu-id="2e8e5-129">[Précédent](developer-app-secrets-storage.md)
[Suivant](../key-takeaways.md)</span><span class="sxs-lookup"><span data-stu-id="2e8e5-129">[Previous](developer-app-secrets-storage.md)
[Next](../key-takeaways.md)</span></span>
