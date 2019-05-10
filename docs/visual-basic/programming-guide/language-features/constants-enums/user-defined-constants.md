---
title: Constantes définies par l'utilisateur (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- constants [Visual Basic], circular references
- Const statement [Visual Basic], user-defined constants
- user-defined constants [Visual Basic]
- scope [Visual Basic], constants
- constants [Visual Basic], user-defined
- circular references between constants [Visual Basic]
ms.assetid: a1206d5c-c45e-4ac2-970a-4a0be6a05fdd
ms.openlocfilehash: 5d4fe5d1b9048f4a8ae22a84e14456318ca38f0f
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64645860"
---
# <a name="user-defined-constants-visual-basic"></a><span data-ttu-id="f7348-102">Constantes définies par l'utilisateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f7348-102">User-Defined Constants (Visual Basic)</span></span>
<span data-ttu-id="f7348-103">Une constante est un nom significatif qui prend la place d’un nombre ou une chaîne qui ne change pas.</span><span class="sxs-lookup"><span data-stu-id="f7348-103">A constant is a meaningful name that takes the place of a number or string that does not change.</span></span> <span data-ttu-id="f7348-104">Les constantes stockent des valeurs qui, comme leur nom l’indique, demeurent constantes tout au long de l’exécution d’une application.</span><span class="sxs-lookup"><span data-stu-id="f7348-104">Constants store values that, as the name implies, remain constant throughout the execution of an application.</span></span> <span data-ttu-id="f7348-105">Vous pouvez utiliser des constantes qui sont définies par les contrôles ou les composants que vous utilisez, ou vous pouvez créer vos propres.</span><span class="sxs-lookup"><span data-stu-id="f7348-105">You can use constants that are defined by the controls or components you work with, or you can create your own.</span></span> <span data-ttu-id="f7348-106">Les constantes que vous créez vous-même sont décrites en tant que *défini par l’utilisateur*.</span><span class="sxs-lookup"><span data-stu-id="f7348-106">Constants you create yourself are described as *user-defined*.</span></span>  
  
 <span data-ttu-id="f7348-107">Vous déclarez une constante avec la `Const` instruction, en utilisant les mêmes instructions que vous le feriez pour la création d’un nom de variable.</span><span class="sxs-lookup"><span data-stu-id="f7348-107">You declare a constant with the `Const` statement, using the same guidelines you would for creating a variable name.</span></span> <span data-ttu-id="f7348-108">Si `Option Strict` est `On`, vous devez déclarer explicitement le type de constante.</span><span class="sxs-lookup"><span data-stu-id="f7348-108">If `Option Strict` is `On`, you must explicitly declare the constant type.</span></span>  
  
## <a name="const-statement-usage"></a><span data-ttu-id="f7348-109">Utilisation de l’instruction const</span><span class="sxs-lookup"><span data-stu-id="f7348-109">Const Statement Usage</span></span>  
 <span data-ttu-id="f7348-110">Un `Const` instruction peut représenter une valeur mathématique ou date/heure :</span><span class="sxs-lookup"><span data-stu-id="f7348-110">A `Const` statement can represent a mathematical or date/time quantity:</span></span>  
  
 [!code-vb[VbEnumsTask#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#10)]  
  
 <span data-ttu-id="f7348-111">Elle peut également définir `String` constantes :</span><span class="sxs-lookup"><span data-stu-id="f7348-111">It also can define `String` constants:</span></span>  
  
 [!code-vb[VbEnumsTask#13](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#13)]  
  
 <span data-ttu-id="f7348-112">L’expression située à droite du signe égal ( `=` ) est souvent un nombre ou une chaîne littérale, mais elle peut également être une expression qui aboutit à un nombre ou une chaîne (bien que cette expression ne peut pas contenir des appels aux fonctions).</span><span class="sxs-lookup"><span data-stu-id="f7348-112">The expression on the right side of the equal sign ( `=` ) is often a number or literal string, but it also can be an expression that results in a number or string (although that expression cannot contain calls to functions).</span></span> <span data-ttu-id="f7348-113">Vous pouvez même définir des constantes en termes de constantes définies précédemment :</span><span class="sxs-lookup"><span data-stu-id="f7348-113">You can even define constants in terms of previously defined constants:</span></span>  
  
 [!code-vb[VbEnumsTask#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#15)]  
  
## <a name="scope-of-user-defined-constants"></a><span data-ttu-id="f7348-114">Portée des constantes définies par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="f7348-114">Scope of User-Defined Constants</span></span>  
 <span data-ttu-id="f7348-115">Un `Const` étendue de l’instruction est identique à celui d’une variable déclarée dans le même emplacement.</span><span class="sxs-lookup"><span data-stu-id="f7348-115">A `Const` statement's scope is the same as that of a variable declared in the same location.</span></span> <span data-ttu-id="f7348-116">Vous pouvez spécifier l’étendue dans une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="f7348-116">You can specify scope in any of the following ways:</span></span>  
  
- <span data-ttu-id="f7348-117">Pour créer une constante qui existe uniquement dans une procédure, vous devez le déclarer dans celle-ci.</span><span class="sxs-lookup"><span data-stu-id="f7348-117">To create a constant that exists only within a procedure, declare it within that procedure.</span></span>  
  
- <span data-ttu-id="f7348-118">Pour créer une constante disponible pour toutes les procédures dans une classe, mais pas pour le code en dehors de ce module, vous devez le déclarer dans la section des déclarations de la classe.</span><span class="sxs-lookup"><span data-stu-id="f7348-118">To create a constant available to all procedures within a class, but not to any code outside that module, declare it in the declarations section of the class.</span></span>  
  
- <span data-ttu-id="f7348-119">Pour créer une constante qui est disponible pour tous les membres d’un assembly, mais pas pour les clients en dehors de l’assembly, déclarez-le à l’aide de la `Friend` mot clé dans la section des déclarations de la classe.</span><span class="sxs-lookup"><span data-stu-id="f7348-119">To create a constant that is available to all members of an assembly, but not to outside clients of the assembly, declare it using the `Friend` keyword in the declarations section of the class.</span></span>  
  
- <span data-ttu-id="f7348-120">Pour créer une constante disponible tout au long de l’application, déclarez-le à l’aide de la `Public` mot clé dans les déclarations de section de la classe.</span><span class="sxs-lookup"><span data-stu-id="f7348-120">To create a constant available throughout the application, declare it using the `Public` keyword in the declarations section the class.</span></span>  
  
 <span data-ttu-id="f7348-121">Pour plus d'informations, voir [Procédure : Déclarez une constante](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-a-constant.md).</span><span class="sxs-lookup"><span data-stu-id="f7348-121">For more information, see [How to: Declare A Constant](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-a-constant.md).</span></span>  
  
### <a name="avoiding-circular-references"></a><span data-ttu-id="f7348-122">Éviter les références circulaires</span><span class="sxs-lookup"><span data-stu-id="f7348-122">Avoiding Circular References</span></span>  
 <span data-ttu-id="f7348-123">Étant donné que les constantes peuvent être définies en termes d’autres constantes, il est possible de créer par inadvertance un *cycle*, ou une référence circulaire entre deux ou plusieurs constantes.</span><span class="sxs-lookup"><span data-stu-id="f7348-123">Because constants can be defined in terms of other constants, it is possible to inadvertently create a *cycle*, or circular reference, between two or more constants.</span></span> <span data-ttu-id="f7348-124">Un cycle se produit lorsque vous avez deux ou plusieurs constantes publiques, chacun d’eux est défini en termes de l’autre, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="f7348-124">A cycle occurs when you have two or more public constants, each of which is defined in terms of the other, as in the following example:</span></span>  
  
 [!code-vb[VbEnumsTask#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#16)]  
[!code-vb[VbEnumsTask#17](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#17)]  
  
 <span data-ttu-id="f7348-125">Si un cycle se produit, Visual Basic génère une erreur du compilateur.</span><span class="sxs-lookup"><span data-stu-id="f7348-125">If a cycle occurs, Visual Basic generates a compiler error.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f7348-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7348-126">See also</span></span>

- [<span data-ttu-id="f7348-127">Const (instruction)</span><span class="sxs-lookup"><span data-stu-id="f7348-127">Const Statement</span></span>](../../../../visual-basic/language-reference/statements/const-statement.md)
- [<span data-ttu-id="f7348-128">Constantes et types de données littérales</span><span class="sxs-lookup"><span data-stu-id="f7348-128">Constant and Literal Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/constant-and-literal-data-types.md)
- [<span data-ttu-id="f7348-129">Constantes et énumérations</span><span class="sxs-lookup"><span data-stu-id="f7348-129">Constants and Enumerations</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/index.md)
- [<span data-ttu-id="f7348-130">Constantes et énumérations</span><span class="sxs-lookup"><span data-stu-id="f7348-130">Constants and Enumerations</span></span>](../../../../visual-basic/language-reference/constants-and-enumerations.md)
- [<span data-ttu-id="f7348-131">Vue d’ensemble des énumérations</span><span class="sxs-lookup"><span data-stu-id="f7348-131">Enumerations Overview</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-overview.md)
- [<span data-ttu-id="f7348-132">Vue d’ensemble des constantes</span><span class="sxs-lookup"><span data-stu-id="f7348-132">Constants Overview</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/constants-overview.md)
- [<span data-ttu-id="f7348-133">Guide pratique pour Déclarer une énumération</span><span class="sxs-lookup"><span data-stu-id="f7348-133">How to: Declare an Enumeration</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md)
- [<span data-ttu-id="f7348-134">Énumérations et qualification de noms</span><span class="sxs-lookup"><span data-stu-id="f7348-134">Enumerations and Name Qualification</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)
- [<span data-ttu-id="f7348-135">Option Strict (instruction)</span><span class="sxs-lookup"><span data-stu-id="f7348-135">Option Strict Statement</span></span>](../../../../visual-basic/language-reference/statements/option-strict-statement.md)
