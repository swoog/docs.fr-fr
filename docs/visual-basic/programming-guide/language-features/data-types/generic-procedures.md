---
title: Procédures génériques dans Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- generic methods [Visual Basic], type inference
- generics [Visual Basic], type inference
- procedures [Visual Basic], generic
- generic procedures
- type inference, generics
- generic methods [Visual Basic]
- type inference
- generics [Visual Basic], procedures
- generic procedures [Visual Basic], type inference
ms.assetid: 95577b28-137f-4d5c-a149-919c828600e5
ms.openlocfilehash: 4aed16ce9eb59da54156a0cd5f1594819788521b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61906592"
---
# <a name="generic-procedures-in-visual-basic"></a><span data-ttu-id="d082b-102">Procédures génériques dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d082b-102">Generic Procedures in Visual Basic</span></span>
<span data-ttu-id="d082b-103">Un *procédure générique*, également appelé un *méthode générique*, est une procédure définie au moins un paramètre de type.</span><span class="sxs-lookup"><span data-stu-id="d082b-103">A *generic procedure*, also called a *generic method*, is a procedure defined with at least one type parameter.</span></span> <span data-ttu-id="d082b-104">Cela permet au code appelant d’adapter les types de données à ses exigences chaque fois qu’il appelle la procédure.</span><span class="sxs-lookup"><span data-stu-id="d082b-104">This allows the calling code to tailor the data types to its requirements each time it calls the procedure.</span></span>  
  
 <span data-ttu-id="d082b-105">Une procédure n’est pas générique simplement en vertu d’en cours de définition à l’intérieur d’une classe générique ou une structure générique.</span><span class="sxs-lookup"><span data-stu-id="d082b-105">A procedure is not generic simply by virtue of being defined inside a generic class or a generic structure.</span></span> <span data-ttu-id="d082b-106">Pour être générique, la procédure doit prendre au moins un paramètre de type, en plus de tous les paramètres normaux que peut prendre.</span><span class="sxs-lookup"><span data-stu-id="d082b-106">To be generic, the procedure must take at least one type parameter, in addition to any normal parameters it might take.</span></span> <span data-ttu-id="d082b-107">Une classe générique ou une structure peut contenir des procédures non génériques et une classe non générique, structure, ou le module peut contenir des procédures génériques.</span><span class="sxs-lookup"><span data-stu-id="d082b-107">A generic class or structure can contain nongeneric procedures, and a nongeneric class, structure, or module can contain generic procedures.</span></span>  
  
 <span data-ttu-id="d082b-108">Une procédure générique peut utiliser ses paramètres de type dans sa liste de paramètres normale, dans son type de retour s’il a un et dans sa procédure de code.</span><span class="sxs-lookup"><span data-stu-id="d082b-108">A generic procedure can use its type parameters in its normal parameter list, in its return type if it has one, and in its procedure code.</span></span>  
  
## <a name="type-inference"></a><span data-ttu-id="d082b-109">Inférence de type</span><span class="sxs-lookup"><span data-stu-id="d082b-109">Type Inference</span></span>  
 <span data-ttu-id="d082b-110">Vous pouvez appeler une procédure générique sans fournir d’arguments de type du tout.</span><span class="sxs-lookup"><span data-stu-id="d082b-110">You can call a generic procedure without supplying any type arguments at all.</span></span> <span data-ttu-id="d082b-111">Si vous l’appelez de cette façon, le compilateur tente de déterminer les types de données appropriées à passer des arguments de type de la procédure.</span><span class="sxs-lookup"><span data-stu-id="d082b-111">If you call it this way, the compiler attempts to determine the appropriate data types to pass to the procedure's type arguments.</span></span> <span data-ttu-id="d082b-112">Il s’agit *l’inférence de type*.</span><span class="sxs-lookup"><span data-stu-id="d082b-112">This is called *type inference*.</span></span> <span data-ttu-id="d082b-113">Le code suivant montre un appel dans lequel le compilateur déduit qu’il doit passer le type `String` au paramètre de type `t`.</span><span class="sxs-lookup"><span data-stu-id="d082b-113">The following code shows a call in which the compiler infers that it should pass type `String` to the type parameter `t`.</span></span>  
  
 [!code-vb[VbVbalrDataTypes#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDataTypes/VB/Class1.vb#15)]  
  
 <span data-ttu-id="d082b-114">Si le compilateur ne peut pas déduire les arguments de type à partir du contexte de votre appel, il signale une erreur.</span><span class="sxs-lookup"><span data-stu-id="d082b-114">If the compiler cannot infer the type arguments from the context of your call, it reports an error.</span></span> <span data-ttu-id="d082b-115">Une des causes possibles de cette erreur est une incompatibilité de rang de tableau.</span><span class="sxs-lookup"><span data-stu-id="d082b-115">One possible cause of such an error is an array rank mismatch.</span></span> <span data-ttu-id="d082b-116">Par exemple, supposons que vous définissez un paramètre normal comme un tableau d’un paramètre de type.</span><span class="sxs-lookup"><span data-stu-id="d082b-116">For example, suppose you define a normal parameter as an array of a type parameter.</span></span> <span data-ttu-id="d082b-117">Si vous appelez la procédure générique en fournissant un tableau d’un rang différent (nombre de dimensions), la différence provoque l’inférence de type échec.</span><span class="sxs-lookup"><span data-stu-id="d082b-117">If you call the generic procedure supplying an array of a different rank (number of dimensions), the mismatch causes type inference to fail.</span></span> <span data-ttu-id="d082b-118">Le code suivant montre un appel dans lequel un tableau à deux dimensions est passé à une procédure qui attend un tableau unidimensionnel.</span><span class="sxs-lookup"><span data-stu-id="d082b-118">The following code shows a call in which a two-dimensional array is passed to a procedure that expects a one-dimensional array.</span></span>  
  
```vb  
Public Sub demoSub(Of t)(ByVal arg() As t)
End Sub

Public Sub callDemoSub()
    Dim twoDimensions(,) As Integer
    demoSub(twoDimensions)
End Sub
```
  
 <span data-ttu-id="d082b-119">Vous pouvez appeler l’inférence de type uniquement en omettant tous les arguments de type.</span><span class="sxs-lookup"><span data-stu-id="d082b-119">You can invoke type inference only by omitting all the type arguments.</span></span> <span data-ttu-id="d082b-120">Si vous fournissez un argument de type, vous devez fournir toutes les.</span><span class="sxs-lookup"><span data-stu-id="d082b-120">If you supply one type argument, you must supply them all.</span></span>  
  
 <span data-ttu-id="d082b-121">Inférence de type est pris en charge uniquement pour les procédures génériques.</span><span class="sxs-lookup"><span data-stu-id="d082b-121">Type inference is supported only for generic procedures.</span></span> <span data-ttu-id="d082b-122">Vous ne pouvez pas appeler l’inférence de type sur les classes génériques, des structures, des interfaces ou des délégués.</span><span class="sxs-lookup"><span data-stu-id="d082b-122">You cannot invoke type inference on generic classes, structures, interfaces, or delegates.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d082b-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="d082b-123">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="d082b-124">Description</span><span class="sxs-lookup"><span data-stu-id="d082b-124">Description</span></span>  
 <span data-ttu-id="d082b-125">L’exemple suivant définit un générique `Function` procédure pour rechercher un élément particulier dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="d082b-125">The following example defines a generic `Function` procedure to find a particular element in an array.</span></span> <span data-ttu-id="d082b-126">Il définit un paramètre de type et l’utilise pour construire les deux paramètres dans la liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="d082b-126">It defines one type parameter and uses it to construct the two parameters in the parameter list.</span></span>  
  
### <a name="code"></a><span data-ttu-id="d082b-127">Code</span><span class="sxs-lookup"><span data-stu-id="d082b-127">Code</span></span>  
 [!code-vb[VbVbalrDataTypes#14](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDataTypes/VB/Class1.vb#14)]  
  
### <a name="comments"></a><span data-ttu-id="d082b-128">Commentaires</span><span class="sxs-lookup"><span data-stu-id="d082b-128">Comments</span></span>  
 <span data-ttu-id="d082b-129">L’exemple précédent doit avoir la possibilité de comparer `searchValue` sur chaque élément de `searchArray`.</span><span class="sxs-lookup"><span data-stu-id="d082b-129">The preceding example requires the ability to compare `searchValue` against each element of `searchArray`.</span></span> <span data-ttu-id="d082b-130">Pour garantir cette capacité, il contraint le paramètre de type `T` pour implémenter le <xref:System.IComparable%601> interface.</span><span class="sxs-lookup"><span data-stu-id="d082b-130">To guarantee this ability, it constrains the type parameter `T` to implement the <xref:System.IComparable%601> interface.</span></span> <span data-ttu-id="d082b-131">Le code utilise le <xref:System.IComparable%601.CompareTo%2A> méthode au lieu du `=` opérateur, car il n’existe aucune garantie qu’un argument de type fourni pour `T` prend en charge la `=` opérateur.</span><span class="sxs-lookup"><span data-stu-id="d082b-131">The code uses the <xref:System.IComparable%601.CompareTo%2A> method instead of the `=` operator, because there is no guarantee that a type argument supplied for `T` supports the `=` operator.</span></span>  
  
 <span data-ttu-id="d082b-132">Vous pouvez tester le `findElement` procédure avec le code suivant.</span><span class="sxs-lookup"><span data-stu-id="d082b-132">You can test the `findElement` procedure with the following code.</span></span>  
  
 [!code-vb[VbVbalrDataTypes#13](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDataTypes/VB/Class1.vb#13)]  
  
 <span data-ttu-id="d082b-133">L’exemple précédent appelle à `MsgBox` afficher « 0 », « 1 » et « -1 » respectivement.</span><span class="sxs-lookup"><span data-stu-id="d082b-133">The preceding calls to `MsgBox` display "0", "1", and "-1" respectively.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d082b-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d082b-134">See also</span></span>

- [<span data-ttu-id="d082b-135">Generic Types in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d082b-135">Generic Types in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)
- [<span data-ttu-id="d082b-136">Guide pratique pour définir une classe qui fournisse des fonctionnalités identiques pour différents types de données</span><span class="sxs-lookup"><span data-stu-id="d082b-136">How to: Define a Class That Can Provide Identical Functionality on Different Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/how-to-define-a-class-that-can-provide-identical-functionality.md)
- [<span data-ttu-id="d082b-137">Guide pratique pour utiliser une classe générique</span><span class="sxs-lookup"><span data-stu-id="d082b-137">How to: Use a Generic Class</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/how-to-use-a-generic-class.md)
- [<span data-ttu-id="d082b-138">Procédures</span><span class="sxs-lookup"><span data-stu-id="d082b-138">Procedures</span></span>](../../../../visual-basic/programming-guide/language-features/procedures/index.md)
- [<span data-ttu-id="d082b-139">Paramètres et arguments d’une procédure</span><span class="sxs-lookup"><span data-stu-id="d082b-139">Procedure Parameters and Arguments</span></span>](../../../../visual-basic/programming-guide/language-features/procedures/procedure-parameters-and-arguments.md)
- [<span data-ttu-id="d082b-140">Liste de types</span><span class="sxs-lookup"><span data-stu-id="d082b-140">Type List</span></span>](../../../../visual-basic/language-reference/statements/type-list.md)
- [<span data-ttu-id="d082b-141">Liste de paramètres</span><span class="sxs-lookup"><span data-stu-id="d082b-141">Parameter List</span></span>](../../../../visual-basic/language-reference/statements/parameter-list.md)
