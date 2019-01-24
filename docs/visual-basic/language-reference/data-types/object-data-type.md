---
title: Type de données d’objet (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Object
- vb.Variant
helpviewer_keywords:
- object variables [Visual Basic], Object type
- data types [Visual Basic], assigning
- Object data type
- Object data type [Visual Basic], reference
ms.assetid: 61ea4a7c-3b3d-48d4-adc4-eacfa91779b2
ms.openlocfilehash: 5a37b571e0600927e0e50fdb1a63bcf8ef194d72
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54617536"
---
# <a name="object-data-type"></a><span data-ttu-id="ceb9d-102">Object Data Type</span><span class="sxs-lookup"><span data-stu-id="ceb9d-102">Object Data Type</span></span>
<span data-ttu-id="ceb9d-103">Contient les adresses qui font référence aux objets.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-103">Holds addresses that refer to objects.</span></span> <span data-ttu-id="ceb9d-104">Vous pouvez affecter n’importe quel type référence (chaîne, tableau, classe ou interface) à une `Object` variable.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-104">You can assign any reference type (string, array, class, or interface) to an `Object` variable.</span></span> <span data-ttu-id="ceb9d-105">Un `Object` variable peut également faire référence à des données de n’importe quel type valeur (numérique, `Boolean`, `Char`, `Date`, structure ou énumération).</span><span class="sxs-lookup"><span data-stu-id="ceb9d-105">An `Object` variable can also refer to data of any value type (numeric, `Boolean`, `Char`, `Date`, structure, or enumeration).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ceb9d-106">Notes</span><span class="sxs-lookup"><span data-stu-id="ceb9d-106">Remarks</span></span>  
 <span data-ttu-id="ceb9d-107">Le `Object` type de données peut pointer vers les données de n’importe quel type de données, y compris toute instance d’objet reconnaît votre application.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-107">The `Object` data type can point to data of any data type, including any object instance your application recognizes.</span></span> <span data-ttu-id="ceb9d-108">Utilisez `Object` lorsque vous ne connaissez pas au moment de la compilation, le type de données la variable peut pointer vers.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-108">Use `Object` when you do not know at compile time what data type the variable might point to.</span></span>  
  
 <span data-ttu-id="ceb9d-109">La valeur par défaut `Object` est `Nothing` (une référence null).</span><span class="sxs-lookup"><span data-stu-id="ceb9d-109">The default value of `Object` is `Nothing` (a null reference).</span></span>  
  
## <a name="data-types"></a><span data-ttu-id="ceb9d-110">Types de données</span><span class="sxs-lookup"><span data-stu-id="ceb9d-110">Data Types</span></span>  
 <span data-ttu-id="ceb9d-111">Vous pouvez assigner une variable, une constante ou une expression de n’importe quel type de données à un `Object` variable.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-111">You can assign a variable, constant, or expression of any data type to an `Object` variable.</span></span> <span data-ttu-id="ceb9d-112">Pour déterminer le type de données un `Object` variable fait actuellement référence, vous pouvez utiliser la <xref:System.Type.GetTypeCode%2A> méthode de la <xref:System.Type?displayProperty=nameWithType> classe.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-112">To determine the data type an `Object` variable currently refers to, you can use the <xref:System.Type.GetTypeCode%2A> method of the <xref:System.Type?displayProperty=nameWithType> class.</span></span> <span data-ttu-id="ceb9d-113">L'exemple suivant illustre ce comportement.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-113">The following example illustrates this.</span></span>  
  
```  
Dim myObject As Object  
' Suppose myObject has now had something assigned to it.  
Dim datTyp As Integer  
datTyp = Type.GetTypeCode(myObject.GetType())  
```  
  
 <span data-ttu-id="ceb9d-114">Le `Object` type de données est un type référence.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-114">The `Object` data type is a reference type.</span></span> <span data-ttu-id="ceb9d-115">Toutefois, Visual Basic traite une `Object` variable comme un type valeur lorsqu’elle fait référence aux données d’un type valeur.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-115">However, Visual Basic treats an `Object` variable as a value type when it refers to data of a value type.</span></span>  
  
## <a name="storage"></a><span data-ttu-id="ceb9d-116">Stockage</span><span class="sxs-lookup"><span data-stu-id="ceb9d-116">Storage</span></span>  
 <span data-ttu-id="ceb9d-117">Tout type de données qu’il fait référence, une `Object` variable ne contient pas la valeur de données elle-même, mais plutôt un pointeur vers la valeur.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-117">Whatever data type it refers to, an `Object` variable does not contain the data value itself, but rather a pointer to the value.</span></span> <span data-ttu-id="ceb9d-118">Elle utilise toujours les quatre octets dans la mémoire de l’ordinateur, mais cela n’inclut pas le stockage pour les données qui représente la valeur de la variable.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-118">It always uses four bytes in computer memory, but this does not include the storage for the data representing the value of the variable.</span></span> <span data-ttu-id="ceb9d-119">En raison du code qui utilise le pointeur pour localiser les données, `Object` variables contenant des types valeur sont légèrement plus lentes que celles explicitement des variables typées.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-119">Because of the code that uses the pointer to locate the data, `Object` variables holding value types are slightly slower to access than explicitly typed variables.</span></span>  
  
## <a name="programming-tips"></a><span data-ttu-id="ceb9d-120">Conseils de programmation</span><span class="sxs-lookup"><span data-stu-id="ceb9d-120">Programming Tips</span></span>  
  
-   <span data-ttu-id="ceb9d-121">**Considérations sur l’interopérabilité.**</span><span class="sxs-lookup"><span data-stu-id="ceb9d-121">**Interop Considerations.**</span></span> <span data-ttu-id="ceb9d-122">Si vous utilisez des composants non écrits pour le .NET Framework, par exemple des objets Automation ou COM, n’oubliez pas que les types pointeur dans d’autres environnements ne sont pas compatibles avec Visual Basic `Object` type.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-122">If you are interfacing with components not written for the .NET Framework, for example Automation or COM objects, keep in mind that pointer types in other environments are not compatible with the Visual Basic `Object` type.</span></span>  
  
-   <span data-ttu-id="ceb9d-123">**Performances**</span><span class="sxs-lookup"><span data-stu-id="ceb9d-123">**Performance.**</span></span> <span data-ttu-id="ceb9d-124">Une variable que vous déclarez avec le `Object` type est suffisamment flexible pour contenir une référence à n’importe quel objet.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-124">A variable you declare with the `Object` type is flexible enough to contain a reference to any object.</span></span> <span data-ttu-id="ceb9d-125">Toutefois, lorsque vous appelez une méthode ou propriété sur une variable de ce type, vous subissez toujours *liaison tardive* (au moment de l’exécution).</span><span class="sxs-lookup"><span data-stu-id="ceb9d-125">However, when you invoke a method or property on such a variable, you always incur *late binding* (at run time).</span></span> <span data-ttu-id="ceb9d-126">Pour forcer *liaison anticipée* (au moment de la compilation) et de meilleures performances, déclarez la variable avec un nom de classe spécifique ou les convertir en type de données spécifique.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-126">To force *early binding* (at compile time) and better performance, declare the variable with a specific class name, or cast it to the specific data type.</span></span>  
  
     <span data-ttu-id="ceb9d-127">Lorsque vous déclarez une variable objet, essayez d’utiliser un type de classe spécifique, par exemple <xref:System.OperatingSystem>, au lieu du généralisée `Object` type.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-127">When you declare an object variable, try to use a specific class type, for example <xref:System.OperatingSystem>, instead of the generalized `Object` type.</span></span> <span data-ttu-id="ceb9d-128">Vous devez également utiliser la classe la plus spécifique disponible, tel que <xref:System.Windows.Forms.TextBox> au lieu de <xref:System.Windows.Forms.Control>, de sorte que vous pouvez accéder à ses propriétés et méthodes.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-128">You should also use the most specific class available, such as <xref:System.Windows.Forms.TextBox> instead of <xref:System.Windows.Forms.Control>, so that you can access its properties and methods.</span></span> <span data-ttu-id="ceb9d-129">Vous pouvez généralement utiliser le **Classes** liste dans le **Explorateur d’objets** pour rechercher les noms de classes disponibles.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-129">You can usually use the **Classes** list in the **Object Browser** to find available class names.</span></span>  
  
-   <span data-ttu-id="ceb9d-130">**Étendues.**</span><span class="sxs-lookup"><span data-stu-id="ceb9d-130">**Widening.**</span></span> <span data-ttu-id="ceb9d-131">Tous les types de données et tous les types référence s’étendent à la `Object` type de données.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-131">All data types and all reference types widen to the `Object` data type.</span></span> <span data-ttu-id="ceb9d-132">Cela signifie que vous pouvez convertir n’importe quel type à `Object` sans rencontrer un <xref:System.OverflowException?displayProperty=nameWithType> erreur.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-132">This means you can convert any type to `Object` without encountering a <xref:System.OverflowException?displayProperty=nameWithType> error.</span></span>  
  
     <span data-ttu-id="ceb9d-133">Toutefois, si vous convertissez des types valeur et `Object`, Visual Basic effectue des opérations appelées *boxing* et *unboxing*, qui vous ralentissent l’exécution.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-133">However, if you convert between value types and `Object`, Visual Basic performs operations called *boxing* and *unboxing*, which make execution slower.</span></span>  
  
-   <span data-ttu-id="ceb9d-134">**Caractères de type.**</span><span class="sxs-lookup"><span data-stu-id="ceb9d-134">**Type Characters.**</span></span> <span data-ttu-id="ceb9d-135">`Object` n’a aucun caractère de type littéral ou un caractère de type identificateur.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-135">`Object` has no literal type character or identifier type character.</span></span>  
  
-   <span data-ttu-id="ceb9d-136">**Type de Framework.**</span><span class="sxs-lookup"><span data-stu-id="ceb9d-136">**Framework Type.**</span></span> <span data-ttu-id="ceb9d-137">Le type correspondant dans le .NET Framework est la <xref:System.Object?displayProperty=nameWithType> classe.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-137">The corresponding type in the .NET Framework is the <xref:System.Object?displayProperty=nameWithType> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ceb9d-138">Exemple</span><span class="sxs-lookup"><span data-stu-id="ceb9d-138">Example</span></span>  
 <span data-ttu-id="ceb9d-139">L’exemple suivant illustre une `Object` variable qui pointe vers une instance d’objet.</span><span class="sxs-lookup"><span data-stu-id="ceb9d-139">The following example illustrates an `Object` variable pointing to an object instance.</span></span>  
  
```  
Dim objDb As Object  
Dim myCollection As New Collection()  
' Suppose myCollection has now been populated.  
objDb = myCollection.Item(1)  
```  
  
## <a name="see-also"></a><span data-ttu-id="ceb9d-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ceb9d-140">See also</span></span>
- <xref:System.Object>
- [<span data-ttu-id="ceb9d-141">Types de données</span><span class="sxs-lookup"><span data-stu-id="ceb9d-141">Data Types</span></span>](../../../visual-basic/language-reference/data-types/index.md)
- [<span data-ttu-id="ceb9d-142">Fonctions de conversion de types</span><span class="sxs-lookup"><span data-stu-id="ceb9d-142">Type Conversion Functions</span></span>](../../../visual-basic/language-reference/functions/type-conversion-functions.md)
- [<span data-ttu-id="ceb9d-143">Liste des conversions</span><span class="sxs-lookup"><span data-stu-id="ceb9d-143">Conversion Summary</span></span>](../../../visual-basic/language-reference/keywords/conversion-summary.md)
- [<span data-ttu-id="ceb9d-144">Utilisation efficace des types de données</span><span class="sxs-lookup"><span data-stu-id="ceb9d-144">Efficient Use of Data Types</span></span>](../../../visual-basic/programming-guide/language-features/data-types/efficient-use-of-data-types.md)
- [<span data-ttu-id="ceb9d-145">Guide pratique pour Déterminer si deux objets sont liés</span><span class="sxs-lookup"><span data-stu-id="ceb9d-145">How to: Determine Whether Two Objects Are Related</span></span>](../../../visual-basic/programming-guide/language-features/variables/how-to-determine-whether-two-objects-are-related.md)
- [<span data-ttu-id="ceb9d-146">Guide pratique pour Déterminer si deux objets sont identiques</span><span class="sxs-lookup"><span data-stu-id="ceb9d-146">How to: Determine Whether Two Objects Are Identical</span></span>](../../../visual-basic/programming-guide/language-features/variables/how-to-determine-whether-two-objects-are-identical.md)
