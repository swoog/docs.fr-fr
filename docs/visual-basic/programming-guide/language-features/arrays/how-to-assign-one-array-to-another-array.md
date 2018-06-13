---
title: 'Comment : assigner un tableau à un autre tableau (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- covariance, arrays
- arrays [Visual Basic], assigning
- arrays [Visual Basic], covariance
ms.assetid: 1ae89ea5-f292-4282-bcfc-e9b06b37fbd5
ms.openlocfilehash: 63c7d187152fcb5ea84378c677aa687f334f63de
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33647928"
---
# <a name="how-to-assign-one-array-to-another-array-visual-basic"></a><span data-ttu-id="c9098-102">Comment : assigner un tableau à un autre tableau (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c9098-102">How to: Assign One Array to Another Array (Visual Basic)</span></span>
<span data-ttu-id="c9098-103">Étant donné que les tableaux sont des objets, vous pouvez les utiliser dans les instructions d’assignation comme les autres types d’objet.</span><span class="sxs-lookup"><span data-stu-id="c9098-103">Because arrays are objects, you can use them in assignment statements like other object types.</span></span> <span data-ttu-id="c9098-104">Une variable tableau conserve un pointeur vers les données constituant les éléments du tableau et les informations de classement et de longueur et une attribution de copie uniquement ce pointeur.</span><span class="sxs-lookup"><span data-stu-id="c9098-104">An array variable holds a pointer to the data constituting the array elements and the rank and length information, and an assignment copies only this pointer.</span></span>  
  
### <a name="to-assign-one-array-to-another-array"></a><span data-ttu-id="c9098-105">Pour assigner un tableau à un autre tableau</span><span class="sxs-lookup"><span data-stu-id="c9098-105">To assign one array to another array</span></span>  
  
1.  <span data-ttu-id="c9098-106">Assurez-vous que les deux tableaux ont le même rang (nombre de dimensions) et les types de données d’élément compatibles.</span><span class="sxs-lookup"><span data-stu-id="c9098-106">Ensure that the two arrays have the same rank (number of dimensions) and compatible element data types.</span></span>  
  
2.  <span data-ttu-id="c9098-107">Utilisez une instruction d’assignation standard pour assigner le tableau source dans le tableau de destination.</span><span class="sxs-lookup"><span data-stu-id="c9098-107">Use a standard assignment statement to assign the source array to the destination array.</span></span> <span data-ttu-id="c9098-108">Ne suivez pas les noms du tableau de parenthèses.</span><span class="sxs-lookup"><span data-stu-id="c9098-108">Do not follow either array name with parentheses.</span></span>  
  
    ```  
    Dim formArray() As System.Windows.Forms.Form  
    Dim controlArray() As System.Windows.Forms.Control  
    controlArray = formArray  
    ```  
  
 <span data-ttu-id="c9098-109">Lorsque vous affectez un tableau à un autre, les règles suivantes s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="c9098-109">When you assign one array to another, the following rules apply:</span></span>  
  
-   <span data-ttu-id="c9098-110">**Rangs identiques.**</span><span class="sxs-lookup"><span data-stu-id="c9098-110">**Equal Ranks.**</span></span> <span data-ttu-id="c9098-111">Le rang (nombre de dimensions) du tableau de destination doit être identique à celui du tableau source.</span><span class="sxs-lookup"><span data-stu-id="c9098-111">The rank (number of dimensions) of the destination array must be the same as that of the source array.</span></span>  
  
     <span data-ttu-id="c9098-112">Condition les rangs des deux tableaux sont égaux, les dimensions n’avez pas besoin être égale.</span><span class="sxs-lookup"><span data-stu-id="c9098-112">Provided the ranks of the two arrays are equal, the dimensions do not need to be equal.</span></span> <span data-ttu-id="c9098-113">Le nombre d’éléments dans une dimension donnée peut changer pendant l’affectation.</span><span class="sxs-lookup"><span data-stu-id="c9098-113">The number of elements in a given dimension can change during assignment.</span></span>  
  
-   <span data-ttu-id="c9098-114">**Types d’élément.**</span><span class="sxs-lookup"><span data-stu-id="c9098-114">**Element Types.**</span></span> <span data-ttu-id="c9098-115">Soit les deux tableaux doivent avoir *type référence* éléments ou les deux tableaux doit avoir *type valeur* éléments.</span><span class="sxs-lookup"><span data-stu-id="c9098-115">Either both arrays must have *reference type* elements or both arrays must have *value type* elements.</span></span> <span data-ttu-id="c9098-116">Pour plus d’informations, consultez [les Types valeur et Types référence](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md).</span><span class="sxs-lookup"><span data-stu-id="c9098-116">For more information, see [Value Types and Reference Types](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md).</span></span>  
  
    -   <span data-ttu-id="c9098-117">Si les deux tableaux ont des éléments de type valeur, les types de données d’élément doivent être exactement le même.</span><span class="sxs-lookup"><span data-stu-id="c9098-117">If both arrays have value type elements, the element data types must be exactly the same.</span></span> <span data-ttu-id="c9098-118">La seule exception à cela est que vous pouvez assigner un tableau de `Enum` éléments dans un tableau du type de base de ce `Enum`.</span><span class="sxs-lookup"><span data-stu-id="c9098-118">The only exception to this is that you can assign an array of `Enum` elements to an array of the base type of that `Enum`.</span></span>  
  
    -   <span data-ttu-id="c9098-119">Si les deux tableaux ont référence des éléments de type, le type d’élément source doit dériver du type d’élément de destination.</span><span class="sxs-lookup"><span data-stu-id="c9098-119">If both arrays have reference type elements, the source element type must derive from the destination element type.</span></span> <span data-ttu-id="c9098-120">Lorsque c’est le cas, les deux tableaux ont la même relation d’héritage que leurs éléments.</span><span class="sxs-lookup"><span data-stu-id="c9098-120">When this is the case, the two arrays have the same inheritance relationship as their elements.</span></span> <span data-ttu-id="c9098-121">Il s’agit *covariance de tableau*.</span><span class="sxs-lookup"><span data-stu-id="c9098-121">This is called *array covariance*.</span></span>  
  
 <span data-ttu-id="c9098-122">Le compilateur signale une erreur si les règles ci-dessus sont violées, par exemple si les types de données ne sont pas compatibles.</span><span class="sxs-lookup"><span data-stu-id="c9098-122">The compiler reports an error if the above rules are violated, for example if the data types are not compatible or the ranks are unequal.</span></span> <span data-ttu-id="c9098-123">Vous pouvez ajouter à votre code pour vous assurer que les tableaux sont compatibles avant de tenter une assignation de gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="c9098-123">You can add error handling to your code to make sure that the arrays are compatible before attempting an assignment.</span></span> <span data-ttu-id="c9098-124">Vous pouvez également utiliser le [opérateur TryCast](../../../../visual-basic/language-reference/operators/trycast-operator.md) mot clé si vous souhaitez éviter de lever une exception.</span><span class="sxs-lookup"><span data-stu-id="c9098-124">You can also use the [TryCast Operator](../../../../visual-basic/language-reference/operators/trycast-operator.md) keyword if you want to avoid throwing an exception.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c9098-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9098-125">See Also</span></span>  
 [<span data-ttu-id="c9098-126">Tableaux</span><span class="sxs-lookup"><span data-stu-id="c9098-126">Arrays</span></span>](../../../../visual-basic/programming-guide/language-features/arrays/index.md)  
 [<span data-ttu-id="c9098-127">Dépannage des tableaux</span><span class="sxs-lookup"><span data-stu-id="c9098-127">Troubleshooting Arrays</span></span>](../../../../visual-basic/programming-guide/language-features/arrays/troubleshooting-arrays.md)  
 [<span data-ttu-id="c9098-128">Enum (instruction)</span><span class="sxs-lookup"><span data-stu-id="c9098-128">Enum Statement</span></span>](../../../../visual-basic/language-reference/statements/enum-statement.md)  
 [<span data-ttu-id="c9098-129">Conversions de tableau</span><span class="sxs-lookup"><span data-stu-id="c9098-129">Array Conversions</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/array-conversions.md)
