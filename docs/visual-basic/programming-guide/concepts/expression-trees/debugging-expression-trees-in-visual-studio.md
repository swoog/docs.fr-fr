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
# <a name="debugging-expression-trees-in-visual-studio-visual-basic"></a><span data-ttu-id="74628-102">Débogage d’arborescences d’Expression dans Visual Studio (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="74628-102">Debugging Expression Trees in Visual Studio (Visual Basic)</span></span>
<span data-ttu-id="74628-103">Vous pouvez analyser la structure et le contenu d’arborescences d’expression quand vous déboguez vos applications.</span><span class="sxs-lookup"><span data-stu-id="74628-103">You can analyze the structure and content of expression trees when you debug your applications.</span></span> <span data-ttu-id="74628-104">Pour obtenir un aperçu rapide de l’arborescence d’expression, vous pouvez utiliser la `DebugView` propriété, qui représente des arborescences d’expression à l’aide d’une syntaxe spéciale décrite [ci-dessous](#debugview-syntax).</span><span class="sxs-lookup"><span data-stu-id="74628-104">To get a quick overview of the expression tree structure, you can use the `DebugView` property, which represents expression trees using a special syntax described [below](#debugview-syntax).</span></span> <span data-ttu-id="74628-105">(Notez que `DebugView` est disponible uniquement en mode débogage.)</span><span class="sxs-lookup"><span data-stu-id="74628-105">(Note that `DebugView` is available only in debug mode.)</span></span>  

![DebugView d’arborescence d’expression dans le débogueur Visual Studio](media/debugging-expression-trees-in-visual-studio/debugview_vb.png)

<span data-ttu-id="74628-107">Dans la mesure où `DebugView` est une chaîne, vous pouvez utiliser la [visualiseur de texte intégré](https://docs.microsoft.com/visualstudio/debugger/view-strings-visualizer#open-a-string-visualizer) à afficher sur plusieurs lignes, en sélectionnant **visualiseur de texte** à partir de l’icône de loupe située à côté le `DebugView` étiquette.</span><span class="sxs-lookup"><span data-stu-id="74628-107">Since `DebugView` is a string, you can use the [built-in Text Visualizer](https://docs.microsoft.com/visualstudio/debugger/view-strings-visualizer#open-a-string-visualizer) to view it across multiple lines, by selecting **Text Visualizer** from the magnifying glass icon next to the `DebugView` label.</span></span>

 ![Visualiseur de texte appliquée aux résultats de « DebugView »](media/debugging-expression-trees-in-visual-studio/string_visualizer_vb.png)

<span data-ttu-id="74628-109">Ou bien, vous pouvez installer et utiliser [un visualiseur personnalisé](https://docs.microsoft.com/visualstudio/debugger/create-custom-visualizers-of-data) pour les arborescences d’expression :</span><span class="sxs-lookup"><span data-stu-id="74628-109">Alternatively, you can install and use [a custom visualizer](https://docs.microsoft.com/visualstudio/debugger/create-custom-visualizers-of-data) for expression trees:</span></span>

* <span data-ttu-id="74628-110">[Expressions lisibles](https://github.com/agileobjects/ReadableExpressions) ([licence MIT](https://github.com/agileobjects/ReadableExpressions/blob/master/LICENSE.md), disponible à la [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=vs-publisher-1232914.ReadableExpressionsVisualizers)), affiche l’arborescence d’expression en tant que C# code :</span><span class="sxs-lookup"><span data-stu-id="74628-110">[Readable Expressions](https://github.com/agileobjects/ReadableExpressions) ([MIT license](https://github.com/agileobjects/ReadableExpressions/blob/master/LICENSE.md), available at the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=vs-publisher-1232914.ReadableExpressionsVisualizers)), renders the expression tree as C# code:</span></span>

  ![Visualiseur d’Expressions lisible](media/debugging-expression-trees-in-visual-studio/readable_expressions_visualizer.png)

* <span data-ttu-id="74628-112">[Visualiseur de l’arborescence expression](https://github.com/zspitz/ExpressionToString#visual-studio-debugger-visualizer-for-expression-trees) ([licence MIT](https://github.com/zspitz/ExpressionToString/blob/master/LICENSE)), fournit une vue graphique de l’arborescence d’expression, ses propriétés et les objets connexes ; et peut rendre l’arborescence d’expression à l’aide de code Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="74628-112">[Expression Tree Visualizer](https://github.com/zspitz/ExpressionToString#visual-studio-debugger-visualizer-for-expression-trees) ([MIT license](https://github.com/zspitz/ExpressionToString/blob/master/LICENSE)), provides a graphical view of the expression tree, its properties, and related objects; and can render the expression tree using Visual Basic code:</span></span>

  ![Visualiseur de ExpressionToString](media/debugging-expression-trees-in-visual-studio/expression_to_string_visualizer_vb.png)

### <a name="to-open-a-visualizer-for-an-expression-tree"></a><span data-ttu-id="74628-114">Pour ouvrir un visualiseur pour une arborescence d’expressions</span><span class="sxs-lookup"><span data-stu-id="74628-114">To open a visualizer for an expression tree</span></span>  
  
1. <span data-ttu-id="74628-115">Cliquez sur l’icône de loupe qui apparaît en regard de l’arborescence d’expression dans **DataTips**, un **espion** fenêtre, le **automatique** fenêtre, ou le **devariableslocales** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="74628-115">Click the magnifying glass icon that appears next to the expression tree in **DataTips**, a **Watch** window, the **Autos** window, or the **Locals** window.</span></span>  
  
     <span data-ttu-id="74628-116">Une liste de visualiseurs disponibles s’affiche. :</span><span class="sxs-lookup"><span data-stu-id="74628-116">A list of available visualizers is displayed.:</span></span> 

      ![Visualiseurs d’ouverture à partir de Visual Studio](media/debugging-expression-trees-in-visual-studio/expression_tree_visualizers_vb.png)

2. <span data-ttu-id="74628-118">Cliquez sur le visualiseur à utiliser.</span><span class="sxs-lookup"><span data-stu-id="74628-118">Click the visualizer you want to use.</span></span>  

## <a name="debugview-syntax"></a><span data-ttu-id="74628-119">`DebugView` Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74628-119">`DebugView` syntax</span></span> 

<span data-ttu-id="74628-120">Chaque type d’expression s’affiche dans le visualiseur, comme décrit dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="74628-120">Each expression type is displayed in the visualizer as described in the following sections.</span></span>

## <a name="parameterexpressions"></a><span data-ttu-id="74628-121">ParameterExpressions</span><span class="sxs-lookup"><span data-stu-id="74628-121">ParameterExpressions</span></span>

<span data-ttu-id="74628-122">Les noms de variables <xref:System.Linq.Expressions.ParameterExpression> s’affichent avec le symbole "$" en préfixe.</span><span class="sxs-lookup"><span data-stu-id="74628-122"><xref:System.Linq.Expressions.ParameterExpression> variable names are displayed with a "$" symbol at the beginning.</span></span>

<span data-ttu-id="74628-123">Si un paramètre n’a pas de nom, un nom généré automatiquement lui est assigné, tel que `$var1` ou `$var2`.</span><span class="sxs-lookup"><span data-stu-id="74628-123">If a parameter does not have a name, it is assigned an automatically generated name, such as `$var1` or `$var2`.</span></span>

### <a name="examples"></a><span data-ttu-id="74628-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="74628-124">Examples</span></span>

- `Expression`

    ```vb
    Dim numParam As ParameterExpression =
    Expression.Parameter(GetType(Integer), "num")
    ```

    <span data-ttu-id="74628-125">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="74628-125">`DebugView` property</span></span>

    `$num`

- `Expression`

    ```vb
    Dim numParam As ParameterExpression =
    Expression.Parameter(GetType(Integer))
    ```

    <span data-ttu-id="74628-126">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="74628-126">`DebugView` property</span></span>

    `$var1`

## <a name="constantexpressions"></a><span data-ttu-id="74628-127">ConstantExpressions</span><span class="sxs-lookup"><span data-stu-id="74628-127">ConstantExpressions</span></span>
 <span data-ttu-id="74628-128">Pour les objets <xref:System.Linq.Expressions.ConstantExpression> qui représentent des valeurs entières, des chaînes et des valeurs `null`, la valeur de la constante est affichée.</span><span class="sxs-lookup"><span data-stu-id="74628-128">For <xref:System.Linq.Expressions.ConstantExpression> objects that represent integer values, strings, and `null`, the value of the constant is displayed.</span></span>

### <a name="examples"></a><span data-ttu-id="74628-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="74628-129">Examples</span></span>

- `Expression`

    ```vb
    Dim num as Integer= 10
    Dim expr As ConstantExpression = Expression.Constant(num)
    ```

    <span data-ttu-id="74628-130">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="74628-130">`DebugView` property</span></span>

    <span data-ttu-id="74628-131">10</span><span class="sxs-lookup"><span data-stu-id="74628-131">10</span></span>

- `Expression`

    ```vb
    Dim num As Double = 10
    Dim expr As ConstantExpression = Expression.Constant(num)
    ```

    <span data-ttu-id="74628-132">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="74628-132">`DebugView` property</span></span>

    <span data-ttu-id="74628-133">10D</span><span class="sxs-lookup"><span data-stu-id="74628-133">10D</span></span>

## <a name="blockexpression"></a><span data-ttu-id="74628-134">BlockExpression</span><span class="sxs-lookup"><span data-stu-id="74628-134">BlockExpression</span></span>

<span data-ttu-id="74628-135">Si le type d’un objet <xref:System.Linq.Expressions.BlockExpression> diffère du type de la dernière expression du bloc, le type est affiché dans la propriété `DebugInfo` entre crochets pointus (\< et >).</span><span class="sxs-lookup"><span data-stu-id="74628-135">If the type of a <xref:System.Linq.Expressions.BlockExpression> object differs from the type of the last expression in the block, the type is displayed in the `DebugInfo` property in angle brackets (\< and >).</span></span> <span data-ttu-id="74628-136">Sinon, le type de l’objet <xref:System.Linq.Expressions.BlockExpression> n’est pas affiché.</span><span class="sxs-lookup"><span data-stu-id="74628-136">Otherwise, the type of the <xref:System.Linq.Expressions.BlockExpression> object is not displayed.</span></span>

### <a name="examples"></a><span data-ttu-id="74628-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="74628-137">Examples</span></span>

- `Expression`

    ```vb
    Dim block As BlockExpression = Expression.Block(Expression.Constant("test"))
    ```

    <span data-ttu-id="74628-138">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="74628-138">`DebugView` property</span></span>

    `.Block() {`

    `"test"`

    `}`

- `Expression`

    ```vb
    Dim block As BlockExpression =
    Expression.Block(GetType(Object), Expression.Constant("test"))
    ```

    <span data-ttu-id="74628-139">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="74628-139">`DebugView` property</span></span>

    `.Block<System.Object>() {`

    `"test"`

    `}`

## <a name="lambdaexpression"></a><span data-ttu-id="74628-140">LambdaExpression</span><span class="sxs-lookup"><span data-stu-id="74628-140">LambdaExpression</span></span>

<span data-ttu-id="74628-141">Les objets <xref:System.Linq.Expressions.LambdaExpression> sont affichés avec leurs types délégués.</span><span class="sxs-lookup"><span data-stu-id="74628-141"><xref:System.Linq.Expressions.LambdaExpression> objects are displayed together with their delegate types.</span></span>

<span data-ttu-id="74628-142">Si une expression lambda n’a pas de nom, un nom généré automatiquement lui est assigné, tel que `#Lambda1` ou `#Lambda2`.</span><span class="sxs-lookup"><span data-stu-id="74628-142">If a lambda expression does not have a name, it is assigned an automatically generated name, such as `#Lambda1` or `#Lambda2`.</span></span>

### <a name="examples"></a><span data-ttu-id="74628-143">Exemples</span><span class="sxs-lookup"><span data-stu-id="74628-143">Examples</span></span>

- `Expression`

    ```vb
    Dim lambda As LambdaExpression =
    Expression.Lambda(Of Func(Of Integer))(Expression.Constant(1))
    ```

    <span data-ttu-id="74628-144">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="74628-144">`DebugView` property</span></span>

    `.Lambda #Lambda1<System.Func'1[System.Int32]>() {`

    `1`

    `}`

- `Expression`

    ```vb
    Dim lambda As LambdaExpression =
    Expression.Lambda(Of Func(Of Integer))(Expression.Constant(1), "SampleLambda", Nothing)
    ```

    <span data-ttu-id="74628-145">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="74628-145">`DebugView` property</span></span>

    `.Lambda SampleLambda<System.Func'1[System.Int32]>() {`

    `1`

    `}`

## <a name="labelexpression"></a><span data-ttu-id="74628-146">LabelExpression</span><span class="sxs-lookup"><span data-stu-id="74628-146">LabelExpression</span></span>

<span data-ttu-id="74628-147">Si vous spécifiez une valeur par défaut pour l’objet <xref:System.Linq.Expressions.LabelExpression>, cette valeur est affichée avant l’objet <xref:System.Linq.Expressions.LabelTarget>.</span><span class="sxs-lookup"><span data-stu-id="74628-147">If you specify a default value for the <xref:System.Linq.Expressions.LabelExpression> object, this value is displayed before the <xref:System.Linq.Expressions.LabelTarget> object.</span></span>

<span data-ttu-id="74628-148">Le jeton `.Label` indique le début de l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="74628-148">The `.Label` token indicates the start of the label.</span></span> <span data-ttu-id="74628-149">Le jeton `.LabelTarget` indique la destination de la cible à laquelle accéder.</span><span class="sxs-lookup"><span data-stu-id="74628-149">The `.LabelTarget` token indicates the destination of the target to jump to.</span></span>

<span data-ttu-id="74628-150">Si une étiquette n’a pas de nom, un nom généré automatiquement lui est assigné, tel que `#Label1` ou `#Label2`.</span><span class="sxs-lookup"><span data-stu-id="74628-150">If a label does not have a name, it is assigned an automatically generated name, such as `#Label1` or `#Label2`.</span></span>

### <a name="examples"></a><span data-ttu-id="74628-151">Exemples</span><span class="sxs-lookup"><span data-stu-id="74628-151">Examples</span></span>

- `Expression`

    ```vb
    Dim target As LabelTarget = Expression.Label(GetType(Integer), "SampleLabel")
    Dim label1 As BlockExpression = Expression.Block(
    Expression.Goto(target, Expression.Constant(0)),
    Expression.Label(target, Expression.Constant(-1)))
    ```

    <span data-ttu-id="74628-152">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="74628-152">`DebugView` property</span></span>

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

    <span data-ttu-id="74628-153">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="74628-153">`DebugView` property</span></span>

    `.Block() {`

    `.Goto #Label1 { };`

    `.Label`

    `.LabelTarget #Label1:`

    `}`

## <a name="checked-operators"></a><span data-ttu-id="74628-154">Opérateurs Checked</span><span class="sxs-lookup"><span data-stu-id="74628-154">Checked Operators</span></span>

<span data-ttu-id="74628-155">Les opérateurs Checked sont affichés précédés du symbole "#".</span><span class="sxs-lookup"><span data-stu-id="74628-155">Checked operators are displayed with the "#" symbol in front of the operator.</span></span> <span data-ttu-id="74628-156">Par exemple, l’opérateur d’addition checked est affiché sous la forme `#+`.</span><span class="sxs-lookup"><span data-stu-id="74628-156">For example, the checked addition operator is displayed as `#+`.</span></span>

### <a name="examples"></a><span data-ttu-id="74628-157">Exemples</span><span class="sxs-lookup"><span data-stu-id="74628-157">Examples</span></span>

- `Expression`

    ```vb
    Dim expr As Expression = Expression.AddChecked(
    Expression.Constant(1), Expression.Constant(2))
    ```

    <span data-ttu-id="74628-158">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="74628-158">`DebugView` property</span></span>

    `1 #+ 2`

- `Expression`

    ```vb
    Dim expr As Expression = Expression.ConvertChecked(
    Expression.Constant(10.0), GetType(Integer))
    ```

    <span data-ttu-id="74628-159">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="74628-159">`DebugView` property</span></span>

    `#(System.Int32)10D`

## <a name="see-also"></a><span data-ttu-id="74628-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74628-160">See also</span></span>

- [<span data-ttu-id="74628-161">Arborescences d’expressions (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="74628-161">Expression Trees (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/expression-trees/index.md)
- [<span data-ttu-id="74628-162">Débogage dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="74628-162">Debugging in Visual Studio</span></span>](/visualstudio/debugger/debugging-in-visual-studio)
- [<span data-ttu-id="74628-163">Créer des visualiseurs personnalisés</span><span class="sxs-lookup"><span data-stu-id="74628-163">Create Custom Visualizers</span></span>](/visualstudio/debugger/create-custom-visualizers-of-data)
