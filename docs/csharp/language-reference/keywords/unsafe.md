---
title: unsafe (référence C#)
ms.date: 07/20/2015
f1_keywords:
- unsafe_CSharpKeyword
- unsafe
helpviewer_keywords:
- unsafe keyword [C#]
ms.assetid: 7e818009-1c6e-4b9e-b769-3728a01586a0
ms.openlocfilehash: c476bdcea4993b27c0e8f8148a985f18a43ba09b
ms.sourcegitcommit: 89c93d05c2281b4c834f48f6c8df1047e1410980
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2018
---
# <a name="unsafe-c-reference"></a><span data-ttu-id="a54be-102">unsafe (référence C#)</span><span class="sxs-lookup"><span data-stu-id="a54be-102">unsafe (C# Reference)</span></span>
<span data-ttu-id="a54be-103">Le mot clé `unsafe` désigne un contexte non sécurisé, qui est requis pour toute opération impliquant des pointeurs.</span><span class="sxs-lookup"><span data-stu-id="a54be-103">The `unsafe` keyword denotes an unsafe context, which is required for any operation involving pointers.</span></span> <span data-ttu-id="a54be-104">Pour plus d’informations, consultez l’article [Pointeurs et code unsafe](../../../csharp/programming-guide/unsafe-code-pointers/index.md).</span><span class="sxs-lookup"><span data-stu-id="a54be-104">For more information, see [Unsafe Code and Pointers](../../../csharp/programming-guide/unsafe-code-pointers/index.md).</span></span>  
  
 <span data-ttu-id="a54be-105">Vous pouvez utiliser le modificateur `unsafe` dans la déclaration d’un type ou d’un membre.</span><span class="sxs-lookup"><span data-stu-id="a54be-105">You can use the `unsafe` modifier in the declaration of a type or a member.</span></span> <span data-ttu-id="a54be-106">Toute l’étendue de texte du type ou du membre est ainsi considérée comme un contexte unsafe.</span><span class="sxs-lookup"><span data-stu-id="a54be-106">The entire textual extent of the type or member is therefore considered an unsafe context.</span></span> <span data-ttu-id="a54be-107">Par exemple, ce qui suit est une méthode déclarée avec le modificateur `unsafe` :</span><span class="sxs-lookup"><span data-stu-id="a54be-107">For example, the following is a method declared with the `unsafe` modifier:</span></span>  
  
```csharp  
      unsafe static void FastCopy(byte[] src, byte[] dst, int count)  
{  
    // Unsafe context: can use pointers here.  
}  
```  
  
 <span data-ttu-id="a54be-108">La portée du contexte unsafe s’étend de la liste de paramètres à la fin de la méthode, de sorte que les pointeurs peuvent également être utilisés dans la liste de paramètres :</span><span class="sxs-lookup"><span data-stu-id="a54be-108">The scope of the unsafe context extends from the parameter list to the end of the method, so pointers can also be used in the parameter list:</span></span>  
  
```csharp  
unsafe static void FastCopy ( byte* ps, byte* pd, int count ) {...}  
```  
  
 <span data-ttu-id="a54be-109">Vous pouvez également avoir recours à un bloc unsafe pour utiliser un code unsafe dans ce bloc.</span><span class="sxs-lookup"><span data-stu-id="a54be-109">You can also use an unsafe block to enable the use of an unsafe code inside this block.</span></span> <span data-ttu-id="a54be-110">Exemple :</span><span class="sxs-lookup"><span data-stu-id="a54be-110">For example:</span></span>  
  
```csharp  
      unsafe  
{  
    // Unsafe context: can use pointers here.  
}  
```  
  
 <span data-ttu-id="a54be-111">Pour compiler du code unsafe, vous devez spécifier l’option de compilateur [/unsafe](../../../csharp/language-reference/compiler-options/unsafe-compiler-option.md).</span><span class="sxs-lookup"><span data-stu-id="a54be-111">To compile unsafe code, you must specify the [/unsafe](../../../csharp/language-reference/compiler-options/unsafe-compiler-option.md) compiler option.</span></span> <span data-ttu-id="a54be-112">Le code unsafe n’est pas vérifiable par le service CLR (Common Language Runtime).</span><span class="sxs-lookup"><span data-stu-id="a54be-112">Unsafe code is not verifiable by the common language runtime.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a54be-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="a54be-113">Example</span></span>  
 [!code-csharp[csrefKeywordsModifiers#22](../../../csharp/language-reference/keywords/codesnippet/CSharp/unsafe_1.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="a54be-114">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="a54be-114">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="a54be-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a54be-115">See Also</span></span>  
 [<span data-ttu-id="a54be-116">Référence C#</span><span class="sxs-lookup"><span data-stu-id="a54be-116">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="a54be-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="a54be-117">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="a54be-118">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="a54be-118">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="a54be-119">fixed, instruction</span><span class="sxs-lookup"><span data-stu-id="a54be-119">fixed Statement</span></span>](../../../csharp/language-reference/keywords/fixed-statement.md)  
 [<span data-ttu-id="a54be-120">Pointeurs et code unsafe</span><span class="sxs-lookup"><span data-stu-id="a54be-120">Unsafe Code and Pointers</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/index.md)  
 [<span data-ttu-id="a54be-121">Mémoires tampons de taille fixe</span><span class="sxs-lookup"><span data-stu-id="a54be-121">Fixed Size Buffers</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/fixed-size-buffers.md)
