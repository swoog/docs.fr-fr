---
title: Implements, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Implements
- Implements
helpviewer_keywords:
- Implements statement [Visual Basic], syntax
- Implements statement [Visual Basic]
- interface implementation [Visual Basic], Implements statement
ms.assetid: 1fafb83f-f55a-4215-8ea9-681e8622613d
ms.openlocfilehash: 805813506b957afb326c71ee4bbb15837726e4e5
ms.sourcegitcommit: 412bbc2e43c3b6ca25b358cdf394be97336f0c24
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/24/2018
ms.locfileid: "42907994"
---
# <a name="implements-statement"></a><span data-ttu-id="dc7f2-102">Implements, instruction</span><span class="sxs-lookup"><span data-stu-id="dc7f2-102">Implements Statement</span></span>
<span data-ttu-id="dc7f2-103">Spécifie une ou plusieurs interfaces, ou les membres d’interface, qui doivent être implémentées dans la classe ou sur définition de la structure dans laquelle elle apparaît.</span><span class="sxs-lookup"><span data-stu-id="dc7f2-103">Specifies one or more interfaces, or interface members, that must be implemented in the class or structure definition in which it appears.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dc7f2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc7f2-104">Syntax</span></span>  
  
```  
Implements interfacename [, ...]  
-or-  
Implements interfacename.interfacemember [, ...]  
```  
  
## <a name="parts"></a><span data-ttu-id="dc7f2-105">Composants</span><span class="sxs-lookup"><span data-stu-id="dc7f2-105">Parts</span></span>  
 `interfacename`  
 <span data-ttu-id="dc7f2-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dc7f2-106">Required.</span></span> <span data-ttu-id="dc7f2-107">Une interface dont les propriétés, procédures et les événements doivent être implémentées par des membres correspondants dans la classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="dc7f2-107">An interface whose properties, procedures, and events are to be implemented by corresponding members in the class or structure.</span></span>  
  
 `interfacemember`  
 <span data-ttu-id="dc7f2-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dc7f2-108">Required.</span></span> <span data-ttu-id="dc7f2-109">Le membre d’une interface est implémentée.</span><span class="sxs-lookup"><span data-stu-id="dc7f2-109">The member of an interface that is being implemented.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dc7f2-110">Notes</span><span class="sxs-lookup"><span data-stu-id="dc7f2-110">Remarks</span></span>  
 <span data-ttu-id="dc7f2-111">Une interface est une collection de prototypes représentant les membres (propriétés, procédures et événements) encapsule l’interface.</span><span class="sxs-lookup"><span data-stu-id="dc7f2-111">An interface is a collection of prototypes representing the members (properties, procedures, and events) the interface encapsulates.</span></span> <span data-ttu-id="dc7f2-112">Interfaces contiennent uniquement les déclarations des membres ; classes et structures implémentent ces membres.</span><span class="sxs-lookup"><span data-stu-id="dc7f2-112">Interfaces contain only the declarations for members; classes and structures implement these members.</span></span> <span data-ttu-id="dc7f2-113">Pour plus d’informations, consultez [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md).</span><span class="sxs-lookup"><span data-stu-id="dc7f2-113">For more information, see [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md).</span></span>  
  
 <span data-ttu-id="dc7f2-114">Le `Implements` instruction doit suivre immédiatement le `Class` ou `Structure` instruction.</span><span class="sxs-lookup"><span data-stu-id="dc7f2-114">The `Implements` statement must immediately follow the `Class` or `Structure` statement.</span></span>  
  
 <span data-ttu-id="dc7f2-115">Lorsque vous implémentez une interface, vous devez implémenter tous les membres déclarés dans l’interface.</span><span class="sxs-lookup"><span data-stu-id="dc7f2-115">When you implement an interface, you must implement all the members declared in the interface.</span></span> <span data-ttu-id="dc7f2-116">L’omission de n’importe quel membre est considérée comme une erreur de syntaxe.</span><span class="sxs-lookup"><span data-stu-id="dc7f2-116">Omitting any member is considered to be a syntax error.</span></span> <span data-ttu-id="dc7f2-117">Pour implémenter un membre, vous spécifiez le [implémente](../../../visual-basic/language-reference/statements/implements-clause.md) mot clé (qui est distinct de la `Implements` instruction) lorsque vous déclarez le membre dans la classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="dc7f2-117">To implement an individual member, you specify the [Implements](../../../visual-basic/language-reference/statements/implements-clause.md) keyword (which is separate from the `Implements` statement) when you declare the member in the class or structure.</span></span> <span data-ttu-id="dc7f2-118">Pour plus d’informations, consultez [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md).</span><span class="sxs-lookup"><span data-stu-id="dc7f2-118">For more information, see [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md).</span></span>  
  
 <span data-ttu-id="dc7f2-119">Les classes peuvent utiliser [privé](../../../visual-basic/language-reference/modifiers/private.md) implémentations des propriétés et procédures, mais ces membres sont accessibles uniquement par la conversion d’une instance de la classe d’implémentation dans une variable déclarée comme étant du type de l’interface.</span><span class="sxs-lookup"><span data-stu-id="dc7f2-119">Classes can use [Private](../../../visual-basic/language-reference/modifiers/private.md) implementations of properties and procedures, but these members are accessible only by casting an instance of the implementing class into a variable declared to be of the type of the interface.</span></span>  
  
## <a name="example"></a><span data-ttu-id="dc7f2-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="dc7f2-120">Example</span></span>  
 <span data-ttu-id="dc7f2-121">L’exemple suivant montre comment utiliser le `Implements` instruction pour implémenter des membres d’une interface.</span><span class="sxs-lookup"><span data-stu-id="dc7f2-121">The following example shows how to use the `Implements` statement to implement members of an interface.</span></span> <span data-ttu-id="dc7f2-122">Il définit une interface nommée `ICustomerInfo` avec un événement, une propriété et une procédure.</span><span class="sxs-lookup"><span data-stu-id="dc7f2-122">It defines an interface named `ICustomerInfo` with an event, a property, and a procedure.</span></span> <span data-ttu-id="dc7f2-123">La classe `customerInfo` implémente tous les membres définis dans l’interface.</span><span class="sxs-lookup"><span data-stu-id="dc7f2-123">The class `customerInfo` implements all the members defined in the interface.</span></span>  
  
 [!code-vb[VbVbalrStatements#33](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/implements-statement_1.vb)]  
  
 <span data-ttu-id="dc7f2-124">Notez que la classe `customerInfo` utilise le `Implements` instruction sur une ligne de code source distinct pour indiquer que la classe implémente tous les membres de la `ICustomerInfo` interface.</span><span class="sxs-lookup"><span data-stu-id="dc7f2-124">Note that the class `customerInfo` uses the `Implements` statement on a separate source code line to indicate that the class implements all the members of the `ICustomerInfo` interface.</span></span> <span data-ttu-id="dc7f2-125">Ensuite, chaque membre dans la classe utilise le `Implements` mot clé dans le cadre de sa déclaration de membre pour indiquer qu’il implémente ce membre d’interface.</span><span class="sxs-lookup"><span data-stu-id="dc7f2-125">Then each member in the class uses the `Implements` keyword as part of its member declaration to indicate that it implements that interface member.</span></span>  
  
## <a name="example"></a><span data-ttu-id="dc7f2-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="dc7f2-126">Example</span></span>  
 <span data-ttu-id="dc7f2-127">Les deux procédures suivantes montrent comment vous pouvez utiliser l’interface implémentée dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="dc7f2-127">The following two procedures show how you could use the interface implemented in the preceding example.</span></span> <span data-ttu-id="dc7f2-128">Pour tester l’implémentation, ajoutez ces procédures à votre projet et l’appel de la `testImplements` procédure.</span><span class="sxs-lookup"><span data-stu-id="dc7f2-128">To test the implementation, add these procedures to your project and call the `testImplements` procedure.</span></span>  
  
 [!code-vb[VbVbalrStatements#34](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/implements-statement_2.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="dc7f2-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc7f2-129">See Also</span></span>  
 [<span data-ttu-id="dc7f2-130">Implements</span><span class="sxs-lookup"><span data-stu-id="dc7f2-130">Implements</span></span>](../../../visual-basic/language-reference/statements/implements-clause.md)  
 [<span data-ttu-id="dc7f2-131">Interface (instruction)</span><span class="sxs-lookup"><span data-stu-id="dc7f2-131">Interface Statement</span></span>](../../../visual-basic/language-reference/statements/interface-statement.md)  
 [<span data-ttu-id="dc7f2-132">Interfaces</span><span class="sxs-lookup"><span data-stu-id="dc7f2-132">Interfaces</span></span>](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
