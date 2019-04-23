---
title: Élément <gcAllowVeryLargeObjects>
ms.date: 03/30/2017
helpviewer_keywords:
- gcAllowVeryLargeObjects element
- <gcAllowVeryLargeObjects> element
ms.assetid: 5c7ea24a-39ac-4e5f-83b7-b9f9a1b556ab
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 19103b2ac6e6dbba930050074fcea3cfd5a97661
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59098014"
---
# <a name="gcallowverylargeobjects-element"></a><span data-ttu-id="0799e-102">\<gcAllowVeryLargeObjects> Element</span><span class="sxs-lookup"><span data-stu-id="0799e-102">\<gcAllowVeryLargeObjects> Element</span></span>
<span data-ttu-id="0799e-103">Sur les plateformes 64 bits, autorise les tableaux dont la taille totale est supérieure à 2 gigaoctets (Go).</span><span class="sxs-lookup"><span data-stu-id="0799e-103">On 64-bit platforms, enables arrays that are greater than 2 gigabytes (GB) in total size.</span></span>  
  
 <span data-ttu-id="0799e-104">\<configuration > élément</span><span class="sxs-lookup"><span data-stu-id="0799e-104">\<configuration> Element</span></span>  
<span data-ttu-id="0799e-105">\<runtime > élément</span><span class="sxs-lookup"><span data-stu-id="0799e-105">\<runtime> Element</span></span>  
<span data-ttu-id="0799e-106">\<gcAllowVeryLargeObjects> Element</span><span class="sxs-lookup"><span data-stu-id="0799e-106">\<gcAllowVeryLargeObjects> Element</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0799e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0799e-107">Syntax</span></span>  
  
```xml  
<gcAllowVeryLargeObjects    
   enabled="true|false" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0799e-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="0799e-108">Attributes and Elements</span></span>  
 <span data-ttu-id="0799e-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="0799e-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0799e-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="0799e-110">Attributes</span></span>  
  
|<span data-ttu-id="0799e-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="0799e-111">Attribute</span></span>|<span data-ttu-id="0799e-112">Description</span><span class="sxs-lookup"><span data-stu-id="0799e-112">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="0799e-113">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="0799e-113">Required attribute.</span></span><br /><br /> <span data-ttu-id="0799e-114">Spécifie si les tableaux qui sont supérieures à 2 Go de taille totale sont activés sur les plateformes 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0799e-114">Specifies whether arrays that are greater than 2 GB in total size are enabled on 64-bit platforms.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="0799e-115">Attribut enabled</span><span class="sxs-lookup"><span data-stu-id="0799e-115">enabled Attribute</span></span>  
  
|<span data-ttu-id="0799e-116">Value</span><span class="sxs-lookup"><span data-stu-id="0799e-116">Value</span></span>|<span data-ttu-id="0799e-117">Description</span><span class="sxs-lookup"><span data-stu-id="0799e-117">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="0799e-118">Supérieure à 2 Go de taille totale des tableaux ne sont pas activés.</span><span class="sxs-lookup"><span data-stu-id="0799e-118">Arrays greater than 2 GB in total size are not enabled.</span></span> <span data-ttu-id="0799e-119">Il s'agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="0799e-119">This is the default.</span></span>|  
|`true`|<span data-ttu-id="0799e-120">Supérieure à 2 Go de taille totale des tableaux sont activés sur les plateformes 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0799e-120">Arrays greater than 2 GB in total size are enabled on 64-bit platforms.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0799e-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0799e-121">Child Elements</span></span>  
 <span data-ttu-id="0799e-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0799e-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0799e-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0799e-123">Parent Elements</span></span>  
  
|<span data-ttu-id="0799e-124">Élément</span><span class="sxs-lookup"><span data-stu-id="0799e-124">Element</span></span>|<span data-ttu-id="0799e-125">Description</span><span class="sxs-lookup"><span data-stu-id="0799e-125">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="0799e-126">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="0799e-126">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="0799e-127">Contient des informations sur les options d'initialisation du runtime.</span><span class="sxs-lookup"><span data-stu-id="0799e-127">Contains information about runtime initialization options.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0799e-128">Notes</span><span class="sxs-lookup"><span data-stu-id="0799e-128">Remarks</span></span>  
 <span data-ttu-id="0799e-129">À l’aide de cet élément dans votre fichier de configuration d’application permet de tableaux supérieurs à 2 Go, mais ne modifie pas les autres limites concernant la taille de l’objet ou de la taille du tableau :</span><span class="sxs-lookup"><span data-stu-id="0799e-129">Using this element in your application configuration file enables arrays that are larger than 2 GB in size, but does not change other limits on object size or array size:</span></span>  
  
-   <span data-ttu-id="0799e-130">Le nombre maximal d’éléments dans un tableau est <xref:System.UInt32.MaxValue?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="0799e-130">The maximum number of elements in an array is <xref:System.UInt32.MaxValue?displayProperty=nameWithType>.</span></span>  
  
-   <span data-ttu-id="0799e-131">L’index maximal dans n’importe quelle dimension unique est 2,147,483,591 (0x7FFFFFC7) pour les tableaux d’octets et des tableaux de structures d’un octet et 2,146,435,071 (0X7FEFFFFF) pour les autres types.</span><span class="sxs-lookup"><span data-stu-id="0799e-131">The maximum index in any single dimension is 2,147,483,591 (0x7FFFFFC7) for byte arrays and arrays of single-byte structures, and 2,146,435,071 (0X7FEFFFFF) for other types.</span></span>  
  
-   <span data-ttu-id="0799e-132">La taille maximale pour les chaînes et autres objets autres que des tableaux est inchangée.</span><span class="sxs-lookup"><span data-stu-id="0799e-132">The maximum size for strings and other non-array objects is unchanged.</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="0799e-133">Avant d’activer cette fonctionnalité, assurez-vous que votre application n’inclut pas le code unsafe qui part du principe que tous les tableaux sont inférieures à 2 Go.</span><span class="sxs-lookup"><span data-stu-id="0799e-133">Before enabling this feature, ensure that your application does not include unsafe code that assumes that all arrays are smaller than 2 GB in size.</span></span> <span data-ttu-id="0799e-134">Par exemple, le code qui utilise des tableaux de mémoires tampons unsafe peut-être expose à des dépassements de mémoire tampon s’il est écrit sur l’hypothèse que les tableaux ne dépassent pas 2 Go.</span><span class="sxs-lookup"><span data-stu-id="0799e-134">For example, unsafe code that uses arrays as buffers might be susceptible to buffer overruns if it is written on the assumption that arrays will not exceed 2 GB.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0799e-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="0799e-135">Example</span></span>  
 <span data-ttu-id="0799e-136">L’exemple suivant montre comment activer cette fonctionnalité pour une application.</span><span class="sxs-lookup"><span data-stu-id="0799e-136">The following example shows how to enable this feature for an application.</span></span>  
  
```xml  
<configuration>  
  <runtime>  
    <gcAllowVeryLargeObjects enabled="true" />  
  </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="0799e-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0799e-137">See also</span></span>

- [<span data-ttu-id="0799e-138">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="0799e-138">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="0799e-139">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="0799e-139">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
