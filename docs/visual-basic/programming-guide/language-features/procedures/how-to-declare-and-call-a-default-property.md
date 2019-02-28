---
title: 'Procédure : Déclarer et appeler une propriété par défaut en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- defaults [Visual Basic], properties
- properties [Visual Basic], default
- procedures [Visual Basic], defining
- default properties [Visual Basic], in Visual Basic
- Visual Basic code, procedures
- Visual Basic code, properties
- default properties
ms.assetid: 68b4026e-09ef-4613-808e-f6287494ff63
ms.openlocfilehash: c7510147e2abdcfbb71cf79412a9125724776685
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56977550"
---
# <a name="how-to-declare-and-call-a-default-property-in-visual-basic"></a><span data-ttu-id="fc874-102">Procédure : Déclarer et appeler une propriété par défaut en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="fc874-102">How to: Declare and Call a Default Property in Visual Basic</span></span>
<span data-ttu-id="fc874-103">Un *propriété par défaut* est une propriété de classe ou structure auquel votre code peut accéder sans la spécifier.</span><span class="sxs-lookup"><span data-stu-id="fc874-103">A *default property* is a class or structure property that your code can access without specifying it.</span></span> <span data-ttu-id="fc874-104">Lors de l’appel des noms de code, une classe ou structure, mais pas une propriété et le contexte autorise l’accès à une propriété, Visual Basic résout l’accès à cette classe ou propriété par défaut de la structure s’il en existe.</span><span class="sxs-lookup"><span data-stu-id="fc874-104">When calling code names a class or structure but not a property, and the context allows access to a property, Visual Basic resolves the access to that class or structure's default property if one exists.</span></span>  
  
 <span data-ttu-id="fc874-105">Une classe ou structure peut avoir au plus une propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="fc874-105">A class or structure can have at most one default property.</span></span> <span data-ttu-id="fc874-106">Toutefois, vous pouvez surcharger une propriété par défaut et avoir plusieurs versions de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="fc874-106">However, you can overload a default property and have more than one version of it.</span></span>  
  
 <span data-ttu-id="fc874-107">Pour plus d’informations, consultez [par défaut](../../../../visual-basic/language-reference/modifiers/default.md).</span><span class="sxs-lookup"><span data-stu-id="fc874-107">For more information, see [Default](../../../../visual-basic/language-reference/modifiers/default.md).</span></span>  
  
### <a name="to-declare-a-default-property"></a><span data-ttu-id="fc874-108">Pour déclarer une propriété par défaut</span><span class="sxs-lookup"><span data-stu-id="fc874-108">To declare a default property</span></span>  
  
1.  <span data-ttu-id="fc874-109">Déclarez la propriété de façon normale.</span><span class="sxs-lookup"><span data-stu-id="fc874-109">Declare the property in the normal way.</span></span> <span data-ttu-id="fc874-110">Ne spécifiez pas le `Shared` ou `Private` mot clé.</span><span class="sxs-lookup"><span data-stu-id="fc874-110">Do not specify the `Shared` or `Private` keyword.</span></span>  
  
2.  <span data-ttu-id="fc874-111">Inclure le `Default` mot clé dans la déclaration de propriété.</span><span class="sxs-lookup"><span data-stu-id="fc874-111">Include the `Default` keyword in the property declaration.</span></span>  
  
3.  <span data-ttu-id="fc874-112">Spécifiez au moins un paramètre pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="fc874-112">Specify at least one parameter for the property.</span></span> <span data-ttu-id="fc874-113">Vous ne pouvez pas définir une propriété par défaut qui n’accepte pas d’au moins un argument.</span><span class="sxs-lookup"><span data-stu-id="fc874-113">You cannot define a default property that does not take at least one argument.</span></span>  
  
     [!code-vb[VbVbcnProcedures#17](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#17)]  
  
### <a name="to-call-a-default-property"></a><span data-ttu-id="fc874-114">Pour appeler une propriété par défaut</span><span class="sxs-lookup"><span data-stu-id="fc874-114">To call a default property</span></span>  
  
1.  <span data-ttu-id="fc874-115">Déclarez une variable du type de classe ou la structure conteneur.</span><span class="sxs-lookup"><span data-stu-id="fc874-115">Declare a variable of the containing class or structure type.</span></span>  
  
     [!code-vb[VbVbcnProcedures#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#16)]  
  
2.  <span data-ttu-id="fc874-116">Utilisez le nom de variable seul dans une expression où vous inclurez normalement le nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="fc874-116">Use the variable name alone in an expression where you would normally include the property name.</span></span>  
  
     [!code-vb[VbVbcnProcedures#21](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#21)]  
  
3.  <span data-ttu-id="fc874-117">Suivez le nom de variable avec une liste d’arguments entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="fc874-117">Follow the variable name with an argument list in parentheses.</span></span> <span data-ttu-id="fc874-118">Une propriété par défaut doit prendre au moins un argument.</span><span class="sxs-lookup"><span data-stu-id="fc874-118">A default property must take at least one argument.</span></span>  
  
     [!code-vb[VbVbcnProcedures#20](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#20)]  
  
4.  <span data-ttu-id="fc874-119">Pour récupérer la valeur de propriété par défaut, utilisez le nom de variable avec une liste d’arguments dans une expression ou après l’égal (`=`) connectez-vous à une instruction d’assignation.</span><span class="sxs-lookup"><span data-stu-id="fc874-119">To retrieve the default property value, use the variable name, with an argument list, in an expression or following the equal (`=`) sign in an assignment statement.</span></span>  
  
     [!code-vb[VbVbcnProcedures#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#15)]  
  
5.  <span data-ttu-id="fc874-120">Pour définir la valeur de propriété par défaut, utilisez le nom de variable avec une liste d’arguments, sur le côté gauche d’une instruction d’assignation.</span><span class="sxs-lookup"><span data-stu-id="fc874-120">To set the default property value, use the variable name, with an argument list, on the left side of an assignment statement.</span></span>  
  
     [!code-vb[VbVbcnProcedures#14](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#14)]  
  
6.  <span data-ttu-id="fc874-121">Vous pouvez toujours spécifier le nom de propriété par défaut avec le nom de variable, comme vous le feriez pour accéder à n’importe quelle autre propriété.</span><span class="sxs-lookup"><span data-stu-id="fc874-121">You can always specify the default property name together with the variable name, just as you would do to access any other property.</span></span>  
  
     [!code-vb[VbVbcnProcedures#19](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#19)]  
  
## <a name="example"></a><span data-ttu-id="fc874-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="fc874-122">Example</span></span>  
 <span data-ttu-id="fc874-123">L’exemple suivant déclare une propriété par défaut sur une classe.</span><span class="sxs-lookup"><span data-stu-id="fc874-123">The following example declares a default property on a class.</span></span>  
  
 [!code-vb[VbVbcnProcedures#12](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#12)]  
  
## <a name="example"></a><span data-ttu-id="fc874-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="fc874-124">Example</span></span>  
 <span data-ttu-id="fc874-125">L’exemple suivant montre comment appeler la propriété par défaut `myProperty` sur la classe `class1`.</span><span class="sxs-lookup"><span data-stu-id="fc874-125">The following example demonstrates how to call the default property `myProperty` on class `class1`.</span></span> <span data-ttu-id="fc874-126">Stockent des valeurs dans les trois instructions d’assignation `myProperty`et le <xref:Microsoft.VisualBasic.Interaction.MsgBox%2A> appel lit les valeurs.</span><span class="sxs-lookup"><span data-stu-id="fc874-126">The three assignment statements store values in `myProperty`, and the <xref:Microsoft.VisualBasic.Interaction.MsgBox%2A> call reads the values.</span></span>  
  
 [!code-vb[VbVbcnProcedures#13](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#13)]  
  
 <span data-ttu-id="fc874-127">L’utilisation la plus courante d’une propriété par défaut est le <xref:Microsoft.VisualBasic.Collection.Item%2A> propriété sur différentes classes de collection.</span><span class="sxs-lookup"><span data-stu-id="fc874-127">The most common use of a default property is the <xref:Microsoft.VisualBasic.Collection.Item%2A> property on various collection classes.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="fc874-128">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="fc874-128">Robust Programming</span></span>  
 <span data-ttu-id="fc874-129">Propriétés par défaut peuvent entraîner une légère réduction dans les caractères de code source, mais ils peuvent rendre votre code plus difficile à lire.</span><span class="sxs-lookup"><span data-stu-id="fc874-129">Default properties can result in a small reduction in source code-characters, but they can make your code more difficult to read.</span></span> <span data-ttu-id="fc874-130">Si le code appelant n’est pas familiarisé avec votre classe ou structure, lorsqu’il fait référence au nom de classe ou structure il ne peut pas être certains que cette référence accède à la classe ou structure lui-même ou une propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="fc874-130">If the calling code is not familiar with your class or structure, when it makes a reference to the class or structure name it cannot be certain whether that reference accesses the class or structure itself, or a default property.</span></span> <span data-ttu-id="fc874-131">Cela peut entraîner des erreurs du compilateur ou des erreurs de logique d’exécution subtiles.</span><span class="sxs-lookup"><span data-stu-id="fc874-131">This can lead to compiler errors or subtle run-time logic errors.</span></span>  
  
 <span data-ttu-id="fc874-132">Vous pouvez légèrement réduire les risques d’erreurs de propriété par défaut en utilisant toujours la [Option Strict, instruction](../../../../visual-basic/language-reference/statements/option-strict-statement.md) pour définir le contrôle de type du compilateur `On`.</span><span class="sxs-lookup"><span data-stu-id="fc874-132">You can somewhat reduce the chance of default property errors by always using the [Option Strict Statement](../../../../visual-basic/language-reference/statements/option-strict-statement.md) to set compiler type checking to `On`.</span></span>  
  
 <span data-ttu-id="fc874-133">Si vous envisagez d’utiliser une classe prédéfinie ou une structure dans votre code, vous devez déterminer s’il possède une propriété par défaut et si c’est le cas, ce que son nom est.</span><span class="sxs-lookup"><span data-stu-id="fc874-133">If you are planning to use a predefined class or structure in your code, you must determine whether it has a default property, and if so, what its name is.</span></span>  
  
 <span data-ttu-id="fc874-134">En raison de ces inconvénients, vous devez envisager de ne pas définir les propriétés par défaut.</span><span class="sxs-lookup"><span data-stu-id="fc874-134">Because of these disadvantages, you should consider not defining default properties.</span></span> <span data-ttu-id="fc874-135">Pour la lisibilité du code, vous devez également envisager de toujours faire explicitement référence à toutes les propriétés, même les propriétés par défaut.</span><span class="sxs-lookup"><span data-stu-id="fc874-135">For code readability, you should also consider always referring to all properties explicitly, even default properties.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fc874-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc874-136">See also</span></span>
- [<span data-ttu-id="fc874-137">Procédures de propriété</span><span class="sxs-lookup"><span data-stu-id="fc874-137">Property Procedures</span></span>](./property-procedures.md)
- [<span data-ttu-id="fc874-138">Paramètres et arguments d’une procédure</span><span class="sxs-lookup"><span data-stu-id="fc874-138">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)
- [<span data-ttu-id="fc874-139">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="fc874-139">Property Statement</span></span>](../../../../visual-basic/language-reference/statements/property-statement.md)
- [<span data-ttu-id="fc874-140">Default</span><span class="sxs-lookup"><span data-stu-id="fc874-140">Default</span></span>](../../../../visual-basic/language-reference/modifiers/default.md)
- [<span data-ttu-id="fc874-141">Différences entre les propriétés et les Variables en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="fc874-141">Differences Between Properties and Variables in Visual Basic</span></span>](./differences-between-properties-and-variables.md)
- [<span data-ttu-id="fc874-142">Guide pratique pour Créer une propriété</span><span class="sxs-lookup"><span data-stu-id="fc874-142">How to: Create a Property</span></span>](./how-to-create-a-property.md)
- [<span data-ttu-id="fc874-143">Guide pratique pour Déclarer une propriété avec des niveaux d’accès mixtes</span><span class="sxs-lookup"><span data-stu-id="fc874-143">How to: Declare a Property with Mixed Access Levels</span></span>](./how-to-declare-a-property-with-mixed-access-levels.md)
- [<span data-ttu-id="fc874-144">Guide pratique pour Appeler une procédure de propriété</span><span class="sxs-lookup"><span data-stu-id="fc874-144">How to: Call a Property Procedure</span></span>](./how-to-call-a-property-procedure.md)
- [<span data-ttu-id="fc874-145">Guide pratique pour Placer une valeur dans une propriété</span><span class="sxs-lookup"><span data-stu-id="fc874-145">How to: Put a Value in a Property</span></span>](./how-to-put-a-value-in-a-property.md)
- [<span data-ttu-id="fc874-146">Guide pratique pour Obtenir une valeur d’une propriété</span><span class="sxs-lookup"><span data-stu-id="fc874-146">How to: Get a Value from a Property</span></span>](./how-to-get-a-value-from-a-property.md)
