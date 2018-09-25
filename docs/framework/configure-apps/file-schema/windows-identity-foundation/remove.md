---
title: '&lt;remove&gt;'
ms.date: 03/30/2017
ms.assetid: 4058e2f1-7db4-4d1a-84dd-1b52836f2ae6
author: BrucePerlerMS
ms.openlocfilehash: 410fef1a43f9202d56c4957b1162c53ee056ae3f
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47074912"
---
# <a name="ltremovegt"></a><span data-ttu-id="7ee85-102">&lt;remove&gt;</span><span class="sxs-lookup"><span data-stu-id="7ee85-102">&lt;remove&gt;</span></span>
<span data-ttu-id="7ee85-103">Supprime le Gestionnaire de jetons de sécurité spécifié de la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="7ee85-103">Removes the specified security token handler from the token handler collection.</span></span>  
  
 <span data-ttu-id="7ee85-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="7ee85-104">\<system.identityModel></span></span>  
<span data-ttu-id="7ee85-105">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="7ee85-105">\<identityConfiguration></span></span>  
<span data-ttu-id="7ee85-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="7ee85-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="7ee85-107">\<remove></span><span class="sxs-lookup"><span data-stu-id="7ee85-107">\<remove></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7ee85-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ee85-108">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <remove type=xs:string >  
      </remove>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7ee85-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="7ee85-109">Attributes and Elements</span></span>  
 <span data-ttu-id="7ee85-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="7ee85-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7ee85-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="7ee85-111">Attributes</span></span>  
  
|<span data-ttu-id="7ee85-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="7ee85-112">Attribute</span></span>|<span data-ttu-id="7ee85-113">Description</span><span class="sxs-lookup"><span data-stu-id="7ee85-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="7ee85-114">type</span><span class="sxs-lookup"><span data-stu-id="7ee85-114">type</span></span>|<span data-ttu-id="7ee85-115">Le nom de type CLR de gestionnaire de jetons à supprimer.</span><span class="sxs-lookup"><span data-stu-id="7ee85-115">The CLR type name of the token handler to be removed.</span></span> <span data-ttu-id="7ee85-116">Pour plus d’informations sur la façon de spécifier le `type` d’attribut, consultez [références de Type personnalisé](https://msdn.microsoft.com/library/7286d2e3-c63d-49fd-abdc-ce2705f22c24).</span><span class="sxs-lookup"><span data-stu-id="7ee85-116">For more information about how to specify the `type` attribute, see [Custom Type References](https://msdn.microsoft.com/library/7286d2e3-c63d-49fd-abdc-ce2705f22c24).</span></span> <span data-ttu-id="7ee85-117">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7ee85-117">Required.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7ee85-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7ee85-118">Child Elements</span></span>  
 <span data-ttu-id="7ee85-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7ee85-119">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="7ee85-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="7ee85-120">Parent Elements</span></span>  
  
|<span data-ttu-id="7ee85-121">Élément</span><span class="sxs-lookup"><span data-stu-id="7ee85-121">Element</span></span>|<span data-ttu-id="7ee85-122">Description</span><span class="sxs-lookup"><span data-stu-id="7ee85-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7ee85-123">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="7ee85-123">\<securityTokenHandlers></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlers.md)|<span data-ttu-id="7ee85-124">Spécifie une collection de gestionnaires de jetons de sécurité qui sont inscrits avec le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="7ee85-124">Specifies a collection of security token handlers that are registered with the endpoint.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="7ee85-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="7ee85-125">Example</span></span>  
 <span data-ttu-id="7ee85-126">Le code XML suivant illustre l’utilisation de la `<add>` et `<remove>` éléments pour remplacer le Gestionnaire de jetons de session par défaut par un gestionnaire de jetons de session personnalisée.</span><span class="sxs-lookup"><span data-stu-id="7ee85-126">The following XML shows the use of the `<add>` and `<remove>` elements to replace the default session token handler with a custom session token handler.</span></span> <span data-ttu-id="7ee85-127">Le code XML provient de la `ClaimsAwareWebFarm` exemple.</span><span class="sxs-lookup"><span data-stu-id="7ee85-127">The XML is taken from the `ClaimsAwareWebFarm` sample.</span></span>  
  
```xml  
<securityTokenHandlers>  
  <remove type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
  <add type="System.IdentityModel.Services.Tokens.MachineKeySessionSecurityTokenHandler, System.IdentityModel.Services, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
</securityTokenHandlers>  
```
