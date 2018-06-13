---
title: Modification de données XML à l’aide de XPathNavigator
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: b1f91616-3115-4264-9821-c66589d11d11
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5c7eb77689c8f7e447ddfb42ff96de3458d3a3b3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33568587"
---
# <a name="editing-xml-data-using-xpathnavigator"></a><span data-ttu-id="03b02-102">Modification de données XML à l’aide de XPathNavigator</span><span class="sxs-lookup"><span data-stu-id="03b02-102">Editing XML Data using XPathNavigator</span></span>
<span data-ttu-id="03b02-103">La classe <xref:System.Xml.XPath.XPathNavigator> fournit des méthodes permettant d'insérer, de modifier et de supprimer des nœuds et des valeurs d'un document XML contenu dans un objet <xref:System.Xml.XmlDocument>.</span><span class="sxs-lookup"><span data-stu-id="03b02-103">The <xref:System.Xml.XPath.XPathNavigator> class provides methods to insert, modify and remove nodes and values from an XML document contained in an <xref:System.Xml.XmlDocument> object.</span></span> <span data-ttu-id="03b02-104">Pour pouvoir utiliser ces méthodes afin d'insérer, de modifier et de supprimer des nœuds et des valeurs, vous devez pouvoir modifier l'objet <xref:System.Xml.XPath.XPathNavigator>, ce qui signifie que sa propriété <xref:System.Xml.XPath.XPathNavigator.CanEdit%2A> doit être définie sur true.</span><span class="sxs-lookup"><span data-stu-id="03b02-104">In order to use any of these methods to insert, modify, and remove nodes and values, the <xref:System.Xml.XPath.XPathNavigator> object must be editable, that is, its <xref:System.Xml.XPath.XPathNavigator.CanEdit%2A> property must be true.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="03b02-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="03b02-105">In This Section</span></span>  
 [<span data-ttu-id="03b02-106">Insertion de données XML à l’aide de XPathNavigator</span><span class="sxs-lookup"><span data-stu-id="03b02-106">Insert XML Data using XPathNavigator</span></span>](../../../../docs/standard/data/xml/insert-xml-data-using-xpathnavigator.md)  
 <span data-ttu-id="03b02-107">Décrit la façon d'insérer des nœuds frères, enfants et d'attribut ainsi que des valeurs dans un objet <xref:System.Xml.XmlDocument> à l'aide de la classe <xref:System.Xml.XPath.XPathNavigator>.</span><span class="sxs-lookup"><span data-stu-id="03b02-107">Describes how to insert sibling, child, attribute nodes and values in to an <xref:System.Xml.XmlDocument> object using the <xref:System.Xml.XPath.XPathNavigator> class.</span></span>  
  
 [<span data-ttu-id="03b02-108">Modification de données XML à l’aide de XPathNavigator</span><span class="sxs-lookup"><span data-stu-id="03b02-108">Modify XML Data using XPathNavigator</span></span>](../../../../docs/standard/data/xml/modify-xml-data-using-xpathnavigator.md)  
 <span data-ttu-id="03b02-109">Décrit la façon de modifier des nœuds et des valeurs dans un objet <xref:System.Xml.XmlDocument> à l'aide de la classe <xref:System.Xml.XPath.XPathNavigator>.</span><span class="sxs-lookup"><span data-stu-id="03b02-109">Describes how to modify nodes and values in an <xref:System.Xml.XmlDocument> object using the <xref:System.Xml.XPath.XPathNavigator> class.</span></span>  
  
 [<span data-ttu-id="03b02-110">Suppression de données XML à l’aide de XPathNavigator</span><span class="sxs-lookup"><span data-stu-id="03b02-110">Remove XML Data using XPathNavigator</span></span>](../../../../docs/standard/data/xml/remove-xml-data-using-xpathnavigator.md)  
 <span data-ttu-id="03b02-111">Décrit la façon de supprimer des nœuds et des valeurs d'un objet <xref:System.Xml.XmlDocument> à l'aide de la classe <xref:System.Xml.XPath.XPathNavigator>.</span><span class="sxs-lookup"><span data-stu-id="03b02-111">Describes how to remove nodes and values from an <xref:System.Xml.XmlDocument> object using the <xref:System.Xml.XPath.XPathNavigator> class.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="03b02-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03b02-112">See Also</span></span>  
 <xref:System.Xml.XmlDocument>  
 <xref:System.Xml.XPath.XPathDocument>  
 <xref:System.Xml.XPath.XPathNavigator>  
 [<span data-ttu-id="03b02-113">Traitement des données XML à l’aide du modèle de données XPath</span><span class="sxs-lookup"><span data-stu-id="03b02-113">Process XML Data Using the XPath Data Model</span></span>](../../../../docs/standard/data/xml/process-xml-data-using-the-xpath-data-model.md)  
 [<span data-ttu-id="03b02-114">Lecture de données XML à l’aide de XPathDocument et XmlDocument</span><span class="sxs-lookup"><span data-stu-id="03b02-114">Reading XML Data using XPathDocument and XmlDocument</span></span>](../../../../docs/standard/data/xml/reading-xml-data-using-xpathdocument-and-xmldocument.md)  
 [<span data-ttu-id="03b02-115">Sélection, évaluation et mise en correspondance de données XML à l’aide de XPathNavigator</span><span class="sxs-lookup"><span data-stu-id="03b02-115">Selecting, Evaluating and Matching XML Data using XPathNavigator</span></span>](../../../../docs/standard/data/xml/selecting-evaluating-and-matching-xml-data-using-xpathnavigator.md)  
 [<span data-ttu-id="03b02-116">Accès à des données XML à l’aide de XPathNavigator</span><span class="sxs-lookup"><span data-stu-id="03b02-116">Accessing XML Data using XPathNavigator</span></span>](../../../../docs/standard/data/xml/accessing-xml-data-using-xpathnavigator.md)  
 [<span data-ttu-id="03b02-117">Validation de schéma à l’aide de XPathNavigator</span><span class="sxs-lookup"><span data-stu-id="03b02-117">Schema Validation using XPathNavigator</span></span>](../../../../docs/standard/data/xml/schema-validation-using-xpathnavigator.md)
