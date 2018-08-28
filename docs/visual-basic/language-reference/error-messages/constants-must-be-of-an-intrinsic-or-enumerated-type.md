---
title: Les constantes doivent être de type intrinsèque ou énuméré, et non de type classe, structure, paramètre de type ou tableau
ms.date: 07/20/2015
f1_keywords:
- vbc30424
- bc30424
helpviewer_keywords:
- BC30424
ms.assetid: 2d402c2f-27ad-428b-b699-d45cd62f7196
ms.openlocfilehash: 4d635d289ed99aed48c296c278bc546971af51da
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "42999199"
---
# <a name="constants-must-be-of-an-intrinsic-or-enumerated-type-not-a-class-structure-type-parameter-or-array-type"></a>Les constantes doivent être de type intrinsèque ou énuméré, et non de type classe, structure, paramètre de type ou tableau
Vous avez tenté de déclarer une constante comme une classe, une structure ou un type de tableau, ou comme un paramètre de type défini par un type générique conteneur.  
  
 Les constantes doivent être de type intrinsèque (`Boolean`, `Byte`, `Date`, `Decimal`, `Double`, `Integer`, `Long`, `Object`, `SByte`, `Short`, `Single`, `String`, `UInteger`, `ULong`, ou `UShort`), ou un `Enum` type basé sur l’un des types intégraux.  
  
 **ID d’erreur :** BC30424  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Déclarez la constante comme intrinsèque ou `Enum` type.  
  
2.  Une constante peut également être une valeur spéciale, tel que `True`, `False`, ou `Nothing`. Le compilateur considère ces valeurs prédéfinies sont du type intrinsèque approprié.  
  
## <a name="see-also"></a>Voir aussi  
 [Constantes et énumérations](../../../visual-basic/language-reference/constants-and-enumerations.md)  
 [Types de données](../../../visual-basic/programming-guide/language-features/data-types/index.md)  
 [Types de données](../../../visual-basic/language-reference/data-types/index.md)
