---
title: "Mises à jour dynamiques de NodeList et NamedNodeMap"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 76c511fd-6704-4ca4-8078-860a68d898ad
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 8a7abbb7344530ca993b8d07b774da17e6d0349b
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="dynamic-updates-to-nodelists-and-namednodemaps"></a><span data-ttu-id="e3550-102">Mises à jour dynamiques de NodeList et NamedNodeMap</span><span class="sxs-lookup"><span data-stu-id="e3550-102">Dynamic Updates to NodeLists and NamedNodeMaps</span></span>
<span data-ttu-id="e3550-103">Dans la mesure où **XmlNodeList** et **XmlNamedNodeMap** contiennent une collection de nœuds, mais où le document XML est chargé en mémoire et est modifié, le World Wide Web Consortium (W3C) établit que ces objets contenant des collections de nœuds doivent être dynamiques.</span><span class="sxs-lookup"><span data-stu-id="e3550-103">Because the **XmlNodeList** and the **XmlNamedNodeMap** contain a set of nodes, yet the XML document is loaded into memory and is being modified, the World Wide Web Consortium (W3C) states that these objects that contain sets of nodes need to be dynamic.</span></span> <span data-ttu-id="e3550-104">Dès lors, si le document sous-jacent change, les données figurant dans ces deux objets doivent changer également.</span><span class="sxs-lookup"><span data-stu-id="e3550-104">That is, if the underlying document changes, then the data in these two objects should change also.</span></span> <span data-ttu-id="e3550-105">C'est pourquoi, si vous avez un **XmlNodeList** contenant tous les éléments enfants d'un élément particulier (par exemple, l'élément X), vous ajoutez un élément supplémentaire, l'élément Q, au document sous l'élément X. Le **XmlNodeList** doit également avoir le nouvel élément Q ajouté à sa collection.</span><span class="sxs-lookup"><span data-stu-id="e3550-105">Therefore, if you have an **XmlNodeList** that contains all the child elements of a particular element (for example, element X), then you add an additional element, element Q, to the document under element X. The **XmlNodeList** should also have that new element Q added to its collection.</span></span> <span data-ttu-id="e3550-106">L'inverse est vrai également.</span><span class="sxs-lookup"><span data-stu-id="e3550-106">The same is true in reverse.</span></span> <span data-ttu-id="e3550-107">Si un nœud est ajouté à **XmlNodeList**, le document sous-jacent est mis à jour en conséquence.</span><span class="sxs-lookup"><span data-stu-id="e3550-107">If a node is added to the **XmlNodeList**, the underlying document is updated as well.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e3550-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3550-108">See Also</span></span>  
 [<span data-ttu-id="e3550-109">DOM (Document Object Model) XML</span><span class="sxs-lookup"><span data-stu-id="e3550-109">XML Document Object Model (DOM)</span></span>](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
