---
title: 'Procédure : Contrôler la portée d’une Variable (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], scope
- declared elements [Visual Basic], scope
- visibility [Visual Basic], declared elements
- variables [Visual Basic], visibility
- scope [Visual Basic], declared elements
- scope [Visual Basic], variables
- scope [Visual Basic], Visual Basic
- declared elements [Visual Basic], visibility
- visibility [Visual Basic], variables
ms.assetid: 44b7f62a-cb5c-4d50-bce9-60ae68f87072
ms.openlocfilehash: 7f1d671f6657c7810ec605533493a340baac39c9
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64610339"
---
# <a name="how-to-control-the-scope-of-a-variable-visual-basic"></a><span data-ttu-id="256b8-102">Procédure : Contrôler la portée d’une Variable (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="256b8-102">How to: Control the Scope of a Variable (Visual Basic)</span></span>
<span data-ttu-id="256b8-103">Normalement, une variable est dans *étendue*, ou est visible par référence, tout au long de la région dans laquelle vous la déclarez.</span><span class="sxs-lookup"><span data-stu-id="256b8-103">Normally, a variable is in *scope*, or visible for reference, throughout the region in which you declare it.</span></span> <span data-ttu-id="256b8-104">Dans de certains cas, la variable *niveau d’accès* peut influencer sa portée.</span><span class="sxs-lookup"><span data-stu-id="256b8-104">In some cases, the variable's *access level* can influence its scope.</span></span>  
  
 <span data-ttu-id="256b8-105">Pour plus d'informations, consultez [Scope in Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/scope.md).</span><span class="sxs-lookup"><span data-stu-id="256b8-105">For more information, see [Scope in Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/scope.md).</span></span>  
  
## <a name="scope-at-block-or-procedure-level"></a><span data-ttu-id="256b8-106">Portée au niveau de la procédure ou de bloc</span><span class="sxs-lookup"><span data-stu-id="256b8-106">Scope at Block or Procedure Level</span></span>  
  
#### <a name="to-make-a-variable-visible-only-within-a-block"></a><span data-ttu-id="256b8-107">Pour rendre une variable visible uniquement dans un bloc</span><span class="sxs-lookup"><span data-stu-id="256b8-107">To make a variable visible only within a block</span></span>  
  
- <span data-ttu-id="256b8-108">Place le [instruction Dim](../../../../visual-basic/language-reference/statements/dim-statement.md) pour la variable entre le début et de fin des instructions de déclaration de ce bloc, par exemple entre les `For` et `Next` instructions d’un `For` boucle.</span><span class="sxs-lookup"><span data-stu-id="256b8-108">Place the [Dim Statement](../../../../visual-basic/language-reference/statements/dim-statement.md) for the variable between the initiating and terminating declaration statements of that block, for example between the `For` and `Next` statements of a `For` loop.</span></span>  
  
     <span data-ttu-id="256b8-109">Vous pouvez faire référence à la variable uniquement à partir du bloc.</span><span class="sxs-lookup"><span data-stu-id="256b8-109">You can refer to the variable only from within the block.</span></span>  
  
#### <a name="to-make-a-variable-visible-only-within-a-procedure"></a><span data-ttu-id="256b8-110">Pour rendre une variable visible uniquement dans une procédure</span><span class="sxs-lookup"><span data-stu-id="256b8-110">To make a variable visible only within a procedure</span></span>  
  
- <span data-ttu-id="256b8-111">Place le `Dim` instruction pour la variable à l’intérieur de la procédure mais en dehors de tout bloc (comme un `With`... `End With` bloc).</span><span class="sxs-lookup"><span data-stu-id="256b8-111">Place the `Dim` statement for the variable inside the procedure but outside any block (such as a `With`...`End With` block).</span></span>  
  
     <span data-ttu-id="256b8-112">Vous pouvez faire référence à la variable uniquement à partir de la procédure, y compris à l’intérieur de n’importe quel bloc contenue dans la procédure.</span><span class="sxs-lookup"><span data-stu-id="256b8-112">You can refer to the variable only from within the procedure, including inside any block contained in the procedure.</span></span>  
  
## <a name="scope-at-module-or-namespace-level"></a><span data-ttu-id="256b8-113">Portée au niveau du Module ou Namespace</span><span class="sxs-lookup"><span data-stu-id="256b8-113">Scope at Module or Namespace Level</span></span>  
 <span data-ttu-id="256b8-114">Pour plus de commodité, le terme unique *au niveau du module* s’appliquent également aux modules, les classes et structures.</span><span class="sxs-lookup"><span data-stu-id="256b8-114">For convenience, the single term *module level* applies equally to modules, classes, and structures.</span></span> <span data-ttu-id="256b8-115">Le niveau d’accès d’une variable de niveau module détermine sa portée.</span><span class="sxs-lookup"><span data-stu-id="256b8-115">The access level of a module level variable determines its scope.</span></span> <span data-ttu-id="256b8-116">L’espace de noms qui contient le module, une classe ou une structure influence également la portée.</span><span class="sxs-lookup"><span data-stu-id="256b8-116">The namespace that contains the module, class, or structure also influences the scope.</span></span>  
  
#### <a name="to-make-a-variable-visible-throughout-a-module-class-or-structure"></a><span data-ttu-id="256b8-117">Pour rendre une variable visible dans l’ensemble d’un module, une classe ou une structure</span><span class="sxs-lookup"><span data-stu-id="256b8-117">To make a variable visible throughout a module, class, or structure</span></span>  
  
1. <span data-ttu-id="256b8-118">Place le `Dim` instruction pour la variable à l’intérieur du module, une classe ou une structure, mais en dehors de toute procédure.</span><span class="sxs-lookup"><span data-stu-id="256b8-118">Place the `Dim` statement for the variable inside the module, class, or structure, but outside any procedure.</span></span>  
  
2. <span data-ttu-id="256b8-119">Inclure le [privé](../../../../visual-basic/language-reference/modifiers/private.md) mot clé dans la `Dim` instruction.</span><span class="sxs-lookup"><span data-stu-id="256b8-119">Include the [Private](../../../../visual-basic/language-reference/modifiers/private.md) keyword in the `Dim` statement.</span></span>  
  
3. <span data-ttu-id="256b8-120">Vous pouvez faire référence à la variable à partir de n’importe où dans le module, une classe ou une structure, mais pas d’à l’extérieur.</span><span class="sxs-lookup"><span data-stu-id="256b8-120">You can refer to the variable from anywhere within the module, class, or structure, but not from outside it.</span></span>  
  
#### <a name="to-make-a-variable-visible-throughout-a-namespace"></a><span data-ttu-id="256b8-121">Pour rendre une variable visible dans l’ensemble d’un espace de noms</span><span class="sxs-lookup"><span data-stu-id="256b8-121">To make a variable visible throughout a namespace</span></span>  
  
1. <span data-ttu-id="256b8-122">Place le `Dim` instruction pour la variable à l’intérieur du module, une classe ou une structure, mais en dehors de toute procédure.</span><span class="sxs-lookup"><span data-stu-id="256b8-122">Place the `Dim` statement for the variable inside the module, class, or structure, but outside any procedure.</span></span>  
  
2. <span data-ttu-id="256b8-123">Inclure le [Friend](../../../../visual-basic/language-reference/modifiers/friend.md) ou [Public](../../../../visual-basic/language-reference/modifiers/public.md) mot clé dans la `Dim` instruction.</span><span class="sxs-lookup"><span data-stu-id="256b8-123">Include the [Friend](../../../../visual-basic/language-reference/modifiers/friend.md) or [Public](../../../../visual-basic/language-reference/modifiers/public.md) keyword in the `Dim` statement.</span></span>  
  
3. <span data-ttu-id="256b8-124">Vous pouvez faire référence à la variable à partir de n’importe où dans l’espace de noms contenant le module, une classe ou une structure.</span><span class="sxs-lookup"><span data-stu-id="256b8-124">You can refer to the variable from anywhere within the namespace containing the module, class, or structure.</span></span>  
  
## <a name="example"></a><span data-ttu-id="256b8-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="256b8-125">Example</span></span>  
 <span data-ttu-id="256b8-126">L’exemple suivant déclare une variable au niveau du module et limite sa visibilité au code dans le module.</span><span class="sxs-lookup"><span data-stu-id="256b8-126">The following example declares a variable at module level and limits its visibility to code within the module.</span></span>  
  
```  
Module demonstrateScope  
    Private strMsg As String  
    Sub initializePrivateVariable()  
        strMsg = "This variable cannot be used outside this module."  
    End Sub  
    Sub usePrivateVariable()  
        MsgBox(strMsg)  
    End Sub  
End Module  
```  
  
 <span data-ttu-id="256b8-127">Dans l’exemple précédent, toutes les procédures définies dans le module `demonstrateScope` peuvent faire référence à la `String` variable `strMsg`.</span><span class="sxs-lookup"><span data-stu-id="256b8-127">In the preceding example, all the procedures defined in module `demonstrateScope` can refer to the `String` variable `strMsg`.</span></span> <span data-ttu-id="256b8-128">Lorsque le `usePrivateVariable` procédure est appelée, elle affiche le contenu de la variable chaîne `strMsg` dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="256b8-128">When the `usePrivateVariable` procedure is called, it displays the contents of the string variable `strMsg` in a dialog box.</span></span>  
  
 <span data-ttu-id="256b8-129">Avec la modification suivante apportée à l’exemple précédent, la variable de chaîne `strMsg` peuvent être référencés par le code n’importe où dans l’espace de noms de sa déclaration.</span><span class="sxs-lookup"><span data-stu-id="256b8-129">With the following alteration to the preceding example, the string variable `strMsg` can be referred to by code anywhere in the namespace of its declaration.</span></span>  
  
```  
Public strMsg As String  
```  
  
## <a name="robust-programming"></a><span data-ttu-id="256b8-130">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="256b8-130">Robust Programming</span></span>  
 <span data-ttu-id="256b8-131">La portée est limitée d’une variable, les opportunités de moins que vous disposez pour accidentellement qui fait référence à la place d’une autre variable portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="256b8-131">The narrower the scope of a variable, the fewer opportunities you have for accidentally referring to it in place of another variable with the same name.</span></span> <span data-ttu-id="256b8-132">Vous pouvez également réduire les problèmes de correspondance de référence.</span><span class="sxs-lookup"><span data-stu-id="256b8-132">You can also minimize problems of reference matching.</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="256b8-133">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="256b8-133">.NET Framework Security</span></span>  
 <span data-ttu-id="256b8-134">La portée est limitée d’une variable, plus le risque qu’un code malveillant peut rendre incorrect l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="256b8-134">The narrower the scope of a variable, the smaller the chances that malicious code can make improper use of it.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="256b8-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="256b8-135">See also</span></span>

- [<span data-ttu-id="256b8-136">Portée dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="256b8-136">Scope in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/declared-elements/scope.md)
- [<span data-ttu-id="256b8-137">Durée de vie en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="256b8-137">Lifetime in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/declared-elements/lifetime.md)
- [<span data-ttu-id="256b8-138">Niveaux d’accès dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="256b8-138">Access levels in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
- [<span data-ttu-id="256b8-139">Variables</span><span class="sxs-lookup"><span data-stu-id="256b8-139">Variables</span></span>](../../../../visual-basic/programming-guide/language-features/variables/index.md)
- [<span data-ttu-id="256b8-140">Déclaration de variable</span><span class="sxs-lookup"><span data-stu-id="256b8-140">Variable Declaration</span></span>](../../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
- [<span data-ttu-id="256b8-141">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="256b8-141">Dim Statement</span></span>](../../../../visual-basic/language-reference/statements/dim-statement.md)
