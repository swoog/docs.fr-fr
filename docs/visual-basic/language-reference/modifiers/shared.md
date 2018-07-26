---
title: Shared (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Shared
helpviewer_keywords:
- Shared keyword [Visual Basic]
- members [Visual Basic], shared
- shared members
- nonshared
- shared [elements VB]
- elements [Visual Basic], shared
ms.assetid: 2bf7cf2c-b0dd-485e-8749-b5d674dab4cd
ms.openlocfilehash: b76d999bfe3f7ae5205cb9486e040c1d6191b78c
ms.sourcegitcommit: dc02d7d95f1e3efcc7166eaf431b0ec0dc9d8dca
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2018
ms.locfileid: "37143529"
---
# <a name="shared-visual-basic"></a><span data-ttu-id="dae51-102">Shared (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="dae51-102">Shared (Visual Basic)</span></span>
<span data-ttu-id="dae51-103">Spécifie qu’un ou plusieurs éléments de programmation déclarés sont associés à une classe ou structure dans son ensemble et pas avec une instance spécifique de la classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="dae51-103">Specifies that one or more declared programming elements are associated with a class or structure at large, and not with a specific instance of the class or structure.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dae51-104">Notes</span><span class="sxs-lookup"><span data-stu-id="dae51-104">Remarks</span></span>  
  
## <a name="when-to-use-shared"></a><span data-ttu-id="dae51-105">Quand utiliser Shared</span><span class="sxs-lookup"><span data-stu-id="dae51-105">When to Use Shared</span></span>  
 <span data-ttu-id="dae51-106">Le partage un membre d’une classe ou structure le rend disponible pour chaque instance, au lieu de *non partagée*, où chaque instance conserve sa propre copie.</span><span class="sxs-lookup"><span data-stu-id="dae51-106">Sharing a member of a class or structure makes it available to every instance, rather than *nonshared*, where each instance keeps its own copy.</span></span> <span data-ttu-id="dae51-107">Cela est utile, par exemple, si la valeur d’une variable s’applique à l’application entière.</span><span class="sxs-lookup"><span data-stu-id="dae51-107">This is useful, for example, if the value of a variable applies to the entire application.</span></span> <span data-ttu-id="dae51-108">Si vous déclarez cette variable comme étant `Shared`, puis toutes les instances accèdent au même emplacement de stockage, et si une instance modifie la valeur de la variable, toutes les instances accéder à la valeur mise à jour.</span><span class="sxs-lookup"><span data-stu-id="dae51-108">If you declare that variable to be `Shared`, then all instances access the same storage location, and if one instance changes the variable's value, all instances access the updated value.</span></span>  
  
 <span data-ttu-id="dae51-109">Partage n’altère pas le niveau d’accès d’un membre.</span><span class="sxs-lookup"><span data-stu-id="dae51-109">Sharing does not alter the access level of a member.</span></span> <span data-ttu-id="dae51-110">Par exemple, un membre de classe permettre être partagé et privés (accessible uniquement à partir de la classe), ou non partagé et public.</span><span class="sxs-lookup"><span data-stu-id="dae51-110">For example, a class member can be shared and private (accessible only from within the class), or nonshared and public.</span></span> <span data-ttu-id="dae51-111">Pour plus d’informations, consultez [niveaux en Visual Basic d’accès](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span><span class="sxs-lookup"><span data-stu-id="dae51-111">For more information, see [Access levels in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span></span>  
  
## <a name="rules"></a><span data-ttu-id="dae51-112">Règles</span><span class="sxs-lookup"><span data-stu-id="dae51-112">Rules</span></span>  
  
-   <span data-ttu-id="dae51-113">**Contexte de déclaration.**</span><span class="sxs-lookup"><span data-stu-id="dae51-113">**Declaration Context.**</span></span> <span data-ttu-id="dae51-114">Vous pouvez utiliser `Shared` seulement au niveau du module.</span><span class="sxs-lookup"><span data-stu-id="dae51-114">You can use `Shared` only at module level.</span></span> <span data-ttu-id="dae51-115">Cela signifie que le contexte de déclaration pour un `Shared` élément doit être une classe ou structure et ne peut pas être un fichier source, un espace de noms ou une procédure.</span><span class="sxs-lookup"><span data-stu-id="dae51-115">This means the declaration context for a `Shared` element must be a class or structure, and cannot be a source file, namespace, or procedure.</span></span>  
  
-   <span data-ttu-id="dae51-116">**Modificateurs combinés.**</span><span class="sxs-lookup"><span data-stu-id="dae51-116">**Combined Modifiers.**</span></span> <span data-ttu-id="dae51-117">Vous ne pouvez pas spécifier `Shared` avec [substitue](../../../visual-basic/language-reference/modifiers/overrides.md), [Overridable](../../../visual-basic/language-reference/modifiers/overridable.md), [NotOverridable](../../../visual-basic/language-reference/modifiers/notoverridable.md), [MustOverride](../../../visual-basic/language-reference/modifiers/mustoverride.md), ou [ Statique](../../../visual-basic/language-reference/modifiers/static.md) dans la même déclaration.</span><span class="sxs-lookup"><span data-stu-id="dae51-117">You cannot specify `Shared` together with [Overrides](../../../visual-basic/language-reference/modifiers/overrides.md), [Overridable](../../../visual-basic/language-reference/modifiers/overridable.md), [NotOverridable](../../../visual-basic/language-reference/modifiers/notoverridable.md), [MustOverride](../../../visual-basic/language-reference/modifiers/mustoverride.md), or [Static](../../../visual-basic/language-reference/modifiers/static.md) in the same declaration.</span></span>  
  
-   <span data-ttu-id="dae51-118">**L’accès à.**</span><span class="sxs-lookup"><span data-stu-id="dae51-118">**Accessing.**</span></span> <span data-ttu-id="dae51-119">Vous accéder à un élément partagé en qualifiant avec son nom de classe ou structure, et non avec le nom de variable d’une instance spécifique de sa classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="dae51-119">You access a shared element by qualifying it with its class or structure name, not with the variable name of a specific instance of its class or structure.</span></span> <span data-ttu-id="dae51-120">Il est même inutile créer une instance d’une classe ou une structure pour accéder à ses membres partagés.</span><span class="sxs-lookup"><span data-stu-id="dae51-120">You do not even have to create an instance of a class or structure to access its shared members.</span></span>  
  
     <span data-ttu-id="dae51-121">L’exemple suivant appelle la procédure partagée <xref:System.Double.IsNaN%2A> exposées par le <xref:System.Double> structure.</span><span class="sxs-lookup"><span data-stu-id="dae51-121">The following example calls the shared procedure <xref:System.Double.IsNaN%2A> exposed by the <xref:System.Double> structure.</span></span>  
  
     `If Double.IsNaN(result) Then MsgBox("Result is mathematically undefined.")`  
  
-   <span data-ttu-id="dae51-122">**Partage implicite.**</span><span class="sxs-lookup"><span data-stu-id="dae51-122">**Implicit Sharing.**</span></span> <span data-ttu-id="dae51-123">Vous ne pouvez pas utiliser le `Shared` modificateur dans une [instruction Const](../../../visual-basic/language-reference/statements/const-statement.md), mais les constantes sont partagées implicitement.</span><span class="sxs-lookup"><span data-stu-id="dae51-123">You cannot use the `Shared` modifier in a [Const Statement](../../../visual-basic/language-reference/statements/const-statement.md), but constants are implicitly shared.</span></span> <span data-ttu-id="dae51-124">De même, vous ne pouvez pas déclarer un membre d’un module ou une interface devant être `Shared`, mais ils sont partagés implicitement.</span><span class="sxs-lookup"><span data-stu-id="dae51-124">Similarly, you cannot declare a member of a module or an interface to be `Shared`, but they are implicitly shared.</span></span>  
  
## <a name="behavior"></a><span data-ttu-id="dae51-125">Comportement</span><span class="sxs-lookup"><span data-stu-id="dae51-125">Behavior</span></span>  
  
-   <span data-ttu-id="dae51-126">**Stockage.**</span><span class="sxs-lookup"><span data-stu-id="dae51-126">**Storage.**</span></span> <span data-ttu-id="dae51-127">Une variable partagée ou un événement est stocké en mémoire uniquement une fois, quel que soit le nombre d’instances de sa classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="dae51-127">A shared variable or event is stored in memory only once, no matter how many or few instances you create of its class or structure.</span></span> <span data-ttu-id="dae51-128">De même, une procédure partagée ou une propriété conserve uniquement un ensemble de variables locales.</span><span class="sxs-lookup"><span data-stu-id="dae51-128">Similarly, a shared procedure or property holds only one set of local variables.</span></span>  
  
-   <span data-ttu-id="dae51-129">**Accès via une Variable d’Instance.**</span><span class="sxs-lookup"><span data-stu-id="dae51-129">**Accessing through an Instance Variable.**</span></span> <span data-ttu-id="dae51-130">Il est possible d’accéder à un élément partagé en qualifiant avec le nom d’une variable qui contient une instance spécifique de sa classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="dae51-130">It is possible to access a shared element by qualifying it with the name of a variable that contains a specific instance of its class or structure.</span></span> <span data-ttu-id="dae51-131">Bien que cela fonctionne généralement comme prévu, le compilateur génère un message d’avertissement et autorise l’accès via le nom de classe ou une structure au lieu de la variable.</span><span class="sxs-lookup"><span data-stu-id="dae51-131">Although this usually works as expected, the compiler generates a warning message and makes the access through the class or structure name instead of the variable.</span></span>  
  
-   <span data-ttu-id="dae51-132">**Accès via une Expression d’Instance.**</span><span class="sxs-lookup"><span data-stu-id="dae51-132">**Accessing through an Instance Expression.**</span></span> <span data-ttu-id="dae51-133">Si vous accédez à un élément partagé via une expression qui retourne une instance de sa classe ou structure, le compilateur autorise l’accès via le nom de classe ou une structure au lieu d’évaluer l’expression.</span><span class="sxs-lookup"><span data-stu-id="dae51-133">If you access a shared element through an expression that returns an instance of its class or structure, the compiler makes the access through the class or structure name instead of evaluating the expression.</span></span> <span data-ttu-id="dae51-134">Cela produit des résultats inattendus si vous souhaitez que l’expression pour effectuer d’autres actions ainsi que de retourner l’instance.</span><span class="sxs-lookup"><span data-stu-id="dae51-134">This produces unexpected results if you intended the expression to perform other actions as well as returning the instance.</span></span> <span data-ttu-id="dae51-135">L'exemple suivant illustre ce comportement.</span><span class="sxs-lookup"><span data-stu-id="dae51-135">The following example illustrates this.</span></span>  
  
    ```vb
    Sub main()  
        shareTotal.total = 10  
        ' The preceding line is the preferred way to access total.  
        Dim instanceVar As New shareTotal  
        instanceVar.total += 100  
        ' The preceding line generates a compiler warning message and  
        ' accesses total through class shareTotal instead of through  
        ' the variable instanceVar. This works as expected and adds  
        ' 100 to total.  
        returnClass().total += 1000  
        ' The preceding line generates a compiler warning message and  
        ' accesses total through class shareTotal instead of calling  
        ' returnClass(). This adds 1000 to total but does not work as  
        ' expected, because the MsgBox in returnClass() does not run.  
        MsgBox("Value of total is " & CStr(shareTotal.total))  
    End Sub  
    Public Function returnClass() As shareTotal  
        MsgBox("Function returnClass() called")  
        Return New shareTotal  
    End Function  
    Public Class shareTotal  
        Public Shared total As Integer  
    End Class  
    ```  
  
     <span data-ttu-id="dae51-136">Dans l’exemple précédent, le compilateur génère un message d’avertissement à chaque fois que le code accède à la variable partagée `total` via une instance.</span><span class="sxs-lookup"><span data-stu-id="dae51-136">In the preceding example, the compiler generates a warning message both times the code accesses the shared variable `total` through an instance.</span></span> <span data-ttu-id="dae51-137">Dans chaque cas, il autorise l’accès directement par le biais de la classe `shareTotal` et ne rend pas utiliser de n’importe quelle instance.</span><span class="sxs-lookup"><span data-stu-id="dae51-137">In each case it makes the access directly through the class `shareTotal` and does not make use of any instance.</span></span> <span data-ttu-id="dae51-138">Dans le cas de l’appel à la procédure prévu `returnClass`, cela signifie qu’il ne génère pas même un appel à `returnClass`, de sorte que l’action supplémentaire d’affichage « Function returnClass() appelée » n’est pas exécutée.</span><span class="sxs-lookup"><span data-stu-id="dae51-138">In the case of the intended call to the procedure `returnClass`, this means it does not even generate a call to `returnClass`, so the additional action of displaying "Function returnClass() called" is not performed.</span></span>  
  
 <span data-ttu-id="dae51-139">Le modificateur `Shared` peut être utilisé dans les contextes suivants :</span><span class="sxs-lookup"><span data-stu-id="dae51-139">The `Shared` modifier can be used in these contexts:</span></span>  
  
 [<span data-ttu-id="dae51-140">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="dae51-140">Dim Statement</span></span>](../../../visual-basic/language-reference/statements/dim-statement.md)  
  
 [<span data-ttu-id="dae51-141">Event (instruction)</span><span class="sxs-lookup"><span data-stu-id="dae51-141">Event Statement</span></span>](../../../visual-basic/language-reference/statements/event-statement.md)  
  
 [<span data-ttu-id="dae51-142">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="dae51-142">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [<span data-ttu-id="dae51-143">Operator (instruction)</span><span class="sxs-lookup"><span data-stu-id="dae51-143">Operator Statement</span></span>](../../../visual-basic/language-reference/statements/operator-statement.md)  
  
 [<span data-ttu-id="dae51-144">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="dae51-144">Property Statement</span></span>](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [<span data-ttu-id="dae51-145">Sub (instruction)</span><span class="sxs-lookup"><span data-stu-id="dae51-145">Sub Statement</span></span>](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="dae51-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dae51-146">See Also</span></span>  
 [<span data-ttu-id="dae51-147">Shadows</span><span class="sxs-lookup"><span data-stu-id="dae51-147">Shadows</span></span>](../../../visual-basic/language-reference/modifiers/shadows.md)  
 [<span data-ttu-id="dae51-148">Static</span><span class="sxs-lookup"><span data-stu-id="dae51-148">Static</span></span>](../../../visual-basic/language-reference/modifiers/static.md)  
 [<span data-ttu-id="dae51-149">Durée de vie en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="dae51-149">Lifetime in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/lifetime.md)  
 [<span data-ttu-id="dae51-150">Procédures</span><span class="sxs-lookup"><span data-stu-id="dae51-150">Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/index.md)  
 [<span data-ttu-id="dae51-151">Structures</span><span class="sxs-lookup"><span data-stu-id="dae51-151">Structures</span></span>](../../../visual-basic/programming-guide/language-features/data-types/structures.md)  
 [<span data-ttu-id="dae51-152">Objets et classes</span><span class="sxs-lookup"><span data-stu-id="dae51-152">Objects and Classes</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
