---
title: <add> de <allowAccounts>
ms.date: 03/30/2017
ms.assetid: 763c7b1f-e7b0-4d99-a42c-4506fcb8da00
ms.openlocfilehash: 1c6764b37b2aa5349b8ccf63e6b7c2bc580b69b9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61701136"
---
# <a name="add-of-allowaccounts"></a><span data-ttu-id="f8840-102">\<add> of \<allowAccounts></span><span class="sxs-lookup"><span data-stu-id="f8840-102">\<add> of \<allowAccounts></span></span>
<span data-ttu-id="f8840-103">Spécifie un compte d’utilisateur pour les processus qui hébergent des services WCF et qui disposent d’accès à la connexion au service de partage.</span><span class="sxs-lookup"><span data-stu-id="f8840-103">Specifies a user account for processes that host WCF services, and are granted connection access to the sharing service.</span></span>  
  
 <span data-ttu-id="f8840-104">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="f8840-104">\<system.serviceModel.activation></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f8840-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8840-105">Syntax</span></span>  
  
```xml  
<allowAccounts>
  <add securityIdentifier="String" />
</allowAccounts>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f8840-106">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="f8840-106">Attributes and Elements</span></span>  
 <span data-ttu-id="f8840-107">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="f8840-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f8840-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="f8840-108">Attributes</span></span>  
  
|<span data-ttu-id="f8840-109">Attribut</span><span class="sxs-lookup"><span data-stu-id="f8840-109">Attribute</span></span>|<span data-ttu-id="f8840-110">Description</span><span class="sxs-lookup"><span data-stu-id="f8840-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f8840-111">securityIdentifier</span><span class="sxs-lookup"><span data-stu-id="f8840-111">securityIdentifier</span></span>|<span data-ttu-id="f8840-112">Chaîne indiquant un identificateur unique utilisée pour identifier un compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f8840-112">A string that specifies a unique identifier used to identify a user account.</span></span> <span data-ttu-id="f8840-113">Les valeurs par défaut sont LocalSystem, Administrateurs, NS, LS et IIS_USRS.</span><span class="sxs-lookup"><span data-stu-id="f8840-113">The default values are LocalSystem, Administrators, NS, LS, and IIS_USRS.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f8840-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f8840-114">Child Elements</span></span>  
 <span data-ttu-id="f8840-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f8840-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f8840-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f8840-116">Parent Elements</span></span>  
  
|<span data-ttu-id="f8840-117">Élément</span><span class="sxs-lookup"><span data-stu-id="f8840-117">Element</span></span>|<span data-ttu-id="f8840-118">Description</span><span class="sxs-lookup"><span data-stu-id="f8840-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f8840-119">\<allowAccounts></span><span class="sxs-lookup"><span data-stu-id="f8840-119">\<allowAccounts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/allowaccounts.md)|<span data-ttu-id="f8840-120">Une collection d’éléments de configuration qui contiennent un `securityIdentifier` attribut pour spécifier les comptes d’utilisateur pour les processus qui hébergent des services WCF et qui disposent d’accès à la connexion au service de partage.</span><span class="sxs-lookup"><span data-stu-id="f8840-120">A collection of configuration elements that contain a `securityIdentifier` attribute to specify user accounts for processes that host WCF services, and are granted connection access to the sharing service.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="f8840-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="f8840-121">Example</span></span>  
 <span data-ttu-id="f8840-122">L’exemple de configuration suivant ajoute à cette collection les cinq identificateurs par défaut correspondant aux comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f8840-122">The following configuration example adds the five default identifiers for user accounts to this collection.</span></span>  
  
```xml  
<allowAccounts>
  <!-- LocalSystem account -->
  <add securityIdentifier="S-1-5-18" />
  <!-- LocalService account -->
  <add securityIdentifier="S-1-5-19" />
  <!-- Administrators account -->
  <add securityIdentifier="S-1-5-20" />
  <!-- Network Service account -->
  <add securityIdentifier="S-1-5-32-544" />
  <!-- IIS_IUSRS account (Vista only) -->
  <add securityIdentifier="S-1-5-32-568" />
</allowAccounts>
```  
  
## <a name="see-also"></a><span data-ttu-id="f8840-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8840-123">See also</span></span>

- <xref:System.ServiceModel.Activation.Configuration.NetTcpSection.AllowAccounts%2A>
- <xref:System.ServiceModel.Activation.Configuration.NetPipeSection.AllowAccounts%2A>
- <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElementCollection>
- <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElement>
