---
title: Modification des déclarations d'espace de noms dans un document XML
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
ms.assetid: a2758f40-e497-4964-8d8d-1bb68af14dcd
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2fa41e8a4e8f5a15d789ddc81c2b94072c6f16b9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33568054"
---
# <a name="changing-namespace-declarations-in-an-xml-document"></a><span data-ttu-id="703ed-102">Modification des déclarations d'espace de noms dans un document XML</span><span class="sxs-lookup"><span data-stu-id="703ed-102">Changing Namespace Declarations in an XML Document</span></span>
<span data-ttu-id="703ed-103">**XmlDocument** expose des déclarations d'espace de noms et des attributs **xmlns** dans le cadre du modèle objet de document.</span><span class="sxs-lookup"><span data-stu-id="703ed-103">The **XmlDocument** exposes namespace declarations and **xmlns** attributes as part of the document object model.</span></span> <span data-ttu-id="703ed-104">Ceux-ci sont stockés dans **XmlDocument**. C'est pourquoi le document peut préserver l'emplacement de ces attributs quand il est enregistré.</span><span class="sxs-lookup"><span data-stu-id="703ed-104">These are stored in the **XmlDocument**, so when you save the document, it can preserve the location of those attributes.</span></span> <span data-ttu-id="703ed-105">Modifier ces attributs n’a aucun effet sur les propriétés **Name**, **NamespaceURI** et **Prefix** d’autres nœuds figurant déjà dans l’arborescence.</span><span class="sxs-lookup"><span data-stu-id="703ed-105">Changing these attributes has no affect on the **Name**, **NamespaceURI**, and **Prefix** properties of other nodes already in the tree.</span></span> <span data-ttu-id="703ed-106">Par exemple, si vous chargez le document suivant, l'élément `test` a un **NamespaceURI** `123.`.</span><span class="sxs-lookup"><span data-stu-id="703ed-106">For example, if you load the following document, then the `test` element has **NamespaceURI** `123.`</span></span>  
  
```xml  
<test xmlns="123"/>  
```  
  
 <span data-ttu-id="703ed-107">Si vous supprimez l'attribut `xmlns` comme suit, l'élément `test` a encore un **NamespaceURI** `123`.</span><span class="sxs-lookup"><span data-stu-id="703ed-107">If you remove the `xmlns` attribute as follows, then the `test` element still has the **NamespaceURI** of `123`.</span></span>  
  
```vb  
doc.documentElement.RemoveAttribute("xmlns")  
```  
  
```csharp  
doc.documentElement.RemoveAttribute("xmlns");  
```  
  
 <span data-ttu-id="703ed-108">De même, si vous ajoutez un autre attribut `xmlns` à l'élément `doc` comme suit, l'élément `test` a encore le **NamespaceURI** `123`.</span><span class="sxs-lookup"><span data-stu-id="703ed-108">Likewise, if you add a different `xmlns` attribute to the `doc` element as follows, then the `test` element still has **NamespaceURI** `123`.</span></span>  
  
```vb  
doc.documentElement.SetAttribute("xmlns","456");  
```  
  
```csharp  
doc.documentElement.SetAttribute("xmlns","456");  
```  
  
 <span data-ttu-id="703ed-109">C'est pourquoi, la modification d'attributs `xmlns` n'a aucune incidence tant que vous n'avez pas enregistré et rechargé l'objet **XmlDocument**.</span><span class="sxs-lookup"><span data-stu-id="703ed-109">Therefore, changing `xmlns` attributes will have no affect until you save and reload the **XmlDocument** object.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="703ed-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="703ed-110">See Also</span></span>  
 [<span data-ttu-id="703ed-111">DOM (Document Object Model) XML</span><span class="sxs-lookup"><span data-stu-id="703ed-111">XML Document Object Model (DOM)</span></span>](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
