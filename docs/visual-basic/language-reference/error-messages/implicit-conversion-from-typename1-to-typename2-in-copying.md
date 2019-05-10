---
title: Option Strict On interdit le passage du type '<typename1>' au type '<typename2>' lors de la recopie de la valeur du paramètre 'ByRef' '<parametername>' dans l'argument correspondant.
ms.date: 07/20/2015
f1_keywords:
- vbc41999
- bc41999
helpviewer_keywords:
- BC41999
ms.assetid: ae48c738-dff8-4c0f-8931-bbb70b2c8b03
ms.openlocfilehash: 7ac0e7961e1a039e505c85a35c7c31353ed6578e
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64661987"
---
# <a name="implicit-conversion-from-typename1-to-typename2-in-copying-the-value-of-byref-parameter-parametername-back-to-the-matching-argument"></a>Conversion implicite de '\<nom_type1 >' à '\<nom_type2 >' lors de la copie de la valeur du paramètre 'ByRef' '\<nom_paramètre >' dans l’argument correspondant.
Une procédure est appelée avec un [ByRef](../../../visual-basic/language-reference/modifiers/byref.md) argument d’un type autre que celui de son paramètre correspondant.  
  
 Si vous passez un argument `ByRef`, Visual Basic copie parfois la valeur d’argument dans une variable locale dans la procédure au lieu de passer une référence. Dans ce cas, lorsque la procédure est retournée, Visual Basic doit copier la valeur de variable locale dans l’argument dans le code appelant.  
  
 Si une valeur d’argument `ByRef` est copiée dans la procédure, et si l’argument et le paramètre sont du même type, aucune conversion n’est nécessaire. Mais si les types sont différents, Visual Basic doit convertir dans les deux sens. Étant donné que vous ne pouvez pas utiliser `CType` ou un des autres mots clés de conversion sur un argument de procédure ou de paramètre, une telle conversion est toujours implicite.  
  
 Par défaut, ce message est un avertissement. Pour plus d’informations sur le masquage des avertissements ou leur traitement en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).  
  
 **ID d’erreur :** BC41999  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Si possible, utilisez un argument d’appel du même type que le paramètre de procédure pour Visual Basic n’a pas besoin d’effectuer de conversion.  
  
- Si vous devez appeler la procédure avec un type d’argument différent du type de paramètre, mais n’avez pas besoin de retourner une valeur dans l’argument d’appel, définissez le paramètre sur [ByVal](../../../visual-basic/language-reference/modifiers/byval.md) au lieu de `ByRef`.  
  
## <a name="see-also"></a>Voir aussi

- [Procédures](../../../visual-basic/programming-guide/language-features/procedures/index.md)
- [Paramètres et arguments d’une procédure](../../../visual-basic/programming-guide/language-features/procedures/procedure-parameters-and-arguments.md)
- [Passage d’un argument par valeur et par référence](../../../visual-basic/programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference.md)
- [Conversions implicites et explicites](../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
