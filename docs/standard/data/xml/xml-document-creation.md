---
title: "Création d'un document XML"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
ms.assetid: 877e9c62-b082-4bfb-bc5b-f47297eb30ef
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: ea67841e44d8d88d2effec92eb1668142c1510f2
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="xml-document-creation"></a><span data-ttu-id="d964c-102">Création d'un document XML</span><span class="sxs-lookup"><span data-stu-id="d964c-102">XML Document Creation</span></span>
<span data-ttu-id="d964c-103">Il existe deux façons de créer un document XML.</span><span class="sxs-lookup"><span data-stu-id="d964c-103">There are two ways to create an XML document.</span></span> <span data-ttu-id="d964c-104">L'une consiste à créer un objet **XmlDocument**, sans paramètre.</span><span class="sxs-lookup"><span data-stu-id="d964c-104">One way is to create an **XmlDocument** with no parameters.</span></span> <span data-ttu-id="d964c-105">L'autre consiste à créer un objet **XmlDocument** et à le passer à XmlNameTable sous la forme d'un paramètre.</span><span class="sxs-lookup"><span data-stu-id="d964c-105">The other way is to create an **XmlDocument** and pass it an XmlNameTable as a parameter.</span></span> <span data-ttu-id="d964c-106">L'exemple suivant indique comment créer un nouveau **XmlDocument** vide dépourvu de paramètre.</span><span class="sxs-lookup"><span data-stu-id="d964c-106">The following example shows how to create a new, empty **XmlDocument** using no parameters.</span></span>  
  
```vb  
Dim doc As New XmlDocument()  
```  
  
```csharp  
XmlDocument doc = new XmlDocument();  
```  
  
 <span data-ttu-id="d964c-107">Une fois le document créé, vous pouvez y charger des données à partir d'une chaîne, d'un flux, d'une URL, d'un lecteur de texte ou d'une classe dérivée **XmlReader** à l'aide de la méthode **Load**.</span><span class="sxs-lookup"><span data-stu-id="d964c-107">Once a document is created, you can load it with data from a string, stream, URL, text reader, or an **XmlReader** derived class using the **Load** method.</span></span> <span data-ttu-id="d964c-108">Il existe également une autre méthode de chargement, appelée **LoadXML**, qui lit le contenu XML d'une chaîne.</span><span class="sxs-lookup"><span data-stu-id="d964c-108">There is also another load method, the **LoadXML** method, which reads XML from a string.</span></span> <span data-ttu-id="d964c-109">Pour plus d'informations sur les diverses méthodes **Load**, consultez [Lecture d'un document XML vers le DOM](../../../../docs/standard/data/xml/reading-an-xml-document-into-the-dom.md).</span><span class="sxs-lookup"><span data-stu-id="d964c-109">For more information on the various **Load** methods, see [Reading an XML Document into the DOM](../../../../docs/standard/data/xml/reading-an-xml-document-into-the-dom.md).</span></span>  
  
 <span data-ttu-id="d964c-110">Il existe une classe appelée **XmlNameTable**.</span><span class="sxs-lookup"><span data-stu-id="d964c-110">There is a class called the **XmlNameTable**.</span></span> <span data-ttu-id="d964c-111">Cette classe est une table d'objets chaîne atomisés.</span><span class="sxs-lookup"><span data-stu-id="d964c-111">This class is a table of atomized string objects.</span></span> <span data-ttu-id="d964c-112">Cette table constitue un moyen efficace pour que l'analyseur XML utilise le même objet chaîne pour tous les noms d'éléments et d'attributs répétés dans un document XML.</span><span class="sxs-lookup"><span data-stu-id="d964c-112">This table provides an efficient means for the XML parser to use the same string object for all repeated element and attribute names in an XML document.</span></span> <span data-ttu-id="d964c-113">Un objet **XmlNameTable** est créé automatiquement lors de la création d'un document, comme le montre l'exemple ci-avant, et est chargé avec des noms d'attributs et d'éléments lors du chargement du document.</span><span class="sxs-lookup"><span data-stu-id="d964c-113">An **XmlNameTable** is automatically created when a document is created as shown above and is loaded with attribute and element names when the document is loaded.</span></span> <span data-ttu-id="d964c-114">Si vous disposez déjà d'un document possédant une table de noms, et que ces noms pourraient être employés utilement dans un autre document, vous pouvez créer un nouveau document à l'aide de la méthode **Load** qui prend **XmlNameTable** comme paramètre.</span><span class="sxs-lookup"><span data-stu-id="d964c-114">If you already have a document with a name table, and those names would be useful in another document, you can create a new document using the **Load** method that takes an **XmlNameTable** as a parameter.</span></span> <span data-ttu-id="d964c-115">Lorsque le document est créé avec cette méthode, il utilise le **XmlNameTable** existant avec tous les attributs et éléments déjà chargés en son sein à partir de l'autre document.</span><span class="sxs-lookup"><span data-stu-id="d964c-115">When the document is created with this method, it uses the existing **XmlNameTable** with all the attributes and elements already loaded into it from the other document.</span></span> <span data-ttu-id="d964c-116">Celui-ci peut être employé pour comparer efficacement des noms d'éléments et d'attributs.</span><span class="sxs-lookup"><span data-stu-id="d964c-116">It can be used for efficiently comparing element and attribute names.</span></span> <span data-ttu-id="d964c-117">Pour plus d'informations sur **XmlNameTable**, consultez [Comparaison d'objets à l'aide de XmlNameTable](../../../../docs/standard/data/xml/object-comparison-using-xmlnametable.md).</span><span class="sxs-lookup"><span data-stu-id="d964c-117">For more information on the **XmlNameTable**, see [Object Comparison Using XmlNameTable](../../../../docs/standard/data/xml/object-comparison-using-xmlnametable.md).</span></span> <span data-ttu-id="d964c-118">Pour référence, consultez <xref:System.Xml.XmlNameTable>.</span><span class="sxs-lookup"><span data-stu-id="d964c-118">For reference, see <xref:System.Xml.XmlNameTable>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d964c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d964c-119">See Also</span></span>  
 [<span data-ttu-id="d964c-120">DOM (Document Object Model) XML</span><span class="sxs-lookup"><span data-stu-id="d964c-120">XML Document Object Model (DOM)</span></span>](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
