---
title: Nombre non valide
ms.date: 07/20/2015
f1_keywords:
- vbrID452
ms.assetid: 7459562b-cd4f-4590-95e0-6126ae3589a5
ms.openlocfilehash: f3207c2cc237ae22c295c2b3ed56f18601625226
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58822248"
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
