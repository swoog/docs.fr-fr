---
title: "Vérification des noms d'attribut et d'élément XML lors de la création de nœuds"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: b489f647-a175-4659-ada4-170058bb41d0
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 36b9761cefb1dba47c88d053773c89e4312dee9d
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="xml-element-and-attribute-name-verification-when-creating-new-nodes"></a><span data-ttu-id="2aa85-102">Vérification des noms d'attribut et d'élément XML lors de la création de nœuds</span><span class="sxs-lookup"><span data-stu-id="2aa85-102">XML Element and Attribute Name Verification when Creating New Nodes</span></span>
<span data-ttu-id="2aa85-103">Le DOM (Document Object Model) XML contrôle la validité des noms lors de la création de nœuds d'élément ou d'attribut.</span><span class="sxs-lookup"><span data-stu-id="2aa85-103">The XML Document Object Model (DOM) checks the validity of the names when creating new element nodes or attribute nodes.</span></span> <span data-ttu-id="2aa85-104">Si ces noms contiennent des caractères non conformes, une exception est levée.</span><span class="sxs-lookup"><span data-stu-id="2aa85-104">If the names contain illegal characters, an exception is thrown.</span></span> <span data-ttu-id="2aa85-105">Pour être certain que les noms sont valides et encodés correctement, vous devez recourir à la classe **XmlConvert** pour encoder le nom et le décoder à nouveau au niveau de l'application.</span><span class="sxs-lookup"><span data-stu-id="2aa85-105">To ensure that names are valid and encoded correctly, you need to use the **XmlConvert** class to encode the name and decode it back at an application level.</span></span> <span data-ttu-id="2aa85-106">**XmlWriter** possède des méthodes qui effectuent des opérations supplémentaires afin de garantir un format correct pour le code XML qui est généré.</span><span class="sxs-lookup"><span data-stu-id="2aa85-106">The **XmlWriter** has methods that do additional work to ensure well-formed XML is generated.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2aa85-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2aa85-107">See Also</span></span>  
 [<span data-ttu-id="2aa85-108">DOM (Document Object Model) XML</span><span class="sxs-lookup"><span data-stu-id="2aa85-108">XML Document Object Model (DOM)</span></span>](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
