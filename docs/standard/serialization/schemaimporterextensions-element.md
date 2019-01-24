---
title: Élément &lt;schemaImporterExtensions&gt;
ms.date: 03/30/2017
helpviewer_keywords:
- XML serialization, configuration
- schemaImporterExtensions element
- <schemaImporterExtensions> element
ms.assetid: 465ef2a0-f909-4ac1-9a56-0ead5c849698
ms.openlocfilehash: dbe85ea817a597db84ddad530d67b1c2b7953f75
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54535366"
---
# <a name="ltschemaimporterextensionsgt-element"></a><span data-ttu-id="366f7-102">Élément &lt;schemaImporterExtensions&gt;</span><span class="sxs-lookup"><span data-stu-id="366f7-102">&lt;schemaImporterExtensions&gt; Element</span></span>
<span data-ttu-id="366f7-103">Contient des types utilisés par le <xref:System.Xml.Serialization.XmlSchemaImporter> pour mapper des types XSD en types .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="366f7-103">Contains types that are used by the <xref:System.Xml.Serialization.XmlSchemaImporter> for mapping of XSD types to .NET Framework types.</span></span> <span data-ttu-id="366f7-104">Pour plus d’informations sur les fichiers de configuration, consultez [Schéma des fichiers de configuration](../../../docs/framework/configure-apps/file-schema/index.md).</span><span class="sxs-lookup"><span data-stu-id="366f7-104">For more information about configuration files, see [Configuration File Schema](../../../docs/framework/configure-apps/file-schema/index.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="366f7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="366f7-105">Syntax</span></span>  
  
```xml  
<schemaImporterExtensions>  
    <!-- Add types -->  
</schemaImporterExtensions>  
```  
  
## <a name="child-elements"></a><span data-ttu-id="366f7-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="366f7-106">Child Elements</span></span>  
  
|<span data-ttu-id="366f7-107">Élément</span><span class="sxs-lookup"><span data-stu-id="366f7-107">Element</span></span>|<span data-ttu-id="366f7-108">Description</span><span class="sxs-lookup"><span data-stu-id="366f7-108">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="366f7-109">\<Ajouter > élément pour \<schemaImporterExtensions ></span><span class="sxs-lookup"><span data-stu-id="366f7-109">\<add> Element for \<schemaImporterExtensions></span></span>](../../../docs/standard/serialization/add-element-for-schemaimporterextensions.md)|<span data-ttu-id="366f7-110">Ajoute des types utilisés par <xref:System.Xml.Serialization.XmlSchemaImporter> pour créer des mappages.</span><span class="sxs-lookup"><span data-stu-id="366f7-110">Adds types that are used by the <xref:System.Xml.Serialization.XmlSchemaImporter> to create mappings.</span></span>|  
  
## <a name="parent-elements"></a><span data-ttu-id="366f7-111">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="366f7-111">Parent Elements</span></span>  
  
|<span data-ttu-id="366f7-112">Élément</span><span class="sxs-lookup"><span data-stu-id="366f7-112">Element</span></span>|<span data-ttu-id="366f7-113">Description</span><span class="sxs-lookup"><span data-stu-id="366f7-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="366f7-114">\<system.xml.serialization>, élément</span><span class="sxs-lookup"><span data-stu-id="366f7-114">\<system.xml.serialization> Element</span></span>](../../../docs/standard/serialization/system-xml-serialization-element.md)|<span data-ttu-id="366f7-115">Élément de niveau supérieur permettant de contrôler la sérialisation XML.</span><span class="sxs-lookup"><span data-stu-id="366f7-115">The top-level element for controlling XML serialization.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="366f7-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="366f7-116">Example</span></span>  
 <span data-ttu-id="366f7-117">L'exemple de code suivant illustre comment ajouter des types utilisés par <xref:System.Xml.Serialization.XmlSchemaImporter> lors du mappage de types XSD en types .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="366f7-117">The following code example illustrates how to add types that are used by the <xref:System.Xml.Serialization.XmlSchemaImporter> when mapping XSD types to .NET Framework types.</span></span>  
  
```xml  
<system.xml.serialization>  
    <schemaImporterExtensions>  
        <add name = "MobileCapabilities" type =   
        "System.Web.Mobile.MobileCapabilities,   
        System.Web.Mobile, Version - 2.0.0.0, Culture = neutral,   
        PublicKeyToken = b03f5f6f11d40a3a" />  
    </schemaImporterExtensions>  
</system.xml.serialization>  
```  
  
## <a name="see-also"></a><span data-ttu-id="366f7-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="366f7-118">See also</span></span>

- <xref:System.Xml.Serialization.XmlSchemaImporter>
- <xref:System.Xml.Serialization.Configuration.DateTimeSerializationSection.DateTimeSerializationMode>
- [<span data-ttu-id="366f7-119">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="366f7-119">Configuration File Schema</span></span>](../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="366f7-120">\<dateTimeSerialization>, élément</span><span class="sxs-lookup"><span data-stu-id="366f7-120">\<dateTimeSerialization> Element</span></span>](../../../docs/standard/serialization/datetimeserialization-element.md)
- [<span data-ttu-id="366f7-121">\<Ajouter > élément pour \<schemaImporterExtensions ></span><span class="sxs-lookup"><span data-stu-id="366f7-121">\<add> Element for \<schemaImporterExtensions></span></span>](../../../docs/standard/serialization/add-element-for-schemaimporterextensions.md)
- [<span data-ttu-id="366f7-122">\<system.xml.serialization>, élément</span><span class="sxs-lookup"><span data-stu-id="366f7-122">\<system.xml.serialization> Element</span></span>](../../../docs/standard/serialization/system-xml-serialization-element.md)
