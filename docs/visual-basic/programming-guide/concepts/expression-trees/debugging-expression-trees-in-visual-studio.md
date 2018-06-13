---
title: Débogage d’arborescences d’Expression dans Visual Studio (Visual Basic)
ms.date: 07/20/2015
ms.assetid: 492cc28f-b7a2-4c47-b582-b3c437b8a5d5
ms.openlocfilehash: 2addba2654067eaaf6c621c927e0992308879ae4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33644236"
---
# <a name="debugging-expression-trees-in-visual-studio-visual-basic"></a><span data-ttu-id="49f09-102">Débogage d’arborescences d’Expression dans Visual Studio (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="49f09-102">Debugging Expression Trees in Visual Studio (Visual Basic)</span></span>
<span data-ttu-id="49f09-103">Vous pouvez analyser la structure et le contenu d’arborescences d’expression quand vous déboguez vos applications.</span><span class="sxs-lookup"><span data-stu-id="49f09-103">You can analyze the structure and content of expression trees when you debug your applications.</span></span> <span data-ttu-id="49f09-104">Pour obtenir une vue d’ensemble rapide de la structure de l’arborescence d’expressions, vous pouvez utiliser la propriété `DebugView`, qui est disponible uniquement en mode débogage.</span><span class="sxs-lookup"><span data-stu-id="49f09-104">To get a quick overview of the expression tree structure, you can use the `DebugView` property, which is available only in debug mode.</span></span> <span data-ttu-id="49f09-105">Pour plus d’informations sur le débogage, consultez [Débogage dans Visual Studio](/visualstudio/debugger/debugging-in-visual-studio).</span><span class="sxs-lookup"><span data-stu-id="49f09-105">For more information about debugging, see [Debugging in Visual Studio](/visualstudio/debugger/debugging-in-visual-studio).</span></span>  
  
 <span data-ttu-id="49f09-106">Afin de mieux représenter le contenu des arborescences d’expressions, la propriété `DebugView` utilise des visualiseurs Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="49f09-106">To better represent the content of expression trees, the `DebugView` property uses Visual Studio visualizers.</span></span> <span data-ttu-id="49f09-107">Pour plus d’informations, consultez [Créer des visualiseurs de données personnalisés](/visualstudio/debugger/create-custom-visualizers-of-data).</span><span class="sxs-lookup"><span data-stu-id="49f09-107">For more information, see [Create Custom Visualizers](/visualstudio/debugger/create-custom-visualizers-of-data).</span></span>  
  
### <a name="to-open-a-visualizer-for-an-expression-tree"></a><span data-ttu-id="49f09-108">Pour ouvrir un visualiseur pour une arborescence d’expressions</span><span class="sxs-lookup"><span data-stu-id="49f09-108">To open a visualizer for an expression tree</span></span>  
  
1.  <span data-ttu-id="49f09-109">Cliquez sur l’icône représentant une loupe qui est située en regard de la propriété `DebugView` d’une arborescence d’expressions dans **DataTips**, dans une fenêtre **Espion**, dans la fenêtre **Automatique** ou dans la fenêtre **Variables locales**.</span><span class="sxs-lookup"><span data-stu-id="49f09-109">Click the magnifying glass icon that appears next to the `DebugView` property of an expression tree in **DataTips**, a **Watch** window, the **Autos** window, or the **Locals** window.</span></span>  
  
     <span data-ttu-id="49f09-110">Une liste de visualiseurs s'affiche.</span><span class="sxs-lookup"><span data-stu-id="49f09-110">A list of visualizers is displayed.</span></span>  
  
2.  <span data-ttu-id="49f09-111">Cliquez sur le visualiseur à utiliser.</span><span class="sxs-lookup"><span data-stu-id="49f09-111">Click the visualizer you want to use.</span></span>  
  
 <span data-ttu-id="49f09-112">Chaque type d’expression s’affiche dans le visualiseur, comme décrit dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="49f09-112">Each expression type is displayed in the visualizer as described in the following sections.</span></span>  
  
## <a name="parameterexpressions"></a><span data-ttu-id="49f09-113">ParameterExpressions</span><span class="sxs-lookup"><span data-stu-id="49f09-113">ParameterExpressions</span></span>  
 <span data-ttu-id="49f09-114">Les noms de variables <xref:System.Linq.Expressions.ParameterExpression> s’affichent avec le symbole "$" en préfixe.</span><span class="sxs-lookup"><span data-stu-id="49f09-114"><xref:System.Linq.Expressions.ParameterExpression> variable names are displayed with a "$" symbol at the beginning.</span></span>  
  
 <span data-ttu-id="49f09-115">Si un paramètre n’a pas de nom, un nom généré automatiquement lui est assigné, tel que `$var1` ou `$var2`.</span><span class="sxs-lookup"><span data-stu-id="49f09-115">If a parameter does not have a name, it is assigned an automatically generated name, such as `$var1` or `$var2`.</span></span>  
  
### <a name="examples"></a><span data-ttu-id="49f09-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="49f09-116">Examples</span></span>  
  
-   `Expression`  
  
    ```vb  
    Dim numParam As ParameterExpression =   
    Expression.Parameter(GetType(Integer), "num")  
    ```  
  
     <span data-ttu-id="49f09-117">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="49f09-117">`DebugView` property</span></span>  
  
     `$num`  
  
-   `Expression`  
  
    ```vb  
    Dim numParam As ParameterExpression =   
    Expression.Parameter(GetType(Integer))  
    ```  
  
     <span data-ttu-id="49f09-118">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="49f09-118">`DebugView` property</span></span>  
  
     `$var1`  
  
## <a name="constantexpressions"></a><span data-ttu-id="49f09-119">ConstantExpressions</span><span class="sxs-lookup"><span data-stu-id="49f09-119">ConstantExpressions</span></span>  
 <span data-ttu-id="49f09-120">Pour les objets <xref:System.Linq.Expressions.ConstantExpression> qui représentent des valeurs entières, des chaînes et des valeurs `null`, la valeur de la constante est affichée.</span><span class="sxs-lookup"><span data-stu-id="49f09-120">For <xref:System.Linq.Expressions.ConstantExpression> objects that represent integer values, strings, and `null`, the value of the constant is displayed.</span></span>  
  
### <a name="examples"></a><span data-ttu-id="49f09-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="49f09-121">Examples</span></span>  
  
-   `Expression`  
  
    ```vb  
    Dim num as Integer= 10  
    Dim expr As ConstantExpression = Expression.Constant(num)  
    ```  
  
     <span data-ttu-id="49f09-122">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="49f09-122">`DebugView` property</span></span>  
  
     <span data-ttu-id="49f09-123">10</span><span class="sxs-lookup"><span data-stu-id="49f09-123">10</span></span>  
  
-   `Expression`  
  
    ```vb  
    Dim num As Double = 10  
    Dim expr As ConstantExpression = Expression.Constant(num)  
    ```  
  
     <span data-ttu-id="49f09-124">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="49f09-124">`DebugView` property</span></span>  
  
     <span data-ttu-id="49f09-125">10D</span><span class="sxs-lookup"><span data-stu-id="49f09-125">10D</span></span>  
  
## <a name="blockexpression"></a><span data-ttu-id="49f09-126">BlockExpression</span><span class="sxs-lookup"><span data-stu-id="49f09-126">BlockExpression</span></span>  
 <span data-ttu-id="49f09-127">Si le type d’un objet <xref:System.Linq.Expressions.BlockExpression> diffère du type de la dernière expression du bloc, le type est affiché dans la propriété `DebugInfo` entre crochets pointus (\< et >).</span><span class="sxs-lookup"><span data-stu-id="49f09-127">If the type of a <xref:System.Linq.Expressions.BlockExpression> object differs from the type of the last expression in the block, the type is displayed in the `DebugInfo` property in angle brackets (\< and >).</span></span> <span data-ttu-id="49f09-128">Sinon, le type de l’objet <xref:System.Linq.Expressions.BlockExpression> n’est pas affiché.</span><span class="sxs-lookup"><span data-stu-id="49f09-128">Otherwise, the type of the <xref:System.Linq.Expressions.BlockExpression> object is not displayed.</span></span>  
  
### <a name="examples"></a><span data-ttu-id="49f09-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="49f09-129">Examples</span></span>  
  
-   `Expression`  
  
    ```vb  
    Dim block As BlockExpression = Expression.Block(Expression.Constant("test"))  
    ```  
  
     <span data-ttu-id="49f09-130">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="49f09-130">`DebugView` property</span></span>  
  
     `.Block() {`  
  
     `"test"`  
  
     `}`  
  
-   `Expression`  
  
    ```vb  
    Dim block As BlockExpression =   
    Expression.Block(GetType(Object), Expression.Constant("test"))  
    ```  
  
     <span data-ttu-id="49f09-131">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="49f09-131">`DebugView` property</span></span>  
  
     `.Block<System.Object>() {`  
  
     `"test"`  
  
     `}`  
  
## <a name="lambdaexpression"></a><span data-ttu-id="49f09-132">LambdaExpression</span><span class="sxs-lookup"><span data-stu-id="49f09-132">LambdaExpression</span></span>  
 <span data-ttu-id="49f09-133">Les objets <xref:System.Linq.Expressions.LambdaExpression> sont affichés avec leurs types délégués.</span><span class="sxs-lookup"><span data-stu-id="49f09-133"><xref:System.Linq.Expressions.LambdaExpression> objects are displayed together with their delegate types.</span></span>  
  
 <span data-ttu-id="49f09-134">Si une expression lambda n’a pas de nom, un nom généré automatiquement lui est assigné, tel que `#Lambda1` ou `#Lambda2`.</span><span class="sxs-lookup"><span data-stu-id="49f09-134">If a lambda expression does not have a name, it is assigned an automatically generated name, such as `#Lambda1` or `#Lambda2`.</span></span>  
  
### <a name="examples"></a><span data-ttu-id="49f09-135">Exemples</span><span class="sxs-lookup"><span data-stu-id="49f09-135">Examples</span></span>  
  
-   `Expression`  
  
    ```vb  
    Dim lambda As LambdaExpression =   
    Expression.Lambda(Of Func(Of Integer))(Expression.Constant(1))  
    ```  
  
     <span data-ttu-id="49f09-136">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="49f09-136">`DebugView` property</span></span>  
  
     `.Lambda #Lambda1<System.Func'1[System.Int32]>() {`  
  
     `1`  
  
     `}`  
  
-   `Expression`  
  
    ```vb  
    Dim lambda As LambdaExpression =   
    Expression.Lambda(Of Func(Of Integer))(Expression.Constant(1), "SampleLamda", Nothing)  
    ```  
  
     <span data-ttu-id="49f09-137">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="49f09-137">`DebugView` property</span></span>  
  
     `.Lambda SampleLambda<System.Func'1[System.Int32]>() {`  
  
     `1`  
  
     `}`  
  
## <a name="labelexpression"></a><span data-ttu-id="49f09-138">LabelExpression</span><span class="sxs-lookup"><span data-stu-id="49f09-138">LabelExpression</span></span>  
 <span data-ttu-id="49f09-139">Si vous spécifiez une valeur par défaut pour l’objet <xref:System.Linq.Expressions.LabelExpression>, cette valeur est affichée avant l’objet <xref:System.Linq.Expressions.LabelTarget>.</span><span class="sxs-lookup"><span data-stu-id="49f09-139">If you specify a default value for the <xref:System.Linq.Expressions.LabelExpression> object, this value is displayed before the <xref:System.Linq.Expressions.LabelTarget> object.</span></span>  
  
 <span data-ttu-id="49f09-140">Le jeton `.Label` indique le début de l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="49f09-140">The `.Label` token indicates the start of the label.</span></span> <span data-ttu-id="49f09-141">Le jeton `.LabelTarget` indique la destination de la cible à laquelle accéder.</span><span class="sxs-lookup"><span data-stu-id="49f09-141">The `.LabelTarget` token indicates the destination of the target to jump to.</span></span>  
  
 <span data-ttu-id="49f09-142">Si une étiquette n’a pas de nom, un nom généré automatiquement lui est assigné, tel que `#Label1` ou `#Label2`.</span><span class="sxs-lookup"><span data-stu-id="49f09-142">If a label does not have a name, it is assigned an automatically generated name, such as `#Label1` or `#Label2`.</span></span>  
  
### <a name="examples"></a><span data-ttu-id="49f09-143">Exemples</span><span class="sxs-lookup"><span data-stu-id="49f09-143">Examples</span></span>  
  
-   `Expression`  
  
    ```vb  
    Dim target As LabelTarget = Expression.Label(GetType(Integer), "SampleLabel")  
    Dim label1 As BlockExpression = Expression.Block(  
    Expression.Goto(target, Expression.Constant(0)),  
    Expression.Label(target, Expression.Constant(-1)))  
    ```  
  
     <span data-ttu-id="49f09-144">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="49f09-144">`DebugView` property</span></span>  
  
     `.Block() {`  
  
     `.Goto SampleLabel { 0 };`  
  
     `.Label`  
  
     `-1`  
  
     `.LabelTarget SampleLabel:`  
  
     `}`  
  
-   `Expression`  
  
    ```vb  
    Dim target As LabelTarget = Expression.Label()  
    Dim block As BlockExpression = Expression.Block(  
    Expression.Goto(target), Expression.Label(target))  
    ```  
  
     <span data-ttu-id="49f09-145">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="49f09-145">`DebugView` property</span></span>  
  
     `.Block() {`  
  
     `.Goto #Label1 { };`  
  
     `.Label`  
  
     `.LabelTarget #Label1:`  
  
     `}`  
  
## <a name="checked-operators"></a><span data-ttu-id="49f09-146">Opérateurs Checked</span><span class="sxs-lookup"><span data-stu-id="49f09-146">Checked Operators</span></span>  
 <span data-ttu-id="49f09-147">Les opérateurs Checked sont affichés précédés du symbole "#".</span><span class="sxs-lookup"><span data-stu-id="49f09-147">Checked operators are displayed with the "#" symbol in front of the operator.</span></span> <span data-ttu-id="49f09-148">Par exemple, l’opérateur d’addition checked est affiché sous la forme `#+`.</span><span class="sxs-lookup"><span data-stu-id="49f09-148">For example, the checked addition operator is displayed as `#+`.</span></span>  
  
### <a name="examples"></a><span data-ttu-id="49f09-149">Exemples</span><span class="sxs-lookup"><span data-stu-id="49f09-149">Examples</span></span>  
  
-   `Expression`  
  
    ```vb  
    Dim expr As Expression = Expression.AddChecked(  
    Expression.Constant(1), Expression.Constant(2))  
    ```  
  
     <span data-ttu-id="49f09-150">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="49f09-150">`DebugView` property</span></span>  
  
     `1 #+ 2`  
  
-   `Expression`  
  
    ```vb  
    Dim expr As Expression = Expression.ConvertChecked(  
    Expression.Constant(10.0), GetType(Integer))  
    ```  
  
     <span data-ttu-id="49f09-151">Propriété `DebugView`</span><span class="sxs-lookup"><span data-stu-id="49f09-151">`DebugView` property</span></span>  
  
     `#(System.Int32)10D`  
  
## <a name="see-also"></a><span data-ttu-id="49f09-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49f09-152">See Also</span></span>  
 [<span data-ttu-id="49f09-153">Arborescences d’expressions (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="49f09-153">Expression Trees (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/expression-trees/index.md)  
 [<span data-ttu-id="49f09-154">Débogage dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="49f09-154">Debugging in Visual Studio</span></span>](/visualstudio/debugger/debugging-in-visual-studio)  
 [<span data-ttu-id="49f09-155">Créer des visualiseurs personnalisés</span><span class="sxs-lookup"><span data-stu-id="49f09-155">Create Custom Visualizers</span></span>](/visualstudio/debugger/create-custom-visualizers-of-data)
