---
title: ReadOnly (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.ReadOnly
helpviewer_keywords:
- ReadOnly keyword [Visual Basic]
- variables [Visual Basic], read-only
- ReadOnly property
- properties [Visual Basic], read-only
- read-only variables
ms.assetid: e868185d-6142-4359-a2fd-a7965cadfce8
ms.openlocfilehash: e2957bf49292dfcafab8e78f4b997247c34ad279
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33599910"
---
# <a name="readonly-visual-basic"></a><span data-ttu-id="d2647-102">ReadOnly (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d2647-102">ReadOnly (Visual Basic)</span></span>
<span data-ttu-id="d2647-103">Spécifie qu’une variable ou une propriété peut être lues mais ne pas écrite.</span><span class="sxs-lookup"><span data-stu-id="d2647-103">Specifies that a variable or property can be read but not written.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d2647-104">Notes</span><span class="sxs-lookup"><span data-stu-id="d2647-104">Remarks</span></span>  
  
## <a name="rules"></a><span data-ttu-id="d2647-105">Règles</span><span class="sxs-lookup"><span data-stu-id="d2647-105">Rules</span></span>  
  
-   <span data-ttu-id="d2647-106">**Contexte de déclaration.**</span><span class="sxs-lookup"><span data-stu-id="d2647-106">**Declaration Context.**</span></span> <span data-ttu-id="d2647-107">Vous pouvez utiliser `ReadOnly` seulement au niveau du module.</span><span class="sxs-lookup"><span data-stu-id="d2647-107">You can use `ReadOnly` only at module level.</span></span> <span data-ttu-id="d2647-108">Cela signifie que le contexte de déclaration pour un `ReadOnly` élément doit être une classe, une structure ou un module et ne peut pas être un fichier source, un espace de noms ou une procédure.</span><span class="sxs-lookup"><span data-stu-id="d2647-108">This means the declaration context for a `ReadOnly` element must be a class, structure, or module, and cannot be a source file, namespace, or procedure.</span></span>  
  
-   <span data-ttu-id="d2647-109">**Modificateurs combinés.**</span><span class="sxs-lookup"><span data-stu-id="d2647-109">**Combined Modifiers.**</span></span> <span data-ttu-id="d2647-110">Vous ne pouvez pas spécifier `ReadOnly` avec `Static` dans la même déclaration.</span><span class="sxs-lookup"><span data-stu-id="d2647-110">You cannot specify `ReadOnly` together with `Static` in the same declaration.</span></span>  
  
-   <span data-ttu-id="d2647-111">**Affectation d’une valeur.**</span><span class="sxs-lookup"><span data-stu-id="d2647-111">**Assigning a Value.**</span></span> <span data-ttu-id="d2647-112">Code utilisant un `ReadOnly` propriété ne peut pas définir sa valeur.</span><span class="sxs-lookup"><span data-stu-id="d2647-112">Code consuming a `ReadOnly` property cannot set its value.</span></span> <span data-ttu-id="d2647-113">Mais le code qui a accès au stockage sous-jacent peut attribuer ou modifier la valeur à tout moment.</span><span class="sxs-lookup"><span data-stu-id="d2647-113">But code that has access to the underlying storage can assign or change the value at any time.</span></span>  
  
     <span data-ttu-id="d2647-114">Vous pouvez affecter une valeur à une `ReadOnly` variable uniquement dans sa déclaration ou dans le constructeur d’une classe ou structure dans laquelle il est défini.</span><span class="sxs-lookup"><span data-stu-id="d2647-114">You can assign a value to a `ReadOnly` variable only in its declaration or in the constructor of a class or structure in which it is defined.</span></span>  
  
## <a name="when-to-use-a-readonly-variable"></a><span data-ttu-id="d2647-115">Quand utiliser une Variable en lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2647-115">When to Use a ReadOnly Variable</span></span>  
 <span data-ttu-id="d2647-116">Il existe des situations dans lesquelles vous ne pouvez pas utiliser un [instruction Const](../../../visual-basic/language-reference/statements/const-statement.md) pour déclarer et assigner une valeur constante.</span><span class="sxs-lookup"><span data-stu-id="d2647-116">There are situations in which you cannot use a [Const Statement](../../../visual-basic/language-reference/statements/const-statement.md) to declare and assign a constant value.</span></span> <span data-ttu-id="d2647-117">Par exemple, la `Const` instruction ne peut pas accepter le type de données que vous souhaitez affecter, ou vous n’êtes peut-être pas en mesure de calculer la valeur au moment de la compilation avec une expression constante.</span><span class="sxs-lookup"><span data-stu-id="d2647-117">For example, the `Const` statement might not accept the data type you want to assign, or you might not be able to compute the value at compile time with a constant expression.</span></span> <span data-ttu-id="d2647-118">Vous ne savez pas encore la valeur au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="d2647-118">You might not even know the value at compile time.</span></span> <span data-ttu-id="d2647-119">Dans ce cas, vous pouvez utiliser un `ReadOnly` variable qui doit contenir une valeur constante.</span><span class="sxs-lookup"><span data-stu-id="d2647-119">In these cases, you can use a `ReadOnly` variable to hold a constant value.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="d2647-120">Si le type de données de la variable est un type référence, comme un tableau ou une instance de la classe, ses membres peuvent être changés même si la variable elle-même est `ReadOnly`.</span><span class="sxs-lookup"><span data-stu-id="d2647-120">If the data type of the variable is a reference type, such as an array or a class instance, its members can be changed even if the variable itself is `ReadOnly`.</span></span> <span data-ttu-id="d2647-121">L'exemple suivant illustre ce comportement.</span><span class="sxs-lookup"><span data-stu-id="d2647-121">The following example illustrates this.</span></span>  
  
 `ReadOnly characterArray() As Char = {"x"c, "y"c, "z"c}`  
  
 `Sub changeArrayElement()`  
  
 `characterArray(1) = "M"c`  
  
 `End Sub`  
  
 <span data-ttu-id="d2647-122">Lors de l’initialisation, le tableau vers lequel pointe `characterArray()` contient « x », « y » et « z ».</span><span class="sxs-lookup"><span data-stu-id="d2647-122">When initialized, the array pointed to by `characterArray()` holds "x", "y", and "z".</span></span> <span data-ttu-id="d2647-123">Étant donné que la variable `characterArray` est `ReadOnly`, vous ne pouvez pas modifier sa valeur initialisée ; c'est-à-dire, vous ne pouvez attribuer un nouveau tableau à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="d2647-123">Because the variable `characterArray` is `ReadOnly`, you cannot change its value once it is initialized; that is, you cannot assign a new array to it.</span></span> <span data-ttu-id="d2647-124">Toutefois, vous pouvez modifier les valeurs d’une ou plusieurs des membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="d2647-124">However, you can change the values of one or more of the array members.</span></span> <span data-ttu-id="d2647-125">Après un appel à la procédure `changeArrayElement`, le tableau vers lequel pointe `characterArray()` contient « x », « M » et « z ».</span><span class="sxs-lookup"><span data-stu-id="d2647-125">Following a call to the procedure `changeArrayElement`, the array pointed to by `characterArray()` holds "x", "M", and "z".</span></span>  
  
 <span data-ttu-id="d2647-126">Notez que cela est similaire à la déclaration d’un paramètre de procédure à être [ByVal](../../../visual-basic/language-reference/modifiers/byval.md), ce qui empêche la procédure de modification de l’argument d’appel lui-même, mais lui permet de modifier ses membres.</span><span class="sxs-lookup"><span data-stu-id="d2647-126">Note that this is similar to declaring a procedure parameter to be [ByVal](../../../visual-basic/language-reference/modifiers/byval.md), which prevents the procedure from changing the calling argument itself but allows it to change its members.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d2647-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="d2647-127">Example</span></span>  
 <span data-ttu-id="d2647-128">L’exemple suivant définit un `ReadOnly` propriété pour la date à laquelle un employé a été embauché.</span><span class="sxs-lookup"><span data-stu-id="d2647-128">The following example defines a `ReadOnly` property for the date on which an employee was hired.</span></span> <span data-ttu-id="d2647-129">La classe stocke la valeur de propriété en interne comme un `Private` variable et seul le code à l’intérieur de la classe peut modifier cette valeur.</span><span class="sxs-lookup"><span data-stu-id="d2647-129">The class stores the property value internally as a `Private` variable, and only code inside the class can change that value.</span></span> <span data-ttu-id="d2647-130">Toutefois, la propriété est `Public`, et tout code qui peut accéder à la classe peut lire la propriété.</span><span class="sxs-lookup"><span data-stu-id="d2647-130">However, the property is `Public`, and any code that can access the class can read the property.</span></span>  
  
 [!code-vb[VbVbalrKeywords#4](../../../visual-basic/language-reference/codesnippet/VisualBasic/readonly_1.vb)]  
  
 <span data-ttu-id="d2647-131">Le modificateur `ReadOnly` peut être utilisé dans les contextes suivants :</span><span class="sxs-lookup"><span data-stu-id="d2647-131">The `ReadOnly` modifier can be used in these contexts:</span></span>  
  
 [<span data-ttu-id="d2647-132">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="d2647-132">Dim Statement</span></span>](../../../visual-basic/language-reference/statements/dim-statement.md)  
  
 [<span data-ttu-id="d2647-133">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="d2647-133">Property Statement</span></span>](../../../visual-basic/language-reference/statements/property-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="d2647-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2647-134">See Also</span></span>  
 [<span data-ttu-id="d2647-135">WriteOnly</span><span class="sxs-lookup"><span data-stu-id="d2647-135">WriteOnly</span></span>](../../../visual-basic/language-reference/modifiers/writeonly.md)  
 [<span data-ttu-id="d2647-136">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d2647-136">Keywords</span></span>](../../../visual-basic/language-reference/keywords/index.md)
