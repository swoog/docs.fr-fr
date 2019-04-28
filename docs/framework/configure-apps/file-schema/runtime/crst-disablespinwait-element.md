---
title: élément de < Crst_DisableSpinWait >
ms.date: 04/18/2019
f1_keywords:
- Crst_DisableSpinWait
helpviewer_keywords:
- Crst_DisableSpinWait element
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6cde26250db0b3d11c51a18b7ebd378953ae0958
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61704828"
---
# <a name="crstdisablespinwait-element"></a><span data-ttu-id="82083-102">\<Crst_DisableSpinWait > élément</span><span class="sxs-lookup"><span data-stu-id="82083-102">\<Crst_DisableSpinWait> element</span></span>

<span data-ttu-id="82083-103">Spécifie s’il faut désactiver l’attente de spins pour une section critique lors de conflits.</span><span class="sxs-lookup"><span data-stu-id="82083-103">Specifies whether to disable spin-waiting for a critical section when contended.</span></span> \ 
  
 <span data-ttu-id="82083-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="82083-104">\<configuration></span></span>  
<span data-ttu-id="82083-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="82083-105">\<runtime></span></span>  
<span data-ttu-id="82083-106">\<Crst_DisableSpinWait></span><span class="sxs-lookup"><span data-stu-id="82083-106">\<Crst_DisableSpinWait></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="82083-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82083-107">Syntax</span></span>  
  
```xml  
<Crst_DisableSpinWait enabled="true | false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="82083-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="82083-108">Attributes and Elements</span></span>

<span data-ttu-id="82083-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="82083-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="82083-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="82083-110">Attributes</span></span>  
  
|<span data-ttu-id="82083-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="82083-111">Attribute</span></span>|<span data-ttu-id="82083-112">Description</span><span class="sxs-lookup"><span data-stu-id="82083-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="82083-113">**enabled**</span><span class="sxs-lookup"><span data-stu-id="82083-113">**enabled**</span></span>|<span data-ttu-id="82083-114">Spécifie si la rotation-en attente pour les sections critiques est activée quand ils sont de conflits.</span><span class="sxs-lookup"><span data-stu-id="82083-114">Specifies whether spin-waiting for critical sections is enabled when they are contended.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="82083-115">Attribut enabled</span><span class="sxs-lookup"><span data-stu-id="82083-115">enabled Attribute</span></span>  
  
|<span data-ttu-id="82083-116">Value</span><span class="sxs-lookup"><span data-stu-id="82083-116">Value</span></span>|<span data-ttu-id="82083-117">Description</span><span class="sxs-lookup"><span data-stu-id="82083-117">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="82083-118">1</span><span class="sxs-lookup"><span data-stu-id="82083-118">1</span></span>|<span data-ttu-id="82083-119">Attente de spins est activé.</span><span class="sxs-lookup"><span data-stu-id="82083-119">Spin-waiting is enabled.</span></span>|  
|<span data-ttu-id="82083-120">0</span><span class="sxs-lookup"><span data-stu-id="82083-120">0</span></span>|<span data-ttu-id="82083-121">Attente de spins est désactivé.</span><span class="sxs-lookup"><span data-stu-id="82083-121">Spin-waiting is disabled.</span></span> <span data-ttu-id="82083-122">Ceci est la valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="82083-122">This is the default</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="82083-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="82083-123">Child Elements</span></span>  
 <span data-ttu-id="82083-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="82083-124">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="82083-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="82083-125">Parent Elements</span></span>  
  
|<span data-ttu-id="82083-126">Élément</span><span class="sxs-lookup"><span data-stu-id="82083-126">Element</span></span>|<span data-ttu-id="82083-127">Description</span><span class="sxs-lookup"><span data-stu-id="82083-127">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="82083-128">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="82083-128">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="82083-129">Contient des informations sur les différents paramètres de configuration du runtime.</span><span class="sxs-lookup"><span data-stu-id="82083-129">Contains information about various runtime configuration settings.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="82083-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="82083-130">Example</span></span>  

<span data-ttu-id="82083-131">L’exemple suivant désactive toupie (spin) en attente dans des sections critiques de conflits.</span><span class="sxs-lookup"><span data-stu-id="82083-131">The following example disables spin-waiting in critical sections when contended.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <Crst_DisableSpinWait enabled="1"/>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="82083-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82083-132">See also</span></span>

- [<span data-ttu-id="82083-133">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="82083-133">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="82083-134">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="82083-134">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
