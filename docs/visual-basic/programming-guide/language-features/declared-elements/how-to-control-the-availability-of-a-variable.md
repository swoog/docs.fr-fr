---
title: 'Procédure : Contrôler la disponibilité d’une Variable (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- access levels, declared elements
- Private keyword [Visual Basic], accessing variables
- access levels, variables
- Public keyword [Visual Basic], accessing variables
- Friend keyword [Visual Basic], accessing variables
- variables [Visual Basic], access level
- declared elements [Visual Basic], access level
- Protected keyword [Visual Basic], accessing variables
ms.assetid: eaf4f073-7922-43ce-ae1e-90ff376ae947
ms.openlocfilehash: fb7c04ac6c24648dfb2a8cfa5e01bf97c6b0b3be
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58841691"
---
# <a name="how-to-control-the-availability-of-a-variable-visual-basic"></a><span data-ttu-id="611eb-102">Procédure : Contrôler la disponibilité d’une Variable (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="611eb-102">How to: Control the Availability of a Variable (Visual Basic)</span></span>
<span data-ttu-id="611eb-103">Vous pouvez contrôler la disponibilité d’une variable en spécifiant son *niveau d’accès*.</span><span class="sxs-lookup"><span data-stu-id="611eb-103">You control the availability of a variable by specifying its *access level*.</span></span> <span data-ttu-id="611eb-104">Le niveau d’accès détermine quel code est autorisé à lire ou écrire dans la variable.</span><span class="sxs-lookup"><span data-stu-id="611eb-104">The access level determines what code has permission to read or write to the variable.</span></span>  
  
-   <span data-ttu-id="611eb-105">*Variables membres* (défini au niveau du module et en dehors de toute procédure) par défaut d’un accès public, ce qui signifie que tout code qui puisse les voir pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="611eb-105">*Member variables* (defined at module level and outside any procedure) default to public access, which means any code that can see them can access them.</span></span> <span data-ttu-id="611eb-106">Vous pouvez le modifier en spécifiant un modificateur d’accès.</span><span class="sxs-lookup"><span data-stu-id="611eb-106">You can change this by specifying an access modifier.</span></span>  
  
-   <span data-ttu-id="611eb-107">*Variables locales* (défini à l’intérieur d’une procédure) nominalement ont un accès public, bien que seul le code dans leur procédure permettre y accéder.</span><span class="sxs-lookup"><span data-stu-id="611eb-107">*Local variables* (defined inside a procedure) nominally have public access, although only code within their procedure can access them.</span></span> <span data-ttu-id="611eb-108">Vous ne pouvez pas modifier le niveau d’accès d’une variable locale, mais vous pouvez modifier le niveau d’accès de la procédure qui le contient.</span><span class="sxs-lookup"><span data-stu-id="611eb-108">You cannot change the access level of a local variable, but you can change the access level of the procedure that contains it.</span></span>  
  
 <span data-ttu-id="611eb-109">Pour plus d’informations, consultez [niveaux en Visual Basic d’accès](../../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span><span class="sxs-lookup"><span data-stu-id="611eb-109">For more information, see [Access levels in Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span></span>  
  
## <a name="private-and-public-access"></a><span data-ttu-id="611eb-110">Accès privé et Public</span><span class="sxs-lookup"><span data-stu-id="611eb-110">Private and Public Access</span></span>  
  
#### <a name="to-make-a-variable-accessible-only-from-within-its-module-class-or-structure"></a><span data-ttu-id="611eb-111">Pour rendre une variable accessible uniquement à partir de son module, une classe ou une structure</span><span class="sxs-lookup"><span data-stu-id="611eb-111">To make a variable accessible only from within its module, class, or structure</span></span>  
  
1.  <span data-ttu-id="611eb-112">Place le [instruction Dim](../../../../visual-basic/language-reference/statements/dim-statement.md) pour la variable à l’intérieur du module, une classe ou une structure, mais en dehors de toute procédure.</span><span class="sxs-lookup"><span data-stu-id="611eb-112">Place the [Dim Statement](../../../../visual-basic/language-reference/statements/dim-statement.md) for the variable inside the module, class, or structure, but outside any procedure.</span></span>  
  
2.  <span data-ttu-id="611eb-113">Inclure le [privé](../../../../visual-basic/language-reference/modifiers/private.md) mot clé dans la `Dim` instruction.</span><span class="sxs-lookup"><span data-stu-id="611eb-113">Include the [Private](../../../../visual-basic/language-reference/modifiers/private.md) keyword in the `Dim` statement.</span></span>  
  
     <span data-ttu-id="611eb-114">Vous pouvez lire ou écrire dans la variable à partir de n’importe où dans le module, une classe ou une structure, mais pas d’à l’extérieur.</span><span class="sxs-lookup"><span data-stu-id="611eb-114">You can read or write to the variable from anywhere within the module, class, or structure, but not from outside it.</span></span>  
  
#### <a name="to-make-a-variable-accessible-from-any-code-that-can-see-it"></a><span data-ttu-id="611eb-115">Pour rendre une variable accessible à partir de n’importe quel code qui peut le consulter</span><span class="sxs-lookup"><span data-stu-id="611eb-115">To make a variable accessible from any code that can see it</span></span>  
  
1.  <span data-ttu-id="611eb-116">Pour une variable membre, placez la `Dim` instruction pour la variable à l’intérieur d’un module, une classe ou une structure, mais en dehors de toute procédure.</span><span class="sxs-lookup"><span data-stu-id="611eb-116">For a member variable, place the `Dim` statement for the variable inside a module, class, or structure, but outside any procedure.</span></span>  
  
2.  <span data-ttu-id="611eb-117">Inclure le [Public](../../../../visual-basic/language-reference/modifiers/public.md) mot clé dans la `Dim` instruction.</span><span class="sxs-lookup"><span data-stu-id="611eb-117">Include the [Public](../../../../visual-basic/language-reference/modifiers/public.md) keyword in the `Dim` statement.</span></span>  
  
     <span data-ttu-id="611eb-118">Vous pouvez lire ou écrire dans la variable à partir de n’importe quel code qui interagit avec votre assembly.</span><span class="sxs-lookup"><span data-stu-id="611eb-118">You can read or write to the variable from any code that interoperates with your assembly.</span></span>  
  
 <span data-ttu-id="611eb-119">- ou -</span><span class="sxs-lookup"><span data-stu-id="611eb-119">-or-</span></span>  
  
1.  <span data-ttu-id="611eb-120">Pour une variable locale, placez la `Dim` instruction pour la variable à l’intérieur d’une procédure.</span><span class="sxs-lookup"><span data-stu-id="611eb-120">For a local variable, place the `Dim` statement for the variable inside a procedure.</span></span>  
  
2.  <span data-ttu-id="611eb-121">N’incluez pas le `Public` mot clé dans la `Dim` instruction.</span><span class="sxs-lookup"><span data-stu-id="611eb-121">Do not include the `Public` keyword in the `Dim` statement.</span></span>  
  
     <span data-ttu-id="611eb-122">Vous pouvez lire ou écrire dans la variable à partir de n’importe où dans la procédure, mais pas d’à l’extérieur.</span><span class="sxs-lookup"><span data-stu-id="611eb-122">You can read or write to the variable from anywhere within the procedure, but not from outside it.</span></span>  
  
## <a name="protected-and-friend-access"></a><span data-ttu-id="611eb-123">Protégé et un accès Friend</span><span class="sxs-lookup"><span data-stu-id="611eb-123">Protected and Friend Access</span></span>  
 <span data-ttu-id="611eb-124">Vous pouvez limiter le niveau d’accès d’une variable à sa classe et toutes les classes dérivées, ou à son assembly.</span><span class="sxs-lookup"><span data-stu-id="611eb-124">You can limit the access level of a variable to its class and any derived classes, or to its assembly.</span></span> <span data-ttu-id="611eb-125">Vous pouvez également spécifier l’union de ces limitations, ce qui permet d’accéder à partir du code dans n’importe quelle classe dérivée ou dans tout autre emplacement dans le même assembly.</span><span class="sxs-lookup"><span data-stu-id="611eb-125">You can also specify the union of these limitations, which allows access from code in any derived class or in any other place in the same assembly.</span></span> <span data-ttu-id="611eb-126">Vous spécifiez cette union en combinant le `Protected` et `Friend` mots clés dans la même déclaration.</span><span class="sxs-lookup"><span data-stu-id="611eb-126">You specify this union by combining the `Protected` and `Friend` keywords in the same declaration.</span></span>  
  
#### <a name="to-make-a-variable-accessible-only-from-within-its-class-and-any-derived-classes"></a><span data-ttu-id="611eb-127">Pour rendre une variable accessible uniquement à partir de sa classe et toutes les classes dérivées</span><span class="sxs-lookup"><span data-stu-id="611eb-127">To make a variable accessible only from within its class and any derived classes</span></span>  
  
1.  <span data-ttu-id="611eb-128">Place le `Dim` instruction pour la variable à l’intérieur d’une classe, mais en dehors de toute procédure.</span><span class="sxs-lookup"><span data-stu-id="611eb-128">Place the `Dim` statement for the variable inside a class, but outside any procedure.</span></span>  
  
2.  <span data-ttu-id="611eb-129">Inclure le [protégé](../../../../visual-basic/language-reference/modifiers/protected.md) mot clé dans la `Dim` instruction.</span><span class="sxs-lookup"><span data-stu-id="611eb-129">Include the [Protected](../../../../visual-basic/language-reference/modifiers/protected.md) keyword in the `Dim` statement.</span></span>  
  
     <span data-ttu-id="611eb-130">Vous pouvez lire ou écrire dans la variable à partir de n’importe où dans la classe, ainsi que depuis n’importe quelle classe dérivée à partir de celui-ci, mais pas d’en dehors de toute classe dans la chaîne de dérivation.</span><span class="sxs-lookup"><span data-stu-id="611eb-130">You can read or write to the variable from anywhere within the class, as well as from within any class derived from it, but not from outside any class in the derivation chain.</span></span>  
  
#### <a name="to-make-a-variable-accessible-only-from-within-the-same-assembly"></a><span data-ttu-id="611eb-131">Pour rendre une variable accessible uniquement à partir du même assembly</span><span class="sxs-lookup"><span data-stu-id="611eb-131">To make a variable accessible only from within the same assembly</span></span>  
  
1.  <span data-ttu-id="611eb-132">Place le `Dim` instruction pour la variable à l’intérieur d’un module, une classe ou une structure, mais en dehors de toute procédure.</span><span class="sxs-lookup"><span data-stu-id="611eb-132">Place the `Dim` statement for the variable inside a module, class, or structure, but outside any procedure.</span></span>  
  
2.  <span data-ttu-id="611eb-133">Inclure le [Friend](../../../../visual-basic/language-reference/modifiers/friend.md) mot clé dans la `Dim` instruction.</span><span class="sxs-lookup"><span data-stu-id="611eb-133">Include the [Friend](../../../../visual-basic/language-reference/modifiers/friend.md) keyword in the `Dim` statement.</span></span>  
  
     <span data-ttu-id="611eb-134">Vous pouvez lire ou écrire dans la variable à partir de n’importe où dans le module, une classe ou une structure, ainsi qu’à partir de n’importe quel code dans le même assembly, mais pas de l’extérieur de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="611eb-134">You can read or write to the variable from anywhere within the module, class, or structure, as well as from any code in the same assembly, but not from outside the assembly.</span></span>  
  
## <a name="example"></a><span data-ttu-id="611eb-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="611eb-135">Example</span></span>  
 <span data-ttu-id="611eb-136">L’exemple suivant montre des déclarations de variables avec `Public`, `Protected`, `Friend`, `Protected Friend`, et `Private` niveaux d’accès.</span><span class="sxs-lookup"><span data-stu-id="611eb-136">The following example shows declarations of variables with `Public`, `Protected`, `Friend`, `Protected Friend`, and `Private` access levels.</span></span> <span data-ttu-id="611eb-137">Notez que lorsque le `Dim` instruction spécifie un niveau d’accès, vous n’avez pas besoin d’inclure le `Dim` mot clé.</span><span class="sxs-lookup"><span data-stu-id="611eb-137">Note that when the `Dim` statement specifies an access level, you do not need to include the `Dim` keyword.</span></span>  
  
```  
Public Class classForEverybody  
Protected Class classForMyHeirs  
Friend stringForThisProject As String  
Protected Friend stringForProjectAndHeirs As String  
Private numberForMeOnly As Integer  
```  
  
## <a name="net-framework-security"></a><span data-ttu-id="611eb-138">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="611eb-138">.NET Framework Security</span></span>  
 <span data-ttu-id="611eb-139">Le plus restrictif le niveau d’accès d’une variable, plus le risque qu’un code malveillant peut rendre incorrect l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="611eb-139">The more restrictive the access level of a variable, the smaller the chances that malicious code can make improper use of it.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="611eb-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="611eb-140">See also</span></span>

- [<span data-ttu-id="611eb-141">Niveaux d’accès dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="611eb-141">Access levels in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
- [<span data-ttu-id="611eb-142">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="611eb-142">Dim Statement</span></span>](../../../../visual-basic/language-reference/statements/dim-statement.md)
- [<span data-ttu-id="611eb-143">Public</span><span class="sxs-lookup"><span data-stu-id="611eb-143">Public</span></span>](../../../../visual-basic/language-reference/modifiers/public.md)
- [<span data-ttu-id="611eb-144">Protected</span><span class="sxs-lookup"><span data-stu-id="611eb-144">Protected</span></span>](../../../../visual-basic/language-reference/modifiers/protected.md)
- [<span data-ttu-id="611eb-145">Friend</span><span class="sxs-lookup"><span data-stu-id="611eb-145">Friend</span></span>](../../../../visual-basic/language-reference/modifiers/friend.md)
- [<span data-ttu-id="611eb-146">Private</span><span class="sxs-lookup"><span data-stu-id="611eb-146">Private</span></span>](../../../../visual-basic/language-reference/modifiers/private.md)
