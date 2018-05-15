---
title: '&lt;schemeSettings&gt; élément (paramètres d’Uri)'
ms.date: 03/30/2017
ms.assetid: 0ae45c6e-8c4c-4c0d-8b9f-a93824648890
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: 40ff62a48a3ba1f4a9b5aed28630ab70d37869fc
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltschemesettingsgt-element-uri-settings"></a><span data-ttu-id="38e0f-102">&lt;schemeSettings&gt; élément (paramètres d’Uri)</span><span class="sxs-lookup"><span data-stu-id="38e0f-102">&lt;schemeSettings&gt; Element (Uri Settings)</span></span>
<span data-ttu-id="38e0f-103">Spécifie la façon dont un <xref:System.Uri> est analysé pour les schémas spécifiques.</span><span class="sxs-lookup"><span data-stu-id="38e0f-103">Specifies how a <xref:System.Uri> will be parsed for specific schemes.</span></span>  
  
 <span data-ttu-id="38e0f-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="38e0f-104">\<configuration></span></span>  
<span data-ttu-id="38e0f-105">\<URI ></span><span class="sxs-lookup"><span data-stu-id="38e0f-105">\<uri></span></span>  
<span data-ttu-id="38e0f-106">\<schemeSettings ></span><span class="sxs-lookup"><span data-stu-id="38e0f-106">\<schemeSettings></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="38e0f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38e0f-107">Syntax</span></span>  
  
```xml  
<schemeSettings>   
</schemeSettings>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="38e0f-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="38e0f-108">Attributes and Elements</span></span>  
 <span data-ttu-id="38e0f-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="38e0f-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="38e0f-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="38e0f-110">Attributes</span></span>  
 <span data-ttu-id="38e0f-111">Aucun</span><span class="sxs-lookup"><span data-stu-id="38e0f-111">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="38e0f-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="38e0f-112">Child Elements</span></span>  
  
|<span data-ttu-id="38e0f-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="38e0f-113">**Element**</span></span>|<span data-ttu-id="38e0f-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="38e0f-114">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="38e0f-115">add</span><span class="sxs-lookup"><span data-stu-id="38e0f-115">add</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/add-element-for-schemesettings-uri-settings.md)|<span data-ttu-id="38e0f-116">Ajoute un paramètre de schéma pour un nom de schéma.</span><span class="sxs-lookup"><span data-stu-id="38e0f-116">Adds a scheme setting for a scheme name.</span></span>|  
|[<span data-ttu-id="38e0f-117">clear</span><span class="sxs-lookup"><span data-stu-id="38e0f-117">clear</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/clear-element-for-schemesettings-uri-settings.md)|<span data-ttu-id="38e0f-118">Efface tous les paramètres de modèle existant.</span><span class="sxs-lookup"><span data-stu-id="38e0f-118">Clears all existing scheme settings.</span></span>|  
|[<span data-ttu-id="38e0f-119">remove</span><span class="sxs-lookup"><span data-stu-id="38e0f-119">remove</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/remove-element-for-schemesettings-uri-settings.md)|<span data-ttu-id="38e0f-120">Supprime un paramètre de schéma pour un nom de schéma.</span><span class="sxs-lookup"><span data-stu-id="38e0f-120">Removes a scheme setting for a scheme name.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="38e0f-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="38e0f-121">Parent Elements</span></span>  
  
|<span data-ttu-id="38e0f-122">**Élément**</span><span class="sxs-lookup"><span data-stu-id="38e0f-122">**Element**</span></span>|<span data-ttu-id="38e0f-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="38e0f-123">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="38e0f-124">URI</span><span class="sxs-lookup"><span data-stu-id="38e0f-124">uri</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/uri-element-uri-settings.md)|<span data-ttu-id="38e0f-125">Contient des paramètres qui spécifient la façon dont le .NET Framework gère les adresses web exprimées à l’aide d’identificateurs de ressource uniforme (URI).</span><span class="sxs-lookup"><span data-stu-id="38e0f-125">Contains settings that specify how the .NET Framework handles web addresses expressed using uniform resource identifiers (URIs).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="38e0f-126">Notes</span><span class="sxs-lookup"><span data-stu-id="38e0f-126">Remarks</span></span>  
 <span data-ttu-id="38e0f-127">Par défaut, le <xref:System.Uri?displayProperty=nameWithType> pour cent de classe n’échappe pas encodée séparateurs de chemin d’accès avant d’exécuter la compression de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="38e0f-127">By default, the <xref:System.Uri?displayProperty=nameWithType> class un-escapes percent encoded path delimiters before executing path compression.</span></span> <span data-ttu-id="38e0f-128">Cela a été implémenté en tant que mécanisme de sécurité contre les attaques comme suit :</span><span class="sxs-lookup"><span data-stu-id="38e0f-128">This was implemented as a security mechanism against attacks like the following:</span></span>  
  
 `http://www.contoso.com/..%2F..%2F/Windows/System32/cmd.exe?/c+dir+c:\`  
  
 <span data-ttu-id="38e0f-129">Si cet URI est passé à des modules ne gère ne pas % correctement les caractères encodés, elle peut entraîner la commande suivante, exécutée par le serveur :</span><span class="sxs-lookup"><span data-stu-id="38e0f-129">If this URI gets passed down to modules not handling percent encoded characters correctly, it could result in the following command being executed by the server:</span></span>  
  
 `c:\Windows\System32\cmd.exe /c dir c:\`  
  
 <span data-ttu-id="38e0f-130">Pour cette raison, <xref:System.Uri?displayProperty=nameWithType> première séparateurs de chemin d’accès n’échappe pas de classe, puis applique la compression de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="38e0f-130">For this reason, <xref:System.Uri?displayProperty=nameWithType> class first un-escapes path delimiters and then applies path compression.</span></span> <span data-ttu-id="38e0f-131">Le résultat du passage de l’URL malveillante ci-dessus pour <xref:System.Uri?displayProperty=nameWithType> classe constructeur se traduit par l’URI suivant :</span><span class="sxs-lookup"><span data-stu-id="38e0f-131">The result of passing the malicious URL above to <xref:System.Uri?displayProperty=nameWithType> class constructor results in the following URI:</span></span>  
  
 `http://www.microsoft.com/Windows/System32/cmd.exe?/c+dir+c:\`  
  
 <span data-ttu-id="38e0f-132">Ce comportement par défaut peut être modifié pour ne pas les délimiteurs de chemin d’accès codé en pourcentage échapper à l’aide de l’option de configuration schemeSettings pour un modèle spécifique.</span><span class="sxs-lookup"><span data-stu-id="38e0f-132">This default behavior can be modified to not un-escape percent encoded path delimiters using the schemeSettings configuration option for a specific scheme.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="38e0f-133">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="38e0f-133">Configuration Files</span></span>  
 <span data-ttu-id="38e0f-134">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="38e0f-134">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="38e0f-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="38e0f-135">Example</span></span>  
 <span data-ttu-id="38e0f-136">L’exemple suivant montre une configuration utilisée par la <xref:System.Uri> classe pour prendre en charge l’échappement ne pas les séparateurs de chemin d’accès encodés en pourcentage pour le schéma http.</span><span class="sxs-lookup"><span data-stu-id="38e0f-136">The following example shows a configuration used by the <xref:System.Uri> class to support not escaping percent-encoded path delimiters for the http scheme.</span></span>  
  
```xml  
<configuration>  
  <uri>  
    <schemeSettings>  
      <add name="http" genericUriParserOptions="DontUnescapePathDotsAndSlashes"/>  
    </schemeSettings>  
  </uri>  
</configuration>  
```  
  
## <a name="element-information"></a><span data-ttu-id="38e0f-137">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="38e0f-137">Element Information</span></span>  
  
|||
|-|-|  
|<span data-ttu-id="38e0f-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="38e0f-138">Namespace</span></span>|<span data-ttu-id="38e0f-139">Système</span><span class="sxs-lookup"><span data-stu-id="38e0f-139">System</span></span>|  
|<span data-ttu-id="38e0f-140">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="38e0f-140">Schema Name</span></span>||  
|<span data-ttu-id="38e0f-141">Fichier de validation</span><span class="sxs-lookup"><span data-stu-id="38e0f-141">Validation File</span></span>||  
|<span data-ttu-id="38e0f-142">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="38e0f-142">Can be Empty</span></span>||  
  
## <a name="see-also"></a><span data-ttu-id="38e0f-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38e0f-143">See Also</span></span>  
 <xref:System.Configuration.SchemeSettingElement?displayProperty=nameWithType>  
 <xref:System.Configuration.SchemeSettingElementCollection?displayProperty=nameWithType>  
 <xref:System.Configuration.UriSection?displayProperty=nameWithType>  
 <xref:System.Configuration.UriSection.SchemeSettings%2A?displayProperty=nameWithType>  
 <xref:System.GenericUriParserOptions?displayProperty=nameWithType>  
 <xref:System.Uri?displayProperty=nameWithType>  
 [<span data-ttu-id="38e0f-144">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="38e0f-144">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
