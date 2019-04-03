---
title: Inherits, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Inherits
- Inherits
helpviewer_keywords:
- Inherits statement [Visual Basic]
- Inherits statement [Visual Basic], syntax
ms.assetid: 9e6fe042-9af3-4341-8093-fc3537770cf2
ms.openlocfilehash: 5ab90e44e2809c1e71d7f100970b7be73af4a732
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58817095"
---
# <a name="inherits-statement"></a><span data-ttu-id="ed9c2-102">Inherits Statement</span><span class="sxs-lookup"><span data-stu-id="ed9c2-102">Inherits Statement</span></span>
<span data-ttu-id="ed9c2-103">Provoque la classe en cours ou interface hérite des attributs, variables, propriétés, procédures et événements d’une autre classe ou ensemble d’interfaces.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-103">Causes the current class or interface to inherit the attributes, variables, properties, procedures, and events from another class or set of interfaces.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ed9c2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed9c2-104">Syntax</span></span>  
  
```  
Inherits basetypenames  
```  
  
## <a name="parts"></a><span data-ttu-id="ed9c2-105">Composants</span><span class="sxs-lookup"><span data-stu-id="ed9c2-105">Parts</span></span>  
  
|<span data-ttu-id="ed9c2-106">Terme</span><span class="sxs-lookup"><span data-stu-id="ed9c2-106">Term</span></span>|<span data-ttu-id="ed9c2-107">Définition</span><span class="sxs-lookup"><span data-stu-id="ed9c2-107">Definition</span></span>|  
|---|---|  
|`basetypenames`|<span data-ttu-id="ed9c2-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-108">Required.</span></span> <span data-ttu-id="ed9c2-109">Le nom de la classe à partir de laquelle cette classe est dérivée.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-109">The name of the class from which this class derives.</span></span><br /><br /> <span data-ttu-id="ed9c2-110">- ou -</span><span class="sxs-lookup"><span data-stu-id="ed9c2-110">-or-</span></span><br /><br /> <span data-ttu-id="ed9c2-111">Les noms des interfaces à partir de laquelle cette interface est dérivée.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-111">The names of the interfaces from which this interface derives.</span></span> <span data-ttu-id="ed9c2-112">Utilisez des virgules pour séparer plusieurs noms.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-112">Use commas to separate multiple names.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ed9c2-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ed9c2-113">Remarks</span></span>  
 <span data-ttu-id="ed9c2-114">Si utilisé, le `Inherits` instruction doit être la première ligne non vide, sans commentaire dans une définition de classe ou interface.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-114">If used, the `Inherits` statement must be the first non-blank, non-comment line in a class or interface definition.</span></span> <span data-ttu-id="ed9c2-115">Elle doit suivre immédiatement le `Class` ou `Interface` instruction.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-115">It should immediately follow the `Class` or `Interface` statement.</span></span>  
  
 <span data-ttu-id="ed9c2-116">Vous pouvez utiliser `Inherits` uniquement dans une classe ou interface.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-116">You can use `Inherits` only in a class or interface.</span></span> <span data-ttu-id="ed9c2-117">Cela signifie que le contexte de déclaration pour un héritage ne peut pas être un fichier source, espace de noms, de structure, module, procédure ou bloc.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-117">This means the declaration context for an inheritance cannot be a source file, namespace, structure, module, procedure, or block.</span></span>  
  
## <a name="rules"></a><span data-ttu-id="ed9c2-118">Règles</span><span class="sxs-lookup"><span data-stu-id="ed9c2-118">Rules</span></span>  
  
-   <span data-ttu-id="ed9c2-119">**Héritage de classes.**</span><span class="sxs-lookup"><span data-stu-id="ed9c2-119">**Class Inheritance.**</span></span> <span data-ttu-id="ed9c2-120">Si une classe utilise le `Inherits` instruction, vous pouvez spécifier qu’une seule classe de base.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-120">If a class uses the `Inherits` statement, you can specify only one base class.</span></span>  
  
     <span data-ttu-id="ed9c2-121">Une classe ne peut pas hériter d’une classe imbriquée dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-121">A class cannot inherit from a class nested within it.</span></span>  
  
-   <span data-ttu-id="ed9c2-122">**Héritage de l’interface.**</span><span class="sxs-lookup"><span data-stu-id="ed9c2-122">**Interface Inheritance.**</span></span> <span data-ttu-id="ed9c2-123">Si une interface utilise le `Inherits` instruction, vous pouvez spécifier une ou plusieurs interfaces de base.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-123">If an interface uses the `Inherits` statement, you can specify one or more base interfaces.</span></span> <span data-ttu-id="ed9c2-124">Vous pouvez hériter de deux interfaces même si chacune définit un membre portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-124">You can inherit from two interfaces even if they each define a member with the same name.</span></span> <span data-ttu-id="ed9c2-125">Si vous procédez ainsi, le code d’implémentation doit utiliser qualification de noms pour spécifier le membre qu’il implémente.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-125">If you do so, the implementing code must use name qualification to specify which member it is implementing.</span></span>  
  
     <span data-ttu-id="ed9c2-126">Une interface ne peut pas hériter d’une autre interface avec un niveau d’accès plus restrictif.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-126">An interface cannot inherit from another interface with a more restrictive access level.</span></span> <span data-ttu-id="ed9c2-127">Par exemple, un `Public` interface ne peut pas hériter d’un `Friend` interface.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-127">For example, a `Public` interface cannot inherit from a `Friend` interface.</span></span>  
  
     <span data-ttu-id="ed9c2-128">Une interface ne peut pas hériter d’une interface imbriquée dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-128">An interface cannot inherit from an interface nested within it.</span></span>  
  
 <span data-ttu-id="ed9c2-129">Un exemple d’héritage de classe dans le .NET Framework est la <xref:System.ArgumentException> (classe), qui hérite de la <xref:System.SystemException> classe.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-129">An example of class inheritance in the .NET Framework is the <xref:System.ArgumentException> class, which inherits from the <xref:System.SystemException> class.</span></span> <span data-ttu-id="ed9c2-130">Cela fournit à <xref:System.ArgumentException> toutes les propriétés prédéfinies et les procédures requises par les exceptions système, telles que la <xref:System.Exception.Message%2A> propriété et la <xref:System.Exception.ToString%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="ed9c2-130">This provides to <xref:System.ArgumentException> all the predefined properties and procedures required by system exceptions, such as the <xref:System.Exception.Message%2A> property and the <xref:System.Exception.ToString%2A> method.</span></span>  
  
 <span data-ttu-id="ed9c2-131">Un exemple d’héritage d’interface dans le .NET Framework est la <xref:System.Collections.ICollection> interface qui hérite de la <xref:System.Collections.IEnumerable> interface.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-131">An example of interface inheritance in the .NET Framework is the <xref:System.Collections.ICollection> interface, which inherits from the <xref:System.Collections.IEnumerable> interface.</span></span> <span data-ttu-id="ed9c2-132">Cela entraîne <xref:System.Collections.ICollection> d’hériter de la définition de l’énumérateur permettant de parcourir une collection.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-132">This causes <xref:System.Collections.ICollection> to inherit the definition of the enumerator required to traverse a collection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ed9c2-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="ed9c2-133">Example</span></span>  
 <span data-ttu-id="ed9c2-134">L’exemple suivant utilise le `Inherits` instruction pour montrer comment une classe nommée `thisClass` peut hériter de tous les membres d’une classe de base nommée `anotherClass`.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-134">The following example uses the `Inherits` statement to show how a class named `thisClass` can inherit all the members of a base class named `anotherClass`.</span></span>  
  
 [!code-vb[VbVbalrStatements#37](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#37)]  
  
## <a name="example"></a><span data-ttu-id="ed9c2-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="ed9c2-135">Example</span></span>  
 <span data-ttu-id="ed9c2-136">L’exemple suivant montre l’héritage de plusieurs interfaces.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-136">The following example shows inheritance of multiple interfaces.</span></span>  
  
 [!code-vb[VbVbalrStatements#38](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#38)]  
  
 <span data-ttu-id="ed9c2-137">L’interface nommée `thisInterface` inclut désormais toutes les définitions dans le <xref:System.IComparable>, <xref:System.IDisposable>, et <xref:System.IFormattable> interfaces que les membres hérités fournissent respectivement pour comparaison spécifique au type de deux objets, libérer les ressources allouées. et l’expression de la valeur d’un objet comme un `String`.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-137">The interface named `thisInterface` now includes all the definitions in the <xref:System.IComparable>, <xref:System.IDisposable>, and <xref:System.IFormattable> interfaces The inherited members provide respectively for type-specific comparison of two objects, releasing allocated resources, and expressing the value of an object as a `String`.</span></span> <span data-ttu-id="ed9c2-138">Une classe qui implémente `thisInterface` doit implémenter chaque membre de chaque interface de base.</span><span class="sxs-lookup"><span data-stu-id="ed9c2-138">A class that implements `thisInterface` must implement every member of every base interface.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ed9c2-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed9c2-139">See also</span></span>

- [<span data-ttu-id="ed9c2-140">MustInherit</span><span class="sxs-lookup"><span data-stu-id="ed9c2-140">MustInherit</span></span>](../../../visual-basic/language-reference/modifiers/mustinherit.md)
- [<span data-ttu-id="ed9c2-141">NotInheritable</span><span class="sxs-lookup"><span data-stu-id="ed9c2-141">NotInheritable</span></span>](../../../visual-basic/language-reference/modifiers/notinheritable.md)
- [<span data-ttu-id="ed9c2-142">Objets et classes</span><span class="sxs-lookup"><span data-stu-id="ed9c2-142">Objects and Classes</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
- [<span data-ttu-id="ed9c2-143">Éléments fondamentaux de l’héritage</span><span class="sxs-lookup"><span data-stu-id="ed9c2-143">Inheritance Basics</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)
- [<span data-ttu-id="ed9c2-144">Interfaces</span><span class="sxs-lookup"><span data-stu-id="ed9c2-144">Interfaces</span></span>](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
