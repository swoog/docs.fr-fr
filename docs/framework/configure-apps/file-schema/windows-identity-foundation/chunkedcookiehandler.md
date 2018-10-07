---
title: '&lt;chunkedCookieHandler&gt;'
ms.date: 03/30/2017
ms.assetid: 7220de45-1d14-4aec-a29e-4a2ea8ac861f
author: BrucePerlerMS
ms.openlocfilehash: f5592e0fd02d34b2882182196e0aa9425672a8fe
ms.sourcegitcommit: 586dbdcaef9767642436b1e4efbe88fb15473d6f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/06/2018
ms.locfileid: "48838297"
---
# <a name="ltchunkedcookiehandlergt"></a><span data-ttu-id="8c1cf-102">&lt;chunkedCookieHandler&gt;</span><span class="sxs-lookup"><span data-stu-id="8c1cf-102">&lt;chunkedCookieHandler&gt;</span></span>
<span data-ttu-id="8c1cf-103">Configure le <xref:System.IdentityModel.Services.ChunkedCookieHandler>.</span><span class="sxs-lookup"><span data-stu-id="8c1cf-103">Configures the <xref:System.IdentityModel.Services.ChunkedCookieHandler>.</span></span> <span data-ttu-id="8c1cf-104">Cet élément peut uniquement être présent si la `mode` attribut de la `<cookieHandler>` élément est « Default » ou « Mémorisé en bloc ».</span><span class="sxs-lookup"><span data-stu-id="8c1cf-104">This element may only be present if the `mode` attribute of the `<cookieHandler>` element is "Default" or "Chunked".</span></span>  
  
 <span data-ttu-id="8c1cf-105">\<system.identityModel.services ></span><span class="sxs-lookup"><span data-stu-id="8c1cf-105">\<system.identityModel.services></span></span>  
<span data-ttu-id="8c1cf-106">\<federationConfiguration ></span><span class="sxs-lookup"><span data-stu-id="8c1cf-106">\<federationConfiguration></span></span>  
<span data-ttu-id="8c1cf-107">\<cookieHandler ></span><span class="sxs-lookup"><span data-stu-id="8c1cf-107">\<cookieHandler></span></span>  
<span data-ttu-id="8c1cf-108">\<chunkedCookieHandler ></span><span class="sxs-lookup"><span data-stu-id="8c1cf-108">\<chunkedCookieHandler></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8c1cf-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c1cf-109">Syntax</span></span>  
  
```xml  
<system.identityModel.services>  
  <federationConfiguration>  
    <cookieHandler mode="Chunked||Default" >  
      <chunkedCookieHandler size=xs:int >  
      </chunkedCookieHandler>  
    </cookieHandler>  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8c1cf-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="8c1cf-110">Attributes and Elements</span></span>  
 <span data-ttu-id="8c1cf-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="8c1cf-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8c1cf-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="8c1cf-112">Attributes</span></span>  
  
|<span data-ttu-id="8c1cf-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="8c1cf-113">Attribute</span></span>|<span data-ttu-id="8c1cf-114">Description</span><span class="sxs-lookup"><span data-stu-id="8c1cf-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="8c1cf-115">Taille du segment</span><span class="sxs-lookup"><span data-stu-id="8c1cf-115">chunkSize</span></span>|<span data-ttu-id="8c1cf-116">La taille maximale, en caractères, les données de cookie HTTP pour un cookie HTTP.</span><span class="sxs-lookup"><span data-stu-id="8c1cf-116">The maximum size, in characters, of the HTTP cookie data for any one HTTP cookie.</span></span> <span data-ttu-id="8c1cf-117">Vous devez être prudent lors de l’ajustement de la taille de segment.</span><span class="sxs-lookup"><span data-stu-id="8c1cf-117">You must be careful when adjusting the chunk size.</span></span> <span data-ttu-id="8c1cf-118">Navigateurs Web présentent des limites différentes sur la taille des cookies et le nombre autorisé par domaine.</span><span class="sxs-lookup"><span data-stu-id="8c1cf-118">Web browsers have different limits on the size of cookies and number allowed per domain.</span></span> <span data-ttu-id="8c1cf-119">Par exemple, la spécification Netscape d’origine stipulé ces limites : total de 300 cookies, 4096 octets par en-tête de cookie (y compris les métadonnées, pas seulement la valeur du cookie) et 20 cookies par domaine.</span><span class="sxs-lookup"><span data-stu-id="8c1cf-119">For example, the original Netscape specification stipulated these limits: 300 cookies total, 4096 bytes per cookie header (including metadata, not just the cookie value), and 20 cookies per domain.</span></span> <span data-ttu-id="8c1cf-120">La valeur par défaut est 2000.</span><span class="sxs-lookup"><span data-stu-id="8c1cf-120">The default is 2000.</span></span> <span data-ttu-id="8c1cf-121">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8c1cf-121">Required.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="8c1cf-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8c1cf-122">Child Elements</span></span>  
 <span data-ttu-id="8c1cf-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="8c1cf-123">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="8c1cf-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="8c1cf-124">Parent Elements</span></span>  
  
|<span data-ttu-id="8c1cf-125">Élément</span><span class="sxs-lookup"><span data-stu-id="8c1cf-125">Element</span></span>|<span data-ttu-id="8c1cf-126">Description</span><span class="sxs-lookup"><span data-stu-id="8c1cf-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8c1cf-127">\<cookieHandler ></span><span class="sxs-lookup"><span data-stu-id="8c1cf-127">\<cookieHandler></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/cookiehandler.md)|<span data-ttu-id="8c1cf-128">Configure le <xref:System.IdentityModel.Services.CookieHandler> qui le <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM) utilise pour lire et écrire des cookies.</span><span class="sxs-lookup"><span data-stu-id="8c1cf-128">Configures the <xref:System.IdentityModel.Services.CookieHandler> that the <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM) uses to read and write cookies.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8c1cf-129">Notes</span><span class="sxs-lookup"><span data-stu-id="8c1cf-129">Remarks</span></span>  
 <span data-ttu-id="8c1cf-130">Lorsque vous spécifiez un <xref:System.IdentityModel.Services.ChunkedCookieHandler> en définissant le `mode` attribut de la `<cookieHandler>` élément à « Default » ou « Chunked », vous pouvez spécifier la taille de segment utilisé par le Gestionnaire de cookie pour lire et écrire des cookies en incluant un `<chunkedCookieHandler>` élément enfant et définition de son `chunkSize` attribut.</span><span class="sxs-lookup"><span data-stu-id="8c1cf-130">When you specify a <xref:System.IdentityModel.Services.ChunkedCookieHandler> by setting the `mode` attribute of the `<cookieHandler>` element to "Default" or "Chunked", you can specify the chunk size that the cookie handler uses to read and write cookies by including a `<chunkedCookieHandler>` child element and setting its `chunkSize` attribute.</span></span> <span data-ttu-id="8c1cf-131">Si le `<chunkedCookieHandler>` élément n’est pas présent, la taille de segment par défaut de 2 000 octets est utilisée.</span><span class="sxs-lookup"><span data-stu-id="8c1cf-131">If the `<chunkedCookieHandler>` element is not present, the default chunk size of 2000 bytes is used.</span></span> <span data-ttu-id="8c1cf-132">Cet élément ne peut pas être spécifié lorsque le `mode` attribut a la valeur « Custom ».</span><span class="sxs-lookup"><span data-stu-id="8c1cf-132">This element cannot be specified when the `mode` attribute is set to "Custom".</span></span>  
  
 <span data-ttu-id="8c1cf-133">Le `<chunkedCookieHandler>` élément est représenté par la <xref:System.IdentityModel.Services.ChunkedCookieHandlerElement> classe.</span><span class="sxs-lookup"><span data-stu-id="8c1cf-133">The `<chunkedCookieHandler>` element is represented by the <xref:System.IdentityModel.Services.ChunkedCookieHandlerElement> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8c1cf-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="8c1cf-134">Example</span></span>  
 <span data-ttu-id="8c1cf-135">L’exemple suivant configure un gestionnaire de cookies mémorisé en bloc qui écrit des cookies en blocs de 3 000 octets.</span><span class="sxs-lookup"><span data-stu-id="8c1cf-135">The following example configures a chunked cookie handler that writes cookies in chunks of 3000 bytes.</span></span>  
  
```xml  
<cookieHandler mode="Chunked">  
    <chunkedCookieHandler chunkSize=3000/>  
</cookieHandler>  
```  
  
## <a name="see-also"></a><span data-ttu-id="8c1cf-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c1cf-136">See Also</span></span>  
 <xref:System.IdentityModel.Services.ChunkedCookieHandler>
