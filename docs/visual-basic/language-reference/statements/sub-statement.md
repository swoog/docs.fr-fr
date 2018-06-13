---
title: Sub, instruction (Visual Basic)
ms.date: 05/12/2018
f1_keywords:
- vb.Sub
helpviewer_keywords:
- Public keyword [Visual Basic], Sub statements
- procedures [Visual Basic], creating
- declaring procedures [Visual Basic], Sub statement
- arguments [Visual Basic], Sub procedures
- As keyword [Visual Basic], Sub statements
- Optional keyword [Visual Basic], Sub statements
- declarations [Visual Basic], procedures
- Sub keyword [Visual Basic]
- Handles keyword [Visual Basic], Sub statements
- Protected Friend keyword [Visual Basic]
- ParamArray keyword [Visual Basic], Sub statements
- Implements keyword [Visual Basic], Sub statements
- Sub statement [Visual Basic]
- subroutines
- ByRef keyword [Visual Basic], Sub statements
- Sub procedures [Visual Basic], Sub statement
- recursive procedures
- Private keyword [Visual Basic], Sub statements
- Friend keyword [Visual Basic], Sub statements
- Exit statement [Visual Basic], Sub statements
- procedures [Visual Basic], Sub
- End keyword [Visual Basic], Sub statements
- ByVal keyword [Visual Basic], Sub statements
- Visual Basic code, Sub procedures
ms.assetid: e347d700-d06c-405b-b302-e9b1edb57dfc
ms.openlocfilehash: 08be38cdbec82914b567ab5b86eed71181efcf57
ms.sourcegitcommit: 22c3c8f74eaa138dbbbb02eb7d720fce87fc30a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2018
ms.locfileid: "34234174"
---
# <a name="sub-statement-visual-basic"></a><span data-ttu-id="f0dd5-102">Sub, instruction (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f0dd5-102">Sub Statement (Visual Basic)</span></span>
<span data-ttu-id="f0dd5-103">Déclare le nom, paramètres et le code qui définissent une `Sub` procédure.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-103">Declares the name, parameters, and code that define a `Sub` procedure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f0dd5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0dd5-104">Syntax</span></span>  
  
```  
[ <attributelist> ] [ Partial ] [ accessmodifier ] [ proceduremodifiers ] [ Shared ] [ Shadows ] [ Async ]  
Sub name [ (Of typeparamlist) ] [ (parameterlist) ] [ Implements implementslist | Handles eventlist ]  
    [ statements ]  
    [ Exit Sub ]  
    [ statements ]  
End Sub  
```  
  
## <a name="parts"></a><span data-ttu-id="f0dd5-105">Composants</span><span class="sxs-lookup"><span data-stu-id="f0dd5-105">Parts</span></span>  
  
-   `attributelist`  
  
     <span data-ttu-id="f0dd5-106">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-106">Optional.</span></span> <span data-ttu-id="f0dd5-107">Consultez [liste d’attributs](attribute-list.md).</span><span class="sxs-lookup"><span data-stu-id="f0dd5-107">See [Attribute List](attribute-list.md).</span></span>  
  
-   `Partial`  
  
     <span data-ttu-id="f0dd5-108">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-108">Optional.</span></span> <span data-ttu-id="f0dd5-109">Indique la définition d’une méthode partielle.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-109">Indicates definition of a partial method.</span></span> <span data-ttu-id="f0dd5-110">Consultez [méthodes partielles](../../../visual-basic/programming-guide/language-features/procedures/partial-methods.md).</span><span class="sxs-lookup"><span data-stu-id="f0dd5-110">See [Partial Methods](../../../visual-basic/programming-guide/language-features/procedures/partial-methods.md).</span></span>  
  
-   `accessmodifier`  
  
     <span data-ttu-id="f0dd5-111">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-111">Optional.</span></span> <span data-ttu-id="f0dd5-112">Il peut s'agir d'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="f0dd5-112">Can be one of the following:</span></span>  
  
    -   [<span data-ttu-id="f0dd5-113">Public</span><span class="sxs-lookup"><span data-stu-id="f0dd5-113">Public</span></span>](../modifiers/public.md)  
  
    -   [<span data-ttu-id="f0dd5-114">Protected</span><span class="sxs-lookup"><span data-stu-id="f0dd5-114">Protected</span></span>](../modifiers/protected.md)  
  
    -   [<span data-ttu-id="f0dd5-115">Friend</span><span class="sxs-lookup"><span data-stu-id="f0dd5-115">Friend</span></span>](../modifiers/friend.md)  
  
    -   [<span data-ttu-id="f0dd5-116">Private</span><span class="sxs-lookup"><span data-stu-id="f0dd5-116">Private</span></span>](../modifiers/private.md)  
  
    - [<span data-ttu-id="f0dd5-117">Protected Friend</span><span class="sxs-lookup"><span data-stu-id="f0dd5-117">Protected Friend</span></span>](../../language-reference/modifiers/protected-friend.md)

    - [<span data-ttu-id="f0dd5-118">Protégé privé</span><span class="sxs-lookup"><span data-stu-id="f0dd5-118">Private Protected</span></span>](../../language-reference/modifiers/private-protected.md)
  
     <span data-ttu-id="f0dd5-119">Consultez [niveaux en Visual Basic d’accès](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span><span class="sxs-lookup"><span data-stu-id="f0dd5-119">See [Access levels in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span></span>  
  
-   `proceduremodifiers`  
  
     <span data-ttu-id="f0dd5-120">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-120">Optional.</span></span> <span data-ttu-id="f0dd5-121">Il peut s'agir d'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="f0dd5-121">Can be one of the following:</span></span>  
  
    -   [<span data-ttu-id="f0dd5-122">Overloads</span><span class="sxs-lookup"><span data-stu-id="f0dd5-122">Overloads</span></span>](../modifiers/overloads.md)  
  
    -   [<span data-ttu-id="f0dd5-123">Overrides</span><span class="sxs-lookup"><span data-stu-id="f0dd5-123">Overrides</span></span>](../modifiers/overrides.md)  
  
    -   [<span data-ttu-id="f0dd5-124">Overridable</span><span class="sxs-lookup"><span data-stu-id="f0dd5-124">Overridable</span></span>](../modifiers/overridable.md)  
  
    -   [<span data-ttu-id="f0dd5-125">NotOverridable</span><span class="sxs-lookup"><span data-stu-id="f0dd5-125">NotOverridable</span></span>](../modifiers/notoverridable.md)  
  
    -   [<span data-ttu-id="f0dd5-126">MustOverride</span><span class="sxs-lookup"><span data-stu-id="f0dd5-126">MustOverride</span></span>](../modifiers/mustoverride.md)  
  
    -   `MustOverride Overrides`  
  
    -   `NotOverridable Overrides`  
  
-   `Shared`  
  
     <span data-ttu-id="f0dd5-127">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-127">Optional.</span></span> <span data-ttu-id="f0dd5-128">Consultez [partagé](../modifiers/shared.md).</span><span class="sxs-lookup"><span data-stu-id="f0dd5-128">See [Shared](../modifiers/shared.md).</span></span>  
  
-   `Shadows`  
  
     <span data-ttu-id="f0dd5-129">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-129">Optional.</span></span> <span data-ttu-id="f0dd5-130">Consultez [ombres](../modifiers/shadows.md).</span><span class="sxs-lookup"><span data-stu-id="f0dd5-130">See [Shadows](../modifiers/shadows.md).</span></span>  
  
-   `Async`  
  
     <span data-ttu-id="f0dd5-131">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-131">Optional.</span></span> <span data-ttu-id="f0dd5-132">Consultez [Async](../modifiers/async.md).</span><span class="sxs-lookup"><span data-stu-id="f0dd5-132">See [Async](../modifiers/async.md).</span></span>  
  
-   `name`  
  
     <span data-ttu-id="f0dd5-133">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-133">Required.</span></span> <span data-ttu-id="f0dd5-134">Nom de la procédure.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-134">Name of the procedure.</span></span> <span data-ttu-id="f0dd5-135">Consultez [noms d’éléments déclarés](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).</span><span class="sxs-lookup"><span data-stu-id="f0dd5-135">See [Declared Element Names](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).</span></span> <span data-ttu-id="f0dd5-136">Pour créer une procédure de constructeur pour une classe, définissez le nom d’un `Sub` procédure pour le `New` (mot clé).</span><span class="sxs-lookup"><span data-stu-id="f0dd5-136">To create a constructor procedure for a class, set the name of a `Sub` procedure to the `New` keyword.</span></span> <span data-ttu-id="f0dd5-137">Pour plus d’informations, consultez [durée de vie : comment les objets sont création et destruction](../../../visual-basic/programming-guide/language-features/objects-and-classes/object-lifetime-how-objects-are-created-and-destroyed.md).</span><span class="sxs-lookup"><span data-stu-id="f0dd5-137">For more information, see [Object Lifetime: How Objects Are Created and Destroyed](../../../visual-basic/programming-guide/language-features/objects-and-classes/object-lifetime-how-objects-are-created-and-destroyed.md).</span></span>  
  
-   `typeparamlist`  
  
     <span data-ttu-id="f0dd5-138">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-138">Optional.</span></span> <span data-ttu-id="f0dd5-139">Liste de paramètres de type pour une procédure générique.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-139">List of type parameters for a generic procedure.</span></span> <span data-ttu-id="f0dd5-140">Consultez [tapez liste](type-list.md).</span><span class="sxs-lookup"><span data-stu-id="f0dd5-140">See [Type List](type-list.md).</span></span>  
  
-   `parameterlist`  
  
     <span data-ttu-id="f0dd5-141">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-141">Optional.</span></span> <span data-ttu-id="f0dd5-142">Liste des noms de variables locales représentant les paramètres de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-142">List of local variable names representing the parameters of this procedure.</span></span> <span data-ttu-id="f0dd5-143">Consultez [liste de paramètres](parameter-list.md).</span><span class="sxs-lookup"><span data-stu-id="f0dd5-143">See [Parameter List](parameter-list.md).</span></span>  
  
-   `Implements`  
  
     <span data-ttu-id="f0dd5-144">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-144">Optional.</span></span> <span data-ttu-id="f0dd5-145">Indique que cette procédure implémente une ou plusieurs `Sub` procédures, chacune étant définie dans une interface implémentée par la classe ou la structure conteneur de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-145">Indicates that this procedure implements one or more `Sub` procedures, each one defined in an interface implemented by this procedure's containing class or structure.</span></span> <span data-ttu-id="f0dd5-146">Consultez [implémente l’instruction](implements-statement.md).</span><span class="sxs-lookup"><span data-stu-id="f0dd5-146">See [Implements Statement](implements-statement.md).</span></span>  
  
-   `implementslist`  
  
     <span data-ttu-id="f0dd5-147">Obligatoire si `Implements` est utilisé.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-147">Required if `Implements` is supplied.</span></span> <span data-ttu-id="f0dd5-148">Liste des procédures `Sub` en cours d'implémentation.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-148">List of `Sub` procedures being implemented.</span></span>  
  
     `implementedprocedure [ , implementedprocedure ... ]`  
  
     <span data-ttu-id="f0dd5-149">Chaque `implementedprocedure` emploie la syntaxe et les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="f0dd5-149">Each `implementedprocedure` has the following syntax and parts:</span></span>  
  
     `interface.definedname`  
  
    |<span data-ttu-id="f0dd5-150">Élément</span><span class="sxs-lookup"><span data-stu-id="f0dd5-150">Part</span></span>|<span data-ttu-id="f0dd5-151">Description</span><span class="sxs-lookup"><span data-stu-id="f0dd5-151">Description</span></span>|  
    |---|---|  
    |`interface`|<span data-ttu-id="f0dd5-152">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-152">Required.</span></span> <span data-ttu-id="f0dd5-153">Nom d’une interface implémentée par cette procédure conteneur de classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-153">Name of an interface implemented by this procedure's containing class or structure.</span></span>|  
    |`definedname`|<span data-ttu-id="f0dd5-154">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-154">Required.</span></span> <span data-ttu-id="f0dd5-155">Nom par lequel la procédure est définie dans `interface`.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-155">Name by which the procedure is defined in `interface`.</span></span>|  
  
-   `Handles`  
  
     <span data-ttu-id="f0dd5-156">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-156">Optional.</span></span> <span data-ttu-id="f0dd5-157">Indique que cette procédure peut gérer un ou plusieurs événements spécifiques.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-157">Indicates that this procedure can handle one or more specific events.</span></span> <span data-ttu-id="f0dd5-158">Consultez [gère](handles-clause.md).</span><span class="sxs-lookup"><span data-stu-id="f0dd5-158">See [Handles](handles-clause.md).</span></span>  
  
-   `eventlist`  
  
     <span data-ttu-id="f0dd5-159">Obligatoire si `Handles` est utilisé.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-159">Required if `Handles` is supplied.</span></span> <span data-ttu-id="f0dd5-160">Liste des événements gérés par cette procédure.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-160">List of events this procedure handles.</span></span>  
  
     `eventspecifier [ , eventspecifier ... ]`  
  
     <span data-ttu-id="f0dd5-161">Chaque `eventspecifier` emploie la syntaxe et les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="f0dd5-161">Each `eventspecifier` has the following syntax and parts:</span></span>  
  
     `eventvariable.event`  
  
    |<span data-ttu-id="f0dd5-162">Élément</span><span class="sxs-lookup"><span data-stu-id="f0dd5-162">Part</span></span>|<span data-ttu-id="f0dd5-163">Description</span><span class="sxs-lookup"><span data-stu-id="f0dd5-163">Description</span></span>|  
    |---|---|  
    |`eventvariable`|<span data-ttu-id="f0dd5-164">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-164">Required.</span></span> <span data-ttu-id="f0dd5-165">Variable objet déclarée avec le type de données de la classe ou structure qui déclenche l’événement.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-165">Object variable declared with the data type of the class or structure that raises the event.</span></span>|  
    |`event`|<span data-ttu-id="f0dd5-166">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-166">Required.</span></span> <span data-ttu-id="f0dd5-167">Nom de l’événement que gère de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-167">Name of the event this procedure handles.</span></span>|  
  
-   `statements`  
  
     <span data-ttu-id="f0dd5-168">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-168">Optional.</span></span> <span data-ttu-id="f0dd5-169">Bloc d’instructions à exécuter dans cette procédure.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-169">Block of statements to run within this procedure.</span></span>  
  
-   `End Sub`  
  
     <span data-ttu-id="f0dd5-170">Termine la définition de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-170">Terminates the definition of this procedure.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f0dd5-171">Notes</span><span class="sxs-lookup"><span data-stu-id="f0dd5-171">Remarks</span></span>  
 <span data-ttu-id="f0dd5-172">Tout le code exécutable doit être à l’intérieur d’une procédure.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-172">All executable code must be inside a procedure.</span></span> <span data-ttu-id="f0dd5-173">Utilisez un `Sub` procédure lorsque vous ne souhaitez pas retourner une valeur au code appelant.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-173">Use a `Sub` procedure when you don't want to return a value to the calling code.</span></span> <span data-ttu-id="f0dd5-174">Utilisez un `Function` procédure lorsque vous souhaitez retourner une valeur.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-174">Use a `Function` procedure when you want to return a value.</span></span>  
  
## <a name="defining-a-sub-procedure"></a><span data-ttu-id="f0dd5-175">Définition d’une procédure Sub</span><span class="sxs-lookup"><span data-stu-id="f0dd5-175">Defining a Sub Procedure</span></span>  
 <span data-ttu-id="f0dd5-176">Vous pouvez définir un `Sub` procédure uniquement au niveau du module.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-176">You can define a `Sub` procedure only at the module level.</span></span> <span data-ttu-id="f0dd5-177">Le contexte de déclaration pour une procédure sub doit, par conséquent, être une classe, une structure, un module ou une interface et ne peut pas être un fichier source, un espace de noms, une procédure ou un bloc.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-177">The declaration context for a sub procedure must, therefore, be a class, a structure, a module, or an interface and can't be a source file, a namespace, a procedure, or a block.</span></span> <span data-ttu-id="f0dd5-178">Pour plus d’informations, consultez [Contextes de déclaration et niveaux d’accès par défaut](declaration-contexts-and-default-access-levels.md).</span><span class="sxs-lookup"><span data-stu-id="f0dd5-178">For more information, see [Declaration Contexts and Default Access Levels](declaration-contexts-and-default-access-levels.md).</span></span>  
  
 <span data-ttu-id="f0dd5-179">`Sub` les procédures par défaut d’un accès public.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-179">`Sub` procedures default to public access.</span></span> <span data-ttu-id="f0dd5-180">Vous pouvez ajuster leurs niveaux d’accès à l’aide des modificateurs d’accès.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-180">You can adjust their access levels by using the access modifiers.</span></span>  
  
 <span data-ttu-id="f0dd5-181">Si la procédure utilise le `Implements` (mot clé), la classe ou la structure conteneur doit avoir un `Implements` instruction qui suit immédiatement sa `Class` ou `Structure` instruction.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-181">If the procedure uses the `Implements` keyword, the containing class or structure must have an `Implements` statement that immediately follows its `Class` or `Structure` statement.</span></span> <span data-ttu-id="f0dd5-182">Le `Implements` instruction doit inclure chaque interface spécifiée dans `implementslist`.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-182">The `Implements` statement must include each interface that's specified in `implementslist`.</span></span> <span data-ttu-id="f0dd5-183">Toutefois, le nom par lequel une interface définit les `Sub` (dans `definedname`) ne doit pas nécessairement correspondre au nom de cette procédure (dans `name`).</span><span class="sxs-lookup"><span data-stu-id="f0dd5-183">However, the name by which an interface defines the `Sub` (in `definedname`) doesn't have to match the name of this procedure (in `name`).</span></span>  
  
## <a name="returning-from-a-sub-procedure"></a><span data-ttu-id="f0dd5-184">Retour à partir d’une procédure Sub</span><span class="sxs-lookup"><span data-stu-id="f0dd5-184">Returning from a Sub Procedure</span></span>  
 <span data-ttu-id="f0dd5-185">Lorsqu’un `Sub` procédure retourne au code appelant, l’exécution se poursuit avec l’instruction après l’instruction qui l’a appelée.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-185">When a `Sub` procedure returns to the calling code, execution continues with the statement after the statement that called it.</span></span>  
  
 <span data-ttu-id="f0dd5-186">L’exemple suivant montre un retour d’un `Sub` procédure.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-186">The following example shows a return from a `Sub` procedure.</span></span>  
  
```vb  
Sub mySub(ByVal q As String)  
    Return  
End Sub   
```  
  
 <span data-ttu-id="f0dd5-187">Le `Exit Sub` et `Return` instructions provoquent la sortie immédiate d’un `Sub` procédure.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-187">The `Exit Sub` and `Return` statements cause an immediate exit from a `Sub` procedure.</span></span> <span data-ttu-id="f0dd5-188">Un nombre quelconque de `Exit Sub` et `Return` instructions peuvent apparaître n’importe où dans la procédure, et vous pouvez mélanger `Exit Sub` et `Return` instructions.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-188">Any number of `Exit Sub` and `Return` statements can appear anywhere in the procedure, and you can mix `Exit Sub` and `Return` statements.</span></span>  
  
## <a name="calling-a-sub-procedure"></a><span data-ttu-id="f0dd5-189">Appel d’une procédure Sub</span><span class="sxs-lookup"><span data-stu-id="f0dd5-189">Calling a Sub Procedure</span></span>  
 <span data-ttu-id="f0dd5-190">Vous appelez un `Sub` procédure en utilisant le nom de la procédure dans une instruction et en suivant ce nom à sa liste d’arguments entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-190">You call a `Sub` procedure by using the procedure name in a statement and then following that name with its argument list in parentheses.</span></span> <span data-ttu-id="f0dd5-191">Vous pouvez omettre les parenthèses uniquement si vous ne fournissez pas d’arguments.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-191">You can omit the parentheses only if you don't supply any arguments.</span></span> <span data-ttu-id="f0dd5-192">Toutefois, votre code est plus lisible si vous incluez toujours les parenthèses.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-192">However, your code is more readable if you always include the parentheses.</span></span>  
  
 <span data-ttu-id="f0dd5-193">A `Sub` procédure et un `Function` procédure peut avoir des paramètres et exécuter une série d’instructions.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-193">A `Sub` procedure and a `Function` procedure  can have parameters and perform a series of statements.</span></span> <span data-ttu-id="f0dd5-194">Toutefois, un `Function` procédure retourne une valeur et qu’une `Sub` ne de procédure.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-194">However, a `Function` procedure returns a value, and a `Sub` procedure doesn't.</span></span> <span data-ttu-id="f0dd5-195">Par conséquent, vous ne pouvez pas utiliser un `Sub` procédure dans une expression.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-195">Therefore, you can't use a `Sub` procedure in an expression.</span></span>  
  
 <span data-ttu-id="f0dd5-196">Vous pouvez utiliser la `Call` mot clé lorsque vous appelez un `Sub` procédure, mais ce mot clé n’est pas recommandé pour la plupart des utilisations.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-196">You can use the `Call` keyword when you call a `Sub` procedure, but that keyword isn't recommended for most uses.</span></span> <span data-ttu-id="f0dd5-197">Pour plus d’informations, consultez [instruction Call](call-statement.md).</span><span class="sxs-lookup"><span data-stu-id="f0dd5-197">For more information, see [Call Statement](call-statement.md).</span></span>  
  
 <span data-ttu-id="f0dd5-198">Visual Basic réorganise quelquefois les expressions arithmétiques pour améliorer les performances internes.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-198">Visual Basic sometimes rearranges arithmetic expressions to increase internal efficiency.</span></span> <span data-ttu-id="f0dd5-199">Pour cette raison, si votre liste d’arguments inclut des expressions qui appellent d’autres procédures, vous ne devez pas supposer que que ces expressions seront appelées dans un ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-199">For that reason, if your argument list includes expressions that call other procedures, you shouldn't assume that those expressions will be called in a particular order.</span></span>  
  
## <a name="async-sub-procedures"></a><span data-ttu-id="f0dd5-200">Procédures Sub Async</span><span class="sxs-lookup"><span data-stu-id="f0dd5-200">Async Sub Procedures</span></span>  
 <span data-ttu-id="f0dd5-201">À l’aide de la fonctionnalité Async, vous pouvez appeler des fonctions asynchrones sans utiliser de rappels explicites ni fractionner manuellement votre code entre plusieurs fonctions ou expressions lambda.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-201">By using the Async feature, you can invoke asynchronous functions without using explicit callbacks or manually splitting your code across multiple functions or lambda expressions.</span></span>  
  
 <span data-ttu-id="f0dd5-202">Si vous marquez une procédure avec le [Async](../modifiers/async.md) modificateur, vous pouvez utiliser la [Await](../../../visual-basic/language-reference/operators/await-operator.md) opérateur dans la procédure.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-202">If you mark a procedure with the [Async](../modifiers/async.md) modifier, you can use the [Await](../../../visual-basic/language-reference/operators/await-operator.md) operator in the procedure.</span></span> <span data-ttu-id="f0dd5-203">Quand le contrôle atteint une `Await` expression dans le `Async` procédure, contrôle retourne à l’appelant, et la progression de la procédure est interrompue jusqu'à ce que la tâche attendue se termine.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-203">When control reaches an `Await` expression in the `Async` procedure, control returns to the caller, and progress in the procedure is suspended until the awaited task completes.</span></span> <span data-ttu-id="f0dd5-204">Lorsque la tâche est terminée, l’exécution peut reprendre dans la procédure.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-204">When the task is complete, execution can resume in the procedure.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f0dd5-205">Un `Async` procédure retourne à l’appelant quand soit le premier objet await qui n’est pas encore terminé est rencontrée ou à la fin de la `Async` procédure est atteint, selon ce qui se produit en premier.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-205">An `Async` procedure returns to the caller when either the first awaited object that’s not yet complete is encountered or the end of the `Async` procedure is reached, whichever occurs first.</span></span>  
  
 <span data-ttu-id="f0dd5-206">Vous pouvez également marquer un [Function, instruction](function-statement.md) avec la `Async` modificateur.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-206">You can also mark a [Function Statement](function-statement.md) with the `Async` modifier.</span></span> <span data-ttu-id="f0dd5-207">Un `Async` fonction peut avoir un type de retour de <xref:System.Threading.Tasks.Task%601> ou <xref:System.Threading.Tasks.Task>.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-207">An `Async` function can have a return type of <xref:System.Threading.Tasks.Task%601> or <xref:System.Threading.Tasks.Task>.</span></span> <span data-ttu-id="f0dd5-208">Un exemple plus loin dans cette rubrique montre un `Async` fonction qui a un type de retour de <xref:System.Threading.Tasks.Task%601>.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-208">An example later in this topic shows an `Async` function that has a return type of <xref:System.Threading.Tasks.Task%601>.</span></span>  
  
 <span data-ttu-id="f0dd5-209">`Async` `Sub` les procédures sont principalement utilisées pour les gestionnaires d’événements, où une valeur ne peut pas être retournée.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-209">`Async` `Sub` procedures are primarily used for event handlers, where a value can't be returned.</span></span> <span data-ttu-id="f0dd5-210">Un `Async``Sub` procédure ne peut pas être attendue et que l’appelant d’une `Async``Sub` procédure ne peut pas intercepter des exceptions qui le `Sub` lève une exception de la procédure.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-210">An `Async``Sub` procedure can't be awaited, and the caller of an `Async``Sub` procedure can't catch exceptions that the `Sub` procedure throws.</span></span>  
  
 <span data-ttu-id="f0dd5-211">Un `Async` procédure ne peut pas déclarer de [ByRef](../modifiers/byref.md) paramètres.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-211">An `Async` procedure can't declare any [ByRef](../modifiers/byref.md) parameters.</span></span>  
  
 <span data-ttu-id="f0dd5-212">Pour plus d’informations sur `Async` les procédures, consultez [programmation asynchrone avec Async et Await](../../../visual-basic/programming-guide/concepts/async/index.md), [flux de contrôle dans les programmes Async](../../../visual-basic/programming-guide/concepts/async/control-flow-in-async-programs.md), et [Types de retour Async](../../../visual-basic/programming-guide/concepts/async/async-return-types.md).</span><span class="sxs-lookup"><span data-stu-id="f0dd5-212">For more information about `Async` procedures, see [Asynchronous Programming with Async and Await](../../../visual-basic/programming-guide/concepts/async/index.md), [Control Flow in Async Programs](../../../visual-basic/programming-guide/concepts/async/control-flow-in-async-programs.md), and [Async Return Types](../../../visual-basic/programming-guide/concepts/async/async-return-types.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="f0dd5-213">Exemple</span><span class="sxs-lookup"><span data-stu-id="f0dd5-213">Example</span></span>  
 <span data-ttu-id="f0dd5-214">L’exemple suivant utilise le `Sub` instruction afin de définir le nom, des paramètres et que le code qui forment le corps d’un `Sub` procédure.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-214">The following example uses the `Sub` statement to define the name, parameters, and code that form the body of a `Sub` procedure.</span></span>  
  
 [!code-vb[VbVbalrStatements#58](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/sub-statement_1.vb)]  
  
## <a name="example"></a><span data-ttu-id="f0dd5-215">Exemple</span><span class="sxs-lookup"><span data-stu-id="f0dd5-215">Example</span></span>  
 <span data-ttu-id="f0dd5-216">Dans l’exemple suivant, `DelayAsync` est un `Async``Function` qui a un type de retour de <xref:System.Threading.Tasks.Task%601>.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-216">In the following example, `DelayAsync` is an `Async``Function` that has a return type of <xref:System.Threading.Tasks.Task%601>.</span></span> <span data-ttu-id="f0dd5-217">`DelayAsync` a une instruction `Return` qui retourne un entier.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-217">`DelayAsync` has a `Return` statement that returns an integer.</span></span> <span data-ttu-id="f0dd5-218">Par conséquent, la déclaration de fonction de `DelayAsync` doit avoir un type de retour de `Task(Of Integer)`.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-218">Therefore, the function declaration of `DelayAsync` must have a return type of `Task(Of Integer)`.</span></span> <span data-ttu-id="f0dd5-219">Étant donné que le type de retour est `Task(Of Integer)`, l’évaluation de la `Await` expression dans `DoSomethingAsync` produit un entier, comme le montre l’instruction suivante : `Dim result As Integer = Await delayTask`.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-219">Because the return type is `Task(Of Integer)`, the evaluation of the `Await` expression in `DoSomethingAsync` produces an integer, as the following statement shows: `Dim result As Integer = Await delayTask`.</span></span>  
  
 <span data-ttu-id="f0dd5-220">Le `startButton_Click` procédure est un exemple d’un `Async Sub` procédure.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-220">The `startButton_Click` procedure is an example of an `Async Sub` procedure.</span></span> <span data-ttu-id="f0dd5-221">Étant donné que `DoSomethingAsync` est un `Async` la tâche pour l’appel à une fonction, `DoSomethingAsync` doit être attendue, comme le montre l’instruction suivante : `Await DoSomethingAsync()`.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-221">Because `DoSomethingAsync` is an `Async` function, the task for the call to `DoSomethingAsync` must be awaited, as the following statement shows: `Await DoSomethingAsync()`.</span></span> <span data-ttu-id="f0dd5-222">Le `startButton_Click``Sub` procédure doit être définie avec la `Async` modificateur, car il possède un `Await` expression.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-222">The `startButton_Click``Sub` procedure must be defined with the `Async` modifier because it has an `Await` expression.</span></span>  
  
 [!code-vb[csAsyncMethod#1](../../../csharp/programming-guide/classes-and-structs/codesnippet/VisualBasic/sub-statement_2.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="f0dd5-223">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0dd5-223">See Also</span></span>  
 [<span data-ttu-id="f0dd5-224">Implements (instruction)</span><span class="sxs-lookup"><span data-stu-id="f0dd5-224">Implements Statement</span></span>](implements-statement.md)  
 [<span data-ttu-id="f0dd5-225">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="f0dd5-225">Function Statement</span></span>](function-statement.md)  
 [<span data-ttu-id="f0dd5-226">Liste de paramètres</span><span class="sxs-lookup"><span data-stu-id="f0dd5-226">Parameter List</span></span>](parameter-list.md)  
 [<span data-ttu-id="f0dd5-227">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="f0dd5-227">Dim Statement</span></span>](dim-statement.md)  
 [<span data-ttu-id="f0dd5-228">Call (instruction)</span><span class="sxs-lookup"><span data-stu-id="f0dd5-228">Call Statement</span></span>](call-statement.md)  
 [<span data-ttu-id="f0dd5-229">Of</span><span class="sxs-lookup"><span data-stu-id="f0dd5-229">Of</span></span>](of-clause.md)  
 [<span data-ttu-id="f0dd5-230">tableaux de paramètres</span><span class="sxs-lookup"><span data-stu-id="f0dd5-230">Parameter Arrays</span></span>](../../../visual-basic/programming-guide/language-features/procedures/parameter-arrays.md)  
 [<span data-ttu-id="f0dd5-231">Guide pratique : utiliser une classe générique</span><span class="sxs-lookup"><span data-stu-id="f0dd5-231">How to: Use a Generic Class</span></span>](../../../visual-basic/programming-guide/language-features/data-types/how-to-use-a-generic-class.md)  
 [<span data-ttu-id="f0dd5-232">Procédures de dépannage</span><span class="sxs-lookup"><span data-stu-id="f0dd5-232">Troubleshooting Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/troubleshooting-procedures.md)  
 [<span data-ttu-id="f0dd5-233">Méthodes partielles</span><span class="sxs-lookup"><span data-stu-id="f0dd5-233">Partial Methods</span></span>](../../../visual-basic/programming-guide/language-features/procedures/partial-methods.md)
