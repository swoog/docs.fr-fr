---
title: "Comment : utiliser la surcharge d'opérateur pour créer une classe de nombres complexes (Guide de programmation C#)"
ms.date: 07/20/2015
helpviewer_keywords:
- complex numbers [C#]
- classes [C#], operator overloading
- operator overloading [C#], complex numbers
- operator overloading [C#], using to create classes
- operators [C#], overloading to create a complex number class
ms.assetid: c9b8d982-5112-413f-bae3-b42ae3248ddf
ms.openlocfilehash: d746355dac1b99690a5a94c829bd35598c6c8be8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33328862"
---
# <a name="how-to-use-operator-overloading-to-create-a-complex-number-class-c-programming-guide"></a><span data-ttu-id="27d39-102">Comment : utiliser la surcharge d'opérateur pour créer une classe de nombres complexes (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="27d39-102">How to: Use Operator Overloading to Create a Complex Number Class (C# Programming Guide)</span></span>
<span data-ttu-id="27d39-103">Cet exemple montre comment utiliser la surcharge d’opérateur pour créer une classe de nombres complexes `Complex` qui définit une addition complexe.</span><span class="sxs-lookup"><span data-stu-id="27d39-103">This example shows how you can use operator overloading to create a complex number class `Complex` that defines complex addition.</span></span> <span data-ttu-id="27d39-104">Le programme affiche les parties imaginaire et réelle des nombres et le résultat de l’addition en utilisant un remplacement de la méthode `ToString`.</span><span class="sxs-lookup"><span data-stu-id="27d39-104">The program displays the imaginary and the real parts of the numbers and the addition result using an override of the `ToString` method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="27d39-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="27d39-105">Example</span></span>  
 [!code-csharp[csProgGuideStatements#16](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-use-operator-overloading-to-create-a-complex-number-class_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="27d39-106">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27d39-106">See Also</span></span>  
 [<span data-ttu-id="27d39-107">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="27d39-107">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="27d39-108">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="27d39-108">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
 [<span data-ttu-id="27d39-109">operator (référence C#)</span><span class="sxs-lookup"><span data-stu-id="27d39-109">operator (C# Reference)</span></span>](../../../csharp/language-reference/keywords/operator.md)  
 <span data-ttu-id="27d39-110">Article [Why are overloaded operators always static in C#?](https://blogs.msdn.microsoft.com/ericlippert/2007/05/14/why-are-overloaded-operators-always-static-in-c/)</span><span class="sxs-lookup"><span data-stu-id="27d39-110">[Why are overloaded operators always static in C#?](https://blogs.msdn.microsoft.com/ericlippert/2007/05/14/why-are-overloaded-operators-always-static-in-c/)</span></span>
