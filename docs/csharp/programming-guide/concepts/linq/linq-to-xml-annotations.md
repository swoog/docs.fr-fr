---
title: Annotations LINQ to XML3
ms.date: 07/20/2015
ms.assetid: 54e7b9d0-07f5-488f-9065-b6e6b870f810
ms.openlocfilehash: 8b8e03b0174ad2bf044c21eb9a9d3391da37fb7f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33320116"
---
# <a name="linq-to-xml-annotations"></a><span data-ttu-id="b85a2-102">Annotations LINQ to XML</span><span class="sxs-lookup"><span data-stu-id="b85a2-102">LINQ to XML Annotations</span></span>
<span data-ttu-id="b85a2-103">Les annotations dans [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] vous permettent d’associer n’importe quel objet arbitraire de n’importe quel type arbitraire à n’importe quel composant XML dans une arborescence XML.</span><span class="sxs-lookup"><span data-stu-id="b85a2-103">Annotations in [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] enable you to associate any arbitrary object of any arbitrary type with any XML component in an XML tree.</span></span>  
  
 <span data-ttu-id="b85a2-104">Pour ajouter une annotation à un composant XML, tel qu'un objet <xref:System.Xml.Linq.XElement> ou <xref:System.Xml.Linq.XAttribute>, vous appelez la méthode <xref:System.Xml.Linq.XObject.AddAnnotation%2A>.</span><span class="sxs-lookup"><span data-stu-id="b85a2-104">To add an annotation to an XML component, such as an <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XAttribute>, you call the <xref:System.Xml.Linq.XObject.AddAnnotation%2A> method.</span></span> <span data-ttu-id="b85a2-105">Vous pouvez récupérer des annotations par type.</span><span class="sxs-lookup"><span data-stu-id="b85a2-105">You retrieve annotations by type.</span></span>  
  
 <span data-ttu-id="b85a2-106">Notez que les annotations ne font pas partie du jeu d'informations XML ; elles ne sont pas sérialisées ou désérialisées.</span><span class="sxs-lookup"><span data-stu-id="b85a2-106">Note that annotations are not part of the XML infoset; they are not serialized or deserialized.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b85a2-107">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b85a2-107">Methods</span></span>  
 <span data-ttu-id="b85a2-108">Vous pouvez utiliser les méthodes suivantes lorsque vous travaillez avec des annotations :</span><span class="sxs-lookup"><span data-stu-id="b85a2-108">You can use the following methods when working with annotations:</span></span>  
  
|<span data-ttu-id="b85a2-109">Méthode</span><span class="sxs-lookup"><span data-stu-id="b85a2-109">Method</span></span>|<span data-ttu-id="b85a2-110">Description</span><span class="sxs-lookup"><span data-stu-id="b85a2-110">Description</span></span>|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XObject.AddAnnotation%2A>|<span data-ttu-id="b85a2-111">Ajoute un objet à la liste d'annotation de <xref:System.Xml.Linq.XObject>.</span><span class="sxs-lookup"><span data-stu-id="b85a2-111">Adds an object to the annotation list of an <xref:System.Xml.Linq.XObject>.</span></span>|  
|<xref:System.Xml.Linq.XObject.Annotation%2A>|<span data-ttu-id="b85a2-112">Obtient le premier objet annotation du type spécifié de <xref:System.Xml.Linq.XObject>.</span><span class="sxs-lookup"><span data-stu-id="b85a2-112">Gets the first annotation object of the specified type from an <xref:System.Xml.Linq.XObject>.</span></span>|  
|<xref:System.Xml.Linq.XObject.Annotations%2A>|<span data-ttu-id="b85a2-113">Obtient une collection d'annotations du type spécifié pour un objet <xref:System.Xml.Linq.XObject>.</span><span class="sxs-lookup"><span data-stu-id="b85a2-113">Gets a collection of annotations of the specified type for an <xref:System.Xml.Linq.XObject>.</span></span>|  
|<xref:System.Xml.Linq.XObject.RemoveAnnotations%2A>|<span data-ttu-id="b85a2-114">Supprime les annotations du type spécifié d’un objet <xref:System.Xml.Linq.XObject>.</span><span class="sxs-lookup"><span data-stu-id="b85a2-114">Removes the annotations of the specified type from an <xref:System.Xml.Linq.XObject>.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b85a2-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b85a2-115">See Also</span></span>  
 [<span data-ttu-id="b85a2-116">Programmation LINQ to XML avancée (C#)</span><span class="sxs-lookup"><span data-stu-id="b85a2-116">Advanced LINQ to XML Programming (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/advanced-linq-to-xml-programming.md)
