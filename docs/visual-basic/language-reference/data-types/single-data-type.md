---
title: Single, type de données (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Single
helpviewer_keywords:
- Single data type
- F literal type character [Visual Basic]
- trailing zeros
- real numbers
- literal type characters [Visual Basic], F
- trailing 0 characters [Visual Basic]
- identifier type characters [Visual Basic], !
- single-precision numbers
- '! identifier type character'
- 0 characters [Visual Basic], trailing
- data types [Visual Basic], assigning
- floating-point numbers [Visual Basic], Single data type
- numbers [Visual Basic], real
- zeros, trailing
- numbers [Visual Basic], floating point
ms.assetid: 224a2795-4cd5-496c-8f7a-a4f05a06d45d
ms.openlocfilehash: b90fdb562f9d65858ac477321a18067cc6e621a2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61971702"
---
# <a name="single-data-type-visual-basic"></a><span data-ttu-id="04c16-102">Single, type de données (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="04c16-102">Single Data Type (Visual Basic)</span></span>
<span data-ttu-id="04c16-103">Contient des nombres à virgule flottante IEEE 32 bits (4 octets) simple précision compris entre - 3,4028235E + 38 signés et - 1, 401298E-45 pour les valeurs négatives et entre 1, 401298E-45 et 3,4028235E + 38 pour les valeurs positives.</span><span class="sxs-lookup"><span data-stu-id="04c16-103">Holds signed IEEE 32-bit (4-byte) single-precision floating-point numbers ranging in value from -3.4028235E+38 through -1.401298E-45 for negative values and from 1.401298E-45 through 3.4028235E+38 for positive values.</span></span> <span data-ttu-id="04c16-104">Nombres en simple précision stockent une approximation d’un nombre réel.</span><span class="sxs-lookup"><span data-stu-id="04c16-104">Single-precision numbers store an approximation of a real number.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="04c16-105">Notes</span><span class="sxs-lookup"><span data-stu-id="04c16-105">Remarks</span></span>  
 <span data-ttu-id="04c16-106">Utilisez le `Single` type de données pour contenir des valeurs à virgule flottante qui ne nécessitent pas la largeur totale des données de `Double`.</span><span class="sxs-lookup"><span data-stu-id="04c16-106">Use the `Single` data type to contain floating-point values that do not require the full data width of `Double`.</span></span> <span data-ttu-id="04c16-107">Dans certains cas, le common language runtime peut être en mesure de compresser vos `Single` variables étroitement ensemble et d’enregistrer la consommation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="04c16-107">In some cases the common language runtime might be able to pack your `Single` variables closely together and save memory consumption.</span></span>  
  
 <span data-ttu-id="04c16-108">La valeur par défaut de `Single` est 0.</span><span class="sxs-lookup"><span data-stu-id="04c16-108">The default value of `Single` is 0.</span></span>  
  
## <a name="programming-tips"></a><span data-ttu-id="04c16-109">Conseils de programmation</span><span class="sxs-lookup"><span data-stu-id="04c16-109">Programming Tips</span></span>  
  
- <span data-ttu-id="04c16-110">**Précision.**</span><span class="sxs-lookup"><span data-stu-id="04c16-110">**Precision.**</span></span> <span data-ttu-id="04c16-111">Lorsque vous travaillez avec des nombres à virgule flottante, n’oubliez pas qu’ils n’ont pas toujours de représentation précise dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="04c16-111">When you work with floating-point numbers, keep in mind that they do not always have a precise representation in memory.</span></span> <span data-ttu-id="04c16-112">Cela peut entraîner des résultats inattendus à partir de certaines opérations, comme la comparaison de valeurs et les `Mod` opérateur.</span><span class="sxs-lookup"><span data-stu-id="04c16-112">This could lead to unexpected results from certain operations, such as value comparison and the `Mod` operator.</span></span> <span data-ttu-id="04c16-113">Pour plus d’informations, consultez [dépannage des Types de données](../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="04c16-113">For more information, see [Troubleshooting Data Types](../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md).</span></span>  
  
- <span data-ttu-id="04c16-114">**Étendues.**</span><span class="sxs-lookup"><span data-stu-id="04c16-114">**Widening.**</span></span> <span data-ttu-id="04c16-115">Le `Single` type de données s’étend à `Double`.</span><span class="sxs-lookup"><span data-stu-id="04c16-115">The `Single` data type widens to `Double`.</span></span> <span data-ttu-id="04c16-116">Cela signifie que vous pouvez convertir `Single` à `Double` sans rencontrer un <xref:System.OverflowException?displayProperty=nameWithType> erreur.</span><span class="sxs-lookup"><span data-stu-id="04c16-116">This means you can convert `Single` to `Double` without encountering a <xref:System.OverflowException?displayProperty=nameWithType> error.</span></span>  
  
- <span data-ttu-id="04c16-117">**Les zéros de fin.**</span><span class="sxs-lookup"><span data-stu-id="04c16-117">**Trailing Zeros.**</span></span> <span data-ttu-id="04c16-118">Les types de données à virgule flottante n’ont pas d’aucune représentation interne du 0 de fin.</span><span class="sxs-lookup"><span data-stu-id="04c16-118">The floating-point data types do not have any internal representation of trailing 0 characters.</span></span> <span data-ttu-id="04c16-119">Par exemple, ils n'effectuent pas de distinction entre 4,2000 et 4.2.</span><span class="sxs-lookup"><span data-stu-id="04c16-119">For example, they do not distinguish between 4.2000 and 4.2.</span></span> <span data-ttu-id="04c16-120">Par conséquent, les caractères 0 de fin n’apparaissent pas lorsque vous affichez ou imprimez les valeurs à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="04c16-120">Consequently, trailing 0 characters do not appear when you display or print floating-point values.</span></span>  
  
- <span data-ttu-id="04c16-121">**Caractères de type.**</span><span class="sxs-lookup"><span data-stu-id="04c16-121">**Type Characters.**</span></span> <span data-ttu-id="04c16-122">L'ajout du caractère de type littéral `F` à un littéral force ce dernier en type de données `Single`.</span><span class="sxs-lookup"><span data-stu-id="04c16-122">Appending the literal type character `F` to a literal forces it to the `Single` data type.</span></span> <span data-ttu-id="04c16-123">L'ajout du caractère de type identificateur `!` à un identificateur force ce dernier en type `Single`.</span><span class="sxs-lookup"><span data-stu-id="04c16-123">Appending the identifier type character `!` to any identifier forces it to `Single`.</span></span>  
  
- <span data-ttu-id="04c16-124">**Type de Framework.**</span><span class="sxs-lookup"><span data-stu-id="04c16-124">**Framework Type.**</span></span> <span data-ttu-id="04c16-125">Le type correspondant dans le .NET Framework est la structure <xref:System.Single?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="04c16-125">The corresponding type in the .NET Framework is the <xref:System.Single?displayProperty=nameWithType> structure.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="04c16-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04c16-126">See also</span></span>

- <xref:System.Single?displayProperty=nameWithType>
- [<span data-ttu-id="04c16-127">Types de données</span><span class="sxs-lookup"><span data-stu-id="04c16-127">Data Types</span></span>](../../../visual-basic/language-reference/data-types/index.md)
- [<span data-ttu-id="04c16-128">Decimal (type de données)</span><span class="sxs-lookup"><span data-stu-id="04c16-128">Decimal Data Type</span></span>](../../../visual-basic/language-reference/data-types/decimal-data-type.md)
- [<span data-ttu-id="04c16-129">Double (type de données)</span><span class="sxs-lookup"><span data-stu-id="04c16-129">Double Data Type</span></span>](../../../visual-basic/language-reference/data-types/double-data-type.md)
- [<span data-ttu-id="04c16-130">Fonctions de conversion de types</span><span class="sxs-lookup"><span data-stu-id="04c16-130">Type Conversion Functions</span></span>](../../../visual-basic/language-reference/functions/type-conversion-functions.md)
- [<span data-ttu-id="04c16-131">Liste des conversions</span><span class="sxs-lookup"><span data-stu-id="04c16-131">Conversion Summary</span></span>](../../../visual-basic/language-reference/keywords/conversion-summary.md)
- [<span data-ttu-id="04c16-132">Utilisation efficace des types de données</span><span class="sxs-lookup"><span data-stu-id="04c16-132">Efficient Use of Data Types</span></span>](../../../visual-basic/programming-guide/language-features/data-types/efficient-use-of-data-types.md)
- [<span data-ttu-id="04c16-133">Dépannage des types de données</span><span class="sxs-lookup"><span data-stu-id="04c16-133">Troubleshooting Data Types</span></span>](../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md)
