---
title: Opérateurs de conversion - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- C# language, conversion operators
- conversion operators [C#]
- operators [C#], conversion
- user-defined conversions [C#]
ms.assetid: c5ad73a3-d57b-4d2b-b4c9-24e3c2856efc
ms.openlocfilehash: 43e81a342377b155fafe26bd0430384cddad5fd4
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64608228"
---
# <a name="conversion-operators-c-programming-guide"></a><span data-ttu-id="456c5-102">Opérateurs de conversion (guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="456c5-102">Conversion operators (C# Programming Guide)</span></span>

<span data-ttu-id="456c5-103">C# permet aux programmeurs de déclarer des conversions sur des classes ou structs afin d’autoriser les conversions dans les deux sens entre ces derniers et d’autres classes ou structs, ou des types de base.</span><span class="sxs-lookup"><span data-stu-id="456c5-103">C# enables programmers to declare conversions on classes or structs so that classes or structs can be converted to and/or from other classes or structs, or basic types.</span></span> <span data-ttu-id="456c5-104">Les conversions sont définies comme des opérateurs et nommées en fonction du type vers lequel s’effectue l’opération.</span><span class="sxs-lookup"><span data-stu-id="456c5-104">Conversions are defined like operators and are named for the type to which they convert.</span></span> <span data-ttu-id="456c5-105">Soit le type de l’argument à convertir, soit le type du résultat de la conversion, mais pas les deux, doit être le type conteneur.</span><span class="sxs-lookup"><span data-stu-id="456c5-105">Either the type of the argument to be converted, or the type of the result of the conversion, but not both, must be the containing type.</span></span>  
  
 [!code-csharp[csProgGuideStatements#10](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideStatements/CS/Statements.cs#10)]  
  
## <a name="conversion-operators-overview"></a><span data-ttu-id="456c5-106">Vue d’ensemble des opérateurs de conversion</span><span class="sxs-lookup"><span data-stu-id="456c5-106">Conversion operators overview</span></span>

 <span data-ttu-id="456c5-107">Les opérateurs de conversion ont les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="456c5-107">Conversion operators have the following properties:</span></span>  
  
- <span data-ttu-id="456c5-108">Les conversions déclarées comme `implicit` se produisent automatiquement selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="456c5-108">Conversions declared as `implicit` occur automatically when it is required.</span></span>  
  
- <span data-ttu-id="456c5-109">Les conversions déclarées comme `explicit` nécessitent qu’un cast soit appelé.</span><span class="sxs-lookup"><span data-stu-id="456c5-109">Conversions declared as `explicit` require a cast to be called.</span></span>  
  
- <span data-ttu-id="456c5-110">Toutes les conversions doivent être déclarées comme `static`.</span><span class="sxs-lookup"><span data-stu-id="456c5-110">All conversions must be declared as `static`.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="456c5-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="456c5-111">Related sections</span></span>

 <span data-ttu-id="456c5-112">Pour plus d'informations :</span><span class="sxs-lookup"><span data-stu-id="456c5-112">For more information:</span></span>  
  
- [<span data-ttu-id="456c5-113">Utilisation d’opérateurs de conversion</span><span class="sxs-lookup"><span data-stu-id="456c5-113">Using Conversion Operators</span></span>](../../../csharp/programming-guide/statements-expressions-operators/using-conversion-operators.md)  
  
- [<span data-ttu-id="456c5-114">Cast et conversions de types</span><span class="sxs-lookup"><span data-stu-id="456c5-114">Casting and Type Conversions</span></span>](../../../csharp/programming-guide/types/casting-and-type-conversions.md)  
  
- [<span data-ttu-id="456c5-115">Guide pratique pour implémenter des conversions définies par l’utilisateur entre des structs</span><span class="sxs-lookup"><span data-stu-id="456c5-115">How to: Implement User-Defined Conversions Between Structs</span></span>](../../../csharp/programming-guide/statements-expressions-operators/how-to-implement-user-defined-conversions-between-structs.md)  
  
- [<span data-ttu-id="456c5-116">explicit</span><span class="sxs-lookup"><span data-stu-id="456c5-116">explicit</span></span>](../../../csharp/language-reference/keywords/explicit.md)  
  
- [<span data-ttu-id="456c5-117">implicit</span><span class="sxs-lookup"><span data-stu-id="456c5-117">implicit</span></span>](../../../csharp/language-reference/keywords/implicit.md)  
  
- [<span data-ttu-id="456c5-118">static</span><span class="sxs-lookup"><span data-stu-id="456c5-118">static</span></span>](../../../csharp/language-reference/keywords/static.md)  
  
## <a name="see-also"></a><span data-ttu-id="456c5-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="456c5-119">See also</span></span>

- <xref:System.Convert>
- [<span data-ttu-id="456c5-120">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="456c5-120">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="456c5-121">Conversions explicites définies par l’utilisateur chaînées en C#</span><span class="sxs-lookup"><span data-stu-id="456c5-121">Chained user-defined explicit conversions in C#</span></span>](https://blogs.msdn.microsoft.com/ericlippert/2007/04/16/chained-user-defined-explicit-conversions-in-c/)
