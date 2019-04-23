---
title: <chunkedCookieHandler>
ms.date: 03/30/2017
ms.assetid: 7220de45-1d14-4aec-a29e-4a2ea8ac861f
author: BrucePerlerMS
ms.openlocfilehash: d9c81d5de7bea343f0d67fa00037763fbae7b8c5
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59120781"
---
# <a name="chunkedcookiehandler"></a><span data-ttu-id="07ba7-101">\<chunkedCookieHandler></span><span class="sxs-lookup"><span data-stu-id="07ba7-101">\<chunkedCookieHandler></span></span>
<span data-ttu-id="07ba7-102">Configure le <xref:System.IdentityModel.Services.ChunkedCookieHandler>.</span><span class="sxs-lookup"><span data-stu-id="07ba7-102">Configures the <xref:System.IdentityModel.Services.ChunkedCookieHandler>.</span></span> <span data-ttu-id="07ba7-103">Cet élément peut uniquement être présent si la `mode` attribut de la `<cookieHandler>` élément est « Default » ou « Mémorisé en bloc ».</span><span class="sxs-lookup"><span data-stu-id="07ba7-103">This element may only be present if the `mode` attribute of the `<cookieHandler>` element is "Default" or "Chunked".</span></span>  
  
 <span data-ttu-id="07ba7-104">\<system.identityModel.services></span><span class="sxs-lookup"><span data-stu-id="07ba7-104">\<system.identityModel.services></span></span>  
<span data-ttu-id="07ba7-105">\<federationConfiguration></span><span class="sxs-lookup"><span data-stu-id="07ba7-105">\<federationConfiguration></span></span>  
<span data-ttu-id="07ba7-106">\<cookieHandler></span><span class="sxs-lookup"><span data-stu-id="07ba7-106">\<cookieHandler></span></span>  
<span data-ttu-id="07ba7-107">\<chunkedCookieHandler></span><span class="sxs-lookup"><span data-stu-id="07ba7-107">\<chunkedCookieHandler></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="07ba7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07ba7-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="07ba7-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="07ba7-109">Attributes and Elements</span></span>  
 <span data-ttu-id="07ba7-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="07ba7-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="07ba7-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="07ba7-111">Attributes</span></span>  
  
|<span data-ttu-id="07ba7-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="07ba7-112">Attribute</span></span>|<span data-ttu-id="07ba7-113">Description</span><span class="sxs-lookup"><span data-stu-id="07ba7-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="07ba7-114">chunkSize</span><span class="sxs-lookup"><span data-stu-id="07ba7-114">chunkSize</span></span>|<span data-ttu-id="07ba7-115">La taille maximale, en caractères, les données de cookie HTTP pour un cookie HTTP.</span><span class="sxs-lookup"><span data-stu-id="07ba7-115">The maximum size, in characters, of the HTTP cookie data for any one HTTP cookie.</span></span> <span data-ttu-id="07ba7-116">Vous devez être prudent lors de l’ajustement de la taille de segment.</span><span class="sxs-lookup"><span data-stu-id="07ba7-116">You must be careful when adjusting the chunk size.</span></span> <span data-ttu-id="07ba7-117">Navigateurs Web présentent des limites différentes sur la taille des cookies et le nombre autorisé par domaine.</span><span class="sxs-lookup"><span data-stu-id="07ba7-117">Web browsers have different limits on the size of cookies and number allowed per domain.</span></span> <span data-ttu-id="07ba7-118">Par exemple, la spécification Netscape d’origine stipulé ces limites : total de 300 cookies, 4096 octets par en-tête de cookie (y compris les métadonnées, pas seulement la valeur du cookie) et 20 cookies par domaine.</span><span class="sxs-lookup"><span data-stu-id="07ba7-118">For example, the original Netscape specification stipulated these limits: 300 cookies total, 4096 bytes per cookie header (including metadata, not just the cookie value), and 20 cookies per domain.</span></span> <span data-ttu-id="07ba7-119">La valeur par défaut est 2000.</span><span class="sxs-lookup"><span data-stu-id="07ba7-119">The default is 2000.</span></span> <span data-ttu-id="07ba7-120">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="07ba7-120">Required.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="07ba7-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="07ba7-121">Child Elements</span></span>  
 <span data-ttu-id="07ba7-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="07ba7-122">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="07ba7-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="07ba7-123">Parent Elements</span></span>  
  
|<span data-ttu-id="07ba7-124">Élément</span><span class="sxs-lookup"><span data-stu-id="07ba7-124">Element</span></span>|<span data-ttu-id="07ba7-125">Description</span><span class="sxs-lookup"><span data-stu-id="07ba7-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="07ba7-126">\<cookieHandler></span><span class="sxs-lookup"><span data-stu-id="07ba7-126">\<cookieHandler></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/cookiehandler.md)|<span data-ttu-id="07ba7-127">Configure le <xref:System.IdentityModel.Services.CookieHandler> qui le <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM) utilise pour lire et écrire des cookies.</span><span class="sxs-lookup"><span data-stu-id="07ba7-127">Configures the <xref:System.IdentityModel.Services.CookieHandler> that the <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM) uses to read and write cookies.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="07ba7-128">Notes</span><span class="sxs-lookup"><span data-stu-id="07ba7-128">Remarks</span></span>  
 <span data-ttu-id="07ba7-129">Lorsque vous spécifiez un <xref:System.IdentityModel.Services.ChunkedCookieHandler> en définissant le `mode` attribut de la `<cookieHandler>` élément à « Default » ou « Chunked », vous pouvez spécifier la taille de segment utilisé par le Gestionnaire de cookie pour lire et écrire des cookies en incluant un `<chunkedCookieHandler>` élément enfant et définition de son `chunkSize` attribut.</span><span class="sxs-lookup"><span data-stu-id="07ba7-129">When you specify a <xref:System.IdentityModel.Services.ChunkedCookieHandler> by setting the `mode` attribute of the `<cookieHandler>` element to "Default" or "Chunked", you can specify the chunk size that the cookie handler uses to read and write cookies by including a `<chunkedCookieHandler>` child element and setting its `chunkSize` attribute.</span></span> <span data-ttu-id="07ba7-130">Si le `<chunkedCookieHandler>` élément n’est pas présent, la taille de segment par défaut de 2 000 octets est utilisée.</span><span class="sxs-lookup"><span data-stu-id="07ba7-130">If the `<chunkedCookieHandler>` element is not present, the default chunk size of 2000 bytes is used.</span></span> <span data-ttu-id="07ba7-131">Cet élément ne peut pas être spécifié lorsque le `mode` attribut a la valeur « Custom ».</span><span class="sxs-lookup"><span data-stu-id="07ba7-131">This element cannot be specified when the `mode` attribute is set to "Custom".</span></span>  
  
 <span data-ttu-id="07ba7-132">Le `<chunkedCookieHandler>` élément est représenté par la <xref:System.IdentityModel.Services.ChunkedCookieHandlerElement> classe.</span><span class="sxs-lookup"><span data-stu-id="07ba7-132">The `<chunkedCookieHandler>` element is represented by the <xref:System.IdentityModel.Services.ChunkedCookieHandlerElement> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="07ba7-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="07ba7-133">Example</span></span>  
 <span data-ttu-id="07ba7-134">L’exemple suivant configure un gestionnaire de cookies mémorisé en bloc qui écrit des cookies en blocs de 3 000 octets.</span><span class="sxs-lookup"><span data-stu-id="07ba7-134">The following example configures a chunked cookie handler that writes cookies in chunks of 3000 bytes.</span></span>  
  
```xml  
<cookieHandler mode="Chunked">  
    <chunkedCookieHandler chunkSize=3000/>  
</cookieHandler>  
```  
  
## <a name="see-also"></a><span data-ttu-id="07ba7-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07ba7-135">See also</span></span>

- <xref:System.IdentityModel.Services.ChunkedCookieHandler>
