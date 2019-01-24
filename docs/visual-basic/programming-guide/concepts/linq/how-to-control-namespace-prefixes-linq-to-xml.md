---
title: 'Procédure : Contrôle les préfixes Namespace (Visual Basic) (LINQ to XML)'
ms.date: 07/20/2015
ms.assetid: 2fcf28a5-31b6-409d-84ea-27c22f71fc9f
ms.openlocfilehash: 91117307caf7e55bd8b512fbd841760616f0b2c5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54623740"
---
# <a name="how-to-control-namespace-prefixes-visual-basic-linq-to-xml"></a><span data-ttu-id="9e6c2-102">Procédure : Contrôle les préfixes Namespace (Visual Basic) (LINQ to XML)</span><span class="sxs-lookup"><span data-stu-id="9e6c2-102">How to: Control Namespace Prefixes (Visual Basic) (LINQ to XML)</span></span>
<span data-ttu-id="9e6c2-103">Cette rubrique décrit comment contrôler les préfixes d'espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="9e6c2-103">This topic describes how you can control namespace prefixes.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9e6c2-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="9e6c2-104">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="9e6c2-105">Description</span><span class="sxs-lookup"><span data-stu-id="9e6c2-105">Description</span></span>  
 <span data-ttu-id="9e6c2-106">Cet exemple déclare deux espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="9e6c2-106">This example declares two namespaces.</span></span> <span data-ttu-id="9e6c2-107">Il spécifie que le `http://www.adventure-works.com` espace de noms a le préfixe `aw`et que le `www.fourthcoffee.com` espace de noms a le préfixe `fc`.</span><span class="sxs-lookup"><span data-stu-id="9e6c2-107">It specifies that the `http://www.adventure-works.com` namespace has the prefix `aw`, and that the `www.fourthcoffee.com` namespace has the prefix of `fc`.</span></span>  
  
### <a name="code"></a><span data-ttu-id="9e6c2-108">Code</span><span class="sxs-lookup"><span data-stu-id="9e6c2-108">Code</span></span>  
  
```vb  
Imports <xmlns:aw="http://www.adventure-works.com">  
Imports <xmlns:fc="www.fourthcoffee.com">  
  
Module Module1  
  
    Sub Main()  
        Dim root As XElement = _  
            <aw:Root>  
                <fc:Child>  
                    <aw:DifferentChild>other content</aw:DifferentChild>  
                </fc:Child>  
                <aw:Child2>c2 content</aw:Child2>  
                <fc:Child3>c3 content</fc:Child3>  
            </aw:Root>  
        Console.WriteLine(root)  
    End Sub  
  
End Module  
```  
  
### <a name="comments"></a><span data-ttu-id="9e6c2-109">Commentaires</span><span class="sxs-lookup"><span data-stu-id="9e6c2-109">Comments</span></span>  
 <span data-ttu-id="9e6c2-110">Cet exemple génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="9e6c2-110">This example produces the following output:</span></span>  
  
```xml  
<aw:Root xmlns:fc="www.fourthcoffee.com" xmlns:aw="http://www.adventure-works.com">  
  <fc:Child>  
    <aw:DifferentChild>other content</aw:DifferentChild>  
  </fc:Child>  
  <aw:Child2>c2 content</aw:Child2>  
  <fc:Child3>c3 content</fc:Child3>  
</aw:Root>  
```  
  
## <a name="see-also"></a><span data-ttu-id="9e6c2-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e6c2-111">See also</span></span>
- [<span data-ttu-id="9e6c2-112">Utilisation des espaces de noms XML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="9e6c2-112">Working with XML Namespaces (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/working-with-xml-namespaces.md)
