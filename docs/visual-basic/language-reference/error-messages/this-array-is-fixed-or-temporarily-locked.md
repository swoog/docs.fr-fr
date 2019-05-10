---
title: Ce tableau est prédéfini ou est temporairement verrouillé (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vbrID10
ms.assetid: de6713a6-51d7-4edb-8515-d5fb544e2091
ms.openlocfilehash: c7b5372b6046e25aad87131ba141cb71c580e12c
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64625940"
---
# <a name="this-array-is-fixed-or-temporarily-locked-visual-basic"></a>Ce tableau est prédéfini ou est temporairement verrouillé (Visual Basic)
Cette erreur a les causes possibles suivantes :  
  
- À l’aide de `ReDim` pour modifier le nombre d’éléments d’un tableau de taille fixe.  
  
- Redimensionnement d’un tableau dynamique au niveau du module, dans lequel un élément a été passé en tant qu’argument à une procédure. Si un élément est passé, le tableau est verrouillé pour empêcher la désallocation de mémoire pour le paramètre de référence dans la procédure.  
  
- Tentative d’assigner une valeur à un `Variant` variable contenant un tableau, mais la `Variant` est actuellement verrouillé.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Rendre le tableau d’origine dynamique non fixe en le déclarant avec `ReDim` (si le tableau est déclaré dans une procédure), ou en le déclarant sans spécifier le nombre d’éléments (si le tableau est déclaré au niveau du module.  
  
2. Déterminer s’il faut vraiment transmettre l’élément, dans la mesure où il est visible dans toutes les procédures dans le module.  
  
3. Déterminez ce qui verrouille le `Variant` et y remédier.  
  
## <a name="see-also"></a>Voir aussi

- [Tableaux](../../../visual-basic/programming-guide/language-features/arrays/index.md)
