---
title: Méthodes d'extension (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.ExtensionMethods
helpviewer_keywords:
- extending data types [Visual Basic]
- extension methods [Visual Basic]
ms.assetid: b8020aae-374d-46a9-bcb7-8cc2390b93b6
ms.openlocfilehash: 9e005d0dc7da154fbaffbf7e02c55445a1213195
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59296236"
---
# <a name="extension-methods-visual-basic"></a>Méthodes d'extension (Visual Basic)
Méthodes d’extension permettent aux développeurs d’ajouter des fonctionnalités personnalisées aux types de données qui sont déjà définis sans créer un nouveau type dérivé. Méthodes d’extension permettent d’écrire une méthode qui peut être appelée comme s’il s’agissait d’une méthode d’instance du type existant.  
  
## <a name="remarks"></a>Notes  
 Une méthode d’extension peut uniquement être un `Sub` procédure ou un `Function` procédure. Vous ne pouvez pas définir une propriété d’extension, un champ ou un événement. Toutes les méthodes d’extension doivent être marqués avec l’attribut d’extension `<Extension()>` à partir de la <xref:System.Runtime.CompilerServices?displayProperty=nameWithType> espace de noms.  
  
 Le premier paramètre dans une définition de méthode d’extension Spécifie le type de données que la méthode étend. Lorsque la méthode est exécutée, le premier paramètre est lié à l’instance du type de données qui appelle la méthode.  
  
## <a name="example"></a>Exemple  
  
### <a name="description"></a>Description  
 L’exemple suivant définit un `Print` extension pour le <xref:System.String> type de données. Utilise la méthode `Console.WriteLine` pour afficher une chaîne. Le paramètre de la `Print` (méthode), `aString`, indique que la méthode étend la <xref:System.String> classe.  
  
 [!code-vb[VbVbalrExtensionMethods#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrExtensionMethods/VB/StringExtensions.vb#1)]  
  
 Notez que la définition de méthode d’extension est marquée avec l’attribut d’extension `<Extension()>`. Le marquage du module dans lequel la méthode est définie est facultatif, mais chaque méthode d’extension doit être marqué. <xref:System.Runtime.CompilerServices> doit être importé afin d’accéder à l’attribut d’extension.  
  
 Méthodes d’extension peuvent être déclarées que dans les modules. En règle générale, le module dans lequel une méthode d’extension est définie n’est pas le même module que celui dans lequel elle est appelée. Au lieu de cela, le module qui contient la méthode d’extension est importé, s’il a besoin être placé dans la portée. Une fois le module qui contient `Print` est dans la portée, la méthode peut être appelée comme s’il s’agissait d’une méthode d’instance ordinaire qui n’accepte aucun argument, tel que `ToUpper`:  
  
 [!code-vb[VbVbalrExtensionMethods#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrExtensionMethods/VB/Class1.vb#2)]  
  
 L’exemple suivant, `PrintAndPunctuate`, est également une extension à <xref:System.String>, cette fois définie avec deux paramètres. Le premier paramètre, `aString`, indique que la méthode d’extension étend <xref:System.String>. Le deuxième paramètre, `punc`, est destinée à être une chaîne de signes de ponctuation qui est passée comme un argument lorsque la méthode est appelée. La méthode affiche la chaîne suivie de la ponctuation.  
  
 [!code-vb[VbVbalrExtensionMethods#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrExtensionMethods/VB/Class2.vb#3)]  
  
 La méthode est appelée en envoyant un argument de chaîne pour `punc`: `example.PrintAndPunctuate(".")`  
  
 L’exemple suivant `Print` et `PrintAndPunctuate` définies et appelées. <xref:System.Runtime.CompilerServices> est importé dans le module de définition afin d’activer l’accès à l’attribut d’extension.  
  
### <a name="code"></a>Code  
  
```vb  
Imports System.Runtime.CompilerServices  
  
Module StringExtensions  
  
    <Extension()>   
    Public Sub Print(ByVal aString As String)  
        Console.WriteLine(aString)  
    End Sub  
  
    <Extension()>   
    Public Sub PrintAndPunctuate(ByVal aString As String,   
                                 ByVal punc As String)  
        Console.WriteLine(aString & punc)  
    End Sub  
  
End Module  
```  
  
 Ensuite, les méthodes d’extension sont placées dans la portée et appelées.  
  
```vb  
Imports ConsoleApplication2.StringExtensions  
Module Module1  
  
    Sub Main()  
  
        Dim example As String = "Example string"  
        example.Print()  
  
        example = "Hello"  
        example.PrintAndPunctuate(".")  
        example.PrintAndPunctuate("!!!!")  
  
    End Sub  
End Module  
```  
  
### <a name="comments"></a>Commentaires  
 Tout ce qui est nécessaire pour être en mesure d’exécuter ces commandes ou des méthodes d’extension similaire est qu’elles dans la portée. Si le module qui contient une méthode d’extension est dans la portée, il est visible dans IntelliSense et peut être appelée comme s’il s’agissait d’une méthode d’instance ordinaire.  
  
 Notez que lorsque les méthodes sont appelées, aucun argument n’est envoyé pour le premier paramètre. Paramètre `aString` dans la méthode précédente définitions est lié à `example`, l’instance de `String` qui les appelle. Le compilateur utilisera `example` comme argument envoyé au premier paramètre.  
  
 Si une méthode d’extension est appelée pour un objet qui a la valeur `Nothing`, la méthode d’extension s’exécute. Cela ne s’applique pas aux méthodes d’instance ordinaire. Vous pouvez explicitement vérifier `Nothing` dans la méthode d’extension.  
  
## <a name="types-that-can-be-extended"></a>Types qui peuvent être étendus  
 Vous pouvez définir une méthode d’extension sur la plupart des types qui peuvent être représentés dans une liste de paramètres Visual Basic, notamment les suivantes :  
  
-   Classes (types référence)  
  
-   Structures (types valeur)  
  
-   Interfaces  
  
-   Délégués  
  
-   Arguments ByRef et ByVal  
  
-   Paramètres de méthode générique  
  
-   Tableaux  
  
 Étant donné que le premier paramètre spécifie le type de données qui s’étend de la méthode d’extension, il est obligatoire et ne peut pas être facultatif. Pour cette raison, `Optional` paramètres et `ParamArray` ne peuvent pas être le premier paramètre dans la liste de paramètres.  
  
 Méthodes d’extension ne sont pas considérés comme dans la liaison tardive. Dans l’exemple suivant, l’instruction `anObject.PrintMe()` déclenche un <xref:System.MissingMemberException> exception, la même exception qu’elle apparaîtrait si la seconde `PrintMe` définition de méthode d’extension ont été supprimés.  
  
 [!code-vb[VbVbalrExtensionMethods#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrExtensionMethods/VB/Class6.vb#9)]  
  
## <a name="best-practices"></a>Meilleures pratiques  
 Méthodes d’extension fournissent un moyen pratique et puissant d’étendre un type existant. Toutefois, pour les utiliser avec succès, il existe quelques points à prendre en compte. Ces considérations s’appliquent principalement aux auteurs de bibliothèques de classes, mais elles peuvent affecter n’importe quelle application qui utilise des méthodes d’extension.  
  
 La plupart du temps, les méthodes d’extension que vous ajoutez aux types que vous ne possédez pas sont plus vulnérables que les méthodes d’extension ajoutées aux types que vous contrôlez. Un certain nombre de choses peut se produire dans les classes que vous n’êtes pas propriétaire et qui peuvent interférer avec vos méthodes d’extension.  
  
-   Si n’importe quel membre d’instance accessible existe avec une signature qui est compatible avec les arguments dans l’instruction d’appel, sans conversions restrictives requises d’un argument au paramètre, la méthode d’instance servira préférence à toute méthode d’extension. Par conséquent, si une méthode d’instance appropriée est ajoutée à une classe à un moment donné, un membre d’extension existant que vous dépendez peut devenir inaccessible.  
  
-   L’auteur d’une méthode d’extension ne peut pas empêcher d’autres programmeurs d’écrire des méthodes d’extension en conflit qui peuvent être prioritaires sur l’extension d’origine.  
  
-   Vous pouvez améliorer la robustesse en plaçant les méthodes d’extension dans leur propre espace de noms. Consommateurs de votre bibliothèque peuvent ensuite inclure un espace de noms exclure ou sélection parmi les espaces de noms, séparément du reste de la bibliothèque.  
  
-   Il peut être plus sûr d’étendre les interfaces plutôt que d’étendre les classes, surtout si vous ne possédez pas l’interface ou la classe. Une modification dans une interface affecte chaque classe qui l’implémente. Par conséquent, l’auteur peut être moins tenté d’ajouter ou modifier les méthodes dans une interface. Toutefois, si une classe implémente deux interfaces qui ont des méthodes d’extension avec la même signature, aucune méthode d’extension est visible.  
  
-   Étendre le type plus spécifique, que vous pouvez. Dans une hiérarchie de types, si vous sélectionnez un type à partir de laquelle d’autres types sont dérivés, il existe des couches de l’introduction de méthodes d’instance ou d’autres méthodes d’extension peuvent interférer avec les vôtres.  
  
## <a name="extension-methods-instance-methods-and-properties"></a>Méthodes d’extension, les propriétés et les méthodes d’Instance  
 Lorsqu’une méthode d’instance dans la portée a une signature qui est compatible avec les arguments d’une instruction appelante, la méthode d’instance est choisie dans la préférence n’importe quelle méthode d’extension. La méthode d’instance est prioritaire même si la méthode d’extension est une meilleure correspondance. Dans l’exemple suivant, `ExampleClass` contient une méthode d’instance nommée `ExampleMethod` qui a un paramètre de type `Integer`. Méthode d’extension `ExampleMethod` étend `ExampleClass`, et a un paramètre de type `Long`.  
  
 [!code-vb[VbVbalrExtensionMethods#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrExtensionMethods/VB/Class4.vb#4)]  
  
 Le premier appel à `ExampleMethod` dans le code suivant appelle la méthode d’extension, car `arg1` est `Long` et est compatible uniquement avec le `Long` paramètre dans la méthode d’extension. Le deuxième appel à `ExampleMethod` a un `Integer` argument, `arg2`, et il appelle la méthode d’instance.  
  
 [!code-vb[VbVbalrExtensionMethods#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrExtensionMethods/VB/Class4.vb#5)]  
  
 Maintenant inversez les types de données des paramètres dans les deux méthodes :  
  
 [!code-vb[VbVbalrExtensionMethods#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrExtensionMethods/VB/Class5.vb#6)]  
  
 Cette fois, le code dans `Main` appelle la méthode d’instance les deux fois. Il s’agit, car les deux `arg1` et `arg2` avoir une conversion étendue vers `Long`, et la méthode d’instance est prioritaire sur la méthode d’extension dans les deux cas.  
  
 [!code-vb[VbVbalrExtensionMethods#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrExtensionMethods/VB/Class5.vb#7)]  
  
 Par conséquent, une méthode d’extension ne peut pas remplacer une méthode d’instance existante. Toutefois, lorsqu’une méthode d’extension a le même nom qu’une méthode d’instance, mais les signatures d’éviter les conflits, les deux méthodes sont accessibles. Par exemple, si classe `ExampleClass` contient une méthode nommée `ExampleMethod` qui n’accepte aucun arguments, méthodes d’extension portant le même nom mais des signatures différentes sont autorisées, comme indiqué dans le code suivant.  
  
 [!code-vb[VbVbalrExtensionMethods#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrExtensionMethods/VB/Module3.vb#8)]  
  
 La sortie de ce code est comme suit :  
  
 `Extension method`  
  
 `Instance method`  
  
 La situation est plus simple avec des propriétés : si une méthode d’extension a le même nom en tant que propriété de la classe qu’elle étend, la méthode d’extension n’est pas visible et n’est pas accessible.  
  
## <a name="extension-method-precedence"></a>Priorité de méthode d’extension  
 Deux méthodes d’extension qui ont des signatures identiques sont dans la portée et accessibles, celui avec une priorité plus élevée est appelé. Priorité d’une méthode d’extension est basée sur le mécanisme utilisé pour placer la méthode dans la portée. La liste suivante montre la hiérarchie des priorités, du plus élevé au plus bas.  
  
1. Méthodes d’extension définies dans le module actuel.  
  
2. Méthodes d’extension définies à l’intérieur des données de types dans l’espace de noms actuel ou l’un de ses parents, avec des espaces de noms enfants étant prioritaires sur les espaces de noms parent.  
  
3. Méthodes d’extension définies dans les importations de type dans le fichier actuel.  
  
4. Méthodes d’extension définies dans les importations d’espace de noms dans le fichier actuel.  
  
5. Méthodes d’extension définies dans les importations de type au niveau du projet.  
  
6. Méthodes d’extension définies dans les importations d’espace de noms au niveau du projet.  
  
 Si la priorité ne résout pas l’ambiguïté, vous pouvez utiliser le nom qualifié complet pour spécifier la méthode que vous appelez. Si le `Print` méthode dans l’exemple précédent est définie dans un module nommé `StringExtensions`, le nom qualifié complet est `StringExtensions.Print(example)` au lieu de `example.Print()`.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Runtime.CompilerServices>
- <xref:System.Runtime.CompilerServices.ExtensionAttribute>
- [Méthodes d’extension](../../../../csharp/programming-guide/classes-and-structs/extension-methods.md)
- [Module, instruction](../../../../visual-basic/language-reference/statements/module-statement.md)
- [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)
- [Paramètres facultatifs](./optional-parameters.md)
- [Tableaux de paramètres](./parameter-arrays.md)
- [Vue d’ensemble des attributs](../../../../visual-basic/programming-guide/concepts/attributes/index.md)
- [Portée dans Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/scope.md)
