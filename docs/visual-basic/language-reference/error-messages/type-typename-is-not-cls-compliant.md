---
title: Le type <typename> n'est pas conforme CLS
ms.date: 07/20/2015
f1_keywords:
- bc40041
- vbc40041
helpviewer_keywords:
- BC40041
ms.assetid: 634132c2-5646-44aa-98c6-f773e2e63882
ms.openlocfilehash: 2805cac71cb36d21f5ab21a5875183803d07a4b4
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65642368"
---
# <a name="type-typename-is-not-cls-compliant"></a>Type \<typename > n’est pas conforme CLS
Une variable, une propriété ou un retour de fonction est déclaré avec un type de données qui n’est pas conforme CLS.  
  
 Pour une application à laquelle se conformer les [indépendance du langage et composants indépendants du langage](../../../standard/language-independence-and-language-independent-components.md) (CLS), il doit utiliser uniquement des types conformes CLS.  
  
 Les types de données Visual Basic suivants ne sont pas conformes CLS :  
  
- [SByte (type de données)](../../../visual-basic/language-reference/data-types/sbyte-data-type.md)  
  
- [UInteger (type de données)](../../../visual-basic/language-reference/data-types/uinteger-data-type.md)  
  
- [ULong (type de données)](../../../visual-basic/language-reference/data-types/ulong-data-type.md)  
  
- [UShort (type de données)](../../../visual-basic/language-reference/data-types/ushort-data-type.md)  
  
 **ID d’erreur :** BC40041  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Si votre application doit être conforme CLS, modifiez le type de données de cet élément vers le type conforme CLS le plus proche. Par exemple, vous pouvez utiliser `UInteger` au lieu de `Integer` si vous n’avez pas besoin de la plage de valeurs située au-dessus de 2 147 483 647. Si vous avez besoin de la plage étendue, vous pouvez remplacer `UInteger` par `Long`.  
  
- Si votre application n’a pas besoin être conforme CLS, il est inutile de modifier quoi que ce soit. Vous devez connaître son non-conformité, toutefois.
