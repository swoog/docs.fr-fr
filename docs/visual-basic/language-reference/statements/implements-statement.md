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
ms.openlocfilehash: 1f0c6b052ead303e0b43465dac2067422abc4ef8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58818867"
---
# <a name="implements-statement"></a><span data-ttu-id="db3f7-102">Implements, instruction</span><span class="sxs-lookup"><span data-stu-id="db3f7-102">Implements Statement</span></span>
<span data-ttu-id="db3f7-103">Spécifie une ou plusieurs interfaces, ou les membres d’interface, qui doivent être implémentées dans la classe ou sur définition de la structure dans laquelle elle apparaît.</span><span class="sxs-lookup"><span data-stu-id="db3f7-103">Specifies one or more interfaces, or interface members, that must be implemented in the class or structure definition in which it appears.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="db3f7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db3f7-104">Syntax</span></span>  
  
```  
Implements interfacename [, ...]  
-or-  
Implements interfacename.interfacemember [, ...]  
```  
  
## <a name="parts"></a><span data-ttu-id="db3f7-105">Composants</span><span class="sxs-lookup"><span data-stu-id="db3f7-105">Parts</span></span>  
 `interfacename`  
 <span data-ttu-id="db3f7-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="db3f7-106">Required.</span></span> <span data-ttu-id="db3f7-107">Une interface dont les propriétés, procédures et les événements doivent être implémentées par des membres correspondants dans la classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="db3f7-107">An interface whose properties, procedures, and events are to be implemented by corresponding members in the class or structure.</span></span>  
  
 `interfacemember`  
 <span data-ttu-id="db3f7-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="db3f7-108">Required.</span></span> <span data-ttu-id="db3f7-109">Le membre d’une interface est implémentée.</span><span class="sxs-lookup"><span data-stu-id="db3f7-109">The member of an interface that is being implemented.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="db3f7-110">Notes</span><span class="sxs-lookup"><span data-stu-id="db3f7-110">Remarks</span></span>  
 <span data-ttu-id="db3f7-111">Une interface est une collection de prototypes représentant les membres (propriétés, procédures et événements) encapsule l’interface.</span><span class="sxs-lookup"><span data-stu-id="db3f7-111">An interface is a collection of prototypes representing the members (properties, procedures, and events) the interface encapsulates.</span></span> <span data-ttu-id="db3f7-112">Interfaces contiennent uniquement les déclarations des membres ; classes et structures implémentent ces membres.</span><span class="sxs-lookup"><span data-stu-id="db3f7-112">Interfaces contain only the declarations for members; classes and structures implement these members.</span></span> <span data-ttu-id="db3f7-113">Pour plus d’informations, consultez [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md).</span><span class="sxs-lookup"><span data-stu-id="db3f7-113">For more information, see [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md).</span></span>  
  
 <span data-ttu-id="db3f7-114">Le `Implements` instruction doit suivre immédiatement le `Class` ou `Structure` instruction.</span><span class="sxs-lookup"><span data-stu-id="db3f7-114">The `Implements` statement must immediately follow the `Class` or `Structure` statement.</span></span>  
  
 <span data-ttu-id="db3f7-115">Lorsque vous implémentez une interface, vous devez implémenter tous les membres déclarés dans l’interface.</span><span class="sxs-lookup"><span data-stu-id="db3f7-115">When you implement an interface, you must implement all the members declared in the interface.</span></span> <span data-ttu-id="db3f7-116">L’omission de n’importe quel membre est considérée comme une erreur de syntaxe.</span><span class="sxs-lookup"><span data-stu-id="db3f7-116">Omitting any member is considered to be a syntax error.</span></span> <span data-ttu-id="db3f7-117">Pour implémenter un membre, vous spécifiez le [implémente](../../../visual-basic/language-reference/statements/implements-clause.md) mot clé (qui est distinct de la `Implements` instruction) lorsque vous déclarez le membre dans la classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="db3f7-117">To implement an individual member, you specify the [Implements](../../../visual-basic/language-reference/statements/implements-clause.md) keyword (which is separate from the `Implements` statement) when you declare the member in the class or structure.</span></span> <span data-ttu-id="db3f7-118">Pour plus d’informations, consultez [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md).</span><span class="sxs-lookup"><span data-stu-id="db3f7-118">For more information, see [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md).</span></span>  
  
 <span data-ttu-id="db3f7-119">Les classes peuvent utiliser [privé](../../../visual-basic/language-reference/modifiers/private.md) implémentations des propriétés et procédures, mais ces membres sont accessibles uniquement par la conversion d’une instance de la classe d’implémentation dans une variable déclarée comme étant du type de l’interface.</span><span class="sxs-lookup"><span data-stu-id="db3f7-119">Classes can use [Private](../../../visual-basic/language-reference/modifiers/private.md) implementations of properties and procedures, but these members are accessible only by casting an instance of the implementing class into a variable declared to be of the type of the interface.</span></span>  
  
## <a name="example"></a><span data-ttu-id="db3f7-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="db3f7-120">Example</span></span>  
 <span data-ttu-id="db3f7-121">L’exemple suivant montre comment utiliser le `Implements` instruction pour implémenter des membres d’une interface.</span><span class="sxs-lookup"><span data-stu-id="db3f7-121">The following example shows how to use the `Implements` statement to implement members of an interface.</span></span> <span data-ttu-id="db3f7-122">Il définit une interface nommée `ICustomerInfo` avec un événement, une propriété et une procédure.</span><span class="sxs-lookup"><span data-stu-id="db3f7-122">It defines an interface named `ICustomerInfo` with an event, a property, and a procedure.</span></span> <span data-ttu-id="db3f7-123">La classe `customerInfo` implémente tous les membres définis dans l’interface.</span><span class="sxs-lookup"><span data-stu-id="db3f7-123">The class `customerInfo` implements all the members defined in the interface.</span></span>  
  
 [!code-vb[VbVbalrStatements#33](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#33)]  
  
 <span data-ttu-id="db3f7-124">Notez que la classe `customerInfo` utilise le `Implements` instruction sur une ligne de code source distinct pour indiquer que la classe implémente tous les membres de la `ICustomerInfo` interface.</span><span class="sxs-lookup"><span data-stu-id="db3f7-124">Note that the class `customerInfo` uses the `Implements` statement on a separate source code line to indicate that the class implements all the members of the `ICustomerInfo` interface.</span></span> <span data-ttu-id="db3f7-125">Ensuite, chaque membre dans la classe utilise le `Implements` mot clé dans le cadre de sa déclaration de membre pour indiquer qu’il implémente ce membre d’interface.</span><span class="sxs-lookup"><span data-stu-id="db3f7-125">Then each member in the class uses the `Implements` keyword as part of its member declaration to indicate that it implements that interface member.</span></span>  
  
## <a name="example"></a><span data-ttu-id="db3f7-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="db3f7-126">Example</span></span>  
 <span data-ttu-id="db3f7-127">Les deux procédures suivantes montrent comment vous pouvez utiliser l’interface implémentée dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="db3f7-127">The following two procedures show how you could use the interface implemented in the preceding example.</span></span> <span data-ttu-id="db3f7-128">Pour tester l’implémentation, ajoutez ces procédures à votre projet et l’appel de la `testImplements` procédure.</span><span class="sxs-lookup"><span data-stu-id="db3f7-128">To test the implementation, add these procedures to your project and call the `testImplements` procedure.</span></span>  
  
 [!code-vb[VbVbalrStatements#34](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#34)]  
  
## <a name="see-also"></a><span data-ttu-id="db3f7-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db3f7-129">See also</span></span>

- [<span data-ttu-id="db3f7-130">Implements</span><span class="sxs-lookup"><span data-stu-id="db3f7-130">Implements</span></span>](../../../visual-basic/language-reference/statements/implements-clause.md)
- [<span data-ttu-id="db3f7-131">Interface (instruction)</span><span class="sxs-lookup"><span data-stu-id="db3f7-131">Interface Statement</span></span>](../../../visual-basic/language-reference/statements/interface-statement.md)
- [<span data-ttu-id="db3f7-132">Interfaces</span><span class="sxs-lookup"><span data-stu-id="db3f7-132">Interfaces</span></span>](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
