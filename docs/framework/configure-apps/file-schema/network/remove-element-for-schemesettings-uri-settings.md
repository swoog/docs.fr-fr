---
title: '&lt;supprimer&gt; , élément de schemeSettings (paramètres d’Uri)'
ms.date: 03/30/2017
ms.assetid: 4095ba51-de20-4f87-b562-018abe422c91
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 3f4e3dbdc3dae425e44cd1c0890e8fef9d42a780
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47072720"
---
# <a name="ltremovegt-element-for-schemesettings-uri-settings"></a><span data-ttu-id="d6766-102">&lt;supprimer&gt; , élément de schemeSettings (paramètres d’Uri)</span><span class="sxs-lookup"><span data-stu-id="d6766-102">&lt;remove&gt; Element for schemeSettings (Uri Settings)</span></span>
<span data-ttu-id="d6766-103">Supprime un paramètre de schéma pour un nom de schéma.</span><span class="sxs-lookup"><span data-stu-id="d6766-103">Removes a scheme setting for a scheme name.</span></span>  
  
 <span data-ttu-id="d6766-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="d6766-104">\<configuration></span></span>  
<span data-ttu-id="d6766-105">\<URI ></span><span class="sxs-lookup"><span data-stu-id="d6766-105">\<uri></span></span>  
<span data-ttu-id="d6766-106">\<schemeSettings ></span><span class="sxs-lookup"><span data-stu-id="d6766-106">\<schemeSettings></span></span>  
<span data-ttu-id="d6766-107">\<remove></span><span class="sxs-lookup"><span data-stu-id="d6766-107">\<remove></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d6766-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6766-108">Syntax</span></span>  
  
```xml  
<remove
  name="http|https"
/>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d6766-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="d6766-109">Attributes and Elements</span></span>  
 <span data-ttu-id="d6766-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="d6766-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d6766-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="d6766-111">Attributes</span></span>  
  
|<span data-ttu-id="d6766-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="d6766-112">Attribute</span></span>|<span data-ttu-id="d6766-113">Description</span><span class="sxs-lookup"><span data-stu-id="d6766-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="d6766-114">name</span><span class="sxs-lookup"><span data-stu-id="d6766-114">name</span></span>|<span data-ttu-id="d6766-115">Le nom du schéma pour lequel ce paramètre s’applique.</span><span class="sxs-lookup"><span data-stu-id="d6766-115">The scheme name for which this setting applies.</span></span> <span data-ttu-id="d6766-116">Les seules valeurs prises en charge sont nom = « http » et le nom = « https ».</span><span class="sxs-lookup"><span data-stu-id="d6766-116">The only supported values are name="http" and name="https".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d6766-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d6766-117">Child Elements</span></span>  
 <span data-ttu-id="d6766-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d6766-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="d6766-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d6766-119">Parent Elements</span></span>  
  
|<span data-ttu-id="d6766-120">Élément</span><span class="sxs-lookup"><span data-stu-id="d6766-120">Element</span></span>|<span data-ttu-id="d6766-121">Description</span><span class="sxs-lookup"><span data-stu-id="d6766-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d6766-122">\<schemeSettings, élément (paramètres d’Uri)</span><span class="sxs-lookup"><span data-stu-id="d6766-122">\<schemeSettings> Element (Uri Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/schemesettings-element-uri-settings.md)|<span data-ttu-id="d6766-123">Spécifie la façon dont un <xref:System.Uri> est analysé pour les schémas spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d6766-123">Specifies how a <xref:System.Uri> will be parsed for specific schemes.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d6766-124">Notes</span><span class="sxs-lookup"><span data-stu-id="d6766-124">Remarks</span></span>  
 <span data-ttu-id="d6766-125">Par défaut, le <xref:System.Uri?displayProperty=nameWithType> % n’échappe pas de classe encodé délimiteurs de chemin d’accès avant d’exécuter la compression de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="d6766-125">By default, the <xref:System.Uri?displayProperty=nameWithType> class un-escapes percent encoded path delimiters before executing path compression.</span></span> <span data-ttu-id="d6766-126">Ceci était implémenté comme un mécanisme de sécurité contre les attaques comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6766-126">This was implemented as a security mechanism against attacks like the following:</span></span>  
  
 `http://www.contoso.com/..%2F..%2F/Windows/System32/cmd.exe?/c+dir+c:\`  
  
 <span data-ttu-id="d6766-127">Si cet URI est passé à des modules ne gère ne pas % caractères encodés correctement, cela peut entraîner la commande suivante en cours d’exécution par le serveur :</span><span class="sxs-lookup"><span data-stu-id="d6766-127">If this URI gets passed down to modules not handling percent encoded characters correctly, it could result in the following command being executed by the server:</span></span>  
  
 `c:\Windows\System32\cmd.exe /c dir c:\`  
  
 <span data-ttu-id="d6766-128">Pour cette raison, <xref:System.Uri?displayProperty=nameWithType> première délimiteurs de chemin d’accès n’échappe pas de classe, puis applique la compression de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="d6766-128">For this reason, <xref:System.Uri?displayProperty=nameWithType> class first un-escapes path delimiters and then applies path compression.</span></span> <span data-ttu-id="d6766-129">Le résultat du passage de l’URL malveillante ci-dessus à <xref:System.Uri?displayProperty=nameWithType> classe les résultats de constructeur dans l’URI suivant :</span><span class="sxs-lookup"><span data-stu-id="d6766-129">The result of passing the malicious URL above to <xref:System.Uri?displayProperty=nameWithType> class constructor results in the following URI:</span></span>  
  
 `http://www.microsoft.com/Windows/System32/cmd.exe?/c+dir+c:\`  
  
 <span data-ttu-id="d6766-130">Ce comportement par défaut peut être modifié pour ne pas les délimiteurs de chemin d’accès codé en pourcentage échapper à l’aide de l’option de configuration schemeSettings pour un modèle spécifique.</span><span class="sxs-lookup"><span data-stu-id="d6766-130">This default behavior can be modified to not un-escape percent encoded path delimiters using the schemeSettings configuration option for a specific scheme.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="d6766-131">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="d6766-131">Configuration Files</span></span>  
 <span data-ttu-id="d6766-132">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="d6766-132">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="d6766-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="d6766-133">Example</span></span>  
 <span data-ttu-id="d6766-134">L’exemple suivant montre une configuration utilisée par la <xref:System.Uri> classe qui supprime les paramètres de schéma pour le schéma http.</span><span class="sxs-lookup"><span data-stu-id="d6766-134">The following example shows a configuration used by the <xref:System.Uri> class that removes any scheme settings for the http scheme.</span></span>  
  
```xml  
<configuration>  
  <uri>  
    <schemeSettings>  
      <remove name="http"/>  
    </schemeSettings>  
  </uri>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="d6766-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6766-135">See Also</span></span>  
 <xref:System.Configuration.SchemeSettingElement?displayProperty=nameWithType>  
 <xref:System.Configuration.SchemeSettingElementCollection?displayProperty=nameWithType>  
 <xref:System.Configuration.UriSection?displayProperty=nameWithType>  
 <xref:System.Configuration.UriSection.SchemeSettings%2A?displayProperty=nameWithType>  
 <xref:System.GenericUriParserOptions?displayProperty=nameWithType>  
 <xref:System.Uri?displayProperty=nameWithType>  
 [<span data-ttu-id="d6766-136">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="d6766-136">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
