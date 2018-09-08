---
title: Élément &lt;system.xml.serialization&gt;
ms.date: 03/30/2017
helpviewer_keywords:
- system.xml.serialization element
- XML serialization, configuration
- <system.xml.serialization> element
ms.assetid: 3ce45919-388a-418c-8968-6df0372c73ec
ms.openlocfilehash: b67c1ec1ec737976e4e50b80b42f34e508dc0224
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44222329"
---
# <a name="ltsystemxmlserializationgt-element"></a><span data-ttu-id="4e8cf-102">Élément &lt;system.xml.serialization&gt;</span><span class="sxs-lookup"><span data-stu-id="4e8cf-102">&lt;system.xml.serialization&gt; Element</span></span>
<span data-ttu-id="4e8cf-103">Élément de niveau supérieur permettant de contrôler la sérialisation XML.</span><span class="sxs-lookup"><span data-stu-id="4e8cf-103">The top-level element for controlling XML serialization.</span></span> <span data-ttu-id="4e8cf-104">Pour plus d’informations sur les fichiers de configuration, consultez [Schéma des fichiers de configuration](../../../docs/framework/configure-apps/file-schema/index.md).</span><span class="sxs-lookup"><span data-stu-id="4e8cf-104">For more information about configuration files, see [Configuration File Schema](../../../docs/framework/configure-apps/file-schema/index.md).</span></span>  
  
 <span data-ttu-id="4e8cf-105">\<configuration></span><span class="sxs-lookup"><span data-stu-id="4e8cf-105">\<configuration></span></span>  
<span data-ttu-id="4e8cf-106">\<system.xml.serialization></span><span class="sxs-lookup"><span data-stu-id="4e8cf-106">\<system.xml.serialization></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4e8cf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e8cf-107">Syntax</span></span>  
  
```xml  
<system.xml.serialization>  
</system.xml.serialization>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4e8cf-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="4e8cf-108">Attributes and Elements</span></span>  
 <span data-ttu-id="4e8cf-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="4e8cf-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4e8cf-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="4e8cf-110">Attributes</span></span>  
 <span data-ttu-id="4e8cf-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4e8cf-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="4e8cf-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4e8cf-112">Child Elements</span></span>  
  
|<span data-ttu-id="4e8cf-113">Élément</span><span class="sxs-lookup"><span data-stu-id="4e8cf-113">Element</span></span>|<span data-ttu-id="4e8cf-114">Description</span><span class="sxs-lookup"><span data-stu-id="4e8cf-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4e8cf-115">\<dateTimeSerialization>, élément</span><span class="sxs-lookup"><span data-stu-id="4e8cf-115">\<dateTimeSerialization> Element</span></span>](../../../docs/standard/serialization/datetimeserialization-element.md)|<span data-ttu-id="4e8cf-116">Détermine le mode de sérialisation des objets <xref:System.DateTime>.</span><span class="sxs-lookup"><span data-stu-id="4e8cf-116">Determines the serialization mode of <xref:System.DateTime> objects.</span></span>|  
|[<span data-ttu-id="4e8cf-117">\<schemaImporterExtensions>, élément</span><span class="sxs-lookup"><span data-stu-id="4e8cf-117">\<schemaImporterExtensions> Element</span></span>](../../../docs/standard/serialization/schemaimporterextensions-element.md)|<span data-ttu-id="4e8cf-118">Contient des types utilisés par le <xref:System.Xml.Serialization.XmlSchemaImporter> pour mapper des types XSD en types .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="4e8cf-118">Contains types that are used by the <xref:System.Xml.Serialization.XmlSchemaImporter> for mapping of XSD types to .NET Framework types.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="4e8cf-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4e8cf-119">Parent Elements</span></span>  
  
|<span data-ttu-id="4e8cf-120">Élément</span><span class="sxs-lookup"><span data-stu-id="4e8cf-120">Element</span></span>|<span data-ttu-id="4e8cf-121">Description</span><span class="sxs-lookup"><span data-stu-id="4e8cf-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4e8cf-122">\<configuration>, élément</span><span class="sxs-lookup"><span data-stu-id="4e8cf-122">\<configuration> Element</span></span>](../../../docs/framework/configure-apps/file-schema/configuration-element.md)|<span data-ttu-id="4e8cf-123">Élément racine dans chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="4e8cf-123">The root element in every configuration file that is used by the common language runtime and .NET Framework applications.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="4e8cf-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="4e8cf-124">Example</span></span>  
 <span data-ttu-id="4e8cf-125">L'exemple de code suivant illustre comment spécifier le mode de sérialisation d'un objet <xref:System.DateTime> et l'ajout de types utilisés par le <xref:System.Xml.Serialization.XmlSchemaImporter> lors du mappage de types XSD en types .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="4e8cf-125">The following code example illustrates how to specify the serialization mode of a <xref:System.DateTime> object, and the addition of types used by the <xref:System.Xml.Serialization.XmlSchemaImporter> when mapping XSD types to .NET Framework types.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="4e8cf-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e8cf-126">See also</span></span>

- <xref:System.Xml.Serialization.XmlSchemaImporter>  
- <xref:System.Xml.Serialization.Configuration.DateTimeSerializationSection.DateTimeSerializationMode>  
- [<span data-ttu-id="4e8cf-127">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="4e8cf-127">Configuration File Schema</span></span>](../../../docs/framework/configure-apps/file-schema/index.md)  
- [<span data-ttu-id="4e8cf-128">\<dateTimeSerialization>, élément</span><span class="sxs-lookup"><span data-stu-id="4e8cf-128">\<dateTimeSerialization> Element</span></span>](../../../docs/standard/serialization/datetimeserialization-element.md)  
- [<span data-ttu-id="4e8cf-129">\<schemaImporterExtensions>, élément</span><span class="sxs-lookup"><span data-stu-id="4e8cf-129">\<schemaImporterExtensions> Element</span></span>](../../../docs/standard/serialization/schemaimporterextensions-element.md)  
- [<span data-ttu-id="4e8cf-130">\<Ajouter > élément pour \<schemaImporterExtensions ></span><span class="sxs-lookup"><span data-stu-id="4e8cf-130">\<add> Element for \<schemaImporterExtensions></span></span>](../../../docs/standard/serialization/add-element-for-schemaimporterextensions.md)
