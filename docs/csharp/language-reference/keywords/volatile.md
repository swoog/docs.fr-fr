---
title: volatile (référence C#)
ms.date: 07/20/2015
f1_keywords:
- volatile_CSharpKeyword
- volatile
helpviewer_keywords:
- volatile keyword [C#]
ms.assetid: 78089bc7-7b38-4cfd-9e49-87ac036af009
ms.openlocfilehash: 7f3aafc1255667f2a3917c6e171ce4ddf0343b41
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33272582"
---
# <a name="volatile-c-reference"></a><span data-ttu-id="0f809-102">volatile (référence C#)</span><span class="sxs-lookup"><span data-stu-id="0f809-102">volatile (C# Reference)</span></span>
<span data-ttu-id="0f809-103">Le mot clé `volatile` indique qu’un champ peut être modifié par plusieurs threads qui s’exécutent simultanément.</span><span class="sxs-lookup"><span data-stu-id="0f809-103">The `volatile` keyword indicates that a field might be modified by multiple threads that are executing at the same time.</span></span> <span data-ttu-id="0f809-104">Les champs qui sont déclarés `volatile` ne sont pas soumis aux optimisations du compilateur qui supposent l’accès par un seul thread.</span><span class="sxs-lookup"><span data-stu-id="0f809-104">Fields that are declared `volatile` are not subject to compiler optimizations that assume access by a single thread.</span></span> <span data-ttu-id="0f809-105">Cela garantit que la valeur la plus à jour est présente dans le champ à tout moment.</span><span class="sxs-lookup"><span data-stu-id="0f809-105">This ensures that the most up-to-date value is present in the field at all times.</span></span>  
  
 <span data-ttu-id="0f809-106">Le modificateur `volatile` est généralement utilisé pour un champ auquel accèdent plusieurs threads sans utiliser l’instruction [lock](../../../csharp/language-reference/keywords/lock-statement.md) pour sérialiser l’accès.</span><span class="sxs-lookup"><span data-stu-id="0f809-106">The `volatile` modifier is usually used for a field that is accessed by multiple threads without using the [lock](../../../csharp/language-reference/keywords/lock-statement.md) statement to serialize access.</span></span>  
  
 <span data-ttu-id="0f809-107">Le mot clé `volatile` peut être appliqué aux champs des types suivants :</span><span class="sxs-lookup"><span data-stu-id="0f809-107">The `volatile` keyword can be applied to fields of these types:</span></span>  
  
-   <span data-ttu-id="0f809-108">Types référence.</span><span class="sxs-lookup"><span data-stu-id="0f809-108">Reference types.</span></span>  
  
-   <span data-ttu-id="0f809-109">Types pointeur (dans un contexte unsafe).</span><span class="sxs-lookup"><span data-stu-id="0f809-109">Pointer types (in an unsafe context).</span></span> <span data-ttu-id="0f809-110">Notez que, même si le pointeur lui-même peut être volatile, l’objet sur lequel il pointe ne le peut pas.</span><span class="sxs-lookup"><span data-stu-id="0f809-110">Note that although the pointer itself can be volatile, the object that it points to cannot.</span></span> <span data-ttu-id="0f809-111">En d’autres termes, vous ne pouvez pas déclarer un pointeur vers un objet volatile.</span><span class="sxs-lookup"><span data-stu-id="0f809-111">In other words, you cannot declare a "pointer to volatile."</span></span>  
  
-   <span data-ttu-id="0f809-112">Types tels que sbyte, byte, short, ushort, int, uint, char, float et bool.</span><span class="sxs-lookup"><span data-stu-id="0f809-112">Types such as sbyte, byte, short, ushort, int, uint, char, float, and bool.</span></span>  
  
-   <span data-ttu-id="0f809-113">Type enum avec l’un des types de base suivants : byte, sbyte, short, ushort, int ou uint.</span><span class="sxs-lookup"><span data-stu-id="0f809-113">An enum type with one of the following base types: byte, sbyte, short, ushort, int, or uint.</span></span>  
  
-   <span data-ttu-id="0f809-114">Paramètres de type générique connus comme des types référence.</span><span class="sxs-lookup"><span data-stu-id="0f809-114">Generic type parameters known to be reference types.</span></span>  
  
-   <span data-ttu-id="0f809-115">Voir <xref:System.IntPtr> et <xref:System.UIntPtr>.</span><span class="sxs-lookup"><span data-stu-id="0f809-115"><xref:System.IntPtr> and <xref:System.UIntPtr>.</span></span>  
  
 <span data-ttu-id="0f809-116">Le mot clé volatile ne peut s’appliquer qu’aux champs d’une classe ou d’une structure.</span><span class="sxs-lookup"><span data-stu-id="0f809-116">The volatile keyword can only be applied to fields of a class or struct.</span></span> <span data-ttu-id="0f809-117">Les variables locales ne peuvent pas être déclarées `volatile`.</span><span class="sxs-lookup"><span data-stu-id="0f809-117">Local variables cannot be declared `volatile`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0f809-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="0f809-118">Example</span></span>  
 <span data-ttu-id="0f809-119">L’exemple ci-dessous montre comment déclarer une variable de champ public comme `volatile`.</span><span class="sxs-lookup"><span data-stu-id="0f809-119">The following example shows how to declare a public field variable as `volatile`.</span></span>  
  
 [!code-csharp[csrefKeywordsModifiers#24](../../../csharp/language-reference/keywords/codesnippet/CSharp/volatile_1.cs)]  
  
## <a name="example"></a><span data-ttu-id="0f809-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="0f809-120">Example</span></span>  
 <span data-ttu-id="0f809-121">L’exemple suivant montre comment il est possible de créer un thread auxiliaire ou de travail et de l’utiliser pour effectuer le traitement en parallèle avec le thread principal.</span><span class="sxs-lookup"><span data-stu-id="0f809-121">The following example demonstrates how an auxiliary or worker thread can be created and used to perform processing in parallel with that of the primary thread.</span></span> <span data-ttu-id="0f809-122">Pour des informations générales sur le multithreading, consultez [Threading (C#)](../../../standard/threading/index.md) et [Threading managé](../../programming-guide/concepts/threading/index.md).</span><span class="sxs-lookup"><span data-stu-id="0f809-122">For background information about multithreading, see [Threading (C#)](../../../standard/threading/index.md) and [Managed Threading](../../programming-guide/concepts/threading/index.md).</span></span>  
  
 [!code-csharp[csProgGuideThreading#1](../../../csharp/language-reference/keywords/codesnippet/CSharp/volatile_2.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="0f809-123">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="0f809-123">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="0f809-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f809-124">See Also</span></span>  
 [<span data-ttu-id="0f809-125">Référence C#</span><span class="sxs-lookup"><span data-stu-id="0f809-125">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="0f809-126">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="0f809-126">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="0f809-127">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="0f809-127">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="0f809-128">Modificateurs</span><span class="sxs-lookup"><span data-stu-id="0f809-128">Modifiers</span></span>](../../../csharp/language-reference/keywords/modifiers.md)
