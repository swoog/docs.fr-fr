---
title: Utilisation d’Azure Key Vault pour protéger les secrets au moment de la production
description: Sécurité dans les microservices .NET et les applications web - Azure Key Vault est un excellent moyen de gérer les secrets d’application qui sont entièrement contrôlés par les administrateurs. Les administrateurs peuvent même affecter et révoquer des valeurs de développement sans que les développeurs aient à les gérer.
author: mjrousos
ms.author: wiwagn
ms.date: 10/19/2018
ms.openlocfilehash: fd2bff04e06bf0561ee0c95d87978f834f192172
ms.sourcegitcommit: 2b986afe4ce9e13bbeec929c9737757eb61de60e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56664040"
---
# <a name="use-azure-key-vault-to-protect-secrets-at-production-time"></a><span data-ttu-id="7e78b-104">Utiliser Azure Key Vault pour protéger les secrets au moment de la production</span><span class="sxs-lookup"><span data-stu-id="7e78b-104">Use Azure Key Vault to protect secrets at production time</span></span>

<span data-ttu-id="7e78b-105">Les secrets stockés comme variables d’environnement ou au moyen de l’outil Secret Manager sont toujours stockés localement sur l’ordinateur et non chiffrés.</span><span class="sxs-lookup"><span data-stu-id="7e78b-105">Secrets stored as environment variables or stored by the Secret Manager tool are still stored locally and unencrypted on the machine.</span></span> <span data-ttu-id="7e78b-106">[Azure Key Vault](https://azure.microsoft.com/services/key-vault/) constitue une option de stockage des secrets plus sûre, offrant un emplacement centralisé et sécurisé pour le stockage des clés et des secrets.</span><span class="sxs-lookup"><span data-stu-id="7e78b-106">A more secure option for storing secrets is [Azure Key Vault](https://azure.microsoft.com/services/key-vault/), which provides a secure, central location for storing keys and secrets.</span></span>

<span data-ttu-id="7e78b-107">Le package **Microsoft.Extensions.Configuration.AzureKeyVault** permet à une application ASP.NET Core de lire des informations de configuration à partir d’Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="7e78b-107">The **Microsoft.Extensions.Configuration.AzureKeyVault** package allows an ASP.NET Core application to read configuration information from Azure Key Vault.</span></span> <span data-ttu-id="7e78b-108">Pour commencer à utiliser des secrets à partir d’Azure Key Valut, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7e78b-108">To start using secrets from an Azure Key Vault, you follow these steps:</span></span>

1. <span data-ttu-id="7e78b-109">Inscrivez votre application en tant qu’application Azure AD.</span><span class="sxs-lookup"><span data-stu-id="7e78b-109">Register your application as an Azure AD application.</span></span> <span data-ttu-id="7e78b-110">(L’accès aux coffres de clés est géré par Azure AD.) Vous pouvez faire cela dans le portail de gestion Azure.\\</span><span class="sxs-lookup"><span data-stu-id="7e78b-110">(Access to key vaults is managed by Azure AD.) This can be done through the Azure management portal.\\</span></span>

   <span data-ttu-id="7e78b-111">Si vous préférez que votre application s’authentifie avec un certificat plutôt qu’un mot de passe ou une clé secrète client, vous pouvez utiliser l’applet de commande PowerShell [New-AzureRmADApplication](/powershell/module/azurerm.resources/new-azurermadapplication).</span><span class="sxs-lookup"><span data-stu-id="7e78b-111">Alternatively, if you want your application to authenticate using a certificate instead of a password or client secret, you can use the [New-AzureRmADApplication](/powershell/module/azurerm.resources/new-azurermadapplication) PowerShell cmdlet.</span></span> <span data-ttu-id="7e78b-112">Le certificat que vous inscrivez auprès d’Azure Key Vault n’a besoin que de votre clé publique.</span><span class="sxs-lookup"><span data-stu-id="7e78b-112">The certificate that you register with Azure Key Vault needs only your public key.</span></span> <span data-ttu-id="7e78b-113">(Votre application utilisera la clé privée.)</span><span class="sxs-lookup"><span data-stu-id="7e78b-113">(Your application will use the private key.)</span></span>

2. <span data-ttu-id="7e78b-114">Accordez à l’application inscrite un accès au coffre de clés en créant un principal de service.</span><span class="sxs-lookup"><span data-stu-id="7e78b-114">Give the registered application access to the key vault by creating a new service principal.</span></span> <span data-ttu-id="7e78b-115">Pour cela, vous pouvez utiliser les commandes PowerShell suivantes :</span><span class="sxs-lookup"><span data-stu-id="7e78b-115">You can do this using the following PowerShell commands:</span></span>

   ```powershell
   $sp = New-AzureRmADServicePrincipal -ApplicationId "<Application ID guid>"
   Set-AzureRmKeyVaultAccessPolicy -VaultName "<VaultName>" -ServicePrincipalName $sp.ServicePrincipalNames[0] -PermissionsToSecrets all -ResourceGroupName "<KeyVault Resource Group>"
   ```

3. <span data-ttu-id="7e78b-116">Ajoutez le coffre de clés comme source de configuration dans votre application en appelant la méthode d’extension <xref:Microsoft.Extensions.Configuration.AzureKeyVaultConfigurationExtensions.AddAzureKeyVault%2A?displayProperty=nameWithType> quand vous créez une instance <xref:Microsoft.Extensions.Configuration.IConfigurationRoot>.</span><span class="sxs-lookup"><span data-stu-id="7e78b-116">Include the key vault as a configuration source in your application by calling the <xref:Microsoft.Extensions.Configuration.AzureKeyVaultConfigurationExtensions.AddAzureKeyVault%2A?displayProperty=nameWithType> extension method when you create an <xref:Microsoft.Extensions.Configuration.IConfigurationRoot> instance.</span></span> <span data-ttu-id="7e78b-117">Notez que l’appel d’`AddAzureKeyVault` nécessite l’ID de l’application qui a été inscrite et qui a obtenu l’accès au coffre de clés aux étapes précédentes.</span><span class="sxs-lookup"><span data-stu-id="7e78b-117">Note that calling `AddAzureKeyVault` requires the application ID that was registered and given access to the key vault in the previous steps.</span></span>

   <span data-ttu-id="7e78b-118">Vous pouvez également utiliser une surcharge de `AddAzureKeyVault` qui accepte un certificat à la place de la clé secrète client en incluant simplement une référence au package [Microsoft.IdentityModel.Clients.ActiveDirectory](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory).</span><span class="sxs-lookup"><span data-stu-id="7e78b-118">You can also use an overload of `AddAzureKeyVault` that takes a certificate in place of the client secret by just including a reference to the [Microsoft.IdentityModel.Clients.ActiveDirectory](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory) package.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7e78b-119">Nous vous recommandons d’inscrire Azure Key Vault en tant que dernier fournisseur de configuration, afin qu’il puisse remplacer les valeurs de configuration des fournisseurs précédents.</span><span class="sxs-lookup"><span data-stu-id="7e78b-119">We recommend you to register Azure Key Vault as the last configuration provider, so it can override configuration values from previous providers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7e78b-120">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="7e78b-120">Additional resources</span></span>

- <span data-ttu-id="7e78b-121">**Utilisation d’Azure Key Vault pour protéger les secrets d’application** \\</span><span class="sxs-lookup"><span data-stu-id="7e78b-121">**Using Azure Key Vault to protect application secrets** \\</span></span>
  [*https://docs.microsoft.com/azure/guidance/guidance-multitenant-identity-keyvault*](/azure/guidance/guidance-multitenant-identity-keyvault)

- <span data-ttu-id="7e78b-122">**Stockage sécurisé des secrets d’application en cours de développement** \\</span><span class="sxs-lookup"><span data-stu-id="7e78b-122">**Safe storage of app secrets during development** \\</span></span>
  [*https://docs.microsoft.com/aspnet/core/security/app-secrets*](/aspnet/core/security/app-secrets)

- <span data-ttu-id="7e78b-123">**Configuration de la protection des données** \\</span><span class="sxs-lookup"><span data-stu-id="7e78b-123">**Configuring data protection** \\</span></span>
  [*https://docs.microsoft.com/aspnet/core/security/data-protection/configuration/overview*](/aspnet/core/security/data-protection/configuration/overview)

- <span data-ttu-id="7e78b-124">**Gestion et durée de vie des clés de protection des données dans ASP.NET Core** \\</span><span class="sxs-lookup"><span data-stu-id="7e78b-124">**Data Protection key management and lifetime in ASP.NET Core** \\</span></span>
  [*https://docs.microsoft.com/aspnet/core/security/data-protection/configuration/default-settings*](/aspnet/core/security/data-protection/configuration/default-settings)

- <span data-ttu-id="7e78b-125">Référentiel GitHub **Microsoft.Extensions.Configuration.KeyPerFile**.</span><span class="sxs-lookup"><span data-stu-id="7e78b-125">**Microsoft.Extensions.Configuration.KeyPerFile** GitHub repository.</span></span> \
  [*https://github.com/aspnet/Configuration/tree/master/src/Config.KeyPerFile*](https://github.com/aspnet/Configuration/tree/master/src/Config.KeyPerFile)

>[!div class="step-by-step"]
><span data-ttu-id="7e78b-126">[Précédent](developer-app-secrets-storage.md)
>[Suivant](../key-takeaways.md)</span><span class="sxs-lookup"><span data-stu-id="7e78b-126">[Previous](developer-app-secrets-storage.md)
[Next](../key-takeaways.md)</span></span>
