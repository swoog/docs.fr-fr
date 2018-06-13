---
title: Suppression de nœuds du DOM
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: 0a98e0ca-0555-45c1-ab69-0d8d20ca1abd
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ec786564e6246f10e10d600f4822442884323557
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33568457"
---
# <a name="removing-nodes-from-the-dom"></a><span data-ttu-id="48d14-102">Suppression de nœuds du DOM</span><span class="sxs-lookup"><span data-stu-id="48d14-102">Removing Nodes from the DOM</span></span>
<span data-ttu-id="48d14-103">Pour supprimer un nœud du DOM (Document Object Model) XML, utilisez la méthode <xref:System.Xml.XmlNode.RemoveChild%2A>.</span><span class="sxs-lookup"><span data-stu-id="48d14-103">To remove a node from the XML Document Object Model (DOM), use the <xref:System.Xml.XmlNode.RemoveChild%2A> method to remove a specific node.</span></span> <span data-ttu-id="48d14-104">La méthode supprime le sous-arbre appartenant au nœud en cours de suppression, du moins s'il ne s'agit pas d'un nœud sans descendant.</span><span class="sxs-lookup"><span data-stu-id="48d14-104">When you remove a node, the method removes the subtree belonging to the node being removed; that is, if it is not a leaf node.</span></span>  
  
 <span data-ttu-id="48d14-105">Pour supprimer plusieurs nœuds du DOM, utilisez la méthode <xref:System.Xml.XmlNode.RemoveAll%2A>, qui permet de supprimer tous les enfants et attributs (le cas échéant) du nœud actuel.</span><span class="sxs-lookup"><span data-stu-id="48d14-105">To remove multiple nodes from the DOM, use the <xref:System.Xml.XmlNode.RemoveAll%2A> method to remove all the children and attributes, if applicable, of the current node.</span></span>  
  
 <span data-ttu-id="48d14-106">Si vous travaillez avec un objet <xref:System.Xml.XmlNamedNodeMap>, vous pouvez supprimer un nœud à l'aide de la méthode <xref:System.Xml.XmlNamedNodeMap.RemoveNamedItem%2A>.</span><span class="sxs-lookup"><span data-stu-id="48d14-106">If you are working with an <xref:System.Xml.XmlNamedNodeMap>, you can remove a node using the <xref:System.Xml.XmlNamedNodeMap.RemoveNamedItem%2A> method.</span></span>  
  
 <span data-ttu-id="48d14-107">Pour plus d'informations sur la suppression d'attributs, consultez [Suppression d'attributs d'un nœud d'élément dans le DOM](../../../../docs/standard/data/xml/removing-attributes-from-an-element-node-in-the-dom.md).</span><span class="sxs-lookup"><span data-stu-id="48d14-107">To remove attributes, see [Removing Attributes from an Element Node in the DOM](../../../../docs/standard/data/xml/removing-attributes-from-an-element-node-in-the-dom.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="48d14-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48d14-108">See Also</span></span>  
 [<span data-ttu-id="48d14-109">DOM (Document Object Model) XML</span><span class="sxs-lookup"><span data-stu-id="48d14-109">XML Document Object Model (DOM)</span></span>](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
