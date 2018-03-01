---
title: "Effet des espaces de noms sur le développement des références d'entité avec les nouveaux nœuds contenant des éléments et attributs"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 64359aee-aab0-4042-9a32-d19789af6ca7
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 9b59f85eb0ef6646345eaef2a409f622c6fe4651
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="namespace-affect-on-entity-reference-expansion-for-new-nodes-containing-elements-and-attributes"></a><span data-ttu-id="37200-102">Effet des espaces de noms sur le développement des références d'entité avec les nouveaux nœuds contenant des éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="37200-102">Namespace Affect on Entity Reference Expansion for New Nodes Containing Elements and Attributes</span></span>
<span data-ttu-id="37200-103">Le contenu d'une déclaration d'entité peut contenir pratiquement n'importe quel élément, c'est pourquoi il est possible qu'il comporte un élément tel que `<!ENTITY aname "<elem>test</elem>">`.</span><span class="sxs-lookup"><span data-stu-id="37200-103">Because the content of an entity declaration can contain almost anything, there is a possibility that the content could contain an element like `<!ENTITY aname "<elem>test</elem>">`.</span></span>  
  
 <span data-ttu-id="37200-104">Lorsque le document XML est analysé, `&aname;` n'est pas développé avec son contenu de remplacement au moment de l'analyse.</span><span class="sxs-lookup"><span data-stu-id="37200-104">When the XML is parsed, `&aname;` is not expanded with its replacement content at parse time.</span></span> <span data-ttu-id="37200-105">Le développement XML n'a pas lieu car la résolution de l'espace de noms pour l'élément ne peut se produire tant que le nœud n'est pas placé dans le document.</span><span class="sxs-lookup"><span data-stu-id="37200-105">The expansion of the XML is not done because resolution of the namespace for the element cannot occur until the node is placed in the document.</span></span> <span data-ttu-id="37200-106">Jusqu'alors, l'espace de noms figurant dans la portée n'est pas détectable.</span><span class="sxs-lookup"><span data-stu-id="37200-106">Until that time, there is no knowledge of what namespace is in scope.</span></span> <span data-ttu-id="37200-107">Lorsque le nœud est placé dans le document, la résolution de l'espace de noms se produit et le contenu d'entité résultant est analysé dans ses nœuds adéquats.</span><span class="sxs-lookup"><span data-stu-id="37200-107">When the node is put into the document, then the namespace resolution occurs, and the resulting entity content is parsed into its appropriate nodes.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="37200-108">Après que le développement a eu lieu sur un nœud de référence d'entité à peine créé, il ne peut se produire à nouveau.</span><span class="sxs-lookup"><span data-stu-id="37200-108">Once the expansion occurs on a newly created entity reference node, it never reoccurs.</span></span> <span data-ttu-id="37200-109">C'est pourquoi les espaces de noms utilisés dans le texte de remplacement de l'élément sont liés au moment de la définition du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="37200-109">Therefore, the namespaces used in the replacement text for the element are bound at the time that the parent node is set.</span></span> <span data-ttu-id="37200-110">Toutefois, l'espace de noms peut être modifié pour des nœuds de référence d'entité existants lorsque vous les supprimez ou les insérez ailleurs, ou bien pour des nœuds de référence d'entité clonés à l'aide de la méthode **CloneNode**.</span><span class="sxs-lookup"><span data-stu-id="37200-110">However, the namespace can be changed for existing entity reference nodes when you remove and insert them somewhere else, or on entity reference nodes that are cloned with the **CloneNode** method.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="37200-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37200-111">See Also</span></span>  
 [<span data-ttu-id="37200-112">DOM (Document Object Model) XML</span><span class="sxs-lookup"><span data-stu-id="37200-112">XML Document Object Model (DOM)</span></span>](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
