---
title: 'Procédure : Trier un tableau en Visual Basic'
ms.date: 07/20/2015
f1_keywords:
- Array.Sort
helpviewer_keywords:
- arrays [Visual Basic], sorting
- examples [Visual Basic], arrays
ms.assetid: 9289aeaa-9626-4698-94a7-1d1fd3702b87
ms.openlocfilehash: 680f488a98d6e7e31b3d077843514fd12f75481c
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65586442"
---
# <a name="how-to-sort-an-array-in-visual-basic"></a>Procédure : Trier un tableau en Visual Basic
Cet exemple déclare un tableau de `String` objets nommés `zooAnimals`, il remplit, puis le tri par ordre alphabétique.  
  
## <a name="example"></a>Exemple  
  
```  
Private Sub sortAnimals()  
    Dim zooAnimals(2) As String  
    zooAnimals(0) = "lion"  
    zooAnimals(1) = "turtle"  
    zooAnimals(2) = "ostrich"  
    Array.Sort(zooAnimals)  
End Sub  
```  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
- L’accès à la <xref:System> espace de noms.  
  
## <a name="robust-programming"></a>Programmation fiable  
 Les conditions ci-dessous peuvent générer une exception.  
  
- Tableau est vide (<xref:System.ArgumentNullException> classe)  
  
- Tableau est multidimensionnel (<xref:System.RankException> classe)  
  
- Un ou plusieurs éléments du tableau n’implémentent pas le <xref:System.IComparable> interface (<xref:System.InvalidOperationException> classe)  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Array.Sort%2A?displayProperty=nameWithType>
- [Tableaux](../../../../visual-basic/programming-guide/language-features/arrays/index.md)
- [Dépannage des tableaux](../../../../visual-basic/programming-guide/language-features/arrays/troubleshooting-arrays.md)
- [Collections](../../concepts/collections.md)
- [For Each...Next (instruction)](../../../../visual-basic/language-reference/statements/for-each-next-statement.md)
