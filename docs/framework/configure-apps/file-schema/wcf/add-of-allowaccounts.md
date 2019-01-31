---
title: <add> de <allowAccounts>
ms.date: 03/30/2017
ms.assetid: 763c7b1f-e7b0-4d99-a42c-4506fcb8da00
ms.openlocfilehash: 6edf0bc2d532deb01f24450b9868bbc240bab413
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55259610"
---
# <a name="add-of-allowaccounts"></a><span data-ttu-id="c12e2-102">\<add> of \<allowAccounts></span><span class="sxs-lookup"><span data-stu-id="c12e2-102">\<add> of \<allowAccounts></span></span>
<span data-ttu-id="c12e2-103">Spécifie un compte d’utilisateur pour les processus qui hébergent des services WCF et qui disposent d’accès à la connexion au service de partage.</span><span class="sxs-lookup"><span data-stu-id="c12e2-103">Specifies a user account for processes that host WCF services, and are granted connection access to the sharing service.</span></span>  
  
 <span data-ttu-id="c12e2-104">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="c12e2-104">\<system.serviceModel.activation></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c12e2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c12e2-105">Syntax</span></span>  
  
```xml  
<allowAccounts>
  <add securityIdentifier="String" />
</allowAccounts>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c12e2-106">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="c12e2-106">Attributes and Elements</span></span>  
 <span data-ttu-id="c12e2-107">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="c12e2-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c12e2-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="c12e2-108">Attributes</span></span>  
  
|<span data-ttu-id="c12e2-109">Attribut</span><span class="sxs-lookup"><span data-stu-id="c12e2-109">Attribute</span></span>|<span data-ttu-id="c12e2-110">Description</span><span class="sxs-lookup"><span data-stu-id="c12e2-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c12e2-111">securityIdentifier</span><span class="sxs-lookup"><span data-stu-id="c12e2-111">securityIdentifier</span></span>|<span data-ttu-id="c12e2-112">Chaîne indiquant un identificateur unique utilisée pour identifier un compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c12e2-112">A string that specifies a unique identifier used to identify a user account.</span></span> <span data-ttu-id="c12e2-113">Les valeurs par défaut sont LocalSystem, Administrateurs, NS, LS et IIS_USRS.</span><span class="sxs-lookup"><span data-stu-id="c12e2-113">The default values are LocalSystem, Administrators, NS, LS, and IIS_USRS.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c12e2-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c12e2-114">Child Elements</span></span>  
 <span data-ttu-id="c12e2-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c12e2-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="c12e2-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c12e2-116">Parent Elements</span></span>  
  
|<span data-ttu-id="c12e2-117">Élément</span><span class="sxs-lookup"><span data-stu-id="c12e2-117">Element</span></span>|<span data-ttu-id="c12e2-118">Description</span><span class="sxs-lookup"><span data-stu-id="c12e2-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c12e2-119">\<allowAccounts></span><span class="sxs-lookup"><span data-stu-id="c12e2-119">\<allowAccounts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/allowaccounts.md)|<span data-ttu-id="c12e2-120">Une collection d’éléments de configuration qui contiennent un `securityIdentifier` attribut pour spécifier les comptes d’utilisateur pour les processus qui hébergent des services WCF et qui disposent d’accès à la connexion au service de partage.</span><span class="sxs-lookup"><span data-stu-id="c12e2-120">A collection of configuration elements that contain a `securityIdentifier` attribute to specify user accounts for processes that host WCF services, and are granted connection access to the sharing service.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="c12e2-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="c12e2-121">Example</span></span>  
 <span data-ttu-id="c12e2-122">L’exemple de configuration suivant ajoute à cette collection les cinq identificateurs par défaut correspondant aux comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c12e2-122">The following configuration example adds the five default identifiers for user accounts to this collection.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="c12e2-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c12e2-123">See also</span></span>
- <xref:System.ServiceModel.Activation.Configuration.NetTcpSection.AllowAccounts%2A>
- <xref:System.ServiceModel.Activation.Configuration.NetPipeSection.AllowAccounts%2A>
- <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElementCollection>
- <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElement>
