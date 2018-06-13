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
ms.openlocfilehash: be8ddb7f9ba08535d12890d1c5c82a9b7b485f3d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33597358"
---
# <a name="paramarray-visual-basic"></a>ParamArray (Visual Basic)
Spécifie qu’un paramètre de procédure prend un tableau facultatif d’éléments du type spécifié. `ParamArray` peut être utilisé uniquement sur le dernier paramètre d’une liste de paramètres.  
  
## <a name="remarks"></a>Notes  
 `ParamArray` vous permet de passer un nombre arbitraire d’arguments à la procédure. A `ParamArray` paramètre est toujours déclaré à l’aide de [ByVal](../../../visual-basic/language-reference/modifiers/byval.md).  
  
 Vous pouvez fournir un ou plusieurs arguments à une `ParamArray` type de paramètre en passant un tableau de données appropriés, une liste séparée par des virgules des valeurs, ou rien du tout. Pour plus d’informations, consultez « Appel d’un ParamArray » dans [tableaux de paramètres](../../../visual-basic/programming-guide/language-features/procedures/parameter-arrays.md).  
  
> [!IMPORTANT]
>  Si vous travaillez dans un tableau qui peut être indéfiniment volumineux, il existe un risque de saturer la capacité interne de votre application. Si vous acceptez un tableau de paramètres à partir du code appelant, vous devez tester sa longueur et prenez les mesures appropriées si elle est trop grande pour votre application.  
  
 Le modificateur `ParamArray` peut être utilisé dans les contextes suivants :  
  
 [Declare (instruction)](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
 [Function (instruction)](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [Property (instruction)](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [Sub (instruction)](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## <a name="see-also"></a>Voir aussi  
 [Mots clés](../../../visual-basic/language-reference/keywords/index.md)  
 [tableaux de paramètres](../../../visual-basic/programming-guide/language-features/procedures/parameter-arrays.md)
