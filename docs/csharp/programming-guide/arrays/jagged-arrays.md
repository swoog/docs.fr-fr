---
title: Tableaux en escalier - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- jagged arrays [C#]
- arrays [C#], jagged
ms.assetid: 537c65a6-0e0a-4a00-a2b8-086f38519c70
ms.openlocfilehash: f517a9a6d6e10f04df70729fb9e641c1f955f28a
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53237855"
---
# <a name="jagged-arrays-c-programming-guide"></a><span data-ttu-id="3ea10-102">Tableaux en escalier (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="3ea10-102">Jagged Arrays (C# Programming Guide)</span></span>

<span data-ttu-id="3ea10-103">Un tableau en escalier est un tableau dont les éléments sont des tableaux.</span><span class="sxs-lookup"><span data-stu-id="3ea10-103">A jagged array is an array whose elements are arrays.</span></span> <span data-ttu-id="3ea10-104">Les éléments d’un tableau en escalier peuvent être de dimensions et de tailles différentes.</span><span class="sxs-lookup"><span data-stu-id="3ea10-104">The elements of a jagged array can be of different dimensions and sizes.</span></span> <span data-ttu-id="3ea10-105">Un tableau en escalier est parfois appelé « tableau de tableaux ».</span><span class="sxs-lookup"><span data-stu-id="3ea10-105">A jagged array is sometimes called an "array of arrays."</span></span> <span data-ttu-id="3ea10-106">Les exemples suivants montrent comment déclarer, initialiser et accéder aux tableaux en escalier.</span><span class="sxs-lookup"><span data-stu-id="3ea10-106">The following examples show how to declare, initialize, and access jagged arrays.</span></span>  
  
 <span data-ttu-id="3ea10-107">Voici une déclaration d’un tableau unidimensionnel qui comporte trois éléments, chacun d’eux étant un tableau unidimensionnel d’entiers :</span><span class="sxs-lookup"><span data-stu-id="3ea10-107">The following is a declaration of a single-dimensional array that has three elements, each of which is a single-dimensional array of integers:</span></span>  
  
 [!code-csharp[csProgGuideArrays#19](../../../csharp/programming-guide/arrays/codesnippet/CSharp/jagged-arrays_1.cs)]  
  
 <span data-ttu-id="3ea10-108">Pour pouvoir utiliser `jaggedArray`, vous devez initialiser ses éléments.</span><span class="sxs-lookup"><span data-stu-id="3ea10-108">Before you can use `jaggedArray`, its elements must be initialized.</span></span> <span data-ttu-id="3ea10-109">Pour ce faire, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="3ea10-109">You can initialize the elements like this:</span></span>  
  
 [!code-csharp[csProgGuideArrays#20](../../../csharp/programming-guide/arrays/codesnippet/CSharp/jagged-arrays_2.cs)]  
  
 <span data-ttu-id="3ea10-110">Chacun des éléments est un tableau unidimensionnel d’entiers.</span><span class="sxs-lookup"><span data-stu-id="3ea10-110">Each of the elements is a single-dimensional array of integers.</span></span> <span data-ttu-id="3ea10-111">Le premier élément est un tableau de 5 entiers, le deuxième est un tableau de 4 entiers et le troisième est un tableau de 2 entiers.</span><span class="sxs-lookup"><span data-stu-id="3ea10-111">The first element is an array of 5 integers, the second is an array of 4 integers, and the third is an array of 2 integers.</span></span>  
  
 <span data-ttu-id="3ea10-112">Il est aussi possible d’utiliser des initialiseurs pour remplir les éléments de tableau de valeurs, auquel cas vous n’avez pas besoin de la taille du tableau.</span><span class="sxs-lookup"><span data-stu-id="3ea10-112">It is also possible to use initializers to fill the array elements with values, in which case you do not need the array size.</span></span> <span data-ttu-id="3ea10-113">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="3ea10-113">For example:</span></span>  
  
 [!code-csharp[csProgGuideArrays#21](../../../csharp/programming-guide/arrays/codesnippet/CSharp/jagged-arrays_3.cs)]  
  
 <span data-ttu-id="3ea10-114">Vous pouvez aussi initialiser le tableau au moment de la déclaration, comme ceci :</span><span class="sxs-lookup"><span data-stu-id="3ea10-114">You can also initialize the array upon declaration like this:</span></span>  
  
 [!code-csharp[csProgGuideArrays#22](../../../csharp/programming-guide/arrays/codesnippet/CSharp/jagged-arrays_4.cs)]  
  
 <span data-ttu-id="3ea10-115">Vous pouvez utiliser la forme abrégée suivante.</span><span class="sxs-lookup"><span data-stu-id="3ea10-115">You can use the following shorthand form.</span></span> <span data-ttu-id="3ea10-116">Notez que vous ne pouvez pas omettre l’opérateur `new` dans l’initialisation des éléments, car il n’existe pas d’initialisation par défaut pour les éléments :</span><span class="sxs-lookup"><span data-stu-id="3ea10-116">Notice that you cannot omit the `new` operator from the elements initialization because there is no default initialization for the elements:</span></span>  
  
 [!code-csharp[csProgGuideArrays#23](../../../csharp/programming-guide/arrays/codesnippet/CSharp/jagged-arrays_5.cs)]  
  
 <span data-ttu-id="3ea10-117">Un tableau en escalier est un tableau de tableaux, et par conséquent ses éléments sont des types référence et sont initialisés sur `null`.</span><span class="sxs-lookup"><span data-stu-id="3ea10-117">A jagged array is an array of arrays, and therefore its elements are reference types and are initialized to `null`.</span></span>  
  
 <span data-ttu-id="3ea10-118">Vous pouvez accéder aux éléments de tableau individuels comme dans ces exemples :</span><span class="sxs-lookup"><span data-stu-id="3ea10-118">You can access individual array elements like these examples:</span></span>  
  
 [!code-csharp[csProgGuideArrays#24](../../../csharp/programming-guide/arrays/codesnippet/CSharp/jagged-arrays_6.cs)]  
  
 <span data-ttu-id="3ea10-119">Il est possible de combiner des tableaux en escalier et des tableaux multidimensionnels.</span><span class="sxs-lookup"><span data-stu-id="3ea10-119">It is possible to mix jagged and multidimensional arrays.</span></span> <span data-ttu-id="3ea10-120">Vous trouverez ci-dessous une déclaration et une initialisation d’un tableau en escalier unidimensionnel composé de trois éléments de tableau à deux dimensions de tailles différentes.</span><span class="sxs-lookup"><span data-stu-id="3ea10-120">The following is a declaration and initialization of a single-dimensional jagged array that contains three two-dimensional array elements of different sizes.</span></span> <span data-ttu-id="3ea10-121">Pour plus d’informations sur les tableaux à deux dimensions, consultez [Tableaux multidimensionnels](../../../csharp/programming-guide/arrays/multidimensional-arrays.md).</span><span class="sxs-lookup"><span data-stu-id="3ea10-121">For more information about two-dimensional arrays, see [Multidimensional Arrays](../../../csharp/programming-guide/arrays/multidimensional-arrays.md).</span></span>  
  
 [!code-csharp[csProgGuideArrays#25](../../../csharp/programming-guide/arrays/codesnippet/CSharp/jagged-arrays_7.cs)]  
  
 <span data-ttu-id="3ea10-122">Vous pouvez accéder aux différents éléments comme le montre cet exemple, qui présente la valeur de l’élément `[1,0]` du premier tableau (valeur `5`) :</span><span class="sxs-lookup"><span data-stu-id="3ea10-122">You can access individual elements as shown in this example, which displays the value of the element `[1,0]` of the first array (value `5`):</span></span>  
  
 [!code-csharp[csProgGuideArrays#26](../../../csharp/programming-guide/arrays/codesnippet/CSharp/jagged-arrays_8.cs)]  
  
 <span data-ttu-id="3ea10-123">La méthode `Length` retourne le nombre de tableaux contenus dans le tableau en escalier.</span><span class="sxs-lookup"><span data-stu-id="3ea10-123">The method `Length` returns the number of arrays contained in the jagged array.</span></span> <span data-ttu-id="3ea10-124">Par exemple, en supposant que vous avez déclaré le tableau précédent, cette ligne :</span><span class="sxs-lookup"><span data-stu-id="3ea10-124">For example, assuming you have declared the previous array, this line:</span></span>  
  
 [!code-csharp[csProgGuideArrays#27](../../../csharp/programming-guide/arrays/codesnippet/CSharp/jagged-arrays_9.cs)]  
  
 <span data-ttu-id="3ea10-125">retourne la valeur 3.</span><span class="sxs-lookup"><span data-stu-id="3ea10-125">returns a value of 3.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3ea10-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="3ea10-126">Example</span></span>

 <span data-ttu-id="3ea10-127">Cet exemple génère un tableau dont les éléments sont eux-mêmes des tableaux.</span><span class="sxs-lookup"><span data-stu-id="3ea10-127">This example builds an array whose elements are themselves arrays.</span></span> <span data-ttu-id="3ea10-128">Chacun des éléments de tableau ont une taille différente.</span><span class="sxs-lookup"><span data-stu-id="3ea10-128">Each one of the array elements has a different size.</span></span>  
  
 [!code-csharp[csProgGuideArrays#18](../../../csharp/programming-guide/arrays/codesnippet/CSharp/jagged-arrays_10.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="3ea10-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ea10-129">See Also</span></span>

- <xref:System.Array>  
- [<span data-ttu-id="3ea10-130">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="3ea10-130">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="3ea10-131">Tableaux</span><span class="sxs-lookup"><span data-stu-id="3ea10-131">Arrays</span></span>](../../../csharp/programming-guide/arrays/index.md)  
- [<span data-ttu-id="3ea10-132">Tableaux unidimensionnels</span><span class="sxs-lookup"><span data-stu-id="3ea10-132">Single-Dimensional Arrays</span></span>](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md)  
- [<span data-ttu-id="3ea10-133">Tableaux multidimensionnels</span><span class="sxs-lookup"><span data-stu-id="3ea10-133">Multidimensional Arrays</span></span>](../../../csharp/programming-guide/arrays/multidimensional-arrays.md)
