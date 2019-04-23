---
title: <remove>, élément de schemeSettings (paramètres d’URI)
ms.date: 03/30/2017
ms.assetid: 4095ba51-de20-4f87-b562-018abe422c91
ms.openlocfilehash: f29ee86deaa150324b40f4fac12ead152553e50d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59104973"
---
# <a name="remove-element-for-schemesettings-uri-settings"></a><span data-ttu-id="5ee2a-102">\<Supprimer >, élément de schemeSettings (paramètres d’Uri)</span><span class="sxs-lookup"><span data-stu-id="5ee2a-102">\<remove> Element for schemeSettings (Uri Settings)</span></span>
<span data-ttu-id="5ee2a-103">Supprime un paramètre de schéma pour un nom de schéma.</span><span class="sxs-lookup"><span data-stu-id="5ee2a-103">Removes a scheme setting for a scheme name.</span></span>  
  
 <span data-ttu-id="5ee2a-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="5ee2a-104">\<configuration></span></span>  
<span data-ttu-id="5ee2a-105">\<uri></span><span class="sxs-lookup"><span data-stu-id="5ee2a-105">\<uri></span></span>  
<span data-ttu-id="5ee2a-106">\<schemeSettings></span><span class="sxs-lookup"><span data-stu-id="5ee2a-106">\<schemeSettings></span></span>  
<span data-ttu-id="5ee2a-107">\<remove></span><span class="sxs-lookup"><span data-stu-id="5ee2a-107">\<remove></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5ee2a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ee2a-108">Syntax</span></span>  
  
```xml  
<remove
  name="http|https"
/>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5ee2a-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="5ee2a-109">Attributes and Elements</span></span>  
 <span data-ttu-id="5ee2a-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="5ee2a-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5ee2a-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="5ee2a-111">Attributes</span></span>  
  
|<span data-ttu-id="5ee2a-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="5ee2a-112">Attribute</span></span>|<span data-ttu-id="5ee2a-113">Description</span><span class="sxs-lookup"><span data-stu-id="5ee2a-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5ee2a-114">name</span><span class="sxs-lookup"><span data-stu-id="5ee2a-114">name</span></span>|<span data-ttu-id="5ee2a-115">Le nom du schéma pour lequel ce paramètre s’applique.</span><span class="sxs-lookup"><span data-stu-id="5ee2a-115">The scheme name for which this setting applies.</span></span> <span data-ttu-id="5ee2a-116">Les seules valeurs prises en charge sont nom = « http » et le nom = « https ».</span><span class="sxs-lookup"><span data-stu-id="5ee2a-116">The only supported values are name="http" and name="https".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5ee2a-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5ee2a-117">Child Elements</span></span>  
 <span data-ttu-id="5ee2a-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="5ee2a-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5ee2a-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5ee2a-119">Parent Elements</span></span>  
  
|<span data-ttu-id="5ee2a-120">Élément</span><span class="sxs-lookup"><span data-stu-id="5ee2a-120">Element</span></span>|<span data-ttu-id="5ee2a-121">Description</span><span class="sxs-lookup"><span data-stu-id="5ee2a-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5ee2a-122">\<schemeSettings, élément (paramètres d’Uri)</span><span class="sxs-lookup"><span data-stu-id="5ee2a-122">\<schemeSettings> Element (Uri Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/schemesettings-element-uri-settings.md)|<span data-ttu-id="5ee2a-123">Spécifie la façon dont un <xref:System.Uri> est analysé pour les schémas spécifiques.</span><span class="sxs-lookup"><span data-stu-id="5ee2a-123">Specifies how a <xref:System.Uri> will be parsed for specific schemes.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5ee2a-124">Notes</span><span class="sxs-lookup"><span data-stu-id="5ee2a-124">Remarks</span></span>  
 <span data-ttu-id="5ee2a-125">Par défaut, le <xref:System.Uri?displayProperty=nameWithType> % n’échappe pas de classe encodé délimiteurs de chemin d’accès avant d’exécuter la compression de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="5ee2a-125">By default, the <xref:System.Uri?displayProperty=nameWithType> class un-escapes percent encoded path delimiters before executing path compression.</span></span> <span data-ttu-id="5ee2a-126">Ceci était implémenté comme un mécanisme de sécurité contre les attaques comme suit :</span><span class="sxs-lookup"><span data-stu-id="5ee2a-126">This was implemented as a security mechanism against attacks like the following:</span></span>  
  
 `http://www.contoso.com/..%2F..%2F/Windows/System32/cmd.exe?/c+dir+c:\`  
  
 <span data-ttu-id="5ee2a-127">Si cet URI est passé à des modules ne gère ne pas % caractères encodés correctement, cela peut entraîner la commande suivante en cours d’exécution par le serveur :</span><span class="sxs-lookup"><span data-stu-id="5ee2a-127">If this URI gets passed down to modules not handling percent encoded characters correctly, it could result in the following command being executed by the server:</span></span>  
  
 `c:\Windows\System32\cmd.exe /c dir c:\`  
  
 <span data-ttu-id="5ee2a-128">Pour cette raison, <xref:System.Uri?displayProperty=nameWithType> première délimiteurs de chemin d’accès n’échappe pas de classe, puis applique la compression de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="5ee2a-128">For this reason, <xref:System.Uri?displayProperty=nameWithType> class first un-escapes path delimiters and then applies path compression.</span></span> <span data-ttu-id="5ee2a-129">Le résultat du passage de l’URL malveillante ci-dessus à <xref:System.Uri?displayProperty=nameWithType> classe les résultats de constructeur dans l’URI suivant :</span><span class="sxs-lookup"><span data-stu-id="5ee2a-129">The result of passing the malicious URL above to <xref:System.Uri?displayProperty=nameWithType> class constructor results in the following URI:</span></span>  
  
 `http://www.microsoft.com/Windows/System32/cmd.exe?/c+dir+c:\`  
  
 <span data-ttu-id="5ee2a-130">Ce comportement par défaut peut être modifié pour ne pas les délimiteurs de chemin d’accès codé en pourcentage échapper à l’aide de l’option de configuration schemeSettings pour un modèle spécifique.</span><span class="sxs-lookup"><span data-stu-id="5ee2a-130">This default behavior can be modified to not un-escape percent encoded path delimiters using the schemeSettings configuration option for a specific scheme.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="5ee2a-131">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="5ee2a-131">Configuration Files</span></span>  
 <span data-ttu-id="5ee2a-132">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="5ee2a-132">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="5ee2a-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="5ee2a-133">Example</span></span>  
 <span data-ttu-id="5ee2a-134">L’exemple suivant montre une configuration utilisée par la <xref:System.Uri> classe qui supprime les paramètres de schéma pour le schéma http.</span><span class="sxs-lookup"><span data-stu-id="5ee2a-134">The following example shows a configuration used by the <xref:System.Uri> class that removes any scheme settings for the http scheme.</span></span>  
  
```xml  
<configuration>  
  <uri>  
    <schemeSettings>  
      <remove name="http"/>  
    </schemeSettings>  
  </uri>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="5ee2a-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ee2a-135">See also</span></span>

- <xref:System.Configuration.SchemeSettingElement?displayProperty=nameWithType>
- <xref:System.Configuration.SchemeSettingElementCollection?displayProperty=nameWithType>
- <xref:System.Configuration.UriSection?displayProperty=nameWithType>
- <xref:System.Configuration.UriSection.SchemeSettings%2A?displayProperty=nameWithType>
- <xref:System.GenericUriParserOptions?displayProperty=nameWithType>
- <xref:System.Uri?displayProperty=nameWithType>
- [<span data-ttu-id="5ee2a-136">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="5ee2a-136">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
