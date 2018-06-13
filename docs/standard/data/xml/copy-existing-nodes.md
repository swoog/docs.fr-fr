---
title: Copie de nœuds existants
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: 2aa8f65c-cc62-4638-9c46-129dc15be786
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2e7f5638d0d1f7bf450be526d7c295d4bb6a79eb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33567911"
---
# <a name="copy-existing-nodes"></a><span data-ttu-id="5fb3a-102">Copie de nœuds existants</span><span class="sxs-lookup"><span data-stu-id="5fb3a-102">Copy Existing Nodes</span></span>
<span data-ttu-id="5fb3a-103">Le DOM (Document Object Model) XML comporte de nombreuses méthodes et propriétés que vous pouvez utiliser pour sélectionner un nœud, par exemple **SelectSingleNode**, **ChildNodes[int i]** ou **Attributes[int i]**.</span><span class="sxs-lookup"><span data-stu-id="5fb3a-103">There are many methods and properties in the XML Document Object Model (DOM)you can use to select a node, such as **SelectSingleNode**, **ChildNodes[int i]**, **Attributes[int i]**.</span></span> <span data-ttu-id="5fb3a-104">Une fois le nœud sélectionné, vous pouvez l’insérer dans l’arborescence à l’aide de l’une des méthodes d’insertion adaptées à ce type de nœud particulier.</span><span class="sxs-lookup"><span data-stu-id="5fb3a-104">Once the node is selected, you can insert it into the tree using one of the insert methods that work for that particular node type.</span></span> <span data-ttu-id="5fb3a-105">La seule restriction à l'insertion d'un nœud dans l'arborescence est que cette opération ne doit pas compromettre la validité du format du document.</span><span class="sxs-lookup"><span data-stu-id="5fb3a-105">The only restriction to inserting a node into the tree is that the document must still be well-formed after the node is inserted.</span></span> <span data-ttu-id="5fb3a-106">Quand un nœud existant est inséré dans l’arborescence DOM, il est supprimé de sa position d’origine et ajouté à sa position de destination.</span><span class="sxs-lookup"><span data-stu-id="5fb3a-106">When an existing node is inserted into the DOM tree, it is removed from its original position and added to its target position.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5fb3a-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fb3a-107">See Also</span></span>  
 [<span data-ttu-id="5fb3a-108">DOM (Document Object Model) XML</span><span class="sxs-lookup"><span data-stu-id="5fb3a-108">XML Document Object Model (DOM)</span></span>](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
