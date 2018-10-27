---
title: Passage des arguments par position et par nom (Visual Basic)
ms.date: 02/01/2018
helpviewer_keywords:
- arguments [Visual Basic], passing by name
- procedures [Visual Basic], arguments
- := passing arguments
- procedure arguments
- Visual Basic code, procedures
- named arguments [Visual Basic], passing arguments
- arguments [Visual Basic], passing by position
- Function procedures [Visual Basic], passing arguments
- named parameters [Visual Basic], passing arguments
- named arguments
- passing parameters [Visual Basic], named parameter arguments
- passing parameters [Visual Basic], by position
- procedures [Visual Basic], calling
- named parameters
- Sub procedures [Visual Basic], passing arguments
- argument passing
- passing parameters [Visual Basic], by name
- argument passing [Visual Basic], by position
- arguments [Visual Basic], listing by name
ms.assetid: 1ad7358f-1da9-48da-a95b-f3c7ed41eff3
ms.openlocfilehash: bdaa0351e288b85a3e35818c0f53ef4d772932e5
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50183865"
---
# <a name="passing-arguments-by-position-and-by-name-visual-basic"></a>Passage des arguments par position et par nom (Visual Basic)
Lorsque vous appelez un `Sub` ou `Function` procédure, vous pouvez passer des arguments *par position* , dans l’ordre dans lequel ils apparaissent dans la définition de la procédure, ou vous pouvez les transmettre *par nom*, sans vu les positionner.  
  
 Quand vous passez un argument par nom, vous spécifiez l’argument déclaré de le nom suivi d’un signe deux-points et un signe égal (`:=`), suivie de la valeur d’argument. Vous pouvez fournir des arguments nommés dans n’importe quel ordre.  
  
 Par exemple, ce qui suit `Sub` procédure accepte trois arguments :  
  
 [!code-vb[SampleProcedure](../../../../../samples/snippets/visualbasic/programming-guide/language-features/passing-named-arguments/module1.vb#1)]  
  
 Lorsque vous appelez cette procédure, vous pouvez fournir les arguments par position, par nom ou à l’aide d’un mélange des deux.  
  
## <a name="passing-arguments-by-position"></a>Passage des Arguments par Position  
 Vous pouvez appeler la `Display` méthode avec ses arguments passés par position et délimités par des virgules, comme indiqué dans l’exemple suivant :  
  
[!code-vb[ByPosition](../../../../../samples/snippets/visualbasic/programming-guide/language-features/passing-named-arguments/module1.vb#2)] 
  
 Si vous omettez un argument facultatif dans une liste d’arguments positionnels, vous devez marquer son emplacement avec une virgule. L’exemple suivant appelle la `Display` méthode sans le `age` argument :  
  
[!code-vb[ByPositionWithOptionalArgument](../../../../../samples/snippets/visualbasic/programming-guide/language-features/passing-named-arguments/module1.vb#3)] 
  
## <a name="passing-arguments-by-name"></a>Passage des Arguments par nom  
 Vous pouvez également appeler `Display` avec les arguments passés par nom, également délimitées par des virgules, comme indiqué dans l’exemple suivant :  
  
[!code-vb[ByName](../../../../../samples/snippets/visualbasic/programming-guide/language-features/passing-named-arguments/module1.vb#4)] 

 Passer des arguments par nom de cette façon est particulièrement utile lorsque vous appelez une procédure qui possède plusieurs arguments facultatifs. Si vous fournissez des arguments par nom, il est inutile d’utiliser des virgules consécutives pour signaler l’absence d’arguments positionnels. Passer des arguments par nom rend également plus facile de suivre les arguments que vous transmettez et celles qui sont omis.  
  
## <a name="mixing-arguments-by-position-and-by-name"></a>Mélange d’Arguments par Position et par nom  

Vous pouvez fournir des arguments par position et par nom dans un seul appel de procédure, comme indiqué dans l’exemple suivant :  
  
[!code-vb[ByNameAndPosition](../../../../../samples/snippets/visualbasic/programming-guide/language-features/passing-named-arguments/module1.vb#5)] 
  
 Dans l’exemple précédent, aucune virgule supplémentaire n’est nécessaire pour contenir le lieu du omis `age` argument, étant donné que `birth` est passé par nom.  
  
Dans les versions de Visual Basic avant la version 15.5, lorsque vous fournissez des arguments par un mélange de position et le nom, les arguments positionnels doivent tous figurer en premier. Une fois que vous fournissez un argument par nom, tous les autres arguments doivent tous être passés par nom.  Par exemple, l’appel suivant à la `Display` méthode affiche l’erreur du compilateur [BC30241 : argument nommé attendu](../../../misc/bc30241.md).

[!code-vb[ByNameAndPosition](../../../../../samples/snippets/visualbasic/programming-guide/language-features/passing-named-arguments/module1.vb#6)] 

À partir de Visual Basic 15.5, les arguments positionnels peuvent suivre les arguments nommés si les arguments de position de fin se trouvent dans la position correcte. Si compilé sous Visual Basic 15.5, l’appel précédent à la `Display` méthode compile correctement et ne génère plus d’erreur du compilateur [BC30241](../../../misc/bc30241.md).  

Cette possibilité de combiner des arguments nommés et positionnels dans n’importe quel ordre est particulièrement utile lorsque vous souhaitez utiliser un argument nommé pour rendre votre code plus lisible. Par exemple, ce qui suit `Person` constructeur de classe requiert deux arguments de type `Person`, qui peuvent être `Nothing`. 

[!code-vb[ByNameAndPosition](../../../../../samples/snippets/visualbasic/programming-guide/language-features/passing-named-arguments/module1.vb#7)] 

À l’aide des arguments nommés et positionnels mixtes permet de faire l’intention du code effacer lorsque la valeur de la `father` et `mother` arguments est `Nothing`:

[!code-vb[ByNameAndPosition](../../../../../samples/snippets/visualbasic/programming-guide/language-features/passing-named-arguments/module1.vb#8)] 

Pour suivre des arguments de position avec des arguments nommés, vous devez ajouter l’élément suivant à votre projet Visual Basic (\*.vbproj) fichier :

```xml
<PropertyGroup>
  <LangVersion>15.5</LangVersion>
</PropertyGroup>
```

Pour plus d’informations, consultez [définition de la version de langage Visual Basic](../../../language-reference/configure-language-version.md).

## <a name="restrictions-on-supplying-arguments-by-name"></a>Restrictions sur la fourniture des Arguments par nom  

Vous ne pouvez pas passer des arguments par nom afin d’éviter d’entrer des arguments requis. Vous pouvez omettre les arguments facultatifs uniquement.  
  
Vous ne pouvez pas passer un tableau de paramètres par nom. Il s’agit, car lorsque vous appelez la procédure, vous fournissez un nombre indéfini de séparées par des virgules des arguments pour le tableau de paramètres, et le compilateur ne peut pas associer plusieurs arguments à un nom unique.  
  
## <a name="see-also"></a>Voir aussi  
 [Procédures](./index.md)  
 [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)  
 [Guide pratique : passer des arguments à une procédure](./how-to-pass-arguments-to-a-procedure.md)  
 [Passage d’un argument par valeur et par référence](./passing-arguments-by-value-and-by-reference.md)  
 [Paramètres facultatifs](./optional-parameters.md)  
 [tableaux de paramètres](./parameter-arrays.md)  
 [Optional](../../../../visual-basic/language-reference/modifiers/optional.md)  
 [ParamArray](../../../../visual-basic/language-reference/modifiers/paramarray.md)
