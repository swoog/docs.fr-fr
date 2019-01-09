---
title: '&lt;add&gt; de &lt;allowAccounts&gt;'
ms.date: 03/30/2017
ms.assetid: 763c7b1f-e7b0-4d99-a42c-4506fcb8da00
ms.openlocfilehash: 443e401e568f4de0432e66c4e03b033f6bfc42f6
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54146171"
---
# <a name="ltaddgt-of-ltallowaccountsgt"></a><span data-ttu-id="11d88-102">&lt;add&gt; de &lt;allowAccounts&gt;</span><span class="sxs-lookup"><span data-stu-id="11d88-102">&lt;add&gt; of &lt;allowAccounts&gt;</span></span>
<span data-ttu-id="11d88-103">Spécifie un compte d’utilisateur pour les processus qui hébergent des services WCF et qui disposent d’accès à la connexion au service de partage.</span><span class="sxs-lookup"><span data-stu-id="11d88-103">Specifies a user account for processes that host WCF services, and are granted connection access to the sharing service.</span></span>  
  
 <span data-ttu-id="11d88-104">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="11d88-104">\<system.serviceModel.activation></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="11d88-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11d88-105">Syntax</span></span>  
  
```xml  
<allowAccounts>
  <add securityIdentifier="String" />
</allowAccounts>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="11d88-106">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="11d88-106">Attributes and Elements</span></span>  
 <span data-ttu-id="11d88-107">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="11d88-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="11d88-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="11d88-108">Attributes</span></span>  
  
|<span data-ttu-id="11d88-109">Attribut</span><span class="sxs-lookup"><span data-stu-id="11d88-109">Attribute</span></span>|<span data-ttu-id="11d88-110">Description</span><span class="sxs-lookup"><span data-stu-id="11d88-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="11d88-111">securityIdentifier</span><span class="sxs-lookup"><span data-stu-id="11d88-111">securityIdentifier</span></span>|<span data-ttu-id="11d88-112">Chaîne indiquant un identificateur unique utilisée pour identifier un compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="11d88-112">A string that specifies a unique identifier used to identify a user account.</span></span> <span data-ttu-id="11d88-113">Les valeurs par défaut sont LocalSystem, Administrateurs, NS, LS et IIS_USRS.</span><span class="sxs-lookup"><span data-stu-id="11d88-113">The default values are LocalSystem, Administrators, NS, LS, and IIS_USRS.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="11d88-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="11d88-114">Child Elements</span></span>  
 <span data-ttu-id="11d88-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="11d88-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="11d88-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="11d88-116">Parent Elements</span></span>  
  
|<span data-ttu-id="11d88-117">Élément</span><span class="sxs-lookup"><span data-stu-id="11d88-117">Element</span></span>|<span data-ttu-id="11d88-118">Description</span><span class="sxs-lookup"><span data-stu-id="11d88-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="11d88-119">\<allowAccounts></span><span class="sxs-lookup"><span data-stu-id="11d88-119">\<allowAccounts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/allowaccounts.md)|<span data-ttu-id="11d88-120">Une collection d’éléments de configuration qui contiennent un `securityIdentifier` attribut pour spécifier les comptes d’utilisateur pour les processus qui hébergent des services WCF et qui disposent d’accès à la connexion au service de partage.</span><span class="sxs-lookup"><span data-stu-id="11d88-120">A collection of configuration elements that contain a `securityIdentifier` attribute to specify user accounts for processes that host WCF services, and are granted connection access to the sharing service.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="11d88-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="11d88-121">Example</span></span>  
 <span data-ttu-id="11d88-122">L’exemple de configuration suivant ajoute à cette collection les cinq identificateurs par défaut correspondant aux comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="11d88-122">The following configuration example adds the five default identifiers for user accounts to this collection.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="11d88-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11d88-123">See Also</span></span>  
 <xref:System.ServiceModel.Activation.Configuration.NetTcpSection.AllowAccounts%2A>  
 <xref:System.ServiceModel.Activation.Configuration.NetPipeSection.AllowAccounts%2A>  
 <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElementCollection>  
 <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElement>
