---
title: Élément &lt;schemaImporterExtensions&gt;
ms.date: 03/30/2017
helpviewer_keywords:
- XML serialization, configuration
- schemaImporterExtensions element
- <schemaImporterExtensions> element
ms.assetid: 465ef2a0-f909-4ac1-9a56-0ead5c849698
ms.openlocfilehash: 8bcd8abb138c645f61bf833b49cda2631d1778dd
ms.sourcegitcommit: fe02afbc39e78afd78cc6050e4a9c12a75f579f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/30/2018
ms.locfileid: "43255627"
---
# <a name="ltschemaimporterextensionsgt-element"></a><span data-ttu-id="99517-102">Élément &lt;schemaImporterExtensions&gt;</span><span class="sxs-lookup"><span data-stu-id="99517-102">&lt;schemaImporterExtensions&gt; Element</span></span>
<span data-ttu-id="99517-103">Contient des types utilisés par le <xref:System.Xml.Serialization.XmlSchemaImporter> pour mapper des types XSD en types .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="99517-103">Contains types that are used by the <xref:System.Xml.Serialization.XmlSchemaImporter> for mapping of XSD types to .NET Framework types.</span></span> <span data-ttu-id="99517-104">Pour plus d’informations sur les fichiers de configuration, consultez [Schéma des fichiers de configuration](../../../docs/framework/configure-apps/file-schema/index.md).</span><span class="sxs-lookup"><span data-stu-id="99517-104">For more information about configuration files, see [Configuration File Schema](../../../docs/framework/configure-apps/file-schema/index.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="99517-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99517-105">Syntax</span></span>  
  
```xml  
<schemaImporterExtensions>  
    <!-- Add types -->  
</schemaImporterExtensions>  
```  
  
## <a name="child-elements"></a><span data-ttu-id="99517-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="99517-106">Child Elements</span></span>  
  
|<span data-ttu-id="99517-107">Élément</span><span class="sxs-lookup"><span data-stu-id="99517-107">Element</span></span>|<span data-ttu-id="99517-108">Description</span><span class="sxs-lookup"><span data-stu-id="99517-108">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="99517-109">\<Ajouter > élément pour \<schemaImporterExtensions ></span><span class="sxs-lookup"><span data-stu-id="99517-109">\<add> Element for \<schemaImporterExtensions></span></span>](../../../docs/standard/serialization/add-element-for-schemaimporterextensions.md)|<span data-ttu-id="99517-110">Ajoute des types utilisés par <xref:System.Xml.Serialization.XmlSchemaImporter> pour créer des mappages.</span><span class="sxs-lookup"><span data-stu-id="99517-110">Adds types that are used by the <xref:System.Xml.Serialization.XmlSchemaImporter> to create mappings.</span></span>|  
  
## <a name="parent-elements"></a><span data-ttu-id="99517-111">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="99517-111">Parent Elements</span></span>  
  
|<span data-ttu-id="99517-112">Élément</span><span class="sxs-lookup"><span data-stu-id="99517-112">Element</span></span>|<span data-ttu-id="99517-113">Description</span><span class="sxs-lookup"><span data-stu-id="99517-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="99517-114">\<system.xml.serialization>, élément</span><span class="sxs-lookup"><span data-stu-id="99517-114">\<system.xml.serialization> Element</span></span>](../../../docs/standard/serialization/system-xml-serialization-element.md)|<span data-ttu-id="99517-115">Élément de niveau supérieur permettant de contrôler la sérialisation XML.</span><span class="sxs-lookup"><span data-stu-id="99517-115">The top-level element for controlling XML serialization.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="99517-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="99517-116">Example</span></span>  
 <span data-ttu-id="99517-117">L'exemple de code suivant illustre comment ajouter des types utilisés par <xref:System.Xml.Serialization.XmlSchemaImporter> lors du mappage de types XSD en types .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="99517-117">The following code example illustrates how to add types that are used by the <xref:System.Xml.Serialization.XmlSchemaImporter> when mapping XSD types to .NET Framework types.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="99517-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99517-118">See Also</span></span>  
 <xref:System.Xml.Serialization.XmlSchemaImporter>  
 <xref:System.Xml.Serialization.Configuration.DateTimeSerializationSection.DateTimeSerializationMode>  
 [<span data-ttu-id="99517-119">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="99517-119">Configuration File Schema</span></span>](../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="99517-120">\<dateTimeSerialization>, élément</span><span class="sxs-lookup"><span data-stu-id="99517-120">\<dateTimeSerialization> Element</span></span>](../../../docs/standard/serialization/datetimeserialization-element.md)  
 [<span data-ttu-id="99517-121">\<Ajouter > élément pour \<schemaImporterExtensions ></span><span class="sxs-lookup"><span data-stu-id="99517-121">\<add> Element for \<schemaImporterExtensions></span></span>](../../../docs/standard/serialization/add-element-for-schemaimporterextensions.md)  
 [<span data-ttu-id="99517-122">\<system.xml.serialization>, élément</span><span class="sxs-lookup"><span data-stu-id="99517-122">\<system.xml.serialization> Element</span></span>](../../../docs/standard/serialization/system-xml-serialization-element.md)
