---
title: <clear>, élément de schemeSettings (paramètres d’URI)
ms.date: 03/30/2017
ms.assetid: 65098332-ce61-4542-ab8d-e7dc0257d31f
ms.openlocfilehash: 132506dc15335b738fcdb026f4d31429bc45a228
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61674686"
---
# <a name="clear-element-for-schemesettings-uri-settings"></a><span data-ttu-id="4b209-102">\<Désactivez >, élément de schemeSettings (paramètres d’Uri)</span><span class="sxs-lookup"><span data-stu-id="4b209-102">\<clear> Element for schemeSettings (Uri Settings)</span></span>
<span data-ttu-id="4b209-103">Efface tous les paramètres existants de schéma.</span><span class="sxs-lookup"><span data-stu-id="4b209-103">Clears all existing scheme settings.</span></span>  
  
 <span data-ttu-id="4b209-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="4b209-104">\<configuration></span></span>  
<span data-ttu-id="4b209-105">\<uri></span><span class="sxs-lookup"><span data-stu-id="4b209-105">\<uri></span></span>  
<span data-ttu-id="4b209-106">\<schemeSettings></span><span class="sxs-lookup"><span data-stu-id="4b209-106">\<schemeSettings></span></span>  
<span data-ttu-id="4b209-107">\<clear></span><span class="sxs-lookup"><span data-stu-id="4b209-107">\<clear></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4b209-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b209-108">Syntax</span></span>  
  
```xml  
<clear/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4b209-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="4b209-109">Attributes and Elements</span></span>  
 <span data-ttu-id="4b209-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="4b209-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4b209-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="4b209-111">Attributes</span></span>  
 <span data-ttu-id="4b209-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4b209-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="4b209-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4b209-113">Child Elements</span></span>  
 <span data-ttu-id="4b209-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4b209-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4b209-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4b209-115">Parent Elements</span></span>  
  
|<span data-ttu-id="4b209-116">Élément</span><span class="sxs-lookup"><span data-stu-id="4b209-116">Element</span></span>|<span data-ttu-id="4b209-117">Description</span><span class="sxs-lookup"><span data-stu-id="4b209-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4b209-118">\<schemeSettings, élément (paramètres d’Uri)</span><span class="sxs-lookup"><span data-stu-id="4b209-118">\<schemeSettings> Element (Uri Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/schemesettings-element-uri-settings.md)|<span data-ttu-id="4b209-119">Spécifie la façon dont un <xref:System.Uri> est analysé pour les schémas spécifiques.</span><span class="sxs-lookup"><span data-stu-id="4b209-119">Specifies how a <xref:System.Uri> will be parsed for specific schemes.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4b209-120">Notes</span><span class="sxs-lookup"><span data-stu-id="4b209-120">Remarks</span></span>  
 <span data-ttu-id="4b209-121">Par défaut, le <xref:System.Uri?displayProperty=nameWithType> % n’échappe pas de classe encodé délimiteurs de chemin d’accès avant d’exécuter la compression de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="4b209-121">By default, the <xref:System.Uri?displayProperty=nameWithType> class un-escapes percent encoded path delimiters before executing path compression.</span></span> <span data-ttu-id="4b209-122">Ceci était implémenté comme un mécanisme de sécurité contre les attaques comme suit :</span><span class="sxs-lookup"><span data-stu-id="4b209-122">This was implemented as a security mechanism against attacks like the following:</span></span>  
  
 `http://www.contoso.com/..%2F..%2F/Windows/System32/cmd.exe?/c+dir+c:\`  
  
 <span data-ttu-id="4b209-123">Si cet URI est passé à des modules ne gère ne pas % caractères encodés correctement, cela peut entraîner la commande suivante en cours d’exécution par le serveur :</span><span class="sxs-lookup"><span data-stu-id="4b209-123">If this URI gets passed down to modules not handling percent encoded characters correctly, it could result in the following command being executed by the server:</span></span>  
  
 `c:\Windows\System32\cmd.exe /c dir c:\`  
  
 <span data-ttu-id="4b209-124">Pour cette raison, <xref:System.Uri?displayProperty=nameWithType> première délimiteurs de chemin d’accès n’échappe pas de classe, puis applique la compression de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="4b209-124">For this reason, <xref:System.Uri?displayProperty=nameWithType> class first un-escapes path delimiters and then applies path compression.</span></span> <span data-ttu-id="4b209-125">Le résultat du passage de l’URL malveillante ci-dessus à <xref:System.Uri?displayProperty=nameWithType> classe les résultats de constructeur dans l’URI suivant :</span><span class="sxs-lookup"><span data-stu-id="4b209-125">The result of passing the malicious URL above to <xref:System.Uri?displayProperty=nameWithType> class constructor results in the following URI:</span></span>  
  
 `http://www.microsoft.com/Windows/System32/cmd.exe?/c+dir+c:\`  
  
 <span data-ttu-id="4b209-126">Ce comportement par défaut peut être modifié pour ne pas les délimiteurs de chemin d’accès codé en pourcentage échapper à l’aide de l’option de configuration schemeSettings pour un modèle spécifique.</span><span class="sxs-lookup"><span data-stu-id="4b209-126">This default behavior can be modified to not un-escape percent encoded path delimiters using the schemeSettings configuration option for a specific scheme.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="4b209-127">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="4b209-127">Configuration Files</span></span>  
 <span data-ttu-id="4b209-128">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="4b209-128">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="4b209-129">Exemple</span><span class="sxs-lookup"><span data-stu-id="4b209-129">Example</span></span>  
 <span data-ttu-id="4b209-130">L’exemple suivant montre une configuration utilisée par la <xref:System.Uri> classe qui efface tous les paramètres de schéma, puis ajoute la prise en charge pour la séquence d’échappement ne pas les délimiteurs de chemin d’encodés en pourcentage pour le schéma http.</span><span class="sxs-lookup"><span data-stu-id="4b209-130">The following example shows a configuration used by the <xref:System.Uri> class that clears all scheme settings and then adds support for not escaping percent-encoded path delimiters for the http scheme.</span></span>  
  
```xml  
<configuration>  
  <uri>  
    <schemeSettings>  
      <clear/>  
      <add name="http" genericUriParserOptions="DontUnescapePathDotsAndSlashes"/>  
    </schemeSettings>  
  </uri>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="4b209-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b209-131">See also</span></span>

- <xref:System.Configuration.SchemeSettingElement?displayProperty=nameWithType>
- <xref:System.Configuration.SchemeSettingElementCollection?displayProperty=nameWithType>
- <xref:System.Configuration.UriSection?displayProperty=nameWithType>
- <xref:System.Configuration.UriSection.SchemeSettings%2A?displayProperty=nameWithType>
- <xref:System.GenericUriParserOptions?displayProperty=nameWithType>
- <xref:System.Uri?displayProperty=nameWithType>
- [<span data-ttu-id="4b209-132">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="4b209-132">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
