---
title: Pointeurs et code unsafe - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- security [C#], type safety
- C# language, unsafe code
- type safety [C#]
- unsafe keyword [C#]
- unsafe code [C#]
- C# language, pointers
- pointers [C#], about pointers
ms.assetid: b0fcca10-a92d-4f2a-835b-b0ccae6739ee
ms.openlocfilehash: 99f0b925a37bff8b6ab1ff46e9ce2f0ea0a38aed
ms.sourcegitcommit: ffd7dd79468a81bbb0d6449f6d65513e050c04c4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2019
ms.locfileid: "65959481"
---
# <a name="unsafe-code-and-pointers-c-programming-guide"></a><span data-ttu-id="3f318-102">Pointeurs et code unsafe (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="3f318-102">Unsafe code and pointers (C# Programming Guide)</span></span>

<span data-ttu-id="3f318-103">Pour conserver la sécurité des types, par défaut, C# ne prend pas en charge les opérations arithmétiques sur les pointeurs.</span><span class="sxs-lookup"><span data-stu-id="3f318-103">To maintain type safety and security, C# does not support pointer arithmetic, by default.</span></span> <span data-ttu-id="3f318-104">Cependant, en utilisant le mot clé [unsafe](../../language-reference/keywords/unsafe.md), vous pouvez définir un contexte non sécurisé dans lequel des pointeurs peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="3f318-104">However, by using the [unsafe](../../language-reference/keywords/unsafe.md) keyword, you can define an unsafe context in which pointers can be used.</span></span> <span data-ttu-id="3f318-105">Pour en savoir plus sur les pointeurs, consultez la rubrique [Types de pointeur](pointer-types.md).</span><span class="sxs-lookup"><span data-stu-id="3f318-105">For more information about pointers, see [Pointer types](pointer-types.md).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="3f318-106">Dans le common language runtime (CLR), le code non sécurisé est appelé « code non vérifiable ».</span><span class="sxs-lookup"><span data-stu-id="3f318-106">In the common language runtime (CLR), unsafe code is referred to as unverifiable code.</span></span> <span data-ttu-id="3f318-107">Le code non sécurisé en C# n’est pas nécessairement dangereux : il s’agit simplement de code dont la sécurité ne peut pas être vérifiée par le CLR.</span><span class="sxs-lookup"><span data-stu-id="3f318-107">Unsafe code in C# is not necessarily dangerous; it is just code whose safety cannot be verified by the CLR.</span></span> <span data-ttu-id="3f318-108">Le CLR exécute du code non sécurisé seulement s’il se trouve dans un assembly entièrement fiable.</span><span class="sxs-lookup"><span data-stu-id="3f318-108">The CLR will therefore only execute unsafe code if it is in a fully trusted assembly.</span></span> <span data-ttu-id="3f318-109">Si vous utilisez du code non sécurisé, il vous incombe de vérifier que votre code n’introduit pas de risques de sécurité ni d’erreurs de pointeur.</span><span class="sxs-lookup"><span data-stu-id="3f318-109">If you use unsafe code, it is your responsibility to ensure that your code does not introduce security risks or pointer errors.</span></span>  
  
## <a name="unsafe-code-overview"></a><span data-ttu-id="3f318-110">Vue d’ensemble du code unsafe</span><span class="sxs-lookup"><span data-stu-id="3f318-110">Unsafe code overview</span></span>

<span data-ttu-id="3f318-111">Le code non sécurisé a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="3f318-111">Unsafe code has the following properties:</span></span>

- <span data-ttu-id="3f318-112">Les méthodes, les types et les blocs de code peuvent être définis comme non sécurisés.</span><span class="sxs-lookup"><span data-stu-id="3f318-112">Methods, types, and code blocks can be defined as unsafe.</span></span>

- <span data-ttu-id="3f318-113">Dans certains cas, le code non sécurisé peut augmenter les performances d’une application en supprimant les vérifications des limites des tableaux.</span><span class="sxs-lookup"><span data-stu-id="3f318-113">In some cases, unsafe code may increase an application's performance by removing array bounds checks.</span></span>

- <span data-ttu-id="3f318-114">Du code non sécurisé est obligatoire quand vous appelez des fonctions natives nécessitant des pointeurs.</span><span class="sxs-lookup"><span data-stu-id="3f318-114">Unsafe code is required when you call native functions that require pointers.</span></span>

- <span data-ttu-id="3f318-115">L’utilisation de code non sécurisé introduit des risques pour la sécurité et la stabilité.</span><span class="sxs-lookup"><span data-stu-id="3f318-115">Using unsafe code introduces security and stability risks.</span></span>

- <span data-ttu-id="3f318-116">Le code qui contient des blocs unsafe doit être compilé avec l’option de compilateur [-unsafe](../../language-reference/compiler-options/unsafe-compiler-option.md).</span><span class="sxs-lookup"><span data-stu-id="3f318-116">The code that contains unsafe blocks must be compiled with the [-unsafe](../../language-reference/compiler-options/unsafe-compiler-option.md) compiler option.</span></span>
  
## <a name="related-sections"></a><span data-ttu-id="3f318-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3f318-117">Related sections</span></span>

<span data-ttu-id="3f318-118">Pour plus d'informations, voir :</span><span class="sxs-lookup"><span data-stu-id="3f318-118">For more information, see:</span></span>

- [<span data-ttu-id="3f318-119">Types de pointeur</span><span class="sxs-lookup"><span data-stu-id="3f318-119">Pointer types</span></span>](pointer-types.md)

- [<span data-ttu-id="3f318-120">Mémoires tampons de taille fixe</span><span class="sxs-lookup"><span data-stu-id="3f318-120">Fixed size buffers</span></span>](fixed-size-buffers.md)

## <a name="c-language-specification"></a><span data-ttu-id="3f318-121">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="3f318-121">C# language specification</span></span>

<span data-ttu-id="3f318-122">Pour en savoir plus, consultez la rubrique [Code unsafe](~/_csharplang/spec/unsafe-code.md) de la [spécification du langage C#](~/_csharplang/spec/introduction.md).</span><span class="sxs-lookup"><span data-stu-id="3f318-122">For more information, see the [Unsafe code](~/_csharplang/spec/unsafe-code.md) topic of the [C# language specification](~/_csharplang/spec/introduction.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3f318-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f318-123">See also</span></span>

- [<span data-ttu-id="3f318-124">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="3f318-124">C# Programming Guide</span></span>](../index.md)
- [<span data-ttu-id="3f318-125">unsafe</span><span class="sxs-lookup"><span data-stu-id="3f318-125">unsafe</span></span>](../../language-reference/keywords/unsafe.md)
