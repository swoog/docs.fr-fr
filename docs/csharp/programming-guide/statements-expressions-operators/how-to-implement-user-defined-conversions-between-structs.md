---
title: "Procédure : Implémenter des conversions définies par l'utilisateur entre des structs - Guide de programmation C#"
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- user-defined conversions [C#]
ms.assetid: 97839aef-8fbc-40d5-9769-6b569bc2710b
ms.openlocfilehash: f33d8791791543704c8a49a44167b94c0f0c86b8
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64608172"
---
# <a name="how-to-implement-user-defined-conversions-between-structs-c-programming-guide"></a><span data-ttu-id="99c90-102">Procédure : Implémenter des conversions définies par l'utilisateur entre des structs (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="99c90-102">How to: Implement User-Defined Conversions Between Structs (C# Programming Guide)</span></span>
<span data-ttu-id="99c90-103">L’exemple suivant définit deux structs, `RomanNumeral` et `BinaryNumeral`, et décrit les conversions entre ces deux structs.</span><span class="sxs-lookup"><span data-stu-id="99c90-103">This example defines two structs, `RomanNumeral` and `BinaryNumeral`, and demonstrates conversions between them.</span></span>  
  
## <a name="example"></a><span data-ttu-id="99c90-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="99c90-104">Example</span></span>  
 [!code-csharp[csProgGuideStatements#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideStatements/CS/Statements.cs#13)]  
  
## <a name="robust-programming"></a><span data-ttu-id="99c90-105">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="99c90-105">Robust Programming</span></span>  
  
- <span data-ttu-id="99c90-106">Dans l’exemple précédent, l’instruction :</span><span class="sxs-lookup"><span data-stu-id="99c90-106">In the previous example, the statement:</span></span>  
  
     [!code-csharp[csProgGuideStatements#14](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideStatements/CS/Statements.cs#14)]  
  
     <span data-ttu-id="99c90-107">convertit un `RomanNumeral` en `BinaryNumeral`.</span><span class="sxs-lookup"><span data-stu-id="99c90-107">performs a conversion from a `RomanNumeral` to a `BinaryNumeral`.</span></span> <span data-ttu-id="99c90-108">Étant donné qu’il n’existe pas de conversion directe de `RomanNumeral` en `BinaryNumeral`, un cast est utilisé pour convertir un `RomanNumeral` en un `int`, et un autre cast est utilisé pour convertir un `int` en un `BinaryNumeral`.</span><span class="sxs-lookup"><span data-stu-id="99c90-108">Because there is no direct conversion from `RomanNumeral` to `BinaryNumeral`, a cast is used to convert from a `RomanNumeral` to an `int`, and another cast to convert from an `int` to a `BinaryNumeral`.</span></span>  
  
- <span data-ttu-id="99c90-109">L’instruction</span><span class="sxs-lookup"><span data-stu-id="99c90-109">Also the statement</span></span>  
  
     [!code-csharp[csProgGuideStatements#15](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideStatements/CS/Statements.cs#15)]  
  
     <span data-ttu-id="99c90-110">convertit un `BinaryNumeral` en `RomanNumeral`.</span><span class="sxs-lookup"><span data-stu-id="99c90-110">performs a conversion from a `BinaryNumeral` to a `RomanNumeral`.</span></span> <span data-ttu-id="99c90-111">Étant donné que `RomanNumeral` définit une conversion implicite d’un `BinaryNumeral`, aucun cast n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="99c90-111">Because `RomanNumeral` defines an implicit conversion from `BinaryNumeral`, no cast is required.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="99c90-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99c90-112">See also</span></span>

- [<span data-ttu-id="99c90-113">Référence C#</span><span class="sxs-lookup"><span data-stu-id="99c90-113">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="99c90-114">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="99c90-114">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="99c90-115">Opérateurs de conversion</span><span class="sxs-lookup"><span data-stu-id="99c90-115">Conversion Operators</span></span>](../../../csharp/programming-guide/statements-expressions-operators/conversion-operators.md)
