---
title: <remove>
ms.date: 03/30/2017
ms.assetid: 4058e2f1-7db4-4d1a-84dd-1b52836f2ae6
author: BrucePerlerMS
ms.openlocfilehash: 17c4d4289cf90b66d52986c054d4807ecff2b3d8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61793885"
---
# <a name="remove"></a><span data-ttu-id="40743-101">\<remove></span><span class="sxs-lookup"><span data-stu-id="40743-101">\<remove></span></span>
<span data-ttu-id="40743-102">Supprime le Gestionnaire de jetons de sécurité spécifié de la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="40743-102">Removes the specified security token handler from the token handler collection.</span></span>  
  
 <span data-ttu-id="40743-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="40743-103">\<system.identityModel></span></span>  
<span data-ttu-id="40743-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="40743-104">\<identityConfiguration></span></span>  
<span data-ttu-id="40743-105">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="40743-105">\<securityTokenHandlers></span></span>  
<span data-ttu-id="40743-106">\<remove></span><span class="sxs-lookup"><span data-stu-id="40743-106">\<remove></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="40743-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40743-107">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="40743-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="40743-108">Attributes and Elements</span></span>  
 <span data-ttu-id="40743-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="40743-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="40743-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="40743-110">Attributes</span></span>  
  
|<span data-ttu-id="40743-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="40743-111">Attribute</span></span>|<span data-ttu-id="40743-112">Description</span><span class="sxs-lookup"><span data-stu-id="40743-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="40743-113">type</span><span class="sxs-lookup"><span data-stu-id="40743-113">type</span></span>|<span data-ttu-id="40743-114">Le nom de type CLR de gestionnaire de jetons à supprimer.</span><span class="sxs-lookup"><span data-stu-id="40743-114">The CLR type name of the token handler to be removed.</span></span> <span data-ttu-id="40743-115">Pour plus d’informations sur la façon de spécifier le `type` d’attribut, consultez [références de Type personnalisé](https://docs.microsoft.com/previous-versions/windows-identity-foundation/gg638728(v=msdn.10)#custom-type-references).</span><span class="sxs-lookup"><span data-stu-id="40743-115">For more information about how to specify the `type` attribute, see [Custom Type References](https://docs.microsoft.com/previous-versions/windows-identity-foundation/gg638728(v=msdn.10)#custom-type-references).</span></span> <span data-ttu-id="40743-116">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="40743-116">Required.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="40743-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="40743-117">Child Elements</span></span>  
 <span data-ttu-id="40743-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="40743-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="40743-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="40743-119">Parent Elements</span></span>  
  
|<span data-ttu-id="40743-120">Élément</span><span class="sxs-lookup"><span data-stu-id="40743-120">Element</span></span>|<span data-ttu-id="40743-121">Description</span><span class="sxs-lookup"><span data-stu-id="40743-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="40743-122">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="40743-122">\<securityTokenHandlers></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlers.md)|<span data-ttu-id="40743-123">Spécifie une collection de gestionnaires de jetons de sécurité qui sont inscrits avec le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="40743-123">Specifies a collection of security token handlers that are registered with the endpoint.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="40743-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="40743-124">Example</span></span>  
 <span data-ttu-id="40743-125">Le code XML suivant illustre l’utilisation de la `<add>` et `<remove>` éléments pour remplacer le Gestionnaire de jetons de session par défaut par un gestionnaire de jetons de session personnalisée.</span><span class="sxs-lookup"><span data-stu-id="40743-125">The following XML shows the use of the `<add>` and `<remove>` elements to replace the default session token handler with a custom session token handler.</span></span> <span data-ttu-id="40743-126">Le code XML provient de la `ClaimsAwareWebFarm` exemple.</span><span class="sxs-lookup"><span data-stu-id="40743-126">The XML is taken from the `ClaimsAwareWebFarm` sample.</span></span>  
  
```xml  
<securityTokenHandlers>  
  <remove type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
  <add type="System.IdentityModel.Services.Tokens.MachineKeySessionSecurityTokenHandler, System.IdentityModel.Services, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
</securityTokenHandlers>  
```
