---
title: Gestion des espaces blancs significatifs ou non lors du chargement du DOM
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 1b141a0a-50d8-4ebd-83cd-a84449bb22b2
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 8a16f90b6d48bc2ffabfd678722fa9b6e61328cd
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="white-space-and-significant-white-space-handling-when-loading-the-dom"></a><span data-ttu-id="1c2fb-102">Gestion des espaces blancs significatifs ou non lors du chargement du DOM</span><span class="sxs-lookup"><span data-stu-id="1c2fb-102">White Space and Significant White Space Handling when Loading the DOM</span></span>
<span data-ttu-id="1c2fb-103">Durant le chargement du document, vous pouvez définir une option qui préserve les espaces blancs et crée des nœuds **XmlWhitespace** dans l'arborescence du document.</span><span class="sxs-lookup"><span data-stu-id="1c2fb-103">When loading the document, you can set the option to preserve white space and create **XmlWhitespace** nodes in the document tree.</span></span> <span data-ttu-id="1c2fb-104">Pour créer des nœuds d'espaces blancs, attribuez la valeur true à la propriété **PreserveWhitespace**.</span><span class="sxs-lookup"><span data-stu-id="1c2fb-104">To create white space nodes, set the **PreserveWhitespace** property to true.</span></span> <span data-ttu-id="1c2fb-105">Si cette propriété a pour valeur **false** (la valeur par défaut), les nœuds d'espaces blancs ne sont pas créés.</span><span class="sxs-lookup"><span data-stu-id="1c2fb-105">If the property is set to **false**, which is the default, white space nodes are not created.</span></span> <span data-ttu-id="1c2fb-106">Les nœuds d'espaces blancs significatifs sont toujours préservés et des nœuds **XmlSignificantWhitespace** sont toujours créés en mémoire pour représenter ces données, quelle que soit la valeur de l'indicateur **PreserveWhitespace**.</span><span class="sxs-lookup"><span data-stu-id="1c2fb-106">Significant white spaces nodes are always preserved, and **XmlSignificantWhitespace** nodes are always created in memory to represent this data, regardless of the setting of the **PreserveWhitespace** flag.</span></span>  
  
 <span data-ttu-id="1c2fb-107">Si le document est chargé à partir d'un lecteur, la définition de la propriété d'indicateur **PreserveWhitespace** sur la classe **XmlDocument** affecte la création de nœuds **XmlWhitespace** uniquement quand la propriété **WhitespaceHandling** sur le **XmlTextReader** n'a pas la valeur **WhitespaceHandling.None**.</span><span class="sxs-lookup"><span data-stu-id="1c2fb-107">If the document is loaded from a reader, then setting of the **PreserveWhitespace** flag property on the **XmlDocument** class affects the creation of **XmlWhitespace** nodes only when the **WhitespaceHandling** property on the **XmlTextReader** is not set to **WhitespaceHandling.None**.</span></span> <span data-ttu-id="1c2fb-108">C'est la valeur de la propriété **WhitespaceHandling** sur le lecteur qui prend le pas sur le paramétrage de cet indicateur sur le **XmlDocument**.</span><span class="sxs-lookup"><span data-stu-id="1c2fb-108">It is the value of the **WhitespaceHandling** property on the reader that takes precedence over the setting of that flag on the **XmlDocument**.</span></span> <span data-ttu-id="1c2fb-109">Pour plus d'informations sur **XmlSignificantWhitespace**, consultez <xref:System.Xml.XmlSignificantWhitespace>.</span><span class="sxs-lookup"><span data-stu-id="1c2fb-109">For more information on **XmlSignificantWhitespace**, see <xref:System.Xml.XmlSignificantWhitespace>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1c2fb-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c2fb-110">See Also</span></span>  
 [<span data-ttu-id="1c2fb-111">DOM (Document Object Model) XML</span><span class="sxs-lookup"><span data-stu-id="1c2fb-111">XML Document Object Model (DOM)</span></span>](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
