---
title: Sérialisation d’arborescences XML (C#)
ms.date: 07/20/2015
ms.assetid: b3937e54-4ce9-4236-ac96-14e7972aa594
ms.openlocfilehash: 8f372a05bd69b801085cba9d9a3b11ae01841a2c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33338349"
---
# <a name="serializing-xml-trees-c"></a><span data-ttu-id="b68e7-102">Sérialisation d’arborescences XML (C#)</span><span class="sxs-lookup"><span data-stu-id="b68e7-102">Serializing XML Trees (C#)</span></span>
<span data-ttu-id="b68e7-103">Sérialiser une arborescence XML signifie générer du code XML à partir de l'arborescence XML.</span><span class="sxs-lookup"><span data-stu-id="b68e7-103">Serializing an XML tree means generating XML from the XML tree.</span></span> <span data-ttu-id="b68e7-104">Vous pouvez sérialiser vers un fichier, vers une implémentation concrète de la classe <xref:System.IO.TextWriter> ou vers une implémentation concrète d'un objet <xref:System.Xml.XmlWriter>.</span><span class="sxs-lookup"><span data-stu-id="b68e7-104">You can serialize to a file, to a concrete implementation of the <xref:System.IO.TextWriter> class, or to a concrete implementation of an <xref:System.Xml.XmlWriter>.</span></span>  
  
 <span data-ttu-id="b68e7-105">Vous pouvez contrôler divers aspects de la sérialisation.</span><span class="sxs-lookup"><span data-stu-id="b68e7-105">You can control various aspects of serialization.</span></span> <span data-ttu-id="b68e7-106">Par exemple, vous pouvez contrôler s'il faut mettre en retrait le code XML sérialisé et s'il faut écrire une déclaration XML.</span><span class="sxs-lookup"><span data-stu-id="b68e7-106">For example, you can control whether to indent the serialized XML, and whether to write an XML declaration.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="b68e7-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b68e7-107">In This Section</span></span>  
  
|<span data-ttu-id="b68e7-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b68e7-108">Topic</span></span>|<span data-ttu-id="b68e7-109">Description</span><span class="sxs-lookup"><span data-stu-id="b68e7-109">Description</span></span>|  
|-----------|-----------------|  
|[<span data-ttu-id="b68e7-110">Conservation des espaces blancs lors de la sérialisation</span><span class="sxs-lookup"><span data-stu-id="b68e7-110">Preserving White Space While Serializing</span></span>](../../../../csharp/programming-guide/concepts/linq/preserving-white-space-while-serializing.md)|<span data-ttu-id="b68e7-111">Décrit comment contrôler le comportement d’espace blanc lors de la sérialisation d’arborescences XML.</span><span class="sxs-lookup"><span data-stu-id="b68e7-111">Describes how to control white space behavior when you serialize XML trees.</span></span>|  
|[<span data-ttu-id="b68e7-112">Sérialisation avec une déclaration XML (C#)</span><span class="sxs-lookup"><span data-stu-id="b68e7-112">Serializing with an XML Declaration (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/serializing-with-an-xml-declaration.md)|<span data-ttu-id="b68e7-113">Décrit comment sérialiser une arborescence XML qui inclut une déclaration XML.</span><span class="sxs-lookup"><span data-stu-id="b68e7-113">Describes how to serialize an XML tree that includes an XML declaration.</span></span>|  
|[<span data-ttu-id="b68e7-114">Sérialisation vers des fichiers, TextWriters et XmlWriters</span><span class="sxs-lookup"><span data-stu-id="b68e7-114">Serializing to Files, TextWriters, and XmlWriters</span></span>](../../../../csharp/programming-guide/concepts/linq/serializing-to-files-textwriters-and-xmlwriters.md)|<span data-ttu-id="b68e7-115">Décrit comment sérialiser un document vers un objet <xref:System.IO.File>, <xref:System.IO.TextWriter> ou <xref:System.Xml.XmlWriter>.</span><span class="sxs-lookup"><span data-stu-id="b68e7-115">Describes how to serialize a document to a <xref:System.IO.File>, a <xref:System.IO.TextWriter>, or an <xref:System.Xml.XmlWriter>.</span></span>|  
|[<span data-ttu-id="b68e7-116">Sérialisation vers un XmlReader (appel de XSLT) (C#)</span><span class="sxs-lookup"><span data-stu-id="b68e7-116">Serializing to an XmlReader (Invoking XSLT) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/serializing-to-an-xmlreader-invoking-xslt.md)|<span data-ttu-id="b68e7-117">Décrit comment créer un objet <xref:System.Xml.XmlReader> qui permet à un autre module de lire le contenu d'une arborescence XML.</span><span class="sxs-lookup"><span data-stu-id="b68e7-117">Describes how to create a <xref:System.Xml.XmlReader> that enables another module to read the contents of an XML tree.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b68e7-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b68e7-118">See Also</span></span>  
 [<span data-ttu-id="b68e7-119">Guide de programmation (LINQ to XML) (C#)</span><span class="sxs-lookup"><span data-stu-id="b68e7-119">Programming Guide (LINQ to XML) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/programming-guide-linq-to-xml.md)
