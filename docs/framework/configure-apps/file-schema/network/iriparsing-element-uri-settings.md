---
title: <iriParsing> Élément (paramètres d’Uri)
ms.date: 03/30/2017
ms.assetid: 953d0b53-445e-41f9-b302-77c4030852ce
ms.openlocfilehash: 710d82b70eb16e88404d4d8bbf38d2d030693103
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59092498"
---
# <a name="iriparsing-element-uri-settings"></a><span data-ttu-id="36c3a-102">\<iriParsing >, élément (paramètres d’Uri)</span><span class="sxs-lookup"><span data-stu-id="36c3a-102">\<iriParsing> Element (Uri Settings)</span></span>
<span data-ttu-id="36c3a-103">Spécifie si l’analyse d’identificateur de ressource internationale (IRI) s’applique à un <xref:System.Uri> et si les règles d’analyse IRI doivent s’appliquer.</span><span class="sxs-lookup"><span data-stu-id="36c3a-103">Specifies if International Resource Identifier (IRI) parsing is applied to a <xref:System.Uri> and whether IRI parsing rules should be applied.</span></span>  
  
## <a name="schema-hierarchy"></a><span data-ttu-id="36c3a-104">Hiérarchie de schéma</span><span class="sxs-lookup"><span data-stu-id="36c3a-104">Schema Hierarchy</span></span>  
 [<span data-ttu-id="36c3a-105">\<configuration > élément</span><span class="sxs-lookup"><span data-stu-id="36c3a-105">\<configuration> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)  
  
 [<span data-ttu-id="36c3a-106">\<URI >, élément (paramètres d’Uri)</span><span class="sxs-lookup"><span data-stu-id="36c3a-106">\<Uri> Element (Uri Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/uri-element-uri-settings.md)  
  
 [<span data-ttu-id="36c3a-107">\<iriParsing></span><span class="sxs-lookup"><span data-stu-id="36c3a-107">\<iriParsing></span></span>](../../../../../docs/framework/configure-apps/file-schema/network/iriparsing-element-uri-settings.md)  
  
## <a name="syntax"></a><span data-ttu-id="36c3a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36c3a-108">Syntax</span></span>  
  
```xml  
<iriParsing  
  enabled="true|false"  
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="36c3a-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="36c3a-109">Attributes and Elements</span></span>  
 <span data-ttu-id="36c3a-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="36c3a-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="36c3a-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="36c3a-111">Attributes</span></span>  
  
|**<span data-ttu-id="36c3a-112">Élément</span><span class="sxs-lookup"><span data-stu-id="36c3a-112">Element</span></span>**|**<span data-ttu-id="36c3a-113">Description</span><span class="sxs-lookup"><span data-stu-id="36c3a-113">Description</span></span>**|  
|-----------------|---------------------|  
|`enabled`|<span data-ttu-id="36c3a-114">Spécifie si l’analyse des IRI est activée.</span><span class="sxs-lookup"><span data-stu-id="36c3a-114">Specifies whether IRI parsing is enabled.</span></span> <span data-ttu-id="36c3a-115">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="36c3a-115">The default value is `false`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="36c3a-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="36c3a-116">Child Elements</span></span>  
 <span data-ttu-id="36c3a-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="36c3a-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="36c3a-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="36c3a-118">Parent Elements</span></span>  
  
|**<span data-ttu-id="36c3a-119">Élément</span><span class="sxs-lookup"><span data-stu-id="36c3a-119">Element</span></span>**|**<span data-ttu-id="36c3a-120">Description</span><span class="sxs-lookup"><span data-stu-id="36c3a-120">Description</span></span>**|  
|-----------------|---------------------|  
|[<span data-ttu-id="36c3a-121">uri</span><span class="sxs-lookup"><span data-stu-id="36c3a-121">uri</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/uri-element-uri-settings.md)|<span data-ttu-id="36c3a-122">Contient des paramètres qui spécifient la façon dont le .NET Framework gère les adresses web exprimées à l’aide d’identificateurs de ressource uniforme (URI).</span><span class="sxs-lookup"><span data-stu-id="36c3a-122">Contains settings that specify how the .NET Framework handles web addresses expressed using uniform resource identifiers (URIs).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="36c3a-123">Notes</span><span class="sxs-lookup"><span data-stu-id="36c3a-123">Remarks</span></span>  
 <span data-ttu-id="36c3a-124">Existant <xref:System.Uri> classe a été étendue dans .NET Framework 3.5.</span><span class="sxs-lookup"><span data-stu-id="36c3a-124">The existing <xref:System.Uri> class has been extended in .NET Framework 3.5.</span></span> <span data-ttu-id="36c3a-125">3.0 SP1 et 2.0 SP1 pour fournir la prise en charge pour les identificateurs IRI (International Resource) et les noms de domaine international (IDN).</span><span class="sxs-lookup"><span data-stu-id="36c3a-125">3.0 SP1, and 2.0 SP1 to provide support for International Resource Identifiers (IRI) and Internationalized Domain Names (IDN).</span></span> <span data-ttu-id="36c3a-126">Les utilisateurs actuels ne verront pas de toute modification du comportement de .NET Framework 2.0, sauf si ils activent spécifiquement les IRI et des IDN prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="36c3a-126">Current users will not see any change from the .NET Framework 2.0 behavior unless they specifically enable IRI and IDN support.</span></span> <span data-ttu-id="36c3a-127">Cela garantit la compatibilité des applications avec les versions antérieures de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="36c3a-127">This ensures application compatibility with prior versions of the .NET Framework.</span></span>  
  
 <span data-ttu-id="36c3a-128">Pour activer la prise en charge des IRI, les deux modifications suivantes sont requises :</span><span class="sxs-lookup"><span data-stu-id="36c3a-128">To enable support for IRI, the following two changes are required:</span></span>  
  
1.  <span data-ttu-id="36c3a-129">Ajoutez la ligne suivante au fichier machine.config sous le répertoire .NET Framework 2.0</span><span class="sxs-lookup"><span data-stu-id="36c3a-129">Add the following line to the machine.config file under the .NET Framework 2.0 directory</span></span>  
  
    ```xml  
    <section name="uri" type="System.Configuration.UriSection, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
    ```  
  
2.  <span data-ttu-id="36c3a-130">Spécifiez si les règles d’analyse des IRI doit être appliquée.</span><span class="sxs-lookup"><span data-stu-id="36c3a-130">Specify whether IRI parsing rules should be applied.</span></span> <span data-ttu-id="36c3a-131">Cela est spécifié dans le fichier machine.config ou app.config.</span><span class="sxs-lookup"><span data-stu-id="36c3a-131">This can be done in the machine.config or in the app.config file.</span></span>  
  
 <span data-ttu-id="36c3a-132">L’activation de l’analyse des IRI (iriParsing activé = `true`) effectue la normalisation et la vérification des caractères selon le IRI les plus récentes des règles dans la RFC 3987.</span><span class="sxs-lookup"><span data-stu-id="36c3a-132">Enabling IRI parsing (iriParsing enabled = `true`) will do normalization and character checking according to the latest IRI rules in RFC 3987.</span></span> <span data-ttu-id="36c3a-133">La valeur par défaut est `false` et permet la normalisation et caractères vérification selon RFC 2396 et RFC 3986 (pour les littéraux IPv6).</span><span class="sxs-lookup"><span data-stu-id="36c3a-133">The default value is `false` and will do normalization and character checking according to RFC 2396 and RFC 3986 (for IPv6 literals).</span></span>  
  
### <a name="configuration-files"></a><span data-ttu-id="36c3a-134">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="36c3a-134">Configuration Files</span></span>  
 <span data-ttu-id="36c3a-135">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="36c3a-135">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="36c3a-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="36c3a-136">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="36c3a-137">Description</span><span class="sxs-lookup"><span data-stu-id="36c3a-137">Description</span></span>  
 <span data-ttu-id="36c3a-138">L’exemple suivant montre une configuration utilisée par la <xref:System.Uri> classe pour prendre en charge l’analyse des IRI et les noms IDN.</span><span class="sxs-lookup"><span data-stu-id="36c3a-138">The following example shows a configuration used by the <xref:System.Uri> class to support IRI parsing and IDN names.</span></span>  
  
### <a name="code"></a><span data-ttu-id="36c3a-139">Code</span><span class="sxs-lookup"><span data-stu-id="36c3a-139">Code</span></span>  
  
```xml  
<configuration>  
  <uri>  
    <idn enabled="All" />  
    <iriParsing enabled="true" />  
  </uri>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="36c3a-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36c3a-140">See also</span></span>

- <xref:System.Configuration.IriParsingElement?displayProperty=nameWithType>
- <xref:System.Configuration.UriSection?displayProperty=nameWithType>
- [<span data-ttu-id="36c3a-141">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="36c3a-141">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
