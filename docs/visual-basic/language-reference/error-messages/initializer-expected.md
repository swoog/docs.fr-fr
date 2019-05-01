---
title: Initialiseur attendu
ms.date: 07/20/2015
f1_keywords:
- vbc30996
- bc30996
helpviewer_keywords:
- BC30996
ms.assetid: 6e183fe0-8888-43ed-a062-01571079455f
ms.openlocfilehash: 0795fdc1c4b177e13979d7555cd7588217b8cb4c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62013801"
---
# <a name="initializer-expected"></a>Initialiseur attendu
Vous avez tenté de déclarer une instance d’une classe à l’aide d’un initialiseur d’objet dans lequel la liste d’initialisation est vide, comme illustré dans l’exemple suivant.  
  
 `' Not valid.`  
  
 `' Dim aStudent As New Student With {}`  
  
 Au moins un champ ou une propriété doit être initialisée dans la liste d’initialiseurs, comme indiqué dans l’exemple suivant.  
  
 `Dim aStudent As New Student With {.year = "Senior"}`  
  
 **ID d’erreur :** BC30996  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Initialiser au moins un champ ou une propriété dans l’initialiseur ou n’utilisez pas un initialiseur d’objet.  
  
## <a name="see-also"></a>Voir aussi

- [Initialiseurs d’objets : Types nommés et anonymes](../../../visual-basic/programming-guide/language-features/objects-and-classes/object-initializers-named-and-anonymous-types.md)
- [Guide pratique pour Déclarez un objet à l’aide d’un initialiseur d’objet](../../../visual-basic/programming-guide/language-features/objects-and-classes/how-to-declare-an-object-by-using-an-object-initializer.md)
