---
title: readonly (référence C#)
ms.date: 07/20/2015
f1_keywords:
- readonly_CSharpKeyword
- readonly
helpviewer_keywords:
- readonly keyword [C#]
ms.assetid: 2f8081f6-0de2-4903-898d-99696c48d2f4
ms.openlocfilehash: d2f8a2f192dc319ad806aeef4bfbaeecc44b07a3
ms.sourcegitcommit: 89c93d05c2281b4c834f48f6c8df1047e1410980
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2018
---
# <a name="readonly-c-reference"></a>readonly (référence C#)
Le mot clé `readonly` est un modificateur que vous pouvez utiliser sur des champs. Lorsqu’une déclaration de champ inclut un modificateur `readonly`, les assignations aux champs introduites par la déclaration peuvent se produire uniquement dans le cadre de la déclaration ou dans un constructeur de la même classe.  
  
## <a name="readonly-field-example"></a>Exemple de champ en lecture seule  
 Dans cet exemple, la valeur du champ `year` ne peut pas être modifiée dans la méthode `ChangeYear`, même si une valeur lui est affectée dans le constructeur de classe :  
  
 [!code-csharp[csrefKeywordsModifiers#14](../../../csharp/language-reference/keywords/codesnippet/CSharp/readonly_1.cs)]  
  
 Vous pouvez affecter une valeur à un champ `readonly` uniquement dans les contextes suivants :  
  
-   Lorsque la variable est initialisée dans la déclaration, par exemple :  
  
    ```csharp  
    public readonly int y = 5;  
    ```  
  
-   Pour un champ d’instance, dans les constructeurs d’instance de la classe qui contient la déclaration de champ, ou pour un champ statique, dans le constructeur statique de la classe qui contient la déclaration de champ. Ce sont également les seuls contextes dans lesquels il est valide de passer un champ `readonly` comme paramètre [out](../../../csharp/language-reference/keywords/out-parameter-modifier.md) ou [ref](../../../csharp/language-reference/keywords/ref.md).  
  
> [!NOTE]
>  Le mot clé `readonly` est différent du mot clé [const](../../../csharp/language-reference/keywords/const.md). Un champ `const` ne peut être initialisé qu'au moment de la déclaration du champ. Un champ `readonly` peut être initialisé dans la déclaration ou dans un constructeur. C'est pourquoi, les champs `readonly` peuvent avoir des valeurs différentes en fonction du constructeur utilisé. De même, alors qu’un champ `const` est une constante au moment de la compilation, le champ `readonly` peut être utilisé pour des constantes au moment de l’exécution, comme dans l’exemple suivant :  
  
```csharp  
public static readonly uint timeStamp = (uint)DateTime.Now.Ticks;  
```  
  
## <a name="comparing-readonly-and-non-readonly-instance-fields"></a>Comparaison de champs d’instance en lecture seule et non en lecture seule  
 [!code-csharp[csrefKeywordsModifiers#15](../../../csharp/language-reference/keywords/codesnippet/CSharp/readonly_2.cs)]  
  
 Dans l’exemple précédent, si vous utilisez une instruction telle que :  
  
 `p2.y = 66;        // Error`  
  
 vous obtenez le message d’erreur du compilateur :  
  
 `The left-hand side of an assignment must be an l-value`  
  
 qui est la même erreur que vous obtenez lorsque vous tentez d’assigner une valeur à une constante.  
  
## <a name="c-language-specification"></a>Spécification du langage C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Référence C#](../../../csharp/language-reference/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Mots clés C#](../../../csharp/language-reference/keywords/index.md)  
 [Modificateurs](../../../csharp/language-reference/keywords/modifiers.md)  
 [const](../../../csharp/language-reference/keywords/const.md)  
 [Champs](../../../csharp/programming-guide/classes-and-structs/fields.md)
