---
title: Static (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Static
helpviewer_keywords:
- static modifier
- Static keyword [Visual Basic]
ms.assetid: 19013910-4658-47b6-a22e-1744b527979e
ms.openlocfilehash: f1031fe005a2fc264b50116b8ea3311dc7065dbc
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64647644"
---
# <a name="static-visual-basic"></a><span data-ttu-id="1b5ef-102">Static (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="1b5ef-102">Static (Visual Basic)</span></span>
<span data-ttu-id="1b5ef-103">Spécifie qu’une ou plusieurs variables locales déclarées doivent continuer à exister et conservent leurs valeurs les plus récentes après l’arrêt de la procédure dans laquelle elles sont déclarées.</span><span class="sxs-lookup"><span data-stu-id="1b5ef-103">Specifies that one or more declared local variables are to continue to exist and retain their latest values after termination of the procedure in which they are declared.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1b5ef-104">Notes</span><span class="sxs-lookup"><span data-stu-id="1b5ef-104">Remarks</span></span>  
 <span data-ttu-id="1b5ef-105">Normalement, une variable locale dans une procédure cesse d’exister dès que la procédure s’arrête.</span><span class="sxs-lookup"><span data-stu-id="1b5ef-105">Normally, a local variable in a procedure ceases to exist as soon as the procedure stops.</span></span> <span data-ttu-id="1b5ef-106">Une variable statique continue d’exister et conserve sa valeur la plus récente.</span><span class="sxs-lookup"><span data-stu-id="1b5ef-106">A static variable continues to exist and retains its most recent value.</span></span> <span data-ttu-id="1b5ef-107">La prochaine fois que votre code appelle la procédure, la variable n’est pas réinitialisée, et elle contient toujours la valeur la plus récente que vous avez attribué à ce dernier.</span><span class="sxs-lookup"><span data-stu-id="1b5ef-107">The next time your code calls the procedure, the variable is not reinitialized, and it still holds the latest value that you assigned to it.</span></span> <span data-ttu-id="1b5ef-108">Une variable statique continue d’exister pour la durée de vie de la classe ou le module qui est défini dans.</span><span class="sxs-lookup"><span data-stu-id="1b5ef-108">A static variable continues to exist for the lifetime of the class or module that it is defined in.</span></span>  
  
## <a name="rules"></a><span data-ttu-id="1b5ef-109">Règles</span><span class="sxs-lookup"><span data-stu-id="1b5ef-109">Rules</span></span>  
  
- <span data-ttu-id="1b5ef-110">**Contexte de déclaration.**</span><span class="sxs-lookup"><span data-stu-id="1b5ef-110">**Declaration Context.**</span></span> <span data-ttu-id="1b5ef-111">Vous pouvez utiliser `Static` uniquement sur les variables locales.</span><span class="sxs-lookup"><span data-stu-id="1b5ef-111">You can use `Static` only on local variables.</span></span> <span data-ttu-id="1b5ef-112">Cela signifie que le contexte de déclaration pour un `Static` variable doit être une procédure ou un bloc dans une procédure, et il ne peut pas être un fichier source, un espace de noms, une classe, une structure ou un module.</span><span class="sxs-lookup"><span data-stu-id="1b5ef-112">This means the declaration context for a `Static` variable must be a procedure or a block in a procedure, and it cannot be a source file, namespace, class, structure, or module.</span></span>  
  
     <span data-ttu-id="1b5ef-113">Vous ne pouvez pas utiliser `Static` à l’intérieur d’une procédure de structure.</span><span class="sxs-lookup"><span data-stu-id="1b5ef-113">You cannot use `Static` inside a structure procedure.</span></span>  
  
- <span data-ttu-id="1b5ef-114">Les types de données de `Static` variables locales ne peut pas être déduits.</span><span class="sxs-lookup"><span data-stu-id="1b5ef-114">The data types of `Static` local variables cannot be inferred.</span></span> <span data-ttu-id="1b5ef-115">Pour plus d’informations, consultez [l’inférence de Type Local](../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md).</span><span class="sxs-lookup"><span data-stu-id="1b5ef-115">For more information, see [Local Type Inference](../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md).</span></span>  
  
- <span data-ttu-id="1b5ef-116">**Modificateurs combinés.**</span><span class="sxs-lookup"><span data-stu-id="1b5ef-116">**Combined Modifiers.**</span></span> <span data-ttu-id="1b5ef-117">Vous ne pouvez pas spécifier `Static` avec `ReadOnly`, `Shadows`, ou `Shared` dans la même déclaration.</span><span class="sxs-lookup"><span data-stu-id="1b5ef-117">You cannot specify `Static` together with `ReadOnly`, `Shadows`, or `Shared` in the same declaration.</span></span>  
  
## <a name="behavior"></a><span data-ttu-id="1b5ef-118">Comportement</span><span class="sxs-lookup"><span data-stu-id="1b5ef-118">Behavior</span></span>  
 <span data-ttu-id="1b5ef-119">Lorsque vous déclarez une variable statique dans un `Shared` procédure, qu’une seule copie de la variable statique est disponible pour l’application entière.</span><span class="sxs-lookup"><span data-stu-id="1b5ef-119">When you declare a static variable in a `Shared` procedure, only one copy of the static variable is available for the whole application.</span></span> <span data-ttu-id="1b5ef-120">Vous appelez un `Shared` nom de la procédure à l’aide de la classe, pas une variable qui pointe vers une instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="1b5ef-120">You call a `Shared` procedure by using the class name, not a variable that points to an instance of the class.</span></span>  
  
 <span data-ttu-id="1b5ef-121">Lorsque vous déclarez une variable statique dans une procédure qui n’est pas `Shared`, seule une copie de la variable est disponible pour chaque instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="1b5ef-121">When you declare a static variable in a procedure that isn't `Shared`, only one copy of the variable is available for each instance of the class.</span></span> <span data-ttu-id="1b5ef-122">Vous appelez une procédure non partagée à l’aide d’une variable qui pointe vers une instance spécifique de la classe.</span><span class="sxs-lookup"><span data-stu-id="1b5ef-122">You call a non-shared procedure by using a variable that points to a specific instance of the class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1b5ef-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="1b5ef-123">Example</span></span>  
 <span data-ttu-id="1b5ef-124">L'exemple suivant montre l'utilisation de `Static`.</span><span class="sxs-lookup"><span data-stu-id="1b5ef-124">The following example demonstrates the use of `Static`.</span></span>  
  
 [!code-vb[VbVbalrKeywords#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/Class1.vb#5)]  
  
 <span data-ttu-id="1b5ef-125">Le `Static` variable `totalSales` est initialisée à 0 qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="1b5ef-125">The `Static` variable `totalSales` is initialized to 0 only one time.</span></span> <span data-ttu-id="1b5ef-126">Chaque fois que vous entrez `updateSales`, `totalSales` a toujours la valeur la plus récente que vous avez calculé pour lui.</span><span class="sxs-lookup"><span data-stu-id="1b5ef-126">Each time that you enter `updateSales`, `totalSales` still has the most recent value that you calculated for it.</span></span>  
  
 <span data-ttu-id="1b5ef-127">Le `Static` modificateur peut être utilisé dans ce contexte :</span><span class="sxs-lookup"><span data-stu-id="1b5ef-127">The `Static` modifier can be used in this context:</span></span>  
  
 [<span data-ttu-id="1b5ef-128">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="1b5ef-128">Dim Statement</span></span>](../../../visual-basic/language-reference/statements/dim-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="1b5ef-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b5ef-129">See also</span></span>

- [<span data-ttu-id="1b5ef-130">Shadows</span><span class="sxs-lookup"><span data-stu-id="1b5ef-130">Shadows</span></span>](../../../visual-basic/language-reference/modifiers/shadows.md)
- [<span data-ttu-id="1b5ef-131">Shared</span><span class="sxs-lookup"><span data-stu-id="1b5ef-131">Shared</span></span>](../../../visual-basic/language-reference/modifiers/shared.md)
- [<span data-ttu-id="1b5ef-132">Durée de vie en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="1b5ef-132">Lifetime in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/lifetime.md)
- [<span data-ttu-id="1b5ef-133">Déclaration de variable</span><span class="sxs-lookup"><span data-stu-id="1b5ef-133">Variable Declaration</span></span>](../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
- [<span data-ttu-id="1b5ef-134">Structures</span><span class="sxs-lookup"><span data-stu-id="1b5ef-134">Structures</span></span>](../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [<span data-ttu-id="1b5ef-135">Inférence de type local</span><span class="sxs-lookup"><span data-stu-id="1b5ef-135">Local Type Inference</span></span>](../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)
- [<span data-ttu-id="1b5ef-136">Objets et classes</span><span class="sxs-lookup"><span data-stu-id="1b5ef-136">Objects and Classes</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
