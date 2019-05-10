---
title: élément de < Crst_DisableSpinWait >
ms.date: 04/18/2019
f1_keywords:
- Crst_DisableSpinWait
helpviewer_keywords:
- Crst_DisableSpinWait element
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f89f0558c11e229fef2ca3cd619e3c033f12c858
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64754673"
---
# <a name="crstdisablespinwait-element"></a><span data-ttu-id="dd8e9-102">\<Crst_DisableSpinWait > élément</span><span class="sxs-lookup"><span data-stu-id="dd8e9-102">\<Crst_DisableSpinWait> element</span></span>

<span data-ttu-id="dd8e9-103">Spécifie s’il faut désactiver l’attente de spins pour une section critique lors de conflits.</span><span class="sxs-lookup"><span data-stu-id="dd8e9-103">Specifies whether to disable spin-waiting for a critical section when contended.</span></span>  
  
 <span data-ttu-id="dd8e9-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="dd8e9-104">\<configuration></span></span>  
<span data-ttu-id="dd8e9-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="dd8e9-105">\<runtime></span></span>  
<span data-ttu-id="dd8e9-106">\<Crst_DisableSpinWait></span><span class="sxs-lookup"><span data-stu-id="dd8e9-106">\<Crst_DisableSpinWait></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dd8e9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd8e9-107">Syntax</span></span>  
  
```xml  
<Crst_DisableSpinWait enabled="true | false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="dd8e9-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="dd8e9-108">Attributes and Elements</span></span>

<span data-ttu-id="dd8e9-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="dd8e9-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="dd8e9-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="dd8e9-110">Attributes</span></span>  
  
|<span data-ttu-id="dd8e9-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="dd8e9-111">Attribute</span></span>|<span data-ttu-id="dd8e9-112">Description</span><span class="sxs-lookup"><span data-stu-id="dd8e9-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="dd8e9-113">**enabled**</span><span class="sxs-lookup"><span data-stu-id="dd8e9-113">**enabled**</span></span>|<span data-ttu-id="dd8e9-114">Spécifie si l’attente de spins pour les sections critiques lorsqu’ils sont de conflits est désactivé.</span><span class="sxs-lookup"><span data-stu-id="dd8e9-114">Specifies whether spin-waiting for critical sections when they are contended is disabled.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="dd8e9-115">Attribut enabled</span><span class="sxs-lookup"><span data-stu-id="dd8e9-115">enabled Attribute</span></span>  
  
|<span data-ttu-id="dd8e9-116">Value</span><span class="sxs-lookup"><span data-stu-id="dd8e9-116">Value</span></span>|<span data-ttu-id="dd8e9-117">Description</span><span class="sxs-lookup"><span data-stu-id="dd8e9-117">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="dd8e9-118">1</span><span class="sxs-lookup"><span data-stu-id="dd8e9-118">1</span></span>|<span data-ttu-id="dd8e9-119">Désactiver l’attente de toupie (spin) lorsqu’une section critique ne peut pas être acquis.</span><span class="sxs-lookup"><span data-stu-id="dd8e9-119">Disable spin-waiting when a critical section cannot be acquired.</span></span>|  
|<span data-ttu-id="dd8e9-120">0</span><span class="sxs-lookup"><span data-stu-id="dd8e9-120">0</span></span>|<span data-ttu-id="dd8e9-121">Ne désactivez pas l’attente de spins lorsqu’une section critique ne peut pas être acquis.</span><span class="sxs-lookup"><span data-stu-id="dd8e9-121">Do not disable spin-waiting when a critical section cannot be acquired.</span></span> <span data-ttu-id="dd8e9-122">Valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="dd8e9-122">This is the default value.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="dd8e9-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dd8e9-123">Child Elements</span></span>  
 <span data-ttu-id="dd8e9-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dd8e9-124">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="dd8e9-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="dd8e9-125">Parent Elements</span></span>  
  
|<span data-ttu-id="dd8e9-126">Élément</span><span class="sxs-lookup"><span data-stu-id="dd8e9-126">Element</span></span>|<span data-ttu-id="dd8e9-127">Description</span><span class="sxs-lookup"><span data-stu-id="dd8e9-127">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="dd8e9-128">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="dd8e9-128">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="dd8e9-129">Contient des informations sur les différents paramètres de configuration du runtime.</span><span class="sxs-lookup"><span data-stu-id="dd8e9-129">Contains information about various runtime configuration settings.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="dd8e9-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="dd8e9-130">Example</span></span>  

<span data-ttu-id="dd8e9-131">L’exemple suivant désactive toupie (spin) en attente dans des sections critiques de conflits.</span><span class="sxs-lookup"><span data-stu-id="dd8e9-131">The following example disables spin-waiting in critical sections when contended.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <Crst_DisableSpinWait enabled="1"/>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="dd8e9-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd8e9-132">See also</span></span>

- [<span data-ttu-id="dd8e9-133">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="dd8e9-133">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="dd8e9-134">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="dd8e9-134">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
