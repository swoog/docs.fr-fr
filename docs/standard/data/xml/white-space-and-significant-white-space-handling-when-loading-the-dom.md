---
title: Gestion des espaces blancs significatifs ou non lors du chargement du DOM
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: 1b141a0a-50d8-4ebd-83cd-a84449bb22b2
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 1d9bbb14320b84a6d417c5c28026b169092de219
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44266707"
---
# <a name="white-space-and-significant-white-space-handling-when-loading-the-dom"></a><span data-ttu-id="1607c-102">Gestion des espaces blancs significatifs ou non lors du chargement du DOM</span><span class="sxs-lookup"><span data-stu-id="1607c-102">White Space and Significant White Space Handling when Loading the DOM</span></span>
<span data-ttu-id="1607c-103">Durant le chargement du document, vous pouvez définir une option qui préserve les espaces blancs et crée des nœuds **XmlWhitespace** dans l'arborescence du document.</span><span class="sxs-lookup"><span data-stu-id="1607c-103">When loading the document, you can set the option to preserve white space and create **XmlWhitespace** nodes in the document tree.</span></span> <span data-ttu-id="1607c-104">Pour créer des nœuds d'espaces blancs, attribuez la valeur true à la propriété **PreserveWhitespace**.</span><span class="sxs-lookup"><span data-stu-id="1607c-104">To create white space nodes, set the **PreserveWhitespace** property to true.</span></span> <span data-ttu-id="1607c-105">Si cette propriété a pour valeur **false** (la valeur par défaut), les nœuds d'espaces blancs ne sont pas créés.</span><span class="sxs-lookup"><span data-stu-id="1607c-105">If the property is set to **false**, which is the default, white space nodes are not created.</span></span> <span data-ttu-id="1607c-106">Les nœuds d'espaces blancs significatifs sont toujours préservés et des nœuds **XmlSignificantWhitespace** sont toujours créés en mémoire pour représenter ces données, quelle que soit la valeur de l'indicateur **PreserveWhitespace**.</span><span class="sxs-lookup"><span data-stu-id="1607c-106">Significant white spaces nodes are always preserved, and **XmlSignificantWhitespace** nodes are always created in memory to represent this data, regardless of the setting of the **PreserveWhitespace** flag.</span></span>  
  
 <span data-ttu-id="1607c-107">Si le document est chargé à partir d'un lecteur, la définition de la propriété d'indicateur **PreserveWhitespace** sur la classe **XmlDocument** affecte la création de nœuds **XmlWhitespace** uniquement quand la propriété **WhitespaceHandling** sur le **XmlTextReader** n'a pas la valeur **WhitespaceHandling.None**.</span><span class="sxs-lookup"><span data-stu-id="1607c-107">If the document is loaded from a reader, then setting of the **PreserveWhitespace** flag property on the **XmlDocument** class affects the creation of **XmlWhitespace** nodes only when the **WhitespaceHandling** property on the **XmlTextReader** is not set to **WhitespaceHandling.None**.</span></span> <span data-ttu-id="1607c-108">C'est la valeur de la propriété **WhitespaceHandling** sur le lecteur qui prend le pas sur le paramétrage de cet indicateur sur le **XmlDocument**.</span><span class="sxs-lookup"><span data-stu-id="1607c-108">It is the value of the **WhitespaceHandling** property on the reader that takes precedence over the setting of that flag on the **XmlDocument**.</span></span> <span data-ttu-id="1607c-109">Pour plus d'informations sur **XmlSignificantWhitespace**, consultez <xref:System.Xml.XmlSignificantWhitespace>.</span><span class="sxs-lookup"><span data-stu-id="1607c-109">For more information on **XmlSignificantWhitespace**, see <xref:System.Xml.XmlSignificantWhitespace>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1607c-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1607c-110">See also</span></span>

- [<span data-ttu-id="1607c-111">DOM (Document Object Model) XML</span><span class="sxs-lookup"><span data-stu-id="1607c-111">XML Document Object Model (DOM)</span></span>](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
