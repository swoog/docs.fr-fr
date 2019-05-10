---
title: Types de données composites (Visual Basic)
ms.date: 04/25/2017
helpviewer_keywords:
- classes [Visual Basic], composite data types
- composite types [Visual Basic]
- composite data types [Visual Basic]
- data types [Visual Basic], composite
- arrays [Visual Basic], composite data types
- structures [Visual Basic], composite data types
- classes [Visual Basic], composite types
- types [Visual Basic], composite
ms.assetid: 62970f2e-52c0-4369-8963-613820f1f434
ms.openlocfilehash: 65ee23c59958eefb94c7ab0c6bef4a7e992a121c
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64601181"
---
# <a name="composite-data-types-visual-basic"></a><span data-ttu-id="09fe0-102">Types de données composites (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="09fe0-102">Composite Data Types (Visual Basic)</span></span>
<span data-ttu-id="09fe0-103">Outre les blocs de Visual Basic de types de données élémentaires, vous pouvez assembler des éléments de différents types pour créer *types de données composites* tels que des structures, des tableaux et des classes.</span><span class="sxs-lookup"><span data-stu-id="09fe0-103">In addition to the elementary data types Visual Basic supplies, you can also assemble items of different types to create *composite data types* such as structures, arrays, and classes.</span></span> <span data-ttu-id="09fe0-104">Vous pouvez créer des types de données composites à partir des types élémentaires et d’autres types composites.</span><span class="sxs-lookup"><span data-stu-id="09fe0-104">You can build composite data types from elementary types and from other composite types.</span></span> <span data-ttu-id="09fe0-105">Par exemple, vous pouvez définir un tableau d’éléments de structure ou une structure avec des membres de tableau.</span><span class="sxs-lookup"><span data-stu-id="09fe0-105">For example, you can define an array of structure elements, or a structure with array members.</span></span>  
  
## <a name="data-types"></a><span data-ttu-id="09fe0-106">Types de données</span><span class="sxs-lookup"><span data-stu-id="09fe0-106">Data Types</span></span>  
 <span data-ttu-id="09fe0-107">Un type composite est différent du type de données d’une de ses composants.</span><span class="sxs-lookup"><span data-stu-id="09fe0-107">A composite type is different from the data type of any of its components.</span></span> <span data-ttu-id="09fe0-108">Par exemple, un tableau de `Integer` éléments n’est pas de la `Integer` type de données.</span><span class="sxs-lookup"><span data-stu-id="09fe0-108">For example, an array of `Integer` elements is not of the `Integer` data type.</span></span>  
  
 <span data-ttu-id="09fe0-109">Un type de données de tableau est représenté normalement à l’aide du type d’élément, parenthèses et des virgules si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="09fe0-109">An array data type is normally represented using the element type, parentheses, and commas as necessary.</span></span> <span data-ttu-id="09fe0-110">Par exemple, un tableau unidimensionnel de `String` éléments est représenté en tant que `String()`et un tableau à deux dimensions de `Boolean` éléments est représenté en tant que `Boolean(,)`.</span><span class="sxs-lookup"><span data-stu-id="09fe0-110">For example, a one-dimensional array of `String` elements is represented as `String()`, and a two-dimensional array of `Boolean` elements is represented as `Boolean(,)`.</span></span>  
  
## <a name="structure-types"></a><span data-ttu-id="09fe0-111">Types de structure</span><span class="sxs-lookup"><span data-stu-id="09fe0-111">Structure Types</span></span>  
 <span data-ttu-id="09fe0-112">Il n’existe aucun type de données unique comprenant toutes les structures.</span><span class="sxs-lookup"><span data-stu-id="09fe0-112">There is no single data type comprising all structures.</span></span> <span data-ttu-id="09fe0-113">Au lieu de cela, chaque définition d’une structure représente un type de données unique, même si deux structures définissent des éléments identiques dans le même ordre.</span><span class="sxs-lookup"><span data-stu-id="09fe0-113">Instead, each definition of a structure represents a unique data type, even if two structures define identical elements in the same order.</span></span> <span data-ttu-id="09fe0-114">Toutefois, si vous créez deux ou plusieurs instances de la même structure, Visual Basic considère qu’ils soient du même type de données.</span><span class="sxs-lookup"><span data-stu-id="09fe0-114">However, if you create two or more instances of the same structure, Visual Basic considers them to be of the same data type.</span></span>  
  
## <a name="tuples"></a><span data-ttu-id="09fe0-115">Tuples</span><span class="sxs-lookup"><span data-stu-id="09fe0-115">Tuples</span></span>

<span data-ttu-id="09fe0-116">Un tuple est une structure léger qui contient deux ou plusieurs champs dont les types sont prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="09fe0-116">A tuple is a lightweight structure that contains two or more fields whose types are predefined.</span></span> <span data-ttu-id="09fe0-117">Tuples sont pris en charge à partir de Visual Basic 2017.</span><span class="sxs-lookup"><span data-stu-id="09fe0-117">Tuples are supported starting with Visual Basic 2017.</span></span> <span data-ttu-id="09fe0-118">Tuples sont couramment utilisées pour retourner plusieurs valeurs à partir d’un seul appel de méthode sans avoir à passer des arguments par référence ou en l’empaquetant les champs renvoyés dans une classe ou une structure plus activable.</span><span class="sxs-lookup"><span data-stu-id="09fe0-118">Tuples are most commonly used to return multiple values from a single method call without having to pass arguments by reference or packaging the returned fields in a more heavy-weight class or structure.</span></span> <span data-ttu-id="09fe0-119">Consultez le [Tuples](tuples.md) rubrique pour plus d’informations sur les tuples.</span><span class="sxs-lookup"><span data-stu-id="09fe0-119">See the [Tuples](tuples.md) topic for more information on tuples.</span></span>

## <a name="array-types"></a><span data-ttu-id="09fe0-120">Types de tableau</span><span class="sxs-lookup"><span data-stu-id="09fe0-120">Array Types</span></span>  
 <span data-ttu-id="09fe0-121">Il n’existe aucun type de données unique comprenant tous les tableaux.</span><span class="sxs-lookup"><span data-stu-id="09fe0-121">There is no single data type comprising all arrays.</span></span> <span data-ttu-id="09fe0-122">Le type de données d’une instance particulière d’un tableau est déterminé par les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="09fe0-122">The data type of a particular instance of an array is determined by the following:</span></span>  
  
- <span data-ttu-id="09fe0-123">Le fait d’être un tableau</span><span class="sxs-lookup"><span data-stu-id="09fe0-123">The fact of being an array</span></span>  
  
- <span data-ttu-id="09fe0-124">Le rang (nombre de dimensions) du tableau</span><span class="sxs-lookup"><span data-stu-id="09fe0-124">The rank (number of dimensions) of the array</span></span>  
  
- <span data-ttu-id="09fe0-125">Le type d’élément du tableau</span><span class="sxs-lookup"><span data-stu-id="09fe0-125">The element type of the array</span></span>  
  
 <span data-ttu-id="09fe0-126">En particulier, la longueur d’une dimension donnée n’est pas partie de l’instance type de données.</span><span class="sxs-lookup"><span data-stu-id="09fe0-126">In particular, the length of a given dimension is not part of the instance's data type.</span></span> <span data-ttu-id="09fe0-127">L'exemple suivant illustre ce comportement.</span><span class="sxs-lookup"><span data-stu-id="09fe0-127">The following example illustrates this.</span></span>  
  
```  
Dim arrayA( ) As Byte = New Byte(12) {}  
Dim arrayB( ) As Byte = New Byte(100) {}  
Dim arrayC( ) As Short = New Short(100) {}  
Dim arrayD( , ) As Short  
Dim arrayE( , ) As Short = New Short(4, 10) {}  
```  
  
 <span data-ttu-id="09fe0-128">Dans l’exemple précédent, les variables tableau `arrayA` et `arrayB` sont considérés comme du même type de données — `Byte()` , même si elles sont initialisées avec des longueurs différentes.</span><span class="sxs-lookup"><span data-stu-id="09fe0-128">In the preceding example, array variables `arrayA` and `arrayB` are considered to be of the same data type — `Byte()` — even though they are initialized to different lengths.</span></span> <span data-ttu-id="09fe0-129">Variables `arrayB` et `arrayC` ne sont pas du même type, car leurs types d’éléments sont différents.</span><span class="sxs-lookup"><span data-stu-id="09fe0-129">Variables `arrayB` and `arrayC` are not of the same type because their element types are different.</span></span> <span data-ttu-id="09fe0-130">Variables `arrayC` et `arrayD` ne sont pas du même type, car leurs rangs sont différents.</span><span class="sxs-lookup"><span data-stu-id="09fe0-130">Variables `arrayC` and `arrayD` are not of the same type because their ranks are different.</span></span> <span data-ttu-id="09fe0-131">Variables `arrayD` et `arrayE` ont le même type — `Short(,)` , car leurs rangs et types d’élément sont identiques, même si `arrayD` n’est pas encore initialisé.</span><span class="sxs-lookup"><span data-stu-id="09fe0-131">Variables `arrayD` and `arrayE` have the same type — `Short(,)` — because their ranks and element types are the same, even though `arrayD` is not yet initialized.</span></span>  
  
 <span data-ttu-id="09fe0-132">Pour plus d’informations sur les tableaux, consultez [tableaux](../../../../visual-basic/programming-guide/language-features/arrays/index.md).</span><span class="sxs-lookup"><span data-stu-id="09fe0-132">For more information on arrays, see [Arrays](../../../../visual-basic/programming-guide/language-features/arrays/index.md).</span></span>  
  
## <a name="class-types"></a><span data-ttu-id="09fe0-133">Types de classes</span><span class="sxs-lookup"><span data-stu-id="09fe0-133">Class Types</span></span>  
 <span data-ttu-id="09fe0-134">Il n’existe aucun type de données unique comprenant toutes les classes.</span><span class="sxs-lookup"><span data-stu-id="09fe0-134">There is no single data type comprising all classes.</span></span> <span data-ttu-id="09fe0-135">Bien qu’une classe peut hériter d’une autre classe, chacun est un type de données distinct.</span><span class="sxs-lookup"><span data-stu-id="09fe0-135">Although one class can inherit from another class, each is a separate data type.</span></span> <span data-ttu-id="09fe0-136">Plusieurs instances de la même classe sont du même type de données.</span><span class="sxs-lookup"><span data-stu-id="09fe0-136">Multiple instances of the same class are of the same data type.</span></span> <span data-ttu-id="09fe0-137">Si vous assignez une variable d’instance de classe vers un autre, non seulement font qu’ils ont les mêmes type de données, ils pointent vers la même instance de classe en mémoire.</span><span class="sxs-lookup"><span data-stu-id="09fe0-137">If you assign one class instance variable to another, not only do they have the same data type, they point to the same class instance in memory.</span></span>  
  
 <span data-ttu-id="09fe0-138">Pour plus d’informations sur les classes, consultez [objets et Classes](../../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md).</span><span class="sxs-lookup"><span data-stu-id="09fe0-138">For more information on classes, see [Objects and Classes](../../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="09fe0-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09fe0-139">See also</span></span>

- [<span data-ttu-id="09fe0-140">Types de données</span><span class="sxs-lookup"><span data-stu-id="09fe0-140">Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/index.md)
- [<span data-ttu-id="09fe0-141">Types de données élémentaires</span><span class="sxs-lookup"><span data-stu-id="09fe0-141">Elementary Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/elementary-data-types.md)
- [<span data-ttu-id="09fe0-142">Generic Types in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="09fe0-142">Generic Types in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)
- [<span data-ttu-id="09fe0-143">Value Types and Reference Types</span><span class="sxs-lookup"><span data-stu-id="09fe0-143">Value Types and Reference Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md)
- [<span data-ttu-id="09fe0-144">Conversions de type en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="09fe0-144">Type Conversions in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/type-conversions.md)
- [<span data-ttu-id="09fe0-145">Structures</span><span class="sxs-lookup"><span data-stu-id="09fe0-145">Structures</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [<span data-ttu-id="09fe0-146">Dépannage des types de données</span><span class="sxs-lookup"><span data-stu-id="09fe0-146">Troubleshooting Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md)
- [<span data-ttu-id="09fe0-147">Guide pratique pour stocker plusieurs valeurs dans une variable</span><span class="sxs-lookup"><span data-stu-id="09fe0-147">How to: Hold More Than One Value in a Variable</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/how-to-hold-more-than-one-value-in-a-variable.md)
