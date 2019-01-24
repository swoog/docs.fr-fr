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
# <a name="how-to-control-namespace-prefixes-visual-basic-linq-to-xml"></a>Procédure : Contrôle les préfixes Namespace (Visual Basic) (LINQ to XML)
Cette rubrique décrit comment contrôler les préfixes d'espaces de noms.  
  
## <a name="example"></a>Exemple  
  
### <a name="description"></a>Description  
 Cet exemple déclare deux espaces de noms. Il spécifie que le `http://www.adventure-works.com` espace de noms a le préfixe `aw`et que le `www.fourthcoffee.com` espace de noms a le préfixe `fc`.  
  
### <a name="code"></a>Code  
  
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
  
### <a name="comments"></a>Commentaires  
 Cet exemple génère la sortie suivante :  
  
```xml  
<aw:Root xmlns:fc="www.fourthcoffee.com" xmlns:aw="http://www.adventure-works.com">  
  <fc:Child>  
    <aw:DifferentChild>other content</aw:DifferentChild>  
  </fc:Child>  
  <aw:Child2>c2 content</aw:Child2>  
  <fc:Child3>c3 content</fc:Child3>  
</aw:Root>  
```  
  
## <a name="see-also"></a>Voir aussi
- [Utilisation des espaces de noms XML (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/working-with-xml-namespaces.md)
