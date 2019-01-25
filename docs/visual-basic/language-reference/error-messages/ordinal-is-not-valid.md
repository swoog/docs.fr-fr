---
title: Nombre non valide
ms.date: 07/20/2015
f1_keywords:
- vbrID452
ms.assetid: 7459562b-cd4f-4590-95e0-6126ae3589a5
ms.openlocfilehash: 351b7ee7f1cfc5199d878c33965770693227ccc4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54618959"
---
# <a name="ordinal-is-not-valid"></a>Nombre non valide
Votre appel à une bibliothèque de liens dynamiques (DLL) spécifie d’utiliser un nombre au lieu d’un nom de procédure, à l’aide de la `#num` syntaxe. Cette erreur a les causes possibles suivantes :  
  
-   Une tentative de convertir le `#num` expression à un nombre a échoué.  
  
-   Le `#num` spécifié ne spécifie pas de n’importe quelle fonction dans la DLL.  
  
-   Une bibliothèque de types a une déclaration non valide, ce qui entraîne une utilisation interne d’un nombre ordinal non valide.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Assurez-vous que l’expression représente un nombre valide, ou appelez la procédure par nom.  
  
2.  Assurez-vous que `#num` identifie une fonction valide dans la DLL.  
  
3.  Isoler la cause du problème en commentant le code de l’appel de procédure. Écrire un `Declare` instruction de la procédure et signaler le problème pour le fournisseur de bibliothèque de types.  
  
## <a name="see-also"></a>Voir aussi
- [Declare (instruction)](../../../visual-basic/language-reference/statements/declare-statement.md)
