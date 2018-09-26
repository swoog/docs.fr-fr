---
title: '&lt;URI&gt; élément (paramètres d’Uri)'
ms.date: 03/30/2017
ms.assetid: c22bab8b-477c-4ae4-8498-65ad409e0847
author: mcleblanc
ms.author: markl
ms.openlocfilehash: a58c27500c0258415c12a5fd8e552b3ee43f50e8
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47108908"
---
# <a name="lturigt-element-uri-settings"></a><span data-ttu-id="d2e06-102">&lt;URI&gt; élément (paramètres d’Uri)</span><span class="sxs-lookup"><span data-stu-id="d2e06-102">&lt;Uri&gt; Element (Uri Settings)</span></span>
<span data-ttu-id="d2e06-103">Contient des paramètres qui spécifient la façon dont le .NET Framework gère les adresses web exprimées à l’aide d’identificateurs de ressource uniforme (URI).</span><span class="sxs-lookup"><span data-stu-id="d2e06-103">Contains settings that specify how the .NET Framework handles web addresses expressed using uniform resource identifiers (URIs).</span></span>  
  
## <a name="schema-hierarchy"></a><span data-ttu-id="d2e06-104">Hiérarchie de schéma</span><span class="sxs-lookup"><span data-stu-id="d2e06-104">Schema Hierarchy</span></span>  
 [<span data-ttu-id="d2e06-105">\<configuration>, élément</span><span class="sxs-lookup"><span data-stu-id="d2e06-105">\<configuration> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)  
  
 [<span data-ttu-id="d2e06-106">\<URI ></span><span class="sxs-lookup"><span data-stu-id="d2e06-106">\<uri></span></span>](../../../../../docs/framework/configure-apps/file-schema/network/uri-element-uri-settings.md)  
  
## <a name="syntax"></a><span data-ttu-id="d2e06-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2e06-107">Syntax</span></span>  
  
```xml  
<uri>  
</uri>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d2e06-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="d2e06-108">Attributes and Elements</span></span>  
 <span data-ttu-id="d2e06-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="d2e06-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d2e06-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="d2e06-110">Attributes</span></span>  
 <span data-ttu-id="d2e06-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d2e06-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="d2e06-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d2e06-112">Child Elements</span></span>  
  
|<span data-ttu-id="d2e06-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="d2e06-113">**Element**</span></span>|<span data-ttu-id="d2e06-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="d2e06-114">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="d2e06-115">IDN</span><span class="sxs-lookup"><span data-stu-id="d2e06-115">idn</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/idn-element-uri-settings.md)|<span data-ttu-id="d2e06-116">Spécifie si l’analyse de nom de domaine international (IDN) s’applique aux noms de domaine.</span><span class="sxs-lookup"><span data-stu-id="d2e06-116">Specifies if Internationalized Domain Name (IDN) parsing is applied to domain names.</span></span>|  
|[<span data-ttu-id="d2e06-117">iriParsing</span><span class="sxs-lookup"><span data-stu-id="d2e06-117">iriParsing</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/iriparsing-element-uri-settings.md)|<span data-ttu-id="d2e06-118">Spécifie si l’analyse de l’identificateur IRI (International Resource) est appliqué à <xref:System.Uri> et si les règles d’analyse IRI doivent être appliquée.</span><span class="sxs-lookup"><span data-stu-id="d2e06-118">Specifies if International Resource Identifier (IRI) parsing is applied to <xref:System.Uri> and whether IRI parsing rules should be applied.</span></span>|  
|[<span data-ttu-id="d2e06-119">schemeSettings</span><span class="sxs-lookup"><span data-stu-id="d2e06-119">schemeSettings</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/schemesettings-element-uri-settings.md)|<span data-ttu-id="d2e06-120">Spécifie la façon dont un <xref:System.Uri> est analysé pour les schémas spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d2e06-120">Specifies how a <xref:System.Uri> will be parsed for specific schemes.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d2e06-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d2e06-121">Parent Elements</span></span>  
  
|<span data-ttu-id="d2e06-122">**Élément**</span><span class="sxs-lookup"><span data-stu-id="d2e06-122">**Element**</span></span>|<span data-ttu-id="d2e06-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="d2e06-123">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="d2e06-124">Configuration</span><span class="sxs-lookup"><span data-stu-id="d2e06-124">configuration</span></span>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)|<span data-ttu-id="d2e06-125">Contient des paramètres pour tous les espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="d2e06-125">Contains settings for all namespaces.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d2e06-126">Notes</span><span class="sxs-lookup"><span data-stu-id="d2e06-126">Remarks</span></span>  
 <span data-ttu-id="d2e06-127">Le `uri` élément contient des paramètres pour les membres de la <xref:System.Uri> classe utilisée par les classes dans le <xref:System.Net> espace de noms.</span><span class="sxs-lookup"><span data-stu-id="d2e06-127">The `uri` element contains settings for members of the <xref:System.Uri> class used by classes in the <xref:System.Net> namespace.</span></span> <span data-ttu-id="d2e06-128">Les paramètres configurent la prise en charge des IRI et des IDN.</span><span class="sxs-lookup"><span data-stu-id="d2e06-128">The settings configure support for IRI and IDN.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d2e06-129">Exemple</span><span class="sxs-lookup"><span data-stu-id="d2e06-129">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="d2e06-130">Description</span><span class="sxs-lookup"><span data-stu-id="d2e06-130">Description</span></span>  
 <span data-ttu-id="d2e06-131">L’exemple suivant montre une configuration utilisée par la <xref:System.Uri> classe pour prendre en charge l’analyse des IRI et les noms IDN.</span><span class="sxs-lookup"><span data-stu-id="d2e06-131">The following example shows a configuration used by the <xref:System.Uri> class to support IRI parsing and IDN names.</span></span> <span data-ttu-id="d2e06-132">L’exemple efface également tous les paramètres de schéma, puis ajoute la prise en charge pour la séquence d’échappement ne pas les délimiteurs de chemin d’encodés en pourcentage pour le schéma http.</span><span class="sxs-lookup"><span data-stu-id="d2e06-132">The example also clears all scheme settings and then adds support for not escaping percent-encoded path delimiters for the http scheme.</span></span>  
  
### <a name="code"></a><span data-ttu-id="d2e06-133">Code</span><span class="sxs-lookup"><span data-stu-id="d2e06-133">Code</span></span>  
  
```xml  
<configuration>  
  <uri>  
    <idn enabled="All" />  
    <iriParsing enabled="true" />  
    <schemeSettings>  
      <clear/>  
      <add name="http" genericUriParserOptions="DontUnescapePathDotsAndSlashes"/>  
    </schemeSettings>  
  </uri>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="d2e06-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2e06-134">See Also</span></span>  
 [<span data-ttu-id="d2e06-135">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="d2e06-135">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
