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
ms.openlocfilehash: 6e361cbe89f4c51f28199b008de817c2d48ef326
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62051856"
---
# <a name="readonly-visual-basic"></a><span data-ttu-id="64729-102">ReadOnly (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="64729-102">ReadOnly (Visual Basic)</span></span>
<span data-ttu-id="64729-103">Spécifie qu’une variable ou une propriété peut être lue mais ne pas écrite.</span><span class="sxs-lookup"><span data-stu-id="64729-103">Specifies that a variable or property can be read but not written.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="64729-104">Notes</span><span class="sxs-lookup"><span data-stu-id="64729-104">Remarks</span></span>  
  
## <a name="rules"></a><span data-ttu-id="64729-105">Règles</span><span class="sxs-lookup"><span data-stu-id="64729-105">Rules</span></span>  
  
- <span data-ttu-id="64729-106">**Contexte de déclaration.**</span><span class="sxs-lookup"><span data-stu-id="64729-106">**Declaration Context.**</span></span> <span data-ttu-id="64729-107">Vous pouvez utiliser `ReadOnly` seulement au niveau du module.</span><span class="sxs-lookup"><span data-stu-id="64729-107">You can use `ReadOnly` only at module level.</span></span> <span data-ttu-id="64729-108">Cela signifie que le contexte de déclaration pour un `ReadOnly` élément doit être une classe, une structure ou un module et ne peut pas être un fichier source, un espace de noms ou une procédure.</span><span class="sxs-lookup"><span data-stu-id="64729-108">This means the declaration context for a `ReadOnly` element must be a class, structure, or module, and cannot be a source file, namespace, or procedure.</span></span>  
  
- <span data-ttu-id="64729-109">**Modificateurs combinés.**</span><span class="sxs-lookup"><span data-stu-id="64729-109">**Combined Modifiers.**</span></span> <span data-ttu-id="64729-110">Vous ne pouvez pas spécifier `ReadOnly` avec `Static` dans la même déclaration.</span><span class="sxs-lookup"><span data-stu-id="64729-110">You cannot specify `ReadOnly` together with `Static` in the same declaration.</span></span>  
  
- <span data-ttu-id="64729-111">**Affectation d’une valeur.**</span><span class="sxs-lookup"><span data-stu-id="64729-111">**Assigning a Value.**</span></span> <span data-ttu-id="64729-112">Code utilisant un `ReadOnly` propriété ne peut pas définir sa valeur.</span><span class="sxs-lookup"><span data-stu-id="64729-112">Code consuming a `ReadOnly` property cannot set its value.</span></span> <span data-ttu-id="64729-113">Mais le code qui a accès au stockage sous-jacent peut attribuer ou modifier la valeur à tout moment.</span><span class="sxs-lookup"><span data-stu-id="64729-113">But code that has access to the underlying storage can assign or change the value at any time.</span></span>  
  
     <span data-ttu-id="64729-114">Vous pouvez affecter une valeur à une `ReadOnly` variable uniquement dans sa déclaration ou dans le constructeur d’une classe ou une structure dans laquelle il est défini.</span><span class="sxs-lookup"><span data-stu-id="64729-114">You can assign a value to a `ReadOnly` variable only in its declaration or in the constructor of a class or structure in which it is defined.</span></span>  
  
## <a name="when-to-use-a-readonly-variable"></a><span data-ttu-id="64729-115">Quand utiliser une Variable en lecture seule</span><span class="sxs-lookup"><span data-stu-id="64729-115">When to Use a ReadOnly Variable</span></span>  
 <span data-ttu-id="64729-116">Il existe des situations dans lesquelles vous ne pouvez pas utiliser un [instruction Const](../../../visual-basic/language-reference/statements/const-statement.md) pour déclarer et affecter une valeur constante.</span><span class="sxs-lookup"><span data-stu-id="64729-116">There are situations in which you cannot use a [Const Statement](../../../visual-basic/language-reference/statements/const-statement.md) to declare and assign a constant value.</span></span> <span data-ttu-id="64729-117">Par exemple, le `Const` instruction ne peut pas accepter le type de données que vous souhaitez affecter, ou vous ne pouvez pas calculer la valeur au moment de la compilation avec une expression constante.</span><span class="sxs-lookup"><span data-stu-id="64729-117">For example, the `Const` statement might not accept the data type you want to assign, or you might not be able to compute the value at compile time with a constant expression.</span></span> <span data-ttu-id="64729-118">Vous ne savez pas encore la valeur au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="64729-118">You might not even know the value at compile time.</span></span> <span data-ttu-id="64729-119">Dans ce cas, vous pouvez utiliser un `ReadOnly` variable qui doit contenir une valeur constante.</span><span class="sxs-lookup"><span data-stu-id="64729-119">In these cases, you can use a `ReadOnly` variable to hold a constant value.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="64729-120">Si le type de données de la variable est un type référence, tel qu’un tableau ou une instance de la classe, ses membres peuvent être modifiées même si la variable elle-même est `ReadOnly`.</span><span class="sxs-lookup"><span data-stu-id="64729-120">If the data type of the variable is a reference type, such as an array or a class instance, its members can be changed even if the variable itself is `ReadOnly`.</span></span> <span data-ttu-id="64729-121">L'exemple suivant illustre ce comportement.</span><span class="sxs-lookup"><span data-stu-id="64729-121">The following example illustrates this.</span></span>  
  
 `ReadOnly characterArray() As Char = {"x"c, "y"c, "z"c}`  
  
 `Sub changeArrayElement()`  
  
 `characterArray(1) = "M"c`  
  
 `End Sub`  
  
 <span data-ttu-id="64729-122">Cas d’initialisation, le tableau vers lequel pointe `characterArray()` contient « x », « y » et « z ».</span><span class="sxs-lookup"><span data-stu-id="64729-122">When initialized, the array pointed to by `characterArray()` holds "x", "y", and "z".</span></span> <span data-ttu-id="64729-123">Étant donné que la variable `characterArray` est `ReadOnly`, vous ne pouvez pas modifier sa valeur initialisée ; c'est-à-dire, vous ne pouvez pas affectez-lui un nouveau tableau.</span><span class="sxs-lookup"><span data-stu-id="64729-123">Because the variable `characterArray` is `ReadOnly`, you cannot change its value once it is initialized; that is, you cannot assign a new array to it.</span></span> <span data-ttu-id="64729-124">Toutefois, vous pouvez modifier les valeurs d’une ou plusieurs des membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="64729-124">However, you can change the values of one or more of the array members.</span></span> <span data-ttu-id="64729-125">Suite à un appel à la procédure `changeArrayElement`, le tableau vers lequel pointe `characterArray()` contient « x », « M » et « z ».</span><span class="sxs-lookup"><span data-stu-id="64729-125">Following a call to the procedure `changeArrayElement`, the array pointed to by `characterArray()` holds "x", "M", and "z".</span></span>  
  
 <span data-ttu-id="64729-126">Notez que cela est similaire à la déclaration d’un paramètre de procédure à être [ByVal](../../../visual-basic/language-reference/modifiers/byval.md), ce qui empêche la procédure de modification de l’argument d’appel lui-même, mais lui permet de modifier ses membres.</span><span class="sxs-lookup"><span data-stu-id="64729-126">Note that this is similar to declaring a procedure parameter to be [ByVal](../../../visual-basic/language-reference/modifiers/byval.md), which prevents the procedure from changing the calling argument itself but allows it to change its members.</span></span>  
  
## <a name="example"></a><span data-ttu-id="64729-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="64729-127">Example</span></span>  
 <span data-ttu-id="64729-128">L’exemple suivant définit un `ReadOnly` propriété pour la date à laquelle un employé a été embauché.</span><span class="sxs-lookup"><span data-stu-id="64729-128">The following example defines a `ReadOnly` property for the date on which an employee was hired.</span></span> <span data-ttu-id="64729-129">La classe stocke la valeur de propriété en interne comme un `Private` variable et seul le code à l’intérieur de la classe peut modifier cette valeur.</span><span class="sxs-lookup"><span data-stu-id="64729-129">The class stores the property value internally as a `Private` variable, and only code inside the class can change that value.</span></span> <span data-ttu-id="64729-130">Toutefois, la propriété est `Public`, et tout code qui peut accéder à la classe peut lire la propriété.</span><span class="sxs-lookup"><span data-stu-id="64729-130">However, the property is `Public`, and any code that can access the class can read the property.</span></span>  
  
 [!code-vb[VbVbalrKeywords#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/Class1.vb#4)]  
  
 <span data-ttu-id="64729-131">Le modificateur `ReadOnly` peut être utilisé dans les contextes suivants :</span><span class="sxs-lookup"><span data-stu-id="64729-131">The `ReadOnly` modifier can be used in these contexts:</span></span>  
  
 [<span data-ttu-id="64729-132">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="64729-132">Dim Statement</span></span>](../../../visual-basic/language-reference/statements/dim-statement.md)  
  
 [<span data-ttu-id="64729-133">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="64729-133">Property Statement</span></span>](../../../visual-basic/language-reference/statements/property-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="64729-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64729-134">See also</span></span>

- [<span data-ttu-id="64729-135">WriteOnly</span><span class="sxs-lookup"><span data-stu-id="64729-135">WriteOnly</span></span>](../../../visual-basic/language-reference/modifiers/writeonly.md)
- [<span data-ttu-id="64729-136">Mots clés</span><span class="sxs-lookup"><span data-stu-id="64729-136">Keywords</span></span>](../../../visual-basic/language-reference/keywords/index.md)
