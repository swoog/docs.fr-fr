---
title: "Collections de nœuds dans NamedNodeMap et NodeList"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 025954b8-7aa8-47c5-a1c1-f81064fb4d65
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: ff327c1a450e9ce712d496bdca2cd2ebbff6adda
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="node-collections-in-namednodemaps-and-nodelists"></a><span data-ttu-id="9b7d2-102">Collections de nœuds dans NamedNodeMap et NodeList</span><span class="sxs-lookup"><span data-stu-id="9b7d2-102">Node Collections in NamedNodeMaps and NodeLists</span></span>
<span data-ttu-id="9b7d2-103">Il est possible d’extraire une collection de nœuds et de les placer dans une collection triée ou non.</span><span class="sxs-lookup"><span data-stu-id="9b7d2-103">You can retrieve a set of nodes and put it in an ordered or unordered collection.</span></span> <span data-ttu-id="9b7d2-104">Si vous regroupez une collection de nœuds dans une collection non triée, cet ensemble est appelé NamedNodeMap par le World Wide Web Consortium (W3C). Ce type de collection vous permet d’extraire des données au moyen de leur nom ou de l’index.</span><span class="sxs-lookup"><span data-stu-id="9b7d2-104">When putting a set of nodes into an unordered collection, the set is called a NamedNodeMap by the World Wide Web Consortium (W3C); you can retrieve the data by name or index in this type of collection.</span></span> <span data-ttu-id="9b7d2-105">En revanche, si vous placez une collection de nœuds dans une collection triée, celle-ci est appelée NodeList par le W3C, et ses données peuvent être extraites au moyen d'un index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="9b7d2-105">Putting a set of nodes in an ordered collection is called a NodeList by the W3C, and the data can be retrieved by a zero-based index.</span></span> <span data-ttu-id="9b7d2-106">NamedNodeMap et NodeList sont décrits par le W3C.</span><span class="sxs-lookup"><span data-stu-id="9b7d2-106">NamedNodeMaps and NodeLists are described by the W3C.</span></span> <span data-ttu-id="9b7d2-107">Leurs implémentations dans Microsoft .NET Framework sont **XmlNamedNodeMap** pour NamedNodeMap et **XmlNodeList** pour NodeList.</span><span class="sxs-lookup"><span data-stu-id="9b7d2-107">The implementations in the Microsoft .NET Framework for the NamedNodeMap is the **XmlNamedNodeMap**, and the NodeList is implemented by the **XmlNodeList**.</span></span>  
  
 <span data-ttu-id="9b7d2-108">Pour obtenir des informations sur la collection non triée, consultez [Extraction de nœuds non triés par leur nom ou par l’index](../../../../docs/standard/data/xml/unordered-node-retrieval-by-name-or-index.md).</span><span class="sxs-lookup"><span data-stu-id="9b7d2-108">For information on the unordered collection, see [Unordered Node Retrieval by Name or Index](../../../../docs/standard/data/xml/unordered-node-retrieval-by-name-or-index.md).</span></span> <span data-ttu-id="9b7d2-109">Pour obtenir des informations sur la collection triée, consultez [Extraction de nœuds triés par l’index](../../../../docs/standard/data/xml/ordered-node-retrieval-by-index.md).</span><span class="sxs-lookup"><span data-stu-id="9b7d2-109">For information on the ordered collection, see [Ordered Node Retrieval by Index](../../../../docs/standard/data/xml/ordered-node-retrieval-by-index.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9b7d2-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b7d2-110">See Also</span></span>  
 [<span data-ttu-id="9b7d2-111">DOM (Document Object Model) XML</span><span class="sxs-lookup"><span data-stu-id="9b7d2-111">XML Document Object Model (DOM)</span></span>](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
