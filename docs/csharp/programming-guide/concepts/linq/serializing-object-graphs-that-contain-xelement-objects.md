---
title: Sérialisation de graphiques d’objets qui contiennent des objets XElement (C#)
ms.date: 07/20/2015
ms.assetid: fcbc3951-3cc4-4d0f-9259-e97549ed68f0
ms.openlocfilehash: 2e82165421d31ec234de4806b59565fa675217ef
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2018
ms.locfileid: "45618446"
---
# <a name="serializing-object-graphs-that-contain-xelement-objects-c"></a><span data-ttu-id="a1fbe-102">Sérialisation de graphiques d’objets qui contiennent des objets XElement (C#)</span><span class="sxs-lookup"><span data-stu-id="a1fbe-102">Serializing Object Graphs that Contain XElement Objects (C#)</span></span>
<span data-ttu-id="a1fbe-103">Cette rubrique présente la fonctionnalité de sérialisation de graphiques d'objets qui contiennent des références à des objets de type <xref:System.Xml.Linq.XElement>.</span><span class="sxs-lookup"><span data-stu-id="a1fbe-103">This topic introduces the capability of serializing object graphs that contain references to objects of type <xref:System.Xml.Linq.XElement>.</span></span> <span data-ttu-id="a1fbe-104">Afin de faciliter ce type de sérialisation, <xref:System.Xml.Linq.XElement> implémente l'interface <xref:System.Xml.Serialization.IXmlSerializable>.</span><span class="sxs-lookup"><span data-stu-id="a1fbe-104">To facility this type of serializing, <xref:System.Xml.Linq.XElement> implements the <xref:System.Xml.Serialization.IXmlSerializable> interface.</span></span>  
  
 <span data-ttu-id="a1fbe-105">Notez que seule la classe <xref:System.Xml.Linq.XElement> implémente la sérialisation.</span><span class="sxs-lookup"><span data-stu-id="a1fbe-105">Note that only the <xref:System.Xml.Linq.XElement> class implements serialization.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="a1fbe-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="a1fbe-106">In This Section</span></span>  
  
|<span data-ttu-id="a1fbe-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="a1fbe-107">Topic</span></span>|<span data-ttu-id="a1fbe-108">Description</span><span class="sxs-lookup"><span data-stu-id="a1fbe-108">Description</span></span>|  
|-----------|-----------------|  
|[<span data-ttu-id="a1fbe-109">Guide pratique pour sérialiser à l’aide de XmlSerializer (C#)</span><span class="sxs-lookup"><span data-stu-id="a1fbe-109">How to: Serialize Using XmlSerializer (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-serialize-using-xmlserializer.md)|<span data-ttu-id="a1fbe-110">Montre comment sérialiser à l'aide de <xref:System.Xml.Serialization.XmlSerializer>.</span><span class="sxs-lookup"><span data-stu-id="a1fbe-110">Demonstrates how to serialize using <xref:System.Xml.Serialization.XmlSerializer>.</span></span>|  
|[<span data-ttu-id="a1fbe-111">Guide pratique pour sérialiser à l’aide de DataContractSerializer (C#)</span><span class="sxs-lookup"><span data-stu-id="a1fbe-111">How to: Serialize Using DataContractSerializer (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-serialize-using-datacontractserializer.md)|<span data-ttu-id="a1fbe-112">Montre comment sérialiser à l'aide de <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="a1fbe-112">Demonstrates how to serialize using <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a1fbe-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1fbe-113">See Also</span></span>

- [<span data-ttu-id="a1fbe-114">Programmation LINQ to XML avancée (C#)</span><span class="sxs-lookup"><span data-stu-id="a1fbe-114">Advanced LINQ to XML Programming (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/advanced-linq-to-xml-programming.md)
