---
title: Sérialisation de graphiques d’objets qui contiennent des objets XElement (C#)
ms.date: 07/20/2015
ms.assetid: fcbc3951-3cc4-4d0f-9259-e97549ed68f0
ms.openlocfilehash: db7354598fc84c6fa3f8ec4e5b53799030459387
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54569139"
---
# <a name="serializing-object-graphs-that-contain-xelement-objects-c"></a><span data-ttu-id="c0e89-102">Sérialisation de graphiques d’objets qui contiennent des objets XElement (C#)</span><span class="sxs-lookup"><span data-stu-id="c0e89-102">Serializing Object Graphs that Contain XElement Objects (C#)</span></span>
<span data-ttu-id="c0e89-103">Cette rubrique présente la fonctionnalité de sérialisation de graphiques d'objets qui contiennent des références à des objets de type <xref:System.Xml.Linq.XElement>.</span><span class="sxs-lookup"><span data-stu-id="c0e89-103">This topic introduces the capability of serializing object graphs that contain references to objects of type <xref:System.Xml.Linq.XElement>.</span></span> <span data-ttu-id="c0e89-104">Afin de faciliter ce type de sérialisation, <xref:System.Xml.Linq.XElement> implémente l'interface <xref:System.Xml.Serialization.IXmlSerializable>.</span><span class="sxs-lookup"><span data-stu-id="c0e89-104">To facility this type of serializing, <xref:System.Xml.Linq.XElement> implements the <xref:System.Xml.Serialization.IXmlSerializable> interface.</span></span>  
  
 <span data-ttu-id="c0e89-105">Notez que seule la classe <xref:System.Xml.Linq.XElement> implémente la sérialisation.</span><span class="sxs-lookup"><span data-stu-id="c0e89-105">Note that only the <xref:System.Xml.Linq.XElement> class implements serialization.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="c0e89-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="c0e89-106">In This Section</span></span>  
  
|<span data-ttu-id="c0e89-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="c0e89-107">Topic</span></span>|<span data-ttu-id="c0e89-108">Description</span><span class="sxs-lookup"><span data-stu-id="c0e89-108">Description</span></span>|  
|-----------|-----------------|  
|[<span data-ttu-id="c0e89-109">Guide pratique pour Sérialiser à l’aide de XmlSerializer (C#)</span><span class="sxs-lookup"><span data-stu-id="c0e89-109">How to: Serialize Using XmlSerializer (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-serialize-using-xmlserializer.md)|<span data-ttu-id="c0e89-110">Montre comment sérialiser à l'aide de <xref:System.Xml.Serialization.XmlSerializer>.</span><span class="sxs-lookup"><span data-stu-id="c0e89-110">Demonstrates how to serialize using <xref:System.Xml.Serialization.XmlSerializer>.</span></span>|  
|[<span data-ttu-id="c0e89-111">Guide pratique pour sérialiser à l’aide de DataContractSerializer (C#)</span><span class="sxs-lookup"><span data-stu-id="c0e89-111">How to: Serialize Using DataContractSerializer (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-serialize-using-datacontractserializer.md)|<span data-ttu-id="c0e89-112">Montre comment sérialiser à l'aide de <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="c0e89-112">Demonstrates how to serialize using <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c0e89-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0e89-113">See also</span></span>

- [<span data-ttu-id="c0e89-114">Programmation LINQ to XML avancée (C#)</span><span class="sxs-lookup"><span data-stu-id="c0e89-114">Advanced LINQ to XML Programming (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/advanced-linq-to-xml-programming.md)
