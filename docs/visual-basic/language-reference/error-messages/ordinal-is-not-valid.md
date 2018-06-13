---
title: Nombre non valide
ms.date: 07/20/2015
f1_keywords:
- vbrID452
ms.assetid: 7459562b-cd4f-4590-95e0-6126ae3589a5
ms.openlocfilehash: 12d73b33e3c025b40c98d84e3507af7be1e1e91a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33593601"
---
# <a name="ordinal-is-not-valid"></a>Nombre non valide
Votre appel à une bibliothèque de liens dynamiques (DLL) indiqué à utiliser un nombre au lieu d’un nom de procédure, à l’aide de la `#num` syntaxe. Cette erreur a les causes possibles suivantes :  
  
-   Une tentative de convertir le `#num` expression à un nombre a échoué.  
  
-   Le `#num` spécifié n’indique pas de fonction dans la DLL.  
  
-   Une bibliothèque de types possède une déclaration non valide, ce qui provoque une utilisation interne d’un nombre ordinal non valide.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Assurez-vous que l’expression représente un nombre valide ou appelez la procédure par nom.  
  
2.  Assurez-vous que `#num` identifie une fonction valide dans la DLL.  
  
3.  Isoler la cause du problème en supprimant le code de l’appel de procédure. Écrire un `Declare` instruction de la procédure et signalez le problème au fournisseur de la bibliothèque de types.  
  
## <a name="see-also"></a>Voir aussi  
 [Declare (instruction)](../../../visual-basic/language-reference/statements/declare-statement.md)
