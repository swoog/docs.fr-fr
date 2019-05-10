---
title: Un tableau déclaré en tant que variable de contrôle de boucle for ne peut pas être déclaré avec une taille initiale
ms.date: 07/20/2015
f1_keywords:
- vbc32039
- bc32039
helpviewer_keywords:
- BC32039
ms.assetid: 1d8b6560-c9eb-4b71-a038-24c6f5a5ce46
ms.openlocfilehash: 9f24dd2a20dc3a4935cd288a20a0e12c1d47bee1
ms.sourcegitcommit: e08b319358a8025cc6aa38737854f7bdb87183d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2019
ms.locfileid: "64912343"
---
# <a name="array-declared-as-for-loop-control-variable-cannot-be-declared-with-an-initial-size"></a>Un tableau déclaré en tant que variable de contrôle de boucle for ne peut pas être déclaré avec une taille initiale
Un `For Each` boucle utilise un tableau en tant que son *élément* variable d’itération initialise, mais ce tableau.  
  
 Les instructions suivantes montrent comment cette erreur peut être générée.  
  
```  
Dim arrayList As New List(Of Integer())  
For Each listElement() As Integer In arrayList  
For Each listElement(1) As Integer In arrayList  
```  
  
 La première `For Each` instruction est la méthode correcte pour accéder aux éléments de `arrayList`. La seconde `For Each` instruction génère cette erreur.  
  
 **ID d’erreur :** BC32039  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Supprimez l’initialisation de la déclaration de la *élément* variable d’itération.  
  
## <a name="see-also"></a>Voir aussi

- [For...Next (instruction)](../../../visual-basic/language-reference/statements/for-next-statement.md)
- [Tableaux](../../../visual-basic/programming-guide/language-features/arrays/index.md)
- [Collections](../../../standard/collections/index.md)
