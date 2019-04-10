---
title: Variable objet ou variable bloc With non définie
ms.date: 07/20/2015
f1_keywords:
- vbrID91
ms.assetid: 2f03e611-f0ed-465c-99a2-a816e034faa3
ms.openlocfilehash: b2c0c47b359e218111c1629ea574303a6d663046
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59297926"
---
# <a name="object-variable-or-with-block-variable-not-set"></a>Variable objet ou variable bloc With non définie
Une variable objet non valide est référencée.   Cette erreur peut se produire pour plusieurs raisons :  
  
-   Une variable a été déclarée sans spécification d’un type. Si une variable est déclarée sans spécification d’un type, par défaut en type `Object`.  
  
     Par exemple, une variable déclarée avec `Dim x` serait de type `Object;` une variable déclarée avec `Dim x As String` serait de type `String`.  
  
    > [!TIP]
    >  Le `Option Strict` instruction n’autorise pas le typage implicite qui aboutit à un `Object` type. Si vous omettez le type, une erreur de compilation se produit. Consultez [Option Strict, instruction](../../../visual-basic/language-reference/statements/option-strict-statement.md).  
  
-   Vous tentez de référencer un objet qui a été défini sur `Nothing`  
  
     .  
  
-   Vous tentez d’accéder à un élément d’une variable de tableau n’a pas été correctement déclaré.  
  
     Par exemple, un tableau déclaré en tant que `products() As String` déclenche l’erreur si vous essayez de faire référence à un élément du tableau `products(3) = "Widget"`. Le tableau ne comporte aucun élément et est traité comme un objet.  
  
-   Vous essayez d’accéder au code dans un `With...End With` bloquer avant le bloc a été initialisé.   Un `With...End With` doit être initialisé en exécutant le `With` point d’entrée instruction.  
  
> [!NOTE]
>  Dans les versions antérieures de Visual Basic ou VBA cette erreur a été également déclenchée en affectant une valeur à une variable sans utiliser le `Set` mot clé (`x = "name"` au lieu de `Set x = "name"`). Le `Set` mot clé n’est plus valide en Visual Basic .net.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Définissez `Option Strict` à `On` en ajoutant le code suivant au début du fichier :  
  
```vb  
Option Strict On  
```  

     When you run the project, a compiler error will appear in the **Error List** for any variable that was specified without a type.  
  
2. Si vous ne souhaitez pas activer `Option Strict`, recherchez le code de toutes les variables qui ont été spécifiées sans un type (`Dim x` au lieu de `Dim x As String`) et ajoutez le type prévu à la déclaration.  
  
3. Vérifiez que vous ne sont pas référence à une variable objet qui a été définie sur `Nothing`.  Rechercher votre code pour le mot clé `Nothing`et de réviser votre code pour que l’objet n’est pas défini sur `Nothing` jusqu'à ce qu’une fois que vous avez les référencé.  
  
4. Assurez-vous que toutes les variables tableau sont dimensionnées avant d’y accéder. Vous pouvez soit attribuer une dimension lorsque vous créez tout d’abord le tableau (`Dim x(5) As String` au lieu de `Dim x() As String`), ou utiliser le `ReDim` mot clé pour définir les dimensions du tableau avant tout d’abord accéder.  
  
5. Assurez-vous que votre `With` est initialisé en exécutant le `With` point d’entrée instruction.  
  
## <a name="see-also"></a>Voir aussi

- [Déclaration des variables objets](../../../visual-basic/programming-guide/language-features/variables/object-variable-declaration.md)
- [ReDim, instruction](../../../visual-basic/language-reference/statements/redim-statement.md)
- [With...End With, instruction](../../../visual-basic/language-reference/statements/with-end-with-statement.md)
