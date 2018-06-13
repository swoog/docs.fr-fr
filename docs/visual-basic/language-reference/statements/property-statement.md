---
title: Property Statement
ms.date: 05/12/2018
f1_keywords:
- vb.PropertySet
- vb.Property
- vb.PropertyGet
helpviewer_keywords:
- Property statement [Visual Basic]
- default modifier
- property procedures [Visual Basic], Property statements
- Property keyword [Visual Basic]
ms.assetid: 3155edaf-8ebd-45c6-9cef-11d5d2dc8d38
ms.openlocfilehash: 3f3ced3f0c441518594820f75243c71fb0c3babd
ms.sourcegitcommit: 22c3c8f74eaa138dbbbb02eb7d720fce87fc30a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2018
ms.locfileid: "34235988"
---
# <a name="property-statement"></a><span data-ttu-id="47ca5-102">Property Statement</span><span class="sxs-lookup"><span data-stu-id="47ca5-102">Property Statement</span></span>
<span data-ttu-id="47ca5-103">Déclare le nom d’une propriété et les procédures de propriété utilisées pour stocker et récupérer la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="47ca5-103">Declares the name of a property, and the property procedures used to store and retrieve the value of the property.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="47ca5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47ca5-104">Syntax</span></span>  
  
```vb  
[ <attributelist> ] [ Default ] [ accessmodifier ]   
[ propertymodifiers ] [ Shared ] [ Shadows ] [ ReadOnly | WriteOnly ] [ Iterator ]  
Property name ( [ parameterlist ] ) [ As returntype ] [ Implements implementslist ]  
    [ <attributelist> ] [ accessmodifier ] Get  
        [ statements ]  
    End Get  
    [ <attributelist> ] [ accessmodifier ] Set ( ByVal value As returntype [, parameterlist ] )  
        [ statements ]  
    End Set  
End Property  
- or -  
[ <attributelist> ] [ Default ] [ accessmodifier ]   
[ propertymodifiers ] [ Shared ] [ Shadows ] [ ReadOnly | WriteOnly ]   
Property name ( [ parameterlist ] ) [ As returntype ] [ Implements implementslist ]  
```  
  
## <a name="parts"></a><span data-ttu-id="47ca5-105">Composants</span><span class="sxs-lookup"><span data-stu-id="47ca5-105">Parts</span></span>  
  
-   `attributelist`  
  
     <span data-ttu-id="47ca5-106">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="47ca5-106">Optional.</span></span> <span data-ttu-id="47ca5-107">Liste des attributs qui s’appliquent à cette propriété ou `Get` ou `Set` procédure.</span><span class="sxs-lookup"><span data-stu-id="47ca5-107">List of attributes that apply to this property or `Get` or `Set` procedure.</span></span> <span data-ttu-id="47ca5-108">Consultez [liste d’attributs](../../../visual-basic/language-reference/statements/attribute-list.md).</span><span class="sxs-lookup"><span data-stu-id="47ca5-108">See [Attribute List](../../../visual-basic/language-reference/statements/attribute-list.md).</span></span>  
  
-   `Default`  
  
     <span data-ttu-id="47ca5-109">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="47ca5-109">Optional.</span></span> <span data-ttu-id="47ca5-110">Spécifie que cette propriété est la propriété par défaut pour la classe ou structure sur lequel elle est définie.</span><span class="sxs-lookup"><span data-stu-id="47ca5-110">Specifies that this property is the default property for the class or structure on which it is defined.</span></span> <span data-ttu-id="47ca5-111">Propriétés par défaut doivent accepter des paramètres et peuvent être définies et récupérées sans spécifier le nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="47ca5-111">Default properties must accept parameters and can be set and retrieved without specifying the property name.</span></span> <span data-ttu-id="47ca5-112">Si vous déclarez la propriété comme `Default`, vous ne pouvez pas utiliser `Private` sur la propriété ou sur un de ses procédures de propriété.</span><span class="sxs-lookup"><span data-stu-id="47ca5-112">If you declare the property as `Default`, you cannot use `Private` on the property or on either of its property procedures.</span></span>  
  
-   `accessmodifier`  
  
     <span data-ttu-id="47ca5-113">Facultatif sur le `Property` instruction et sur l’une de le `Get` et `Set` instructions.</span><span class="sxs-lookup"><span data-stu-id="47ca5-113">Optional on the `Property` statement and on at most one of the `Get` and `Set` statements.</span></span> <span data-ttu-id="47ca5-114">Il peut s'agir d'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="47ca5-114">Can be one of the following:</span></span>  
  
    -   [<span data-ttu-id="47ca5-115">Public</span><span class="sxs-lookup"><span data-stu-id="47ca5-115">Public</span></span>](../../../visual-basic/language-reference/modifiers/public.md)  
  
    -   [<span data-ttu-id="47ca5-116">Protected</span><span class="sxs-lookup"><span data-stu-id="47ca5-116">Protected</span></span>](../../../visual-basic/language-reference/modifiers/protected.md)  
  
    -   [<span data-ttu-id="47ca5-117">Friend</span><span class="sxs-lookup"><span data-stu-id="47ca5-117">Friend</span></span>](../../../visual-basic/language-reference/modifiers/friend.md)  
  
    -   [<span data-ttu-id="47ca5-118">Private</span><span class="sxs-lookup"><span data-stu-id="47ca5-118">Private</span></span>](../../../visual-basic/language-reference/modifiers/private.md)  
  
    - [<span data-ttu-id="47ca5-119">Protected Friend</span><span class="sxs-lookup"><span data-stu-id="47ca5-119">Protected Friend</span></span>](../../language-reference/modifiers/protected-friend.md) 

    - [<span data-ttu-id="47ca5-120">Protégé privé</span><span class="sxs-lookup"><span data-stu-id="47ca5-120">Private Protected</span></span>](../../language-reference/modifiers/private-protected.md)
  
     <span data-ttu-id="47ca5-121">Consultez [niveaux en Visual Basic d’accès](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span><span class="sxs-lookup"><span data-stu-id="47ca5-121">See [Access levels in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span></span>  
  
-   `propertymodifiers`  
  
     <span data-ttu-id="47ca5-122">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="47ca5-122">Optional.</span></span> <span data-ttu-id="47ca5-123">Il peut s'agir d'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="47ca5-123">Can be one of the following:</span></span>  
  
    -   [<span data-ttu-id="47ca5-124">Overloads</span><span class="sxs-lookup"><span data-stu-id="47ca5-124">Overloads</span></span>](../../../visual-basic/language-reference/modifiers/overloads.md)  
  
    -   [<span data-ttu-id="47ca5-125">Overrides</span><span class="sxs-lookup"><span data-stu-id="47ca5-125">Overrides</span></span>](../../../visual-basic/language-reference/modifiers/overrides.md)  
  
    -   [<span data-ttu-id="47ca5-126">Overridable</span><span class="sxs-lookup"><span data-stu-id="47ca5-126">Overridable</span></span>](../../../visual-basic/language-reference/modifiers/overridable.md)  
  
    -   [<span data-ttu-id="47ca5-127">NotOverridable</span><span class="sxs-lookup"><span data-stu-id="47ca5-127">NotOverridable</span></span>](../../../visual-basic/language-reference/modifiers/notoverridable.md)  
  
    -   [<span data-ttu-id="47ca5-128">MustOverride</span><span class="sxs-lookup"><span data-stu-id="47ca5-128">MustOverride</span></span>](../../../visual-basic/language-reference/modifiers/mustoverride.md)  
  
    -   `MustOverride Overrides`  
  
    -   `NotOverridable Overrides`  
  
-   `Shared`  
  
     <span data-ttu-id="47ca5-129">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="47ca5-129">Optional.</span></span> <span data-ttu-id="47ca5-130">Consultez [partagé](../../../visual-basic/language-reference/modifiers/shared.md).</span><span class="sxs-lookup"><span data-stu-id="47ca5-130">See [Shared](../../../visual-basic/language-reference/modifiers/shared.md).</span></span>  
  
-   `Shadows`  
  
     <span data-ttu-id="47ca5-131">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="47ca5-131">Optional.</span></span> <span data-ttu-id="47ca5-132">Consultez [ombres](../../../visual-basic/language-reference/modifiers/shadows.md).</span><span class="sxs-lookup"><span data-stu-id="47ca5-132">See [Shadows](../../../visual-basic/language-reference/modifiers/shadows.md).</span></span>  
  
-   `ReadOnly`  
  
     <span data-ttu-id="47ca5-133">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="47ca5-133">Optional.</span></span> <span data-ttu-id="47ca5-134">Consultez [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).</span><span class="sxs-lookup"><span data-stu-id="47ca5-134">See [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).</span></span>  
  
-   `WriteOnly`  
  
     <span data-ttu-id="47ca5-135">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="47ca5-135">Optional.</span></span> <span data-ttu-id="47ca5-136">Consultez [WriteOnly](../../../visual-basic/language-reference/modifiers/writeonly.md).</span><span class="sxs-lookup"><span data-stu-id="47ca5-136">See [WriteOnly](../../../visual-basic/language-reference/modifiers/writeonly.md).</span></span>  
  
-   `Iterator`  
  
     <span data-ttu-id="47ca5-137">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="47ca5-137">Optional.</span></span> <span data-ttu-id="47ca5-138">Consultez [itérateur](../../../visual-basic/language-reference/modifiers/iterator.md).</span><span class="sxs-lookup"><span data-stu-id="47ca5-138">See [Iterator](../../../visual-basic/language-reference/modifiers/iterator.md).</span></span>  
  
-   `name`  
  
     <span data-ttu-id="47ca5-139">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="47ca5-139">Required.</span></span> <span data-ttu-id="47ca5-140">Nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="47ca5-140">Name of the property.</span></span> <span data-ttu-id="47ca5-141">Consultez [noms d’éléments déclarés](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).</span><span class="sxs-lookup"><span data-stu-id="47ca5-141">See [Declared Element Names](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).</span></span>  
  
-   `parameterlist`  
  
     <span data-ttu-id="47ca5-142">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="47ca5-142">Optional.</span></span> <span data-ttu-id="47ca5-143">Liste des noms de variables locales représentant les paramètres de cette propriété et les éventuels paramètres supplémentaires de la `Set` procédure.</span><span class="sxs-lookup"><span data-stu-id="47ca5-143">List of local variable names representing the parameters of this property, and possible additional parameters of the `Set` procedure.</span></span> <span data-ttu-id="47ca5-144">Consultez [liste de paramètres](../../../visual-basic/language-reference/statements/parameter-list.md).</span><span class="sxs-lookup"><span data-stu-id="47ca5-144">See [Parameter List](../../../visual-basic/language-reference/statements/parameter-list.md).</span></span>  
  
-   `returntype`  
  
     <span data-ttu-id="47ca5-145">Obligatoire si `Option``Strict` est `On`.</span><span class="sxs-lookup"><span data-stu-id="47ca5-145">Required if `Option``Strict` is `On`.</span></span> <span data-ttu-id="47ca5-146">Type de données de la valeur retournée par cette propriété.</span><span class="sxs-lookup"><span data-stu-id="47ca5-146">Data type of the value returned by this property.</span></span>  
  
-   `Implements`  
  
     <span data-ttu-id="47ca5-147">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="47ca5-147">Optional.</span></span> <span data-ttu-id="47ca5-148">Indique que cette propriété implémente une ou plusieurs propriétés, chacune étant définie dans une interface implémentée par la classe ou la structure conteneur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="47ca5-148">Indicates that this property implements one or more properties, each one defined in an interface implemented by this property's containing class or structure.</span></span> <span data-ttu-id="47ca5-149">Consultez [implémente l’instruction](../../../visual-basic/language-reference/statements/implements-statement.md).</span><span class="sxs-lookup"><span data-stu-id="47ca5-149">See [Implements Statement](../../../visual-basic/language-reference/statements/implements-statement.md).</span></span>  
  
-   `implementslist`  
  
     <span data-ttu-id="47ca5-150">Obligatoire si `Implements` est utilisé.</span><span class="sxs-lookup"><span data-stu-id="47ca5-150">Required if `Implements` is supplied.</span></span> <span data-ttu-id="47ca5-151">Liste de propriétés en cours d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="47ca5-151">List of properties being implemented.</span></span>  
  
     `implementedproperty [ , implementedproperty ... ]`  
  
     <span data-ttu-id="47ca5-152">Chaque `implementedproperty` emploie la syntaxe et les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="47ca5-152">Each `implementedproperty` has the following syntax and parts:</span></span>  
  
     `interface.definedname`  
  
    |<span data-ttu-id="47ca5-153">Élément</span><span class="sxs-lookup"><span data-stu-id="47ca5-153">Part</span></span>|<span data-ttu-id="47ca5-154">Description</span><span class="sxs-lookup"><span data-stu-id="47ca5-154">Description</span></span>|  
    |---|---|  
    |`interface`|<span data-ttu-id="47ca5-155">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="47ca5-155">Required.</span></span> <span data-ttu-id="47ca5-156">Nom d’une interface implémentée par cette propriété de classe ou la structure conteneur.</span><span class="sxs-lookup"><span data-stu-id="47ca5-156">Name of an interface implemented by this property's containing class or structure.</span></span>|  
    |`definedname`|<span data-ttu-id="47ca5-157">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="47ca5-157">Required.</span></span> <span data-ttu-id="47ca5-158">Nom par lequel la propriété est définie dans `interface`.</span><span class="sxs-lookup"><span data-stu-id="47ca5-158">Name by which the property is defined in `interface`.</span></span>|  
  
-   `Get`  
  
     <span data-ttu-id="47ca5-159">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="47ca5-159">Optional.</span></span> <span data-ttu-id="47ca5-160">Obligatoire si la propriété est marquée `WriteOnly`.</span><span class="sxs-lookup"><span data-stu-id="47ca5-160">Required if the property is marked `WriteOnly`.</span></span> <span data-ttu-id="47ca5-161">Démarre un `Get` procédure de propriété qui est utilisée pour retourner la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="47ca5-161">Starts a `Get` property procedure that is used to return the value of the property.</span></span>  
  
-   `statements`  
  
     <span data-ttu-id="47ca5-162">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="47ca5-162">Optional.</span></span> <span data-ttu-id="47ca5-163">Bloc d’instructions à exécuter dans le `Get` ou `Set` procédure.</span><span class="sxs-lookup"><span data-stu-id="47ca5-163">Block of statements to run within the `Get` or `Set` procedure.</span></span>  
  
-   `End Get`  
  
     <span data-ttu-id="47ca5-164">Met fin à la `Get` procédure de propriété.</span><span class="sxs-lookup"><span data-stu-id="47ca5-164">Terminates the `Get` property procedure.</span></span>  
  
-   `Set`  
  
     <span data-ttu-id="47ca5-165">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="47ca5-165">Optional.</span></span> <span data-ttu-id="47ca5-166">Obligatoire si la propriété est marquée `ReadOnly`.</span><span class="sxs-lookup"><span data-stu-id="47ca5-166">Required if the property is marked `ReadOnly`.</span></span> <span data-ttu-id="47ca5-167">Démarre un `Set` procédure de propriété qui est utilisé pour stocker la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="47ca5-167">Starts a `Set` property procedure that is used to store the value of the property.</span></span>  
  
-   `End Set`  
  
     <span data-ttu-id="47ca5-168">Met fin à la `Set` procédure de propriété.</span><span class="sxs-lookup"><span data-stu-id="47ca5-168">Terminates the `Set` property procedure.</span></span>  
  
-   `End Property`  
  
     <span data-ttu-id="47ca5-169">Termine la définition de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="47ca5-169">Terminates the definition of this property.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="47ca5-170">Notes</span><span class="sxs-lookup"><span data-stu-id="47ca5-170">Remarks</span></span>  
 <span data-ttu-id="47ca5-171">La `Property` instruction introduit la déclaration d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="47ca5-171">The `Property` statement introduces the declaration of a property.</span></span> <span data-ttu-id="47ca5-172">Une propriété peut avoir un `Get` procédure (lecture seule), un `Set` procédure (écriture seule), ou les deux (lecture-écriture).</span><span class="sxs-lookup"><span data-stu-id="47ca5-172">A property can have a `Get` procedure (read only), a `Set` procedure (write only), or both (read-write).</span></span> <span data-ttu-id="47ca5-173">Vous pouvez omettre le `Get` et `Set` procédure lors de l’utilisation d’une propriété implémentée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="47ca5-173">You can omit the `Get` and `Set` procedure when using an auto-implemented property.</span></span> <span data-ttu-id="47ca5-174">Pour plus d’informations, consultez [Propriétés implémentées automatiquement](../../../visual-basic/programming-guide/language-features/procedures/auto-implemented-properties.md).</span><span class="sxs-lookup"><span data-stu-id="47ca5-174">For more information, see [Auto-Implemented Properties](../../../visual-basic/programming-guide/language-features/procedures/auto-implemented-properties.md).</span></span>  
  
 <span data-ttu-id="47ca5-175">Vous pouvez utiliser `Property` uniquement au niveau de la classe.</span><span class="sxs-lookup"><span data-stu-id="47ca5-175">You can use `Property` only at class level.</span></span> <span data-ttu-id="47ca5-176">Cela signifie que la *contexte de déclaration* pour une propriété doit être une classe, une structure, un module ou une interface et ne peut pas être un fichier source, un espace de noms, une procédure ou un bloc.</span><span class="sxs-lookup"><span data-stu-id="47ca5-176">This means the *declaration context* for a property must be a class, structure, module, or interface, and cannot be a source file, namespace, procedure, or block.</span></span> <span data-ttu-id="47ca5-177">Pour plus d’informations, consultez [Contextes de déclaration et niveaux d’accès par défaut](../../../visual-basic/language-reference/statements/declaration-contexts-and-default-access-levels.md).</span><span class="sxs-lookup"><span data-stu-id="47ca5-177">For more information, see [Declaration Contexts and Default Access Levels](../../../visual-basic/language-reference/statements/declaration-contexts-and-default-access-levels.md).</span></span>  
  
 <span data-ttu-id="47ca5-178">Par défaut, les propriétés utilisent un accès public.</span><span class="sxs-lookup"><span data-stu-id="47ca5-178">By default, properties use public access.</span></span> <span data-ttu-id="47ca5-179">Vous pouvez ajuster le niveau d’accès d’une propriété avec un modificateur d’accès sur le `Property` instruction et que vous pouvez éventuellement ajuster une de ses procédures de propriété à un niveau d’accès plus restrictif.</span><span class="sxs-lookup"><span data-stu-id="47ca5-179">You can adjust a property's access level with an access modifier on the `Property` statement, and you can optionally adjust one of its property procedures to a more restrictive access level.</span></span>  
  
 <span data-ttu-id="47ca5-180">Visual Basic passe un paramètre à la `Set` procédure pendant les assignations de propriété.</span><span class="sxs-lookup"><span data-stu-id="47ca5-180">Visual Basic passes a parameter to the `Set` procedure during property assignments.</span></span> <span data-ttu-id="47ca5-181">Si vous ne fournissez pas un paramètre pour `Set`, l’environnement de développement intégré (IDE) utilise un paramètre implicite nommé `value`.</span><span class="sxs-lookup"><span data-stu-id="47ca5-181">If you do not supply a parameter for `Set`, the integrated development environment (IDE) uses an implicit parameter named `value`.</span></span> <span data-ttu-id="47ca5-182">Ce paramètre conserve la valeur à affecter à la propriété.</span><span class="sxs-lookup"><span data-stu-id="47ca5-182">This parameter holds the value to be assigned to the property.</span></span> <span data-ttu-id="47ca5-183">En général, stockez la valeur dans une variable locale privée et de la retourner chaque fois que le `Get` procédure est appelée.</span><span class="sxs-lookup"><span data-stu-id="47ca5-183">You typically store this value in a private local variable and return it whenever the `Get` procedure is called.</span></span>  
  
## <a name="rules"></a><span data-ttu-id="47ca5-184">Règles</span><span class="sxs-lookup"><span data-stu-id="47ca5-184">Rules</span></span>  
  
-   <span data-ttu-id="47ca5-185">**Niveaux d’accès mixtes.**</span><span class="sxs-lookup"><span data-stu-id="47ca5-185">**Mixed Access Levels.**</span></span> <span data-ttu-id="47ca5-186">Si vous définissez une propriété en lecture-écriture, vous pouvez éventuellement spécifier un niveau d’accès différent pour un le `Get` ou `Set` procédure, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="47ca5-186">If you are defining a read-write property, you can optionally specify a different access level for either the `Get` or the `Set` procedure, but not both.</span></span> <span data-ttu-id="47ca5-187">Si vous faites cela, le niveau d’accès de la procédure doit être plus restrictif que le niveau d’accès de la propriété.</span><span class="sxs-lookup"><span data-stu-id="47ca5-187">If you do this, the procedure access level must be more restrictive than the property's access level.</span></span> <span data-ttu-id="47ca5-188">Par exemple, si la propriété est déclarée `Friend`, vous pouvez déclarer le `Set` procédure `Private`, mais pas `Public`.</span><span class="sxs-lookup"><span data-stu-id="47ca5-188">For example, if the property is declared `Friend`, you can declare the `Set` procedure `Private`, but not `Public`.</span></span>  
  
     <span data-ttu-id="47ca5-189">Si vous définissez un `ReadOnly` ou `WriteOnly` propriété, la procédure de propriété unique (`Get` ou `Set`, respectivement) représente la propriété.</span><span class="sxs-lookup"><span data-stu-id="47ca5-189">If you are defining a `ReadOnly` or `WriteOnly` property, the single property procedure (`Get` or `Set`, respectively) represents all of the property.</span></span> <span data-ttu-id="47ca5-190">Vous ne pouvez pas déclarer un niveau d’accès différent pour cette procédure, parce que seront définis à deux niveaux d’accès pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="47ca5-190">You cannot declare a different access level for such a procedure, because that would set two access levels for the property.</span></span>  
  
-   <span data-ttu-id="47ca5-191">**Type de retour.**</span><span class="sxs-lookup"><span data-stu-id="47ca5-191">**Return Type.**</span></span> <span data-ttu-id="47ca5-192">La `Property` instruction peut déclarer le type de données de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="47ca5-192">The `Property` statement can declare the data type of the value it returns.</span></span> <span data-ttu-id="47ca5-193">Vous pouvez spécifier n’importe quel type de données ou le nom d’une énumération, structure, classe ou d’interface.</span><span class="sxs-lookup"><span data-stu-id="47ca5-193">You can specify any data type or the name of an enumeration, structure, class, or interface.</span></span>  
  
     <span data-ttu-id="47ca5-194">Si vous ne spécifiez pas `returntype`, la propriété renvoie `Object`.</span><span class="sxs-lookup"><span data-stu-id="47ca5-194">If you do not specify `returntype`, the property returns `Object`.</span></span>  
  
-   <span data-ttu-id="47ca5-195">**Mise en œuvre.**</span><span class="sxs-lookup"><span data-stu-id="47ca5-195">**Implementation.**</span></span> <span data-ttu-id="47ca5-196">Si cette propriété utilise la `Implements` (mot clé), la classe ou la structure conteneur doit avoir un `Implements` instruction qui suit immédiatement sa `Class` ou `Structure` instruction.</span><span class="sxs-lookup"><span data-stu-id="47ca5-196">If this property uses the `Implements` keyword, the containing class or structure must have an `Implements` statement immediately following its `Class` or `Structure` statement.</span></span> <span data-ttu-id="47ca5-197">Le `Implements` doit inclure chaque interface spécifiée dans `implementslist`.</span><span class="sxs-lookup"><span data-stu-id="47ca5-197">The `Implements` statement must include each interface specified in `implementslist`.</span></span> <span data-ttu-id="47ca5-198">Toutefois, le nom par lequel une interface définit les `Property` (dans `definedname`) pas nécessairement être le même que le nom de la propriété (dans `name`).</span><span class="sxs-lookup"><span data-stu-id="47ca5-198">However, the name by which an interface defines the `Property` (in `definedname`) does not have to be the same as the name of this property (in `name`).</span></span>  
  
## <a name="behavior"></a><span data-ttu-id="47ca5-199">Comportement</span><span class="sxs-lookup"><span data-stu-id="47ca5-199">Behavior</span></span>  
  
-   <span data-ttu-id="47ca5-200">**Retour d’une procédure de propriété.**</span><span class="sxs-lookup"><span data-stu-id="47ca5-200">**Returning from a Property Procedure.**</span></span> <span data-ttu-id="47ca5-201">Lorsque le `Get` ou `Set` procédure retourne au code appelant, l’exécution se poursuit avec l’instruction qui suit l’instruction qui l’a appelée.</span><span class="sxs-lookup"><span data-stu-id="47ca5-201">When the `Get` or `Set` procedure returns to the calling code, execution continues with the statement following the statement that invoked it.</span></span>  
  
     <span data-ttu-id="47ca5-202">Le `Exit Property` et `Return` instructions provoquent la sortie immédiate d’une procédure de propriété.</span><span class="sxs-lookup"><span data-stu-id="47ca5-202">The `Exit Property` and `Return` statements cause an immediate exit from a property procedure.</span></span> <span data-ttu-id="47ca5-203">Un nombre quelconque de `Exit Property` et `Return` instructions peuvent apparaître n’importe où dans la procédure, et vous pouvez mélanger `Exit Property` et `Return` instructions.</span><span class="sxs-lookup"><span data-stu-id="47ca5-203">Any number of `Exit Property` and `Return` statements can appear anywhere in the procedure, and you can mix `Exit Property` and `Return` statements.</span></span>  
  
-   <span data-ttu-id="47ca5-204">**Valeur de retour.**</span><span class="sxs-lookup"><span data-stu-id="47ca5-204">**Return Value.**</span></span> <span data-ttu-id="47ca5-205">Pour retourner une valeur d’un `Get` procédure, vous pouvez affecter la valeur au nom de propriété ou l’inclure dans un `Return` instruction.</span><span class="sxs-lookup"><span data-stu-id="47ca5-205">To return a value from a `Get` procedure, you can either assign the value to the property name or include it in a `Return` statement.</span></span> <span data-ttu-id="47ca5-206">L’exemple suivant affecte la valeur de retour au nom de propriété `quoteForTheDay` , puis utilise la `Exit Property` instruction à retourner.</span><span class="sxs-lookup"><span data-stu-id="47ca5-206">The following example assigns the return value to the property name `quoteForTheDay` and then uses the `Exit Property` statement to return.</span></span>  
  
     [!code-vb[VbVbalrStatements#27](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/property-statement_1.vb)]  
  
     [!code-vb[VbVbalrStatements#28](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/property-statement_2.vb)]  
  
     <span data-ttu-id="47ca5-207">Si vous utilisez `Exit Property` sans lui assigner une valeur à `name`, le `Get` procédure retourne la valeur par défaut pour le type de données de la propriété.</span><span class="sxs-lookup"><span data-stu-id="47ca5-207">If you use `Exit Property` without assigning a value to `name`, the `Get` procedure returns the default value for the property's data type.</span></span>  
  
     <span data-ttu-id="47ca5-208">Le `Return` instruction en même temps affecte le `Get` procédure retourner de valeur et termine la procédure.</span><span class="sxs-lookup"><span data-stu-id="47ca5-208">The `Return` statement at the same time assigns the `Get` procedure return value and exits the procedure.</span></span> <span data-ttu-id="47ca5-209">L’exemple suivant illustre ce point.</span><span class="sxs-lookup"><span data-stu-id="47ca5-209">The following example shows this.</span></span>  
  
     [!code-vb[VbVbalrStatements#27](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/property-statement_1.vb)]  
  
     [!code-vb[VbVbalrStatements#29](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/property-statement_3.vb)]  
  
## <a name="example"></a><span data-ttu-id="47ca5-210">Exemple</span><span class="sxs-lookup"><span data-stu-id="47ca5-210">Example</span></span>  
 <span data-ttu-id="47ca5-211">L’exemple suivant déclare une propriété dans une classe.</span><span class="sxs-lookup"><span data-stu-id="47ca5-211">The following example declares a property in a class.</span></span>  
  
 [!code-vb[VbVbalrStatements#51](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/property-statement_4.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="47ca5-212">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47ca5-212">See Also</span></span>  
 [<span data-ttu-id="47ca5-213">Propriétés implémentées automatiquement</span><span class="sxs-lookup"><span data-stu-id="47ca5-213">Auto-Implemented Properties</span></span>](../../../visual-basic/programming-guide/language-features/procedures/auto-implemented-properties.md)  
 [<span data-ttu-id="47ca5-214">Objets et classes</span><span class="sxs-lookup"><span data-stu-id="47ca5-214">Objects and Classes</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)  
 [<span data-ttu-id="47ca5-215">Get (instruction)</span><span class="sxs-lookup"><span data-stu-id="47ca5-215">Get Statement</span></span>](../../../visual-basic/language-reference/statements/get-statement.md)  
 [<span data-ttu-id="47ca5-216">Set (instruction)</span><span class="sxs-lookup"><span data-stu-id="47ca5-216">Set Statement</span></span>](../../../visual-basic/language-reference/statements/set-statement.md)  
 [<span data-ttu-id="47ca5-217">Liste de paramètres</span><span class="sxs-lookup"><span data-stu-id="47ca5-217">Parameter List</span></span>](../../../visual-basic/language-reference/statements/parameter-list.md)  
 [<span data-ttu-id="47ca5-218">Default</span><span class="sxs-lookup"><span data-stu-id="47ca5-218">Default</span></span>](../../../visual-basic/language-reference/modifiers/default.md)
