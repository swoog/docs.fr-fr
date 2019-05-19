---
title: Débogage d’arborescences d’Expression dans Visual Studio (Visual Basic)
ms.date: 07/20/2015
ms.assetid: 492cc28f-b7a2-4c47-b582-b3c437b8a5d5
ms.openlocfilehash: 7fc97d898c5956b5a569036e6e0fe1174714576d
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65879825"
---
# <a name="debugging-expression-trees-in-visual-studio-visual-basic"></a>Débogage d’arborescences d’Expression dans Visual Studio (Visual Basic)
Vous pouvez analyser la structure et le contenu d’arborescences d’expression quand vous déboguez vos applications. Pour obtenir un aperçu rapide de l’arborescence d’expression, vous pouvez utiliser la `DebugView` propriété, qui représente des arborescences d’expression à l’aide d’une syntaxe spéciale décrite [ci-dessous](#debugview-syntax). (Notez que `DebugView` est disponible uniquement en mode débogage.)  

![DebugView d’arborescence d’expression dans le débogueur Visual Studio](media/debugging-expression-trees-in-visual-studio/debugview_vb.png)

Dans la mesure où `DebugView` est une chaîne, vous pouvez utiliser la [visualiseur de texte intégré](https://docs.microsoft.com/visualstudio/debugger/view-strings-visualizer#open-a-string-visualizer) à afficher sur plusieurs lignes, en sélectionnant **visualiseur de texte** à partir de l’icône de loupe située à côté le `DebugView` étiquette.

 ![Visualiseur de texte appliquée aux résultats de « DebugView »](media/debugging-expression-trees-in-visual-studio/string_visualizer_vb.png)

Ou bien, vous pouvez installer et utiliser [un visualiseur personnalisé](https://docs.microsoft.com/visualstudio/debugger/create-custom-visualizers-of-data) pour les arborescences d’expression :

* [Expressions lisibles](https://github.com/agileobjects/ReadableExpressions) ([licence MIT](https://github.com/agileobjects/ReadableExpressions/blob/master/LICENSE.md), disponible à la [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=vs-publisher-1232914.ReadableExpressionsVisualizers)), affiche l’arborescence d’expression en tant que C# code :

  ![Visualiseur d’Expressions lisible](media/debugging-expression-trees-in-visual-studio/readable_expressions_visualizer.png)

* [Visualiseur de l’arborescence expression](https://github.com/zspitz/ExpressionToString#visual-studio-debugger-visualizer-for-expression-trees) ([licence MIT](https://github.com/zspitz/ExpressionToString/blob/master/LICENSE)), fournit une vue graphique de l’arborescence d’expression, ses propriétés et les objets connexes ; et peut rendre l’arborescence d’expression à l’aide de code Visual Basic :

  ![Visualiseur de ExpressionToString](media/debugging-expression-trees-in-visual-studio/expression_to_string_visualizer_vb.png)

### <a name="to-open-a-visualizer-for-an-expression-tree"></a>Pour ouvrir un visualiseur pour une arborescence d’expressions  
  
1. Cliquez sur l’icône de loupe qui apparaît en regard de l’arborescence d’expression dans **DataTips**, un **espion** fenêtre, le **automatique** fenêtre, ou le **devariableslocales** fenêtre.  
  
     Une liste de visualiseurs disponibles s’affiche. : 

      ![Visualiseurs d’ouverture à partir de Visual Studio](media/debugging-expression-trees-in-visual-studio/expression_tree_visualizers_vb.png)

2. Cliquez sur le visualiseur à utiliser.  

## <a name="debugview-syntax"></a>`DebugView` Syntaxe 

Chaque type d’expression s’affiche dans le visualiseur, comme décrit dans les sections suivantes.

## <a name="parameterexpressions"></a>ParameterExpressions

Les noms de variables <xref:System.Linq.Expressions.ParameterExpression> s’affichent avec le symbole "$" en préfixe.

Si un paramètre n’a pas de nom, un nom généré automatiquement lui est assigné, tel que `$var1` ou `$var2`.

### <a name="examples"></a>Exemples

- `Expression`

    ```vb
    Dim numParam As ParameterExpression =
    Expression.Parameter(GetType(Integer), "num")
    ```

    Propriété `DebugView`

    `$num`

- `Expression`

    ```vb
    Dim numParam As ParameterExpression =
    Expression.Parameter(GetType(Integer))
    ```

    Propriété `DebugView`

    `$var1`

## <a name="constantexpressions"></a>ConstantExpressions
 Pour les objets <xref:System.Linq.Expressions.ConstantExpression> qui représentent des valeurs entières, des chaînes et des valeurs `null`, la valeur de la constante est affichée.

### <a name="examples"></a>Exemples

- `Expression`

    ```vb
    Dim num as Integer= 10
    Dim expr As ConstantExpression = Expression.Constant(num)
    ```

    Propriété `DebugView`

    10

- `Expression`

    ```vb
    Dim num As Double = 10
    Dim expr As ConstantExpression = Expression.Constant(num)
    ```

    Propriété `DebugView`

    10D

## <a name="blockexpression"></a>BlockExpression

Si le type d’un objet <xref:System.Linq.Expressions.BlockExpression> diffère du type de la dernière expression du bloc, le type est affiché dans la propriété `DebugInfo` entre crochets pointus (\< et >). Sinon, le type de l’objet <xref:System.Linq.Expressions.BlockExpression> n’est pas affiché.

### <a name="examples"></a>Exemples

- `Expression`

    ```vb
    Dim block As BlockExpression = Expression.Block(Expression.Constant("test"))
    ```

    Propriété `DebugView`

    `.Block() {`

    `"test"`

    `}`

- `Expression`

    ```vb
    Dim block As BlockExpression =
    Expression.Block(GetType(Object), Expression.Constant("test"))
    ```

    Propriété `DebugView`

    `.Block<System.Object>() {`

    `"test"`

    `}`

## <a name="lambdaexpression"></a>LambdaExpression

Les objets <xref:System.Linq.Expressions.LambdaExpression> sont affichés avec leurs types délégués.

Si une expression lambda n’a pas de nom, un nom généré automatiquement lui est assigné, tel que `#Lambda1` ou `#Lambda2`.

### <a name="examples"></a>Exemples

- `Expression`

    ```vb
    Dim lambda As LambdaExpression =
    Expression.Lambda(Of Func(Of Integer))(Expression.Constant(1))
    ```

    Propriété `DebugView`

    `.Lambda #Lambda1<System.Func'1[System.Int32]>() {`

    `1`

    `}`

- `Expression`

    ```vb
    Dim lambda As LambdaExpression =
    Expression.Lambda(Of Func(Of Integer))(Expression.Constant(1), "SampleLambda", Nothing)
    ```

    Propriété `DebugView`

    `.Lambda SampleLambda<System.Func'1[System.Int32]>() {`

    `1`

    `}`

## <a name="labelexpression"></a>LabelExpression

Si vous spécifiez une valeur par défaut pour l’objet <xref:System.Linq.Expressions.LabelExpression>, cette valeur est affichée avant l’objet <xref:System.Linq.Expressions.LabelTarget>.

Le jeton `.Label` indique le début de l’étiquette. Le jeton `.LabelTarget` indique la destination de la cible à laquelle accéder.

Si une étiquette n’a pas de nom, un nom généré automatiquement lui est assigné, tel que `#Label1` ou `#Label2`.

### <a name="examples"></a>Exemples

- `Expression`

    ```vb
    Dim target As LabelTarget = Expression.Label(GetType(Integer), "SampleLabel")
    Dim label1 As BlockExpression = Expression.Block(
    Expression.Goto(target, Expression.Constant(0)),
    Expression.Label(target, Expression.Constant(-1)))
    ```

    Propriété `DebugView`

    `.Block() {`

    `.Goto SampleLabel { 0 };`

    `.Label`

    `-1`

    `.LabelTarget SampleLabel:`

    `}`

- `Expression`

    ```vb
    Dim target As LabelTarget = Expression.Label()
    Dim block As BlockExpression = Expression.Block(
    Expression.Goto(target), Expression.Label(target))
    ```

    Propriété `DebugView`

    `.Block() {`

    `.Goto #Label1 { };`

    `.Label`

    `.LabelTarget #Label1:`

    `}`

## <a name="checked-operators"></a>Opérateurs Checked

Les opérateurs Checked sont affichés précédés du symbole "#". Par exemple, l’opérateur d’addition checked est affiché sous la forme `#+`.

### <a name="examples"></a>Exemples

- `Expression`

    ```vb
    Dim expr As Expression = Expression.AddChecked(
    Expression.Constant(1), Expression.Constant(2))
    ```

    Propriété `DebugView`

    `1 #+ 2`

- `Expression`

    ```vb
    Dim expr As Expression = Expression.ConvertChecked(
    Expression.Constant(10.0), GetType(Integer))
    ```

    Propriété `DebugView`

    `#(System.Int32)10D`

## <a name="see-also"></a>Voir aussi

- [Arborescences d’expressions (Visual Basic)](../../../../visual-basic/programming-guide/concepts/expression-trees/index.md)
- [Débogage dans Visual Studio](/visualstudio/debugger/debugging-in-visual-studio)
- [Créer des visualiseurs personnalisés](/visualstudio/debugger/create-custom-visualizers-of-data)
