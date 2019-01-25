---
title: Élément &lt;system.xml.serialization&gt;
ms.date: 03/30/2017
helpviewer_keywords:
- system.xml.serialization element
- XML serialization, configuration
- <system.xml.serialization> element
ms.assetid: 3ce45919-388a-418c-8968-6df0372c73ec
ms.openlocfilehash: 8b85eef0f2c3bbb2d0d4a5548f5cbb4a66b0431d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54609562"
---
# <a name="ltsystemxmlserializationgt-element"></a><span data-ttu-id="dcc87-102">Élément &lt;system.xml.serialization&gt;</span><span class="sxs-lookup"><span data-stu-id="dcc87-102">&lt;system.xml.serialization&gt; Element</span></span>
<span data-ttu-id="dcc87-103">Élément de niveau supérieur permettant de contrôler la sérialisation XML.</span><span class="sxs-lookup"><span data-stu-id="dcc87-103">The top-level element for controlling XML serialization.</span></span> <span data-ttu-id="dcc87-104">Pour plus d’informations sur les fichiers de configuration, consultez [Schéma des fichiers de configuration](../../../docs/framework/configure-apps/file-schema/index.md).</span><span class="sxs-lookup"><span data-stu-id="dcc87-104">For more information about configuration files, see [Configuration File Schema](../../../docs/framework/configure-apps/file-schema/index.md).</span></span>  
  
 <span data-ttu-id="dcc87-105">\<configuration></span><span class="sxs-lookup"><span data-stu-id="dcc87-105">\<configuration></span></span>  
<span data-ttu-id="dcc87-106">\<system.xml.serialization></span><span class="sxs-lookup"><span data-stu-id="dcc87-106">\<system.xml.serialization></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dcc87-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dcc87-107">Syntax</span></span>  
  
```xml  
<system.xml.serialization>  
</system.xml.serialization>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="dcc87-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="dcc87-108">Attributes and Elements</span></span>  
 <span data-ttu-id="dcc87-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="dcc87-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="dcc87-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="dcc87-110">Attributes</span></span>  
 <span data-ttu-id="dcc87-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dcc87-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="dcc87-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dcc87-112">Child Elements</span></span>  
  
|<span data-ttu-id="dcc87-113">Élément</span><span class="sxs-lookup"><span data-stu-id="dcc87-113">Element</span></span>|<span data-ttu-id="dcc87-114">Description</span><span class="sxs-lookup"><span data-stu-id="dcc87-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="dcc87-115">\<dateTimeSerialization>, élément</span><span class="sxs-lookup"><span data-stu-id="dcc87-115">\<dateTimeSerialization> Element</span></span>](../../../docs/standard/serialization/datetimeserialization-element.md)|<span data-ttu-id="dcc87-116">Détermine le mode de sérialisation des objets <xref:System.DateTime>.</span><span class="sxs-lookup"><span data-stu-id="dcc87-116">Determines the serialization mode of <xref:System.DateTime> objects.</span></span>|  
|[<span data-ttu-id="dcc87-117">\<schemaImporterExtensions>, élément</span><span class="sxs-lookup"><span data-stu-id="dcc87-117">\<schemaImporterExtensions> Element</span></span>](../../../docs/standard/serialization/schemaimporterextensions-element.md)|<span data-ttu-id="dcc87-118">Contient des types utilisés par le <xref:System.Xml.Serialization.XmlSchemaImporter> pour mapper des types XSD en types .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="dcc87-118">Contains types that are used by the <xref:System.Xml.Serialization.XmlSchemaImporter> for mapping of XSD types to .NET Framework types.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="dcc87-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="dcc87-119">Parent Elements</span></span>  
  
|<span data-ttu-id="dcc87-120">Élément</span><span class="sxs-lookup"><span data-stu-id="dcc87-120">Element</span></span>|<span data-ttu-id="dcc87-121">Description</span><span class="sxs-lookup"><span data-stu-id="dcc87-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="dcc87-122">\<configuration>, élément</span><span class="sxs-lookup"><span data-stu-id="dcc87-122">\<configuration> Element</span></span>](../../../docs/framework/configure-apps/file-schema/configuration-element.md)|<span data-ttu-id="dcc87-123">Élément racine dans chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="dcc87-123">The root element in every configuration file that is used by the common language runtime and .NET Framework applications.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="dcc87-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="dcc87-124">Example</span></span>  
 <span data-ttu-id="dcc87-125">L'exemple de code suivant illustre comment spécifier le mode de sérialisation d'un objet <xref:System.DateTime> et l'ajout de types utilisés par le <xref:System.Xml.Serialization.XmlSchemaImporter> lors du mappage de types XSD en types .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="dcc87-125">The following code example illustrates how to specify the serialization mode of a <xref:System.DateTime> object, and the addition of types used by the <xref:System.Xml.Serialization.XmlSchemaImporter> when mapping XSD types to .NET Framework types.</span></span>  
  
```xml  
<system.xml.serialization>  
    <xmlSerializer checkDeserializeAdvances="false" />  
    <dateTimeSerialization mode = "Local" />  
    <schemaImporterExtensions>  
        <add   
        name = "MobileCapabilities"   
        type = "System.Web.Mobile.MobileCapabilities,   
        System.Web.Mobile, Version - 2.0.0.0, Culture = neuutral,   
        PublicKeyToken = b03f5f6f11d40a3a" />  
    </schemaImporterExtensions>  
</system.sxml.serialization>  
```  
  
## <a name="see-also"></a><span data-ttu-id="dcc87-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dcc87-126">See also</span></span>

- <xref:System.Xml.Serialization.XmlSchemaImporter>
- <xref:System.Xml.Serialization.Configuration.DateTimeSerializationSection.DateTimeSerializationMode>
- [<span data-ttu-id="dcc87-127">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="dcc87-127">Configuration File Schema</span></span>](../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="dcc87-128">\<dateTimeSerialization>, élément</span><span class="sxs-lookup"><span data-stu-id="dcc87-128">\<dateTimeSerialization> Element</span></span>](../../../docs/standard/serialization/datetimeserialization-element.md)
- [<span data-ttu-id="dcc87-129">\<schemaImporterExtensions>, élément</span><span class="sxs-lookup"><span data-stu-id="dcc87-129">\<schemaImporterExtensions> Element</span></span>](../../../docs/standard/serialization/schemaimporterextensions-element.md)
- [<span data-ttu-id="dcc87-130">\<Ajouter > élément pour \<schemaImporterExtensions ></span><span class="sxs-lookup"><span data-stu-id="dcc87-130">\<add> Element for \<schemaImporterExtensions></span></span>](../../../docs/standard/serialization/add-element-for-schemaimporterextensions.md)
