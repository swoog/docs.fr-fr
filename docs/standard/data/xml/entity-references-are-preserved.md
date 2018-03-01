---
title: "Conservation des références d'entité"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 000a6cae-5972-40d6-bd6c-a9b7d9649b3c
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: f5a867d1301355f4c9a77654556229274f96d00c
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="entity-references-are-preserved"></a><span data-ttu-id="08bea-102">Conservation des références d'entité</span><span class="sxs-lookup"><span data-stu-id="08bea-102">Entity References are Preserved</span></span>
<span data-ttu-id="08bea-103">Si une référence d’entité n’est pas développée, mais préservée, le DOM (Document Object Model) XML crée un nœud **XmlEntityReference** quand il rencontre une référence d’entité.</span><span class="sxs-lookup"><span data-stu-id="08bea-103">When the entity reference is not expanded, but preserved, the XML Document Object Model (DOM) builds an **XmlEntityReference** node when it encounters an entity reference.</span></span>  
  
 <span data-ttu-id="08bea-104">À l'aide du code XML suivant,</span><span class="sxs-lookup"><span data-stu-id="08bea-104">Using the following XML,</span></span>  
  
```xml  
<author>Fred</author>  
<pubinfo>Published by &publisher;</pubinfo>  
```  
  
 <span data-ttu-id="08bea-105">le DOM crée un nœud **XmlEntityReference** quand il rencontre la référence `&publisher;`.</span><span class="sxs-lookup"><span data-stu-id="08bea-105">the DOM builds an **XmlEntityReference** node when it encounters the `&publisher;` reference.</span></span> <span data-ttu-id="08bea-106">**XmlEntityReference** contient des nœuds enfants copiés à partir du contenu dans la déclaration d'entité.</span><span class="sxs-lookup"><span data-stu-id="08bea-106">The **XmlEntityReference** contains child nodes copied from the content in the entity declaration.</span></span> <span data-ttu-id="08bea-107">L'exemple de code précédent contient du texte dans la déclaration d'entité, c'est pourquoi un nœud **XmlText** est créé en tant que nœud enfant du nœud de référence d'entité.</span><span class="sxs-lookup"><span data-stu-id="08bea-107">The preceding code example contains text in the entity declaration, so an **XmlText** node is created as the child node of the entity reference node.</span></span>  
  
 <span data-ttu-id="08bea-108">![Arborescence pour références d’entité préservées](../../../../docs/standard/data/xml/media/xmlentityref-notexpanded-nodes.gif "xmlentityref_notexpanded_nodes")</span><span class="sxs-lookup"><span data-stu-id="08bea-108">![Tree structure for preserved entity references](../../../../docs/standard/data/xml/media/xmlentityref-notexpanded-nodes.gif "xmlentityref_notexpanded_nodes")</span></span>  
<span data-ttu-id="08bea-109">Structure d’arborescence avec références d’entité préservées</span><span class="sxs-lookup"><span data-stu-id="08bea-109">Tree structure for entity references that are preserved</span></span>  
  
 <span data-ttu-id="08bea-110">Les nœuds enfants de **XmlEntityReference** sont des copies de tous les nœuds enfants créés à partir du nœud **XmlEntity** quand la déclaration d'entité a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="08bea-110">The child nodes of the **XmlEntityReference** are copies of all the child nodes created from the **XmlEntity** node when the entity declaration was encountered.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="08bea-111">Les nœuds copiés à partir de **XmlEntity** ne constituent pas toujours des copies exactes une fois placés sous le nœud de référence d'entité.</span><span class="sxs-lookup"><span data-stu-id="08bea-111">The nodes copied from the **XmlEntity** are not always exact copies once placed under the entity reference node.</span></span> <span data-ttu-id="08bea-112">Il peut y avoir des espaces de noms qui sont dans la portée au niveau du nœud de référence d'entité et qui ont une incidence sur la configuration finale des nœuds enfants.</span><span class="sxs-lookup"><span data-stu-id="08bea-112">There can be namespaces that are in scope at the entity reference node, and that affects the final configuration of the child nodes.</span></span>  
  
 <span data-ttu-id="08bea-113">Par défaut, des entités générales telles que `&abc;` sont préservées et les nœuds **XmlEntityReference** sont toujours créés.</span><span class="sxs-lookup"><span data-stu-id="08bea-113">By default, general entities like `&abc;` are preserved and **XmlEntityReference** nodes always created.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="08bea-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08bea-114">See Also</span></span>  
 [<span data-ttu-id="08bea-115">DOM (Document Object Model) XML</span><span class="sxs-lookup"><span data-stu-id="08bea-115">XML Document Object Model (DOM)</span></span>](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
