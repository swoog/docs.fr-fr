---
title: typeof (référence C#)
ms.date: 07/20/2015
f1_keywords:
- typeof
- typeof_CSharpKeyword
helpviewer_keywords:
- typeof keyword [C#]
ms.assetid: 0c08d880-515e-46bb-8cd2-48b8dd62c08d
ms.openlocfilehash: 2493e78fd0782eebee17afd979e1c429339d0a3f
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43486803"
---
# <a name="typeof-c-reference"></a><span data-ttu-id="e0fab-102">typeof (référence C#)</span><span class="sxs-lookup"><span data-stu-id="e0fab-102">typeof (C# Reference)</span></span>
<span data-ttu-id="e0fab-103">Permet d’obtenir l’objet `System.Type` pour un type.</span><span class="sxs-lookup"><span data-stu-id="e0fab-103">Used to obtain the `System.Type` object for a type.</span></span> <span data-ttu-id="e0fab-104">Une expression `typeof` prend la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="e0fab-104">A `typeof` expression takes the following form:</span></span>  
  
```csharp  
System.Type type = typeof(int);  
```  
  
## <a name="remarks"></a><span data-ttu-id="e0fab-105">Notes</span><span class="sxs-lookup"><span data-stu-id="e0fab-105">Remarks</span></span>  
 <span data-ttu-id="e0fab-106">Pour obtenir le type au moment de l’exécution d’une expression, vous pouvez utiliser la méthode <xref:System.Object.GetType%2A> du .NET Framework, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="e0fab-106">To obtain the run-time type of an expression, you can use the .NET Framework method <xref:System.Object.GetType%2A>, as in the following example:</span></span>  
  
```csharp  
int i = 0;  
System.Type type = i.GetType();  
```  
  
 <span data-ttu-id="e0fab-107">L’opérateur `typeof` ne peut pas être surchargé.</span><span class="sxs-lookup"><span data-stu-id="e0fab-107">The `typeof` operator cannot be overloaded.</span></span>  
  
 <span data-ttu-id="e0fab-108">L’opérateur `typeof` peut également être utilisé sur les types génériques ouverts.</span><span class="sxs-lookup"><span data-stu-id="e0fab-108">The `typeof` operator can also be used on open generic types.</span></span> <span data-ttu-id="e0fab-109">Les types avec plusieurs paramètres de type doivent avoir le nombre approprié de virgules dans la spécification.</span><span class="sxs-lookup"><span data-stu-id="e0fab-109">Types with more than one type parameter must have the appropriate number of commas in the specification.</span></span> <span data-ttu-id="e0fab-110">L’exemple suivant montre comment déterminer si le type de retour d’une méthode est un <xref:System.Collections.Generic.IEnumerable%601> générique.</span><span class="sxs-lookup"><span data-stu-id="e0fab-110">The following example shows how to determine whether the return type of a method is a generic <xref:System.Collections.Generic.IEnumerable%601>.</span></span> <span data-ttu-id="e0fab-111"><xref:System.Type.GetInterface%2A?displayProperty=nameWithType> retourne `null` si le type de retour n’est pas un type générique <xref:System.Collections.Generic.IEnumerable%601>.</span><span class="sxs-lookup"><span data-stu-id="e0fab-111"><xref:System.Type.GetInterface%2A?displayProperty=nameWithType> will return `null` if the return type is not an <xref:System.Collections.Generic.IEnumerable%601> generic type.</span></span>
  
 [!code-csharp[typeof_3.cs](~/samples/snippets/csharp/keywords/typeof/typeof_3.cs)]   
  
## <a name="example"></a><span data-ttu-id="e0fab-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="e0fab-112">Example</span></span>  
 [!code-csharp[csrefKeywordsOperator#12](../../../csharp/language-reference/keywords/codesnippet/CSharp/typeof_1.cs)]  
  
## <a name="example"></a><span data-ttu-id="e0fab-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="e0fab-113">Example</span></span>  
 <span data-ttu-id="e0fab-114">Cet exemple utilise la méthode <xref:System.Object.GetType%2A> pour déterminer le type utilisé pour contenir le résultat d’un calcul numérique.</span><span class="sxs-lookup"><span data-stu-id="e0fab-114">This sample uses the <xref:System.Object.GetType%2A> method to determine the type that is used to contain the result of a numeric calculation.</span></span> <span data-ttu-id="e0fab-115">Cela dépend des besoins de stockage du nombre résultant.</span><span class="sxs-lookup"><span data-stu-id="e0fab-115">This depends on the storage requirements of the resulting number.</span></span>  
  
 [!code-csharp[csrefKeywordsOperator#13](../../../csharp/language-reference/keywords/codesnippet/CSharp/typeof_2.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="e0fab-116">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="e0fab-116">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="e0fab-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0fab-117">See Also</span></span>

- <xref:System.Type?displayProperty=nameWithType>  
- [<span data-ttu-id="e0fab-118">Référence C#</span><span class="sxs-lookup"><span data-stu-id="e0fab-118">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="e0fab-119">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="e0fab-119">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="e0fab-120">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="e0fab-120">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="e0fab-121">is</span><span class="sxs-lookup"><span data-stu-id="e0fab-121">is</span></span>](../../../csharp/language-reference/keywords/is.md)  
- [<span data-ttu-id="e0fab-122">Mots clés des opérateurs</span><span class="sxs-lookup"><span data-stu-id="e0fab-122">Operator Keywords</span></span>](../../../csharp/language-reference/keywords/operator-keywords.md)
