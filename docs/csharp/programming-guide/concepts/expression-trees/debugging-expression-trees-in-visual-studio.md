---
title: Débogage d’arborescences d’expression dans Visual Studio (C#)
ms.date: 07/20/2015
ms.assetid: 1369fa25-0fbd-4b92-98d0-8df79c49c27a
ms.openlocfilehash: 95a01a98e771e04afd296428ed56e9518bad9ac2
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59330404"
---
# <a name="debugging-expression-trees-in-visual-studio-c"></a><span data-ttu-id="9a2d6-102">Débogage d’arborescences d’expression dans Visual Studio (C#)</span><span class="sxs-lookup"><span data-stu-id="9a2d6-102">Debugging Expression Trees in Visual Studio (C#)</span></span>
<span data-ttu-id="9a2d6-103">Vous pouvez analyser la structure et le contenu d’arborescences d’expression quand vous déboguez vos applications.</span><span class="sxs-lookup"><span data-stu-id="9a2d6-103">You can analyze the structure and content of expression trees when you debug your applications.</span></span> <span data-ttu-id="9a2d6-104">Pour obtenir une vue d’ensemble rapide de la structure de l’arborescence d’expressions, vous pouvez utiliser la propriété `DebugView`, qui est disponible uniquement en mode débogage.</span><span class="sxs-lookup"><span data-stu-id="9a2d6-104">To get a quick overview of the expression tree structure, you can use the `DebugView` property, which is available only in debug mode.</span></span> <span data-ttu-id="9a2d6-105">Pour plus d’informations sur le débogage, consultez [Débogage dans Visual Studio](/visualstudio/debugger/debugging-in-visual-studio).</span><span class="sxs-lookup"><span data-stu-id="9a2d6-105">For more information about debugging, see [Debugging in Visual Studio](/visualstudio/debugger/debugging-in-visual-studio).</span></span>  
  
 <span data-ttu-id="9a2d6-106">Afin de mieux représenter le contenu des arborescences d’expressions, la propriété `DebugView` utilise des visualiseurs Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9a2d6-106">To better represent the content of expression trees, the `DebugView` property uses Visual Studio visualizers.</span></span> <span data-ttu-id="9a2d6-107">Pour plus d’informations, consultez [Créer des visualiseurs de données personnalisés](/visualstudio/debugger/create-custom-visualizers-of-data).</span><span class="sxs-lookup"><span data-stu-id="9a2d6-107">For more information, see [Create Custom Visualizers](/visualstudio/debugger/create-custom-visualizers-of-data).</span></span>  
  
### <a name="to-open-a-visualizer-for-an-expression-tree"></a><span data-ttu-id="9a2d6-108">Pour ouvrir un visualiseur pour une arborescence d’expressions</span><span class="sxs-lookup"><span data-stu-id="9a2d6-108">To open a visualizer for an expression tree</span></span>  
  
1. <span data-ttu-id="9a2d6-109">Cliquez sur l’icône représentant une loupe qui est située en regard de la propriété `DebugView` d’une arborescence d’expressions dans **DataTips**, dans une fenêtre **Espion**, dans la fenêtre **Automatique** ou dans la fenêtre **Variables locales**.</span><span class="sxs-lookup"><span data-stu-id="9a2d6-109">Click the magnifying glass icon that appears next to the `DebugView` property of an expression tree in **DataTips**, a **Watch** window, the **Autos** window, or the **Locals** window.</span></span>  
  
     <span data-ttu-id="9a2d6-110">Une liste de visualiseurs s'affiche.</span><span class="sxs-lookup"><span data-stu-id="9a2d6-110">A list of visualizers is displayed.</span></span>  
  
2. <span data-ttu-id="9a2d6-111">Cliquez sur le visualiseur à utiliser.</span><span class="sxs-lookup"><span data-stu-id="9a2d6-111">Click the visualizer you want to use.</span></span>  
  
 <span data-ttu-id="9a2d6-112">Chaque type d’expression s’affiche dans le visualiseur, comme décrit dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="9a2d6-112">Each expression type is displayed in the visualizer as described in the following sections.</span></span>  
  
## <a name="parameterexpressions"></a><span data-ttu-id="9a2d6-113">ParameterExpressions</span><span class="sxs-lookup"><span data-stu-id="9a2d6-113">ParameterExpressions</span></span>  
 <xref:System.Linq.Expressions.ParameterExpression> <span data-ttu-id="9a2d6-114">Les noms de variables s’affichent avec le symbole « $ » en préfixe.</span><span class="sxs-lookup"><span data-stu-id="9a2d6-114">variable names are displayed with a "$" symbol at the beginning.</span></span>  
  
 <span data-ttu-id="9a2d6-115">Si un paramètre n’a pas de nom, un nom généré automatiquement lui est assigné, tel que `$var1` ou `$var2`.</span><span class="sxs-lookup"><span data-stu-id="9a2d6-115">If a parameter does not have a name, it is assigned an automatically generated name, such as `$var1` or `$var2`.</span></span>  
  
### <a name="examples"></a><span data-ttu-id="9a2d6-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="9a2d6-116">Examples</span></span>  
  
|<span data-ttu-id="9a2d6-117">Expression</span><span class="sxs-lookup"><span data-stu-id="9a2d6-117">Expression</span></span>|`DebugView` <span data-ttu-id="9a2d6-118">propriété</span><span class="sxs-lookup"><span data-stu-id="9a2d6-118">property</span></span>|  
|----------------|--------------------------|  
|`ParameterExpression numParam =  Expression.Parameter(typeof(int), "num");`|`$num`|  
|`ParameterExpression numParam =  Expression.Parameter(typeof(int));`|`$var1`|  
  
## <a name="constantexpressions"></a><span data-ttu-id="9a2d6-119">ConstantExpressions</span><span class="sxs-lookup"><span data-stu-id="9a2d6-119">ConstantExpressions</span></span>  
 <span data-ttu-id="9a2d6-120">Pour les objets <xref:System.Linq.Expressions.ConstantExpression> qui représentent des valeurs entières, des chaînes et des valeurs `null`, la valeur de la constante est affichée.</span><span class="sxs-lookup"><span data-stu-id="9a2d6-120">For <xref:System.Linq.Expressions.ConstantExpression> objects that represent integer values, strings, and `null`, the value of the constant is displayed.</span></span>  
  
 <span data-ttu-id="9a2d6-121">Pour les types numériques comportant des suffixes standard comme littéraux C#, le suffixe est ajouté à la valeur.</span><span class="sxs-lookup"><span data-stu-id="9a2d6-121">For numeric types that have standard suffixes as C# literals, the suffix is added to the value.</span></span> <span data-ttu-id="9a2d6-122">Le tableau suivant indique les suffixes associés aux différents types numériques.</span><span class="sxs-lookup"><span data-stu-id="9a2d6-122">The following table shows the suffixes associated with various numeric types.</span></span>  
  
|<span data-ttu-id="9a2d6-123">Type</span><span class="sxs-lookup"><span data-stu-id="9a2d6-123">Type</span></span>|<span data-ttu-id="9a2d6-124">Suffixe</span><span class="sxs-lookup"><span data-stu-id="9a2d6-124">Suffix</span></span>|  
|----------|------------|  
|<xref:System.UInt32>|<span data-ttu-id="9a2d6-125">U</span><span class="sxs-lookup"><span data-stu-id="9a2d6-125">U</span></span>|  
|<xref:System.Int64>|<span data-ttu-id="9a2d6-126">L</span><span class="sxs-lookup"><span data-stu-id="9a2d6-126">L</span></span>|  
|<xref:System.UInt64>|<span data-ttu-id="9a2d6-127">UL</span><span class="sxs-lookup"><span data-stu-id="9a2d6-127">UL</span></span>|  
|<xref:System.Double>|<span data-ttu-id="9a2d6-128">D</span><span class="sxs-lookup"><span data-stu-id="9a2d6-128">D</span></span>|  
|<xref:System.Single>|<span data-ttu-id="9a2d6-129">F</span><span class="sxs-lookup"><span data-stu-id="9a2d6-129">F</span></span>|  
|<xref:System.Decimal>|<span data-ttu-id="9a2d6-130">M</span><span class="sxs-lookup"><span data-stu-id="9a2d6-130">M</span></span>|  
  
### <a name="examples"></a><span data-ttu-id="9a2d6-131">Exemples</span><span class="sxs-lookup"><span data-stu-id="9a2d6-131">Examples</span></span>  
  
|<span data-ttu-id="9a2d6-132">Expression</span><span class="sxs-lookup"><span data-stu-id="9a2d6-132">Expression</span></span>|`DebugView` <span data-ttu-id="9a2d6-133">propriété</span><span class="sxs-lookup"><span data-stu-id="9a2d6-133">property</span></span>|  
|----------------|--------------------------|  
|`int num = 10; ConstantExpression expr = Expression.Constant(num);`|<span data-ttu-id="9a2d6-134">10</span><span class="sxs-lookup"><span data-stu-id="9a2d6-134">10</span></span>|  
|`double num = 10; ConstantExpression expr = Expression.Constant(num);`|<span data-ttu-id="9a2d6-135">10D</span><span class="sxs-lookup"><span data-stu-id="9a2d6-135">10D</span></span>|  
  
## <a name="blockexpression"></a><span data-ttu-id="9a2d6-136">BlockExpression</span><span class="sxs-lookup"><span data-stu-id="9a2d6-136">BlockExpression</span></span>  
 <span data-ttu-id="9a2d6-137">Si le type d’un objet <xref:System.Linq.Expressions.BlockExpression> diffère du type de la dernière expression du bloc, le type est affiché dans la propriété `DebugInfo` entre crochets pointus (\< et >).</span><span class="sxs-lookup"><span data-stu-id="9a2d6-137">If the type of a <xref:System.Linq.Expressions.BlockExpression> object differs from the type of the last expression in the block, the type is displayed in the `DebugInfo` property in angle brackets (\< and >).</span></span> <span data-ttu-id="9a2d6-138">Sinon, le type de l’objet <xref:System.Linq.Expressions.BlockExpression> n’est pas affiché.</span><span class="sxs-lookup"><span data-stu-id="9a2d6-138">Otherwise, the type of the <xref:System.Linq.Expressions.BlockExpression> object is not displayed.</span></span>  
  
### <a name="examples"></a><span data-ttu-id="9a2d6-139">Exemples</span><span class="sxs-lookup"><span data-stu-id="9a2d6-139">Examples</span></span>  
  
|<span data-ttu-id="9a2d6-140">Expression</span><span class="sxs-lookup"><span data-stu-id="9a2d6-140">Expression</span></span>|`DebugView` <span data-ttu-id="9a2d6-141">propriété</span><span class="sxs-lookup"><span data-stu-id="9a2d6-141">property</span></span>|  
|----------------|--------------------------|  
|`BlockExpression block = Expression.Block(Expression.Constant("test"));`|`.Block() {`<br /><br /> `"test"`<br /><br /> `}`|  
|`BlockExpression block =  Expression.Block(typeof(Object), Expression.Constant("test"));`|`.Block<System.Object>() {`<br /><br /> `"test"`<br /><br /> `}`|  
  
## <a name="lambdaexpression"></a><span data-ttu-id="9a2d6-142">LambdaExpression</span><span class="sxs-lookup"><span data-stu-id="9a2d6-142">LambdaExpression</span></span>  
 <xref:System.Linq.Expressions.LambdaExpression> <span data-ttu-id="9a2d6-143">Les objets s’affichent avec leurs types délégués.</span><span class="sxs-lookup"><span data-stu-id="9a2d6-143">objects are displayed together with their delegate types.</span></span>  
  
 <span data-ttu-id="9a2d6-144">Si une expression lambda n’a pas de nom, un nom généré automatiquement lui est assigné, tel que `#Lambda1` ou `#Lambda2`.</span><span class="sxs-lookup"><span data-stu-id="9a2d6-144">If a lambda expression does not have a name, it is assigned an automatically generated name, such as `#Lambda1` or `#Lambda2`.</span></span>  
  
### <a name="examples"></a><span data-ttu-id="9a2d6-145">Exemples</span><span class="sxs-lookup"><span data-stu-id="9a2d6-145">Examples</span></span>  
  
|<span data-ttu-id="9a2d6-146">Expression</span><span class="sxs-lookup"><span data-stu-id="9a2d6-146">Expression</span></span>|`DebugView` <span data-ttu-id="9a2d6-147">propriété</span><span class="sxs-lookup"><span data-stu-id="9a2d6-147">property</span></span>|  
|----------------|--------------------------|  
|`LambdaExpression lambda =  Expression.Lambda<Func<int>>(Expression.Constant(1));`|`.Lambda #Lambda1<System.Func'1[System.Int32]>() {`<br /><br /> `1`<br /><br /> `}`|  
|`LambdaExpression lambda =  Expression.Lambda<Func<int>>(Expression.Constant(1), "SampleLambda", null);`|`.Lambda SampleLambda<System.Func'1[System.Int32]>() {`<br /><br /> `1`<br /><br /> `}`|  
  
## <a name="labelexpression"></a><span data-ttu-id="9a2d6-148">LabelExpression</span><span class="sxs-lookup"><span data-stu-id="9a2d6-148">LabelExpression</span></span>  
 <span data-ttu-id="9a2d6-149">Si vous spécifiez une valeur par défaut pour l’objet <xref:System.Linq.Expressions.LabelExpression>, cette valeur est affichée avant l’objet <xref:System.Linq.Expressions.LabelTarget>.</span><span class="sxs-lookup"><span data-stu-id="9a2d6-149">If you specify a default value for the <xref:System.Linq.Expressions.LabelExpression> object, this value is displayed before the <xref:System.Linq.Expressions.LabelTarget> object.</span></span>  
  
 <span data-ttu-id="9a2d6-150">Le jeton `.Label` indique le début de l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="9a2d6-150">The `.Label` token indicates the start of the label.</span></span> <span data-ttu-id="9a2d6-151">Le jeton `.LabelTarget` indique la destination de la cible à laquelle accéder.</span><span class="sxs-lookup"><span data-stu-id="9a2d6-151">The `.LabelTarget` token indicates the destination of the target to jump to.</span></span>  
  
 <span data-ttu-id="9a2d6-152">Si une étiquette n’a pas de nom, un nom généré automatiquement lui est assigné, tel que `#Label1` ou `#Label2`.</span><span class="sxs-lookup"><span data-stu-id="9a2d6-152">If a label does not have a name, it is assigned an automatically generated name, such as `#Label1` or `#Label2`.</span></span>  
  
### <a name="examples"></a><span data-ttu-id="9a2d6-153">Exemples</span><span class="sxs-lookup"><span data-stu-id="9a2d6-153">Examples</span></span>  
  
|<span data-ttu-id="9a2d6-154">Expression</span><span class="sxs-lookup"><span data-stu-id="9a2d6-154">Expression</span></span>|`DebugView` <span data-ttu-id="9a2d6-155">propriété</span><span class="sxs-lookup"><span data-stu-id="9a2d6-155">property</span></span>|  
|----------------|--------------------------|  
|`LabelTarget target = Expression.Label(typeof(int), "SampleLabel"); BlockExpression block = Expression.Block( Expression.Goto(target, Expression.Constant(0)), Expression.Label(target, Expression.Constant(-1)));`|`.Block() {`<br /><br /> `.Goto SampleLabel { 0 };`<br /><br /> `.Label`<br /><br /> `-1`<br /><br /> `.LabelTarget SampleLabel:`<br /><br /> `}`|  
|`LabelTarget target = Expression.Label(); BlockExpression block = Expression.Block( Expression.Goto(target5), Expression.Label(target5));`|`.Block() {`<br /><br /> `.Goto #Label1 { };`<br /><br /> `.Label`<br /><br /> `.LabelTarget #Label1:`<br /><br /> `}`|  
  
## <a name="checked-operators"></a><span data-ttu-id="9a2d6-156">Opérateurs Checked</span><span class="sxs-lookup"><span data-stu-id="9a2d6-156">Checked Operators</span></span>  
 <span data-ttu-id="9a2d6-157">Les opérateurs Checked sont affichés précédés du symbole "#".</span><span class="sxs-lookup"><span data-stu-id="9a2d6-157">Checked operators are displayed with the "#" symbol in front of the operator.</span></span> <span data-ttu-id="9a2d6-158">Par exemple, l’opérateur d’addition checked est affiché sous la forme `#+`.</span><span class="sxs-lookup"><span data-stu-id="9a2d6-158">For example, the checked addition operator is displayed as `#+`.</span></span>  
  
### <a name="examples"></a><span data-ttu-id="9a2d6-159">Exemples</span><span class="sxs-lookup"><span data-stu-id="9a2d6-159">Examples</span></span>  
  
|<span data-ttu-id="9a2d6-160">Expression</span><span class="sxs-lookup"><span data-stu-id="9a2d6-160">Expression</span></span>|`DebugView` <span data-ttu-id="9a2d6-161">propriété</span><span class="sxs-lookup"><span data-stu-id="9a2d6-161">property</span></span>|  
|----------------|--------------------------|  
|`Expression expr = Expression.AddChecked( Expression.Constant(1), Expression.Constant(2));`|`1 #+ 2`|  
|`Expression expr = Expression.ConvertChecked( Expression.Constant(10.0), typeof(int));`|`#(System.Int32)10D`|  
  
## <a name="see-also"></a><span data-ttu-id="9a2d6-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a2d6-162">See also</span></span>

- [<span data-ttu-id="9a2d6-163">Arborescences d’expressions (C#)</span><span class="sxs-lookup"><span data-stu-id="9a2d6-163">Expression Trees (C#)</span></span>](../../../../csharp/programming-guide/concepts/expression-trees/index.md)
- [<span data-ttu-id="9a2d6-164">Débogage dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9a2d6-164">Debugging in Visual Studio</span></span>](/visualstudio/debugger/debugging-in-visual-studio)
- [<span data-ttu-id="9a2d6-165">Créer des visualiseurs personnalisés</span><span class="sxs-lookup"><span data-stu-id="9a2d6-165">Create Custom Visualizers</span></span>](/visualstudio/debugger/create-custom-visualizers-of-data)
