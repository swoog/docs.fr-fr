---
title: Élément &lt;dateTimeSerialization&gt;
ms.date: 03/30/2017
helpviewer_keywords:
- dateTimeSerialization element
- XML serialization, configuration
- <dateTimeSerialization> element
ms.assetid: 90fda55c-7730-41e9-bc4b-6423a4b920af
ms.openlocfilehash: 15fad472288a72a079991f41e6c2859776d78cca
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43723355"
---
# <a name="ltdatetimeserializationgt-element"></a><span data-ttu-id="9078d-102">Élément &lt;dateTimeSerialization&gt;</span><span class="sxs-lookup"><span data-stu-id="9078d-102">&lt;dateTimeSerialization&gt; Element</span></span>
<span data-ttu-id="9078d-103">Détermine le mode de sérialisation des objets <xref:System.DateTime>.</span><span class="sxs-lookup"><span data-stu-id="9078d-103">Determines the serialization mode of <xref:System.DateTime> objects.</span></span>  
  
 <span data-ttu-id="9078d-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="9078d-104">\<configuration></span></span>  
<span data-ttu-id="9078d-105">\<dateTimeSerialization></span><span class="sxs-lookup"><span data-stu-id="9078d-105">\<dateTimeSerialization></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9078d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9078d-106">Syntax</span></span>  
  
```xml  
<dateTimeSerialization  
    mode = "Roundtrip" | "Local"  
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9078d-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="9078d-107">Attributes and Elements</span></span>  
 <span data-ttu-id="9078d-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="9078d-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9078d-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="9078d-109">Attributes</span></span>  
  
|<span data-ttu-id="9078d-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="9078d-110">Attributes</span></span>|<span data-ttu-id="9078d-111">Description</span><span class="sxs-lookup"><span data-stu-id="9078d-111">Description</span></span>|  
|----------------|-----------------|  
|`mode`|<span data-ttu-id="9078d-112">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="9078d-112">Optional.</span></span> <span data-ttu-id="9078d-113">Spécifie le mode de sérialisation.</span><span class="sxs-lookup"><span data-stu-id="9078d-113">Specifies the serialization mode.</span></span> <span data-ttu-id="9078d-114">Affectez-le à l'une des valeurs <xref:System.Xml.Serialization.Configuration.DateTimeSerializationSection.DateTimeSerializationMode>.</span><span class="sxs-lookup"><span data-stu-id="9078d-114">Set to one of the <xref:System.Xml.Serialization.Configuration.DateTimeSerializationSection.DateTimeSerializationMode> values.</span></span> <span data-ttu-id="9078d-115">La valeur par défaut est **RoundTrip**.</span><span class="sxs-lookup"><span data-stu-id="9078d-115">The default is **RoundTrip**.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9078d-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9078d-116">Child Elements</span></span>  
 <span data-ttu-id="9078d-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9078d-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9078d-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9078d-118">Parent Elements</span></span>  
  
|<span data-ttu-id="9078d-119">Élément</span><span class="sxs-lookup"><span data-stu-id="9078d-119">Element</span></span>|<span data-ttu-id="9078d-120">Description</span><span class="sxs-lookup"><span data-stu-id="9078d-120">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="9078d-121">system.xml.serialization</span><span class="sxs-lookup"><span data-stu-id="9078d-121">system.xml.serialization</span></span>|<span data-ttu-id="9078d-122">Élément de niveau supérieur permettant de contrôler la sérialisation XML.</span><span class="sxs-lookup"><span data-stu-id="9078d-122">The top-level element for controlling XML serialization.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9078d-123">Notes</span><span class="sxs-lookup"><span data-stu-id="9078d-123">Remarks</span></span>  
 <span data-ttu-id="9078d-124">Dans les versions 1.0, 1.1, 2.0 et ultérieures du .NET Framework, quand cette propriété a la valeur **Local**, les objets <xref:System.DateTime> sont toujours mis en forme avec l’heure locale.</span><span class="sxs-lookup"><span data-stu-id="9078d-124">In versions 1.0, 1.1, 2.0 and later versions of the .NET Framework, when this property is set to **Local**, <xref:System.DateTime> objects are always formatted as the local time.</span></span> <span data-ttu-id="9078d-125">Autrement dit, les informations du fuseau horaire local sont toujours incluses avec les données sérialisées.</span><span class="sxs-lookup"><span data-stu-id="9078d-125">That is, local time zone information is always included with the serialized data.</span></span> <span data-ttu-id="9078d-126">Affectez la valeur **Local** à cette propriété pour garantir la compatibilité avec les versions antérieures du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="9078d-126">Set this property to **Local** to ensure compatibility with older versions of the .NET Framework.</span></span>  
  
 <span data-ttu-id="9078d-127">Dans les versions 2.0 et ultérieures du .NET Framework dont la propriété a la valeur **Roundtrip**, les objets <xref:System.DateTime> sont examinés pour déterminer s’ils se trouvent dans le fuseau horaire local ou UTC, ou encore dans un fuseau horaire non spécifié.</span><span class="sxs-lookup"><span data-stu-id="9078d-127">In version 2.0 and later versions of the .NET Framework that have this property set to **Roundtrip**, <xref:System.DateTime> objects are examined to determine whether they are in the local, UTC, or an unspecified time zone.</span></span> <span data-ttu-id="9078d-128">Les objets <xref:System.DateTime> sont ensuite sérialisés de manière à ce que ces informations soient conservées.</span><span class="sxs-lookup"><span data-stu-id="9078d-128">The <xref:System.DateTime> objects are then serialized in such a way that this information is preserved.</span></span> <span data-ttu-id="9078d-129">Il s'agit du comportement par défaut, recommandé pour toutes les nouvelles applications qui ne communiquent pas avec les versions antérieures du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="9078d-129">This is the default behavior and is the recommended behavior for all new applications that do not communicate with older versions of the framework.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9078d-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9078d-130">See Also</span></span>  
 <xref:System.DateTime>  
 <xref:System.Xml.Serialization.XmlSchemaImporter>  
 <xref:System.Xml.Serialization.Configuration.DateTimeSerializationSection.DateTimeSerializationMode>  
 [<span data-ttu-id="9078d-131">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="9078d-131">Configuration File Schema</span></span>](../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="9078d-132">\<schemaImporterExtensions>, élément</span><span class="sxs-lookup"><span data-stu-id="9078d-132">\<schemaImporterExtensions> Element</span></span>](../../../docs/standard/serialization/schemaimporterextensions-element.md)  
 [<span data-ttu-id="9078d-133">\<Ajouter > élément pour \<schemaImporterExtensions ></span><span class="sxs-lookup"><span data-stu-id="9078d-133">\<add> Element for \<schemaImporterExtensions></span></span>](../../../docs/standard/serialization/add-element-for-schemaimporterextensions.md)  
 [<span data-ttu-id="9078d-134">\<system.xml.serialization>, élément</span><span class="sxs-lookup"><span data-stu-id="9078d-134">\<system.xml.serialization> Element</span></span>](../../../docs/standard/serialization/system-xml-serialization-element.md)
