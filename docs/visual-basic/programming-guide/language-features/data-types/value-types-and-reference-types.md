---
title: Types valeur et types référence
ms.date: 07/20/2015
helpviewer_keywords:
- reference data types [Visual Basic]
- reference types [Visual Basic]
- value types [Visual Basic]
- value data types [Visual Basic]
- types [Visual Basic]
- data types [Visual Basic], value types
- data types [Visual Basic], reference types
ms.assetid: fc82ce15-5a40-4c5c-a1e1-a556830e7391
ms.openlocfilehash: 9456316f71a213905bcb50336533c4e618f5174a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33651581"
---
# <a name="value-types-and-reference-types"></a><span data-ttu-id="ac561-102">Types valeur et types référence</span><span class="sxs-lookup"><span data-stu-id="ac561-102">Value Types and Reference Types</span></span>
<span data-ttu-id="ac561-103">En Visual Basic, les types de données sont implémentés en fonction de leur classification.</span><span class="sxs-lookup"><span data-stu-id="ac561-103">In Visual Basic, data types are implemented based on their classification.</span></span> <span data-ttu-id="ac561-104">Les types de données Visual Basic peuvent être classées en fonction du fait qu’une variable d’un type particulier enregistre ses propres données ou un pointeur vers les données.</span><span class="sxs-lookup"><span data-stu-id="ac561-104">The Visual Basic data types can be classified according to whether a variable of a particular type stores its own data or a pointer to the data.</span></span> <span data-ttu-id="ac561-105">Si elle enregistre ses propres données, il est un *type valeur*; si elle contient un pointeur vers les données ailleurs dans la mémoire, il s’agit d’un *type référence*.</span><span class="sxs-lookup"><span data-stu-id="ac561-105">If it stores its own data it is a *value type*; if it holds a pointer to data elsewhere in memory it is a *reference type*.</span></span>  
  
## <a name="value-types"></a><span data-ttu-id="ac561-106">Types valeur</span><span class="sxs-lookup"><span data-stu-id="ac561-106">Value Types</span></span>  
 <span data-ttu-id="ac561-107">Un type de données est un *type valeur* s’il conserve des données au sein de sa propre allocation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="ac561-107">A data type is a *value type* if it holds the data within its own memory allocation.</span></span> <span data-ttu-id="ac561-108">Types valeur sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ac561-108">Value types include the following:</span></span>  
  
-   <span data-ttu-id="ac561-109">Tous les types de données numériques</span><span class="sxs-lookup"><span data-stu-id="ac561-109">All numeric data types</span></span>  
  
-   <span data-ttu-id="ac561-110">`Boolean`, `Char` et `Date`</span><span class="sxs-lookup"><span data-stu-id="ac561-110">`Boolean`, `Char`, and `Date`</span></span>  
  
-   <span data-ttu-id="ac561-111">Toutes les structures, même si leurs membres sont des types référence</span><span class="sxs-lookup"><span data-stu-id="ac561-111">All structures, even if their members are reference types</span></span>  
  
-   <span data-ttu-id="ac561-112">Énumérations, car leur type sous-jacent est toujours `SByte`, `Short`, `Integer`, `Long`, `Byte`, `UShort`, `UInteger`, ou `ULong`</span><span class="sxs-lookup"><span data-stu-id="ac561-112">Enumerations, since their underlying type is always `SByte`, `Short`, `Integer`, `Long`, `Byte`, `UShort`, `UInteger`, or `ULong`</span></span>  
  
 <span data-ttu-id="ac561-113">Chaque structure est un type valeur, même s’il contient des membres de type référence.</span><span class="sxs-lookup"><span data-stu-id="ac561-113">Every structure is a value type, even if it contains reference type members.</span></span> <span data-ttu-id="ac561-114">Pour cette raison, types valeur tels que `Char` et `Integer` sont implémentés par les structures du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ac561-114">For this reason, value types such as `Char` and `Integer` are implemented by .NET Framework structures.</span></span>  
  
 <span data-ttu-id="ac561-115">Vous pouvez déclarer un type valeur à l’aide du mot clé réservé, par exemple, `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="ac561-115">You can declare a value type by using the reserved keyword, for example, `Decimal`.</span></span> <span data-ttu-id="ac561-116">Vous pouvez également utiliser le `New` mot clé à initialiser un type valeur.</span><span class="sxs-lookup"><span data-stu-id="ac561-116">You can also use the `New` keyword to initialize a value type.</span></span> <span data-ttu-id="ac561-117">Cela est particulièrement utile si le type possède un constructeur qui accepte des paramètres.</span><span class="sxs-lookup"><span data-stu-id="ac561-117">This is especially useful if the type has a constructor that takes parameters.</span></span> <span data-ttu-id="ac561-118">Est un exemple de ce le <xref:System.Decimal.%23ctor%28System.Int32%2CSystem.Int32%2CSystem.Int32%2CSystem.Boolean%2CSystem.Byte%29> constructeur, ce qui génère un nouveau `Decimal` valeur à partir des parties fournis.</span><span class="sxs-lookup"><span data-stu-id="ac561-118">An example of this is the <xref:System.Decimal.%23ctor%28System.Int32%2CSystem.Int32%2CSystem.Int32%2CSystem.Boolean%2CSystem.Byte%29> constructor, which builds a new `Decimal` value from the supplied parts.</span></span>  
  
## <a name="reference-types"></a><span data-ttu-id="ac561-119">Types référence</span><span class="sxs-lookup"><span data-stu-id="ac561-119">Reference Types</span></span>  
 <span data-ttu-id="ac561-120">A *type référence* contient un pointeur vers un autre emplacement de mémoire qui contient les données.</span><span class="sxs-lookup"><span data-stu-id="ac561-120">A *reference type* contains a pointer to another memory location that holds the data.</span></span> <span data-ttu-id="ac561-121">Types référence sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ac561-121">Reference types include the following:</span></span>  
  
-   `String`  
  
-   <span data-ttu-id="ac561-122">Tous les tableaux, même si leurs éléments sont des types valeur</span><span class="sxs-lookup"><span data-stu-id="ac561-122">All arrays, even if their elements are value types</span></span>  
  
-   <span data-ttu-id="ac561-123">Types de classe, tels que <xref:System.Windows.Forms.Form></span><span class="sxs-lookup"><span data-stu-id="ac561-123">Class types, such as <xref:System.Windows.Forms.Form></span></span>  
  
-   <span data-ttu-id="ac561-124">Délégués</span><span class="sxs-lookup"><span data-stu-id="ac561-124">Delegates</span></span>  
  
 <span data-ttu-id="ac561-125">Une classe est un *type référence*.</span><span class="sxs-lookup"><span data-stu-id="ac561-125">A class is a *reference type*.</span></span> <span data-ttu-id="ac561-126">Pour cette raison, les types référence comme `Object` et `String` sont pris en charge par [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] classes.</span><span class="sxs-lookup"><span data-stu-id="ac561-126">For this reason, reference types such as `Object` and `String` are supported by [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] classes.</span></span> <span data-ttu-id="ac561-127">Notez que chaque tableau est un type référence, même si ses membres sont des types valeur.</span><span class="sxs-lookup"><span data-stu-id="ac561-127">Note that every array is a reference type, even if its members are value types.</span></span>  
  
 <span data-ttu-id="ac561-128">Étant donné que chaque type référence représente une classe sous-jacente de .NET Framework, vous devez utiliser le [nouvel opérateur](../../../../visual-basic/language-reference/operators/new-operator.md) mot clé lorsque vous l’initialisez.</span><span class="sxs-lookup"><span data-stu-id="ac561-128">Since every reference type represents an underlying .NET Framework class, you must use the [New Operator](../../../../visual-basic/language-reference/operators/new-operator.md) keyword when you initialize it.</span></span> <span data-ttu-id="ac561-129">L’instruction suivante initialise un tableau.</span><span class="sxs-lookup"><span data-stu-id="ac561-129">The following statement initializes an array.</span></span>  
  
```  
Dim totals() As Single = New Single(8) {}  
```  
  
## <a name="elements-that-are-not-types"></a><span data-ttu-id="ac561-130">Éléments qui ne sont pas des Types</span><span class="sxs-lookup"><span data-stu-id="ac561-130">Elements That Are Not Types</span></span>  
 <span data-ttu-id="ac561-131">Les éléments de programmation suivants ne sont pas éligibles en tant que types, car vous ne pouvez pas spécifier un d'entre eux en tant que type de données pour un élément déclaré :</span><span class="sxs-lookup"><span data-stu-id="ac561-131">The following programming elements do not qualify as types, because you cannot specify any of them as a data type for a declared element:</span></span>  
  
-   <span data-ttu-id="ac561-132">Espaces de noms</span><span class="sxs-lookup"><span data-stu-id="ac561-132">Namespaces</span></span>  
  
-   <span data-ttu-id="ac561-133">Modules</span><span class="sxs-lookup"><span data-stu-id="ac561-133">Modules</span></span>  
  
-   <span data-ttu-id="ac561-134">Événements</span><span class="sxs-lookup"><span data-stu-id="ac561-134">Events</span></span>  
  
-   <span data-ttu-id="ac561-135">Propriétés et procédures</span><span class="sxs-lookup"><span data-stu-id="ac561-135">Properties and procedures</span></span>  
  
-   <span data-ttu-id="ac561-136">Variables, des constantes et des champs</span><span class="sxs-lookup"><span data-stu-id="ac561-136">Variables, constants, and fields</span></span>  
  
## <a name="working-with-the-object-data-type"></a><span data-ttu-id="ac561-137">Utilisation du Type de données objet</span><span class="sxs-lookup"><span data-stu-id="ac561-137">Working with the Object Data Type</span></span>  
 <span data-ttu-id="ac561-138">Vous pouvez affecter un type référence ou un type valeur à une variable de la `Object` type de données.</span><span class="sxs-lookup"><span data-stu-id="ac561-138">You can assign either a reference type or a value type to a variable of the `Object` data type.</span></span> <span data-ttu-id="ac561-139">Une `Object` variable conserve toujours un pointeur vers les données, jamais les données elles-mêmes.</span><span class="sxs-lookup"><span data-stu-id="ac561-139">An `Object` variable always holds a pointer to the data, never the data itself.</span></span> <span data-ttu-id="ac561-140">Toutefois, si vous assignez un type valeur à une `Object` variable, il se comporte comme si elle contenait ses propres données.</span><span class="sxs-lookup"><span data-stu-id="ac561-140">However, if you assign a value type to an `Object` variable, it behaves as if it holds its own data.</span></span> <span data-ttu-id="ac561-141">Pour plus d’informations, consultez [Type de données d’objet](../../../../visual-basic/language-reference/data-types/object-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="ac561-141">For more information, see [Object Data Type](../../../../visual-basic/language-reference/data-types/object-data-type.md).</span></span>  
  
 <span data-ttu-id="ac561-142">Vous pouvez déterminer si une `Object` variable agit comme un type référence ou un type valeur en la passant à la <xref:Microsoft.VisualBasic.Information.IsReference%2A> méthode dans le <xref:Microsoft.VisualBasic.Information> classe de la <xref:Microsoft.VisualBasic?displayProperty=nameWithType> espace de noms.</span><span class="sxs-lookup"><span data-stu-id="ac561-142">You can find out whether an `Object` variable is acting as a reference type or a value type by passing it to the <xref:Microsoft.VisualBasic.Information.IsReference%2A> method in the <xref:Microsoft.VisualBasic.Information> class of the <xref:Microsoft.VisualBasic?displayProperty=nameWithType> namespace.</span></span> <span data-ttu-id="ac561-143"><xref:Microsoft.VisualBasic.Information.IsReference%2A?displayProperty=nameWithType> Retourne `True` si le contenu de la `Object` variable représente un type référence.</span><span class="sxs-lookup"><span data-stu-id="ac561-143"><xref:Microsoft.VisualBasic.Information.IsReference%2A?displayProperty=nameWithType> returns `True` if the content of the `Object` variable represents a reference type.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ac561-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac561-144">See Also</span></span>  
 [<span data-ttu-id="ac561-145">Types valeur Nullable</span><span class="sxs-lookup"><span data-stu-id="ac561-145">Nullable Value Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)  
 [<span data-ttu-id="ac561-146">Conversions de type dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="ac561-146">Type Conversions in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/type-conversions.md)  
 [<span data-ttu-id="ac561-147">Structure (instruction)</span><span class="sxs-lookup"><span data-stu-id="ac561-147">Structure Statement</span></span>](../../../../visual-basic/language-reference/statements/structure-statement.md)  
 [<span data-ttu-id="ac561-148">Utilisation efficace des types de données</span><span class="sxs-lookup"><span data-stu-id="ac561-148">Efficient Use of Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/efficient-use-of-data-types.md)  
 [<span data-ttu-id="ac561-149">Object (type de données)</span><span class="sxs-lookup"><span data-stu-id="ac561-149">Object Data Type</span></span>](../../../../visual-basic/language-reference/data-types/object-data-type.md)  
 [<span data-ttu-id="ac561-150">Types de données</span><span class="sxs-lookup"><span data-stu-id="ac561-150">Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/index.md)
