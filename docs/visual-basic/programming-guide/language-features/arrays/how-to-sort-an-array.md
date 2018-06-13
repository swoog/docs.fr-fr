---
title: 'Comment : trier un tableau dans Visual Basic'
ms.date: 07/20/2015
f1_keywords:
- Array.Sort
helpviewer_keywords:
- arrays [Visual Basic], sorting
- examples [Visual Basic], arrays
ms.assetid: 9289aeaa-9626-4698-94a7-1d1fd3702b87
ms.openlocfilehash: a067c40e1dd0e881516cbc7769cb9afb879d1b9d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33646296"
---
# <a name="how-to-sort-an-array-in-visual-basic"></a>Comment : trier un tableau dans Visual Basic
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
  
-   Accès à Mscorlib.dll et <xref:System> espace de noms.  
  
## <a name="robust-programming"></a>Programmation fiable  
 Les conditions ci-dessous peuvent générer une exception.  
  
-   Le tableau est vide (<xref:System.ArgumentNullException> classe)  
  
-   Le tableau est multidimensionnel (<xref:System.RankException> classe)  
  
-   Un ou plusieurs éléments du tableau n’implémentent pas le <xref:System.IComparable> interface (<xref:System.InvalidOperationException> classe)  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Array.Sort%2A?displayProperty=nameWithType>  
 [Tableaux](../../../../visual-basic/programming-guide/language-features/arrays/index.md)  
 [Dépannage des tableaux](../../../../visual-basic/programming-guide/language-features/arrays/troubleshooting-arrays.md)  
 [Collections](../../concepts/collections.md)  
 [For Each...Next (instruction)](../../../../visual-basic/language-reference/statements/for-each-next-statement.md)
