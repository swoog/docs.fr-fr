---
title: '&lt;customCookieHandler&gt;'
ms.date: 03/30/2017
ms.assetid: a03b153d-5ec6-4915-9031-6f0c3fd348be
author: BrucePerlerMS
ms.openlocfilehash: 51ca91de5c77727f5f5506118461d19354f12c14
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47081589"
---
# <a name="ltcustomcookiehandlergt"></a><span data-ttu-id="e98f8-102">&lt;customCookieHandler&gt;</span><span class="sxs-lookup"><span data-stu-id="e98f8-102">&lt;customCookieHandler&gt;</span></span>
<span data-ttu-id="e98f8-103">Définit le type de gestionnaire de cookie personnalisé.</span><span class="sxs-lookup"><span data-stu-id="e98f8-103">Sets the custom cookie handler type.</span></span> <span data-ttu-id="e98f8-104">Cet élément peut uniquement être présent si la `mode` attribut de la `<cookieHandler>` élément est « Custom ».</span><span class="sxs-lookup"><span data-stu-id="e98f8-104">This element may only be present if the `mode` attribute of the `<cookieHandler>` element is "Custom".</span></span> <span data-ttu-id="e98f8-105">Le type personnalisé doit être dérivé du <xref:System.IdentityModel.Services.CookieHandler> classe.</span><span class="sxs-lookup"><span data-stu-id="e98f8-105">The custom type must be derived from the <xref:System.IdentityModel.Services.CookieHandler> class.</span></span>  
  
 <span data-ttu-id="e98f8-106">\<system.identityModel.services ></span><span class="sxs-lookup"><span data-stu-id="e98f8-106">\<system.identityModel.services></span></span>  
<span data-ttu-id="e98f8-107">\<federationConfiguration ></span><span class="sxs-lookup"><span data-stu-id="e98f8-107">\<federationConfiguration></span></span>  
<span data-ttu-id="e98f8-108">\<cookieHandler ></span><span class="sxs-lookup"><span data-stu-id="e98f8-108">\<cookieHandler></span></span>  
<span data-ttu-id="e98f8-109">\<customCookieHandler ></span><span class="sxs-lookup"><span data-stu-id="e98f8-109">\<customCookieHandler></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e98f8-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e98f8-110">Syntax</span></span>  
  
```xml  
<system.identityModel.services>  
  <federationConfiguration>  
    <cookieHandler mode="Custom">  
      <customCookieHandler type="MyNamespace.MyCustomCookieHandler, MyAssembly" >  
      </customCookieHandler>  
    </cookieHandler>  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e98f8-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="e98f8-111">Attributes and Elements</span></span>  
 <span data-ttu-id="e98f8-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="e98f8-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e98f8-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="e98f8-113">Attributes</span></span>  
  
|<span data-ttu-id="e98f8-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="e98f8-114">Attribute</span></span>|<span data-ttu-id="e98f8-115">Description</span><span class="sxs-lookup"><span data-stu-id="e98f8-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e98f8-116">type</span><span class="sxs-lookup"><span data-stu-id="e98f8-116">type</span></span>|<span data-ttu-id="e98f8-117">Spécifie un type personnalisé qui dérive de la <xref:System.IdentityModel.Services.CookieHandler> classe.</span><span class="sxs-lookup"><span data-stu-id="e98f8-117">Specifies a custom type that derives from the <xref:System.IdentityModel.Services.CookieHandler> class.</span></span> <span data-ttu-id="e98f8-118">Pour plus d’informations sur la façon de spécifier le `type` d’attribut, consultez [références de Type personnalisé](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span><span class="sxs-lookup"><span data-stu-id="e98f8-118">For more information about how to specify the `type` attribute, see [Custom Type References](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e98f8-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e98f8-119">Child Elements</span></span>  
 <span data-ttu-id="e98f8-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e98f8-120">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="e98f8-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e98f8-121">Parent Elements</span></span>  
  
|<span data-ttu-id="e98f8-122">Élément</span><span class="sxs-lookup"><span data-stu-id="e98f8-122">Element</span></span>|<span data-ttu-id="e98f8-123">Description</span><span class="sxs-lookup"><span data-stu-id="e98f8-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e98f8-124">\<cookieHandler ></span><span class="sxs-lookup"><span data-stu-id="e98f8-124">\<cookieHandler></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/cookiehandler.md)|<span data-ttu-id="e98f8-125">Configure le <xref:System.IdentityModel.Services.CookieHandler> qui le <xref:System.IdentityModel.Services.SessionAuthenticationModule> utilise pour lire et écrire des cookies.</span><span class="sxs-lookup"><span data-stu-id="e98f8-125">Configures the <xref:System.IdentityModel.Services.CookieHandler> that the <xref:System.IdentityModel.Services.SessionAuthenticationModule> uses to read and write cookies.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e98f8-126">Notes</span><span class="sxs-lookup"><span data-stu-id="e98f8-126">Remarks</span></span>  
 <span data-ttu-id="e98f8-127">Lorsque vous spécifiez un gestionnaire de cookie personnalisé en définissant le `mode` attribut de la `<cookieHandler>` élément « Personnalisé », vous devez spécifier le type du Gestionnaire de cookie personnalisé en incluant un `<customCookieHandler>` élément enfant qui fait référence au type de gestionnaire de cookie.</span><span class="sxs-lookup"><span data-stu-id="e98f8-127">When you specify a custom cookie handler by setting the `mode` attribute of the `<cookieHandler>` element to "Custom", you must specify the type of the custom cookie handler by including a `<customCookieHandler>` child element that references the cookie handler type.</span></span> <span data-ttu-id="e98f8-128">Cet élément ne peut pas être spécifié lorsque le `mode` attribut a la valeur « Chunked » ou « Default ».</span><span class="sxs-lookup"><span data-stu-id="e98f8-128">This element cannot be specified when the `mode` attribute is set to "Chunked" or "Default".</span></span> <span data-ttu-id="e98f8-129">Gestionnaires de cookie personnalisé doivent dériver de la <xref:System.IdentityModel.Services.CookieHandler> classe.</span><span class="sxs-lookup"><span data-stu-id="e98f8-129">Custom cookie handlers must derive from the <xref:System.IdentityModel.Services.CookieHandler> class.</span></span>  
  
 <span data-ttu-id="e98f8-130">Le `<customCookieHandler>` élément est représenté par la <xref:System.IdentityModel.Configuration.CustomTypeElement> classe.</span><span class="sxs-lookup"><span data-stu-id="e98f8-130">The `<customCookieHandler>` element is represented by the <xref:System.IdentityModel.Configuration.CustomTypeElement> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e98f8-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="e98f8-131">Example</span></span>  
 <span data-ttu-id="e98f8-132">L’exemple suivant configure le module SAM pour utiliser un gestionnaire de cookie personnalisé de type `MyNamespace.MyCustomCookieHandler`.</span><span class="sxs-lookup"><span data-stu-id="e98f8-132">The following example configures the SAM to use a custom cookie handler of type `MyNamespace.MyCustomCookieHandler`.</span></span>  
  
```xml  
<cookieHandler mode="Custom">  
    <customCookieHandler type="MyNamespace.MyCustomCookieHandler, MyAssembly" />  
</cookieHandler>  
```  
  
## <a name="see-also"></a><span data-ttu-id="e98f8-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e98f8-133">See Also</span></span>  
 <xref:System.IdentityModel.Services.CookieHandler>
