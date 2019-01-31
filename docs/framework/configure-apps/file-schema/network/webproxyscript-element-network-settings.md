---
title: <webProxyScript>, élément (paramètres réseau)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#webProxyScript
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/settings/webProxyScript
helpviewer_keywords:
- <webProxyScript> element
- webProxyScript element
ms.assetid: a13c26db-6218-4af3-9696-38f24b23bfac
ms.openlocfilehash: e823d6065ea23f3a47dad6853a1b9e1237a616c9
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55257822"
---
# <a name="webproxyscript-element-network-settings"></a><span data-ttu-id="ac956-102">\<webProxyScript >, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="ac956-102">\<webProxyScript> Element (Network Settings)</span></span>
<span data-ttu-id="ac956-103">Configure les caractéristiques du script utilisé pour découvrir les proxys Web.</span><span class="sxs-lookup"><span data-stu-id="ac956-103">Configures the characteristics of the script used to discover Web proxies.</span></span>  
  
 <span data-ttu-id="ac956-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="ac956-104">\<configuration></span></span>  
<span data-ttu-id="ac956-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="ac956-105">\<system.net></span></span>  
<span data-ttu-id="ac956-106">\<settings></span><span class="sxs-lookup"><span data-stu-id="ac956-106">\<settings></span></span>  
<span data-ttu-id="ac956-107">\<webProxyScript></span><span class="sxs-lookup"><span data-stu-id="ac956-107">\<webProxyScript></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ac956-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac956-108">Syntax</span></span>  
  
```xml  
<webProxyScript  
  downloadTimeout="hh:mm:ss"  
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ac956-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="ac956-109">Attributes and Elements</span></span>  
 <span data-ttu-id="ac956-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="ac956-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ac956-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="ac956-111">Attributes</span></span>  
  
|<span data-ttu-id="ac956-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="ac956-112">Attribute</span></span>|<span data-ttu-id="ac956-113">Description</span><span class="sxs-lookup"><span data-stu-id="ac956-113">Description</span></span>|  
|---------------|-----------------|  
|`downloadTimeout`|<span data-ttu-id="ac956-114">Spécifie la durée maximale de téléchargement du script en heures, minutes et secondes.</span><span class="sxs-lookup"><span data-stu-id="ac956-114">Specifies the maximum time to download the script in hours, minutes, and seconds.</span></span> <span data-ttu-id="ac956-115">La valeur par défaut est une minute.</span><span class="sxs-lookup"><span data-stu-id="ac956-115">The default value is one minute.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ac956-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ac956-116">Child Elements</span></span>  
 <span data-ttu-id="ac956-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ac956-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ac956-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ac956-118">Parent Elements</span></span>  
  
|<span data-ttu-id="ac956-119">Élément</span><span class="sxs-lookup"><span data-stu-id="ac956-119">Element</span></span>|<span data-ttu-id="ac956-120">Description</span><span class="sxs-lookup"><span data-stu-id="ac956-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ac956-121">settings</span><span class="sxs-lookup"><span data-stu-id="ac956-121">settings</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/settings-element-network-settings.md)|<span data-ttu-id="ac956-122">Configure les options réseau de base pour l’espace de noms <xref:System.Net>.</span><span class="sxs-lookup"><span data-stu-id="ac956-122">Configures basic network options for the <xref:System.Net> namespace.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ac956-123">Notes</span><span class="sxs-lookup"><span data-stu-id="ac956-123">Remarks</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="ac956-124">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="ac956-124">Configuration Files</span></span>  
 <span data-ttu-id="ac956-125">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="ac956-125">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ac956-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac956-126">See also</span></span>
- [<span data-ttu-id="ac956-127">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="ac956-127">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
