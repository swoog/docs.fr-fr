---
title: volatile (référence C#)
ms.date: 07/20/2015
f1_keywords:
- volatile_CSharpKeyword
- volatile
helpviewer_keywords:
- volatile keyword [C#]
ms.assetid: 78089bc7-7b38-4cfd-9e49-87ac036af009
ms.openlocfilehash: be7e081b18702710c00b5b86a9bc152800f0cf3d
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43526217"
---
# <a name="volatile-c-reference"></a><span data-ttu-id="d65f8-102">volatile (référence C#)</span><span class="sxs-lookup"><span data-stu-id="d65f8-102">volatile (C# Reference)</span></span>
<span data-ttu-id="d65f8-103">Le mot clé `volatile` indique qu’un champ peut être modifié par plusieurs threads qui s’exécutent simultanément.</span><span class="sxs-lookup"><span data-stu-id="d65f8-103">The `volatile` keyword indicates that a field might be modified by multiple threads that are executing at the same time.</span></span> <span data-ttu-id="d65f8-104">Les champs qui sont déclarés `volatile` ne sont pas soumis aux optimisations du compilateur qui supposent l’accès par un seul thread.</span><span class="sxs-lookup"><span data-stu-id="d65f8-104">Fields that are declared `volatile` are not subject to compiler optimizations that assume access by a single thread.</span></span> <span data-ttu-id="d65f8-105">Ces restrictions garantissent que tous les threads observent les écritures volatiles effectuées par un autre thread dans l’ordre dans lequel elles ont été effectuées.</span><span class="sxs-lookup"><span data-stu-id="d65f8-105">These restrictions ensure that all threads will observe volatile writes performed by any other thread in the order in which they were performed.</span></span> <span data-ttu-id="d65f8-106">Rien ne garantit que les écritures volatiles présentent un ordre total unique, tel que le voient tous les threads d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d65f8-106">There is no guarantee of a single total ordering of volatile writes as seen from all threads of execution.</span></span>  
  
 <span data-ttu-id="d65f8-107">Le modificateur `volatile` est généralement utilisé pour un champ auquel accèdent plusieurs threads sans utiliser l’instruction [lock](../../../csharp/language-reference/keywords/lock-statement.md) pour sérialiser l’accès.</span><span class="sxs-lookup"><span data-stu-id="d65f8-107">The `volatile` modifier is usually used for a field that is accessed by multiple threads without using the [lock](../../../csharp/language-reference/keywords/lock-statement.md) statement to serialize access.</span></span>  
  
 <span data-ttu-id="d65f8-108">Le mot clé `volatile` peut être appliqué aux champs des types suivants :</span><span class="sxs-lookup"><span data-stu-id="d65f8-108">The `volatile` keyword can be applied to fields of these types:</span></span>  
  
-   <span data-ttu-id="d65f8-109">Types référence.</span><span class="sxs-lookup"><span data-stu-id="d65f8-109">Reference types.</span></span>  
  
-   <span data-ttu-id="d65f8-110">Types pointeur (dans un contexte unsafe).</span><span class="sxs-lookup"><span data-stu-id="d65f8-110">Pointer types (in an unsafe context).</span></span> <span data-ttu-id="d65f8-111">Notez que, même si le pointeur lui-même peut être volatile, l’objet sur lequel il pointe ne le peut pas.</span><span class="sxs-lookup"><span data-stu-id="d65f8-111">Note that although the pointer itself can be volatile, the object that it points to cannot.</span></span> <span data-ttu-id="d65f8-112">En d’autres termes, vous ne pouvez pas déclarer un pointeur vers un objet volatile.</span><span class="sxs-lookup"><span data-stu-id="d65f8-112">In other words, you cannot declare a "pointer to volatile."</span></span>  
  
-   <span data-ttu-id="d65f8-113">Types tels que sbyte, byte, short, ushort, int, uint, char, float et bool.</span><span class="sxs-lookup"><span data-stu-id="d65f8-113">Types such as sbyte, byte, short, ushort, int, uint, char, float, and bool.</span></span>  
  
-   <span data-ttu-id="d65f8-114">Type enum avec l’un des types de base suivants : byte, sbyte, short, ushort, int ou uint.</span><span class="sxs-lookup"><span data-stu-id="d65f8-114">An enum type with one of the following base types: byte, sbyte, short, ushort, int, or uint.</span></span>  
  
-   <span data-ttu-id="d65f8-115">Paramètres de type générique connus comme des types référence.</span><span class="sxs-lookup"><span data-stu-id="d65f8-115">Generic type parameters known to be reference types.</span></span>  
  
-   <span data-ttu-id="d65f8-116">Voir <xref:System.IntPtr> et <xref:System.UIntPtr>.</span><span class="sxs-lookup"><span data-stu-id="d65f8-116"><xref:System.IntPtr> and <xref:System.UIntPtr>.</span></span>  
  
 <span data-ttu-id="d65f8-117">Le mot clé volatile ne peut s’appliquer qu’aux champs d’une classe ou d’une structure.</span><span class="sxs-lookup"><span data-stu-id="d65f8-117">The volatile keyword can only be applied to fields of a class or struct.</span></span> <span data-ttu-id="d65f8-118">Les variables locales ne peuvent pas être déclarées `volatile`.</span><span class="sxs-lookup"><span data-stu-id="d65f8-118">Local variables cannot be declared `volatile`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d65f8-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="d65f8-119">Example</span></span>  
 <span data-ttu-id="d65f8-120">L’exemple ci-dessous montre comment déclarer une variable de champ public comme `volatile`.</span><span class="sxs-lookup"><span data-stu-id="d65f8-120">The following example shows how to declare a public field variable as `volatile`.</span></span>  
  
 [!code-csharp[csrefKeywordsModifiers#24](../../../csharp/language-reference/keywords/codesnippet/CSharp/volatile_1.cs)]  
  
## <a name="example"></a><span data-ttu-id="d65f8-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="d65f8-121">Example</span></span>  
 <span data-ttu-id="d65f8-122">L’exemple suivant montre comment il est possible de créer un thread auxiliaire ou de travail et de l’utiliser pour effectuer le traitement en parallèle avec le thread principal.</span><span class="sxs-lookup"><span data-stu-id="d65f8-122">The following example demonstrates how an auxiliary or worker thread can be created and used to perform processing in parallel with that of the primary thread.</span></span> <span data-ttu-id="d65f8-123">Pour obtenir des informations générales sur le multithreading, consultez [Threading managé](../../../standard/threading/index.md) et [Threading (C#)](../../programming-guide/concepts/threading/index.md).</span><span class="sxs-lookup"><span data-stu-id="d65f8-123">For background information about multithreading, see [Managed Threading](../../../standard/threading/index.md) and [Threading (C#)](../../programming-guide/concepts/threading/index.md).</span></span>  
  
 [!code-csharp[csProgGuideThreading#1](../../../csharp/language-reference/keywords/codesnippet/CSharp/volatile_2.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="d65f8-124">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="d65f8-124">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="d65f8-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d65f8-125">See Also</span></span>

- [<span data-ttu-id="d65f8-126">Référence C#</span><span class="sxs-lookup"><span data-stu-id="d65f8-126">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="d65f8-127">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="d65f8-127">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="d65f8-128">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="d65f8-128">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="d65f8-129">Modificateurs</span><span class="sxs-lookup"><span data-stu-id="d65f8-129">Modifiers</span></span>](../../../csharp/language-reference/keywords/modifiers.md)
