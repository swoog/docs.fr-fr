---
title: ParamArray (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.ParamArray
- ParamArray
helpviewer_keywords:
- ParamArray keyword [Visual Basic]
- ParamArray keyword [Visual Basic], syntax
ms.assetid: a5f18789-92bd-488f-9c7e-cf3719963635
ms.openlocfilehash: 16a69e547d14c619d427aa8860e9bf4002b6db04
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54703599"
---
# <a name="paramarray-visual-basic"></a>ParamArray (Visual Basic)
Spécifie qu’un paramètre de procédure accepte un tableau facultatif d’éléments du type spécifié. `ParamArray` peut être utilisé uniquement sur le dernier paramètre d’une liste de paramètres.  
  
## <a name="remarks"></a>Notes  
 `ParamArray` permet de passer un nombre arbitraire d’arguments à la procédure. Un `ParamArray` paramètre est toujours déclaré à l’aide de [ByVal](../../../visual-basic/language-reference/modifiers/byval.md).  
  
 Vous pouvez fournir un ou plusieurs arguments à un `ParamArray` en passant un tableau des données appropriées de type de paramètre, une liste séparée par des virgules de valeurs, ou rien du tout. Pour plus d’informations, consultez « Appel d’un ParamArray » dans [tableaux de paramètres](../../../visual-basic/programming-guide/language-features/procedures/parameter-arrays.md).  
  
> [!IMPORTANT]
>  Chaque fois que vous avez affaire à un tableau qui peut s’avérer indéfiniment volumineux, il existe un risque de saturer la capacité interne de votre application. Si vous acceptez un tableau de paramètres à partir du code appelant, vous devez tester sa longueur et prendre les mesures appropriées si elle est trop grande pour votre application.  
  
 Le modificateur `ParamArray` peut être utilisé dans les contextes suivants :  
  
 [Declare (instruction)](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
 [Function (instruction)](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [Property (instruction)](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [Sub (instruction)](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## <a name="see-also"></a>Voir aussi
- [Mots clés](../../../visual-basic/language-reference/keywords/index.md)
- [tableaux de paramètres](../../../visual-basic/programming-guide/language-features/procedures/parameter-arrays.md)
