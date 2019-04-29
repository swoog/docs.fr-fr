---
title: Booléen, type de données (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.FALSE
- vb.TRUE
- vb.Boolean
helpviewer_keywords:
- Boolean data type
- Boolean values [Visual Basic], False keyword
- False keyword [Visual Basic]
- True keyword [Visual Basic]
- Boolean values [Visual Basic], True keyword
ms.assetid: 4858e630-4813-4216-a55e-f4d0feb884e4
ms.openlocfilehash: 7b64302d801a08f976de0ec969983c821f7a8471
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61796992"
---
# <a name="boolean-data-type-visual-basic"></a><span data-ttu-id="9c8d2-102">Booléen, type de données (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="9c8d2-102">Boolean Data Type (Visual Basic)</span></span>
<span data-ttu-id="9c8d2-103">Contient les valeurs qui peuvent être uniquement `True` ou `False`.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-103">Holds values that can be only `True` or `False`.</span></span> <span data-ttu-id="9c8d2-104">Les mots clés `True` et `False` correspondent aux deux États de `Boolean` variables.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-104">The keywords `True` and `False` correspond to the two states of `Boolean` variables.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9c8d2-105">Notes</span><span class="sxs-lookup"><span data-stu-id="9c8d2-105">Remarks</span></span>  
 <span data-ttu-id="9c8d2-106">Utilisez le [Type de données booléen (Visual Basic)](../../../visual-basic/language-reference/data-types/boolean-data-type.md) destiné à contenir les valeurs de deux États tels que vrai/faux, Oui/Non, ou désactivez-les.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-106">Use the [Boolean Data Type (Visual Basic)](../../../visual-basic/language-reference/data-types/boolean-data-type.md) to contain two-state values such as true/false, yes/no, or on/off.</span></span>  
  
 <span data-ttu-id="9c8d2-107">La valeur par défaut de `Boolean` est `False`.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-107">The default value of `Boolean` is `False`.</span></span>  
  
 <span data-ttu-id="9c8d2-108">`Boolean` les valeurs ne sont pas stockées sous forme de nombres et les valeurs stockées ne sont pas destinées à être équivalentes aux nombres.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-108">`Boolean` values are not stored as numbers, and the stored values are not intended to be equivalent to numbers.</span></span> <span data-ttu-id="9c8d2-109">Vous devez jamais écrire du code qui s’appuie sur des valeurs numériques équivalentes pour `True` et `False`.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-109">You should never write code that relies on equivalent numeric values for `True` and `False`.</span></span> <span data-ttu-id="9c8d2-110">Si possible, vous devez limiter l’utilisation de `Boolean` variables aux valeurs logiques pour lesquelles elles sont conçues.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-110">Whenever possible, you should restrict usage of `Boolean` variables to the logical values for which they are designed.</span></span>  
  
## <a name="type-conversions"></a><span data-ttu-id="9c8d2-111">Conversions de type</span><span class="sxs-lookup"><span data-stu-id="9c8d2-111">Type Conversions</span></span>  
 <span data-ttu-id="9c8d2-112">Lorsque Visual Basic convertit les valeurs de type de données numériques à `Boolean`, 0 devient `False` et toutes les autres valeurs deviennent `True`.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-112">When Visual Basic converts numeric data type values to `Boolean`, 0 becomes `False` and all other values become `True`.</span></span> <span data-ttu-id="9c8d2-113">Lorsque Visual Basic convertit `Boolean` valeurs en types numériques, `False` devient 0 et `True` devient -1.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-113">When Visual Basic converts `Boolean` values to numeric types, `False` becomes 0 and `True` becomes -1.</span></span>  
  
 <span data-ttu-id="9c8d2-114">Lorsque vous effectuez une conversion entre `Boolean` valeurs et types de données numériques, n’oubliez pas que les méthodes de conversion de .NET Framework ne produisent pas toujours les mêmes résultats que les mots clés de conversion Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-114">When you convert between `Boolean` values and numeric data types, keep in mind that the .NET Framework conversion methods do not always produce the same results as the Visual Basic conversion keywords.</span></span> <span data-ttu-id="9c8d2-115">Il s’agit, car la conversion Visual Basic conserve un comportement compatible avec les versions précédentes.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-115">This is because the Visual Basic conversion retains behavior compatible with previous versions.</span></span> <span data-ttu-id="9c8d2-116">Pour plus d’informations, consultez « Le Type booléenne ne se convertit pas correctement en Type numérique » dans [dépannage des Types de données](../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="9c8d2-116">For more information, see "Boolean Type Does Not Convert to Numeric Type Accurately" in [Troubleshooting Data Types](../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md).</span></span>  
  
## <a name="programming-tips"></a><span data-ttu-id="9c8d2-117">Conseils de programmation</span><span class="sxs-lookup"><span data-stu-id="9c8d2-117">Programming Tips</span></span>  
  
- <span data-ttu-id="9c8d2-118">**Nombres négatifs.**</span><span class="sxs-lookup"><span data-stu-id="9c8d2-118">**Negative Numbers.**</span></span> <span data-ttu-id="9c8d2-119">`Boolean` n’est pas un type numérique et ne peut pas représenter une valeur négative.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-119">`Boolean` is not a numeric type and cannot represent a negative value.</span></span> <span data-ttu-id="9c8d2-120">Dans tous les cas, vous ne devez pas utiliser `Boolean` pour contenir des valeurs numériques.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-120">In any case, you should not use `Boolean` to hold numeric values.</span></span>  
  
- <span data-ttu-id="9c8d2-121">**Caractères de type.**</span><span class="sxs-lookup"><span data-stu-id="9c8d2-121">**Type Characters.**</span></span> <span data-ttu-id="9c8d2-122">`Boolean` n’a aucun caractère de type littéral ou un caractère de type identificateur.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-122">`Boolean` has no literal type character or identifier type character.</span></span>  
  
- <span data-ttu-id="9c8d2-123">**Type de Framework.**</span><span class="sxs-lookup"><span data-stu-id="9c8d2-123">**Framework Type.**</span></span> <span data-ttu-id="9c8d2-124">Le type correspondant dans le .NET Framework est la structure <xref:System.Boolean?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-124">The corresponding type in the .NET Framework is the <xref:System.Boolean?displayProperty=nameWithType> structure.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9c8d2-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="9c8d2-125">Example</span></span>  
 <span data-ttu-id="9c8d2-126">Dans l’exemple suivant, `runningVB` est un `Boolean` variable, qui enregistre une simple valeur yes/no.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-126">In the following example, `runningVB` is a `Boolean` variable, which stores a simple yes/no setting.</span></span>  
  
```  
Dim runningVB As Boolean  
' Check to see if program is running on Visual Basic engine.  
If scriptEngine = "VB" Then  
    runningVB = True  
End If  
```  
  
## <a name="see-also"></a><span data-ttu-id="9c8d2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c8d2-127">See also</span></span>

- <xref:System.Boolean?displayProperty=nameWithType>
- [<span data-ttu-id="9c8d2-128">Types de données</span><span class="sxs-lookup"><span data-stu-id="9c8d2-128">Data Types</span></span>](../../../visual-basic/language-reference/data-types/index.md)
- [<span data-ttu-id="9c8d2-129">Fonctions de conversion de types</span><span class="sxs-lookup"><span data-stu-id="9c8d2-129">Type Conversion Functions</span></span>](../../../visual-basic/language-reference/functions/type-conversion-functions.md)
- [<span data-ttu-id="9c8d2-130">Liste des conversions</span><span class="sxs-lookup"><span data-stu-id="9c8d2-130">Conversion Summary</span></span>](../../../visual-basic/language-reference/keywords/conversion-summary.md)
- [<span data-ttu-id="9c8d2-131">Utilisation efficace des types de données</span><span class="sxs-lookup"><span data-stu-id="9c8d2-131">Efficient Use of Data Types</span></span>](../../../visual-basic/programming-guide/language-features/data-types/efficient-use-of-data-types.md)
- [<span data-ttu-id="9c8d2-132">Dépannage des types de données</span><span class="sxs-lookup"><span data-stu-id="9c8d2-132">Troubleshooting Data Types</span></span>](../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md)
- [<span data-ttu-id="9c8d2-133">CType (fonction)</span><span class="sxs-lookup"><span data-stu-id="9c8d2-133">CType Function</span></span>](../../../visual-basic/language-reference/functions/ctype-function.md)
