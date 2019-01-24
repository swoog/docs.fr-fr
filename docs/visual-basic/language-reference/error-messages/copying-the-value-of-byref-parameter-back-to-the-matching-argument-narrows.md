---
title: Copie de la valeur de &#39;ByRef&#39; paramètre &#39; &lt;nom_paramètre&gt; &#39; dans l’argument correspondant passe du type &#39; &lt;nom_type1&gt; &#39; type &#39; &lt;nom_type2&gt;&#39;
ms.date: 07/20/2015
f1_keywords:
- bc32053
- vbc32053
helpviewer_keywords:
- BC32053
ms.assetid: 281564b7-99f7-451f-b10d-f985e831bb25
ms.openlocfilehash: ec733ecd605d0a9db840ea3f0c3e0e3b5b698054
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54506274"
---
# <a name="copying-the-value-of-39byref39-parameter-39ltparameternamegt39-back-to-the-matching-argument-narrows-from-type-39lttypename1gt39-to-type-39lttypename2gt39"></a>Copie de la valeur de &#39;ByRef&#39; paramètre &#39; &lt;nom_paramètre&gt; &#39; dans l’argument correspondant passe du type &#39; &lt;nom_type1&gt; &#39; type &#39; &lt;nom_type2&gt;&#39;
Une procédure est appelée avec un argument qui s’étend au type de paramètre correspondant, et la conversion à partir du paramètre à l’argument est restrictive.  
  
 Quand vous définissez une classe ou une structure, vous pouvez définir un ou plusieurs opérateurs de conversion pour convertir le type de la classe ou de la structure en d’autres types. Vous pouvez également définir des opérateurs de conversion inverse pour convertir ces autres types vers le type de votre classe ou de votre structure. Lorsque vous utilisez votre type de classe ou structure dans un appel de procédure, Visual Basic peut utiliser ces opérateurs de conversion pour convertir le type d’un argument pour le type de son paramètre correspondant.  
  
 Si vous passez l’argument [ByRef](../../../visual-basic/language-reference/modifiers/byref.md), Visual Basic copie parfois la valeur d’argument dans une variable locale dans la procédure au lieu de passer une référence. Dans ce cas, lorsque la procédure est retournée, Visual Basic doit copier la valeur de variable locale dans l’argument dans le code appelant.  
  
 Si une valeur d’argument `ByRef` est copiée dans la procédure, et si l’argument et le paramètre sont du même type, aucune conversion n’est nécessaire. Mais si les types sont différents, Visual Basic doit convertir dans les deux sens. Si un des types est votre type de classe ou structure, Visual Basic doit le convertir à la fois vers et à partir de l’autre type. Si une de ces conversions est étendue, la conversion inverse peut être restrictive.  
  
 **ID d’erreur :** BC32053  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Si possible, utilisez un argument d’appel du même type que le paramètre de procédure pour Visual Basic n’a pas besoin d’effectuer de conversion.  
  
-   Si vous devez appeler la procédure avec un type d’argument différent du type de paramètre, mais n’avez pas besoin de retourner une valeur dans l’argument d’appel, définissez le paramètre sur [ByVal](../../../visual-basic/language-reference/modifiers/byval.md) au lieu de `ByRef`.  
  
-   Si vous avez besoin de retourner une valeur dans l’argument d’appel, définissez l’opérateur de conversion inverse comme [Widening](../../../visual-basic/language-reference/modifiers/widening.md), si possible.  
  
## <a name="see-also"></a>Voir aussi
- [Procédures](../../../visual-basic/programming-guide/language-features/procedures/index.md)
- [Paramètres et arguments d’une procédure](../../../visual-basic/programming-guide/language-features/procedures/procedure-parameters-and-arguments.md)
- [Passage d’un argument par valeur et par référence](../../../visual-basic/programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference.md)
- [Procédures d’opérateur](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md)
- [Operator (instruction)](../../../visual-basic/language-reference/statements/operator-statement.md)
- [Guide pratique pour Définir un opérateur](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-an-operator.md)
- [Guide pratique pour Définir un opérateur de Conversion](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md)
- [Conversions de type en Visual Basic](../../../visual-basic/programming-guide/language-features/data-types/type-conversions.md)
- [Conversions étendues et restrictives](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
