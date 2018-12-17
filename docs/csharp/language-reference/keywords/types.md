---
title: Types (référence C#)
ms.date: 07/20/2015
helpviewer_keywords:
- types [C#]
- data types [C#], type system
ms.assetid: 16b984df-f417-4e02-b1e6-4589d4a614ea
ms.openlocfilehash: f5a3ad9fef108c1eec2ba63d68bc5015d2f6c430
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53142955"
---
# <a name="types-c-reference"></a><span data-ttu-id="30a54-102">Types (référence C#)</span><span class="sxs-lookup"><span data-stu-id="30a54-102">Types (C# Reference)</span></span>

<span data-ttu-id="30a54-103">Le système de types C# comporte les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="30a54-103">The C# typing system contains the following categories:</span></span>

- [<span data-ttu-id="30a54-104">Types valeur</span><span class="sxs-lookup"><span data-stu-id="30a54-104">Value types</span></span>](value-types.md)

- [<span data-ttu-id="30a54-105">Types référence</span><span class="sxs-lookup"><span data-stu-id="30a54-105">Reference types</span></span>](reference-types.md)

- [<span data-ttu-id="30a54-106">Types de pointeur</span><span class="sxs-lookup"><span data-stu-id="30a54-106">Pointer types</span></span>](../../programming-guide/unsafe-code-pointers/pointer-types.md)

 <span data-ttu-id="30a54-107">Les variables de types valeur stockent des données alors que les variables de types référence stockent les références aux données réelles.</span><span class="sxs-lookup"><span data-stu-id="30a54-107">Variables that are value types store data, and those that are reference types store references to the actual data.</span></span> <span data-ttu-id="30a54-108">Les instances de types référence sont également considérées comme des objets.</span><span class="sxs-lookup"><span data-stu-id="30a54-108">Instances of reference types are also referred to as objects.</span></span> <span data-ttu-id="30a54-109">Les types pointeur ne peuvent être utilisés qu’en mode [unsafe](unsafe.md).</span><span class="sxs-lookup"><span data-stu-id="30a54-109">Pointer types can be used only in [unsafe](unsafe.md) mode.</span></span>

 <span data-ttu-id="30a54-110">Il est possible de convertir un type valeur en un type référence, puis de revenir au type valeur, en effectuant une conversion [boxing et unboxing](../../../csharp/programming-guide/types/boxing-and-unboxing.md).</span><span class="sxs-lookup"><span data-stu-id="30a54-110">It's possible to convert a value type to a reference type, and back again to a value type, by using [boxing and unboxing](../../../csharp/programming-guide/types/boxing-and-unboxing.md).</span></span> <span data-ttu-id="30a54-111">Vous ne pouvez pas convertir un type référence en type valeur, sauf s’il s’agit d’un type valeur boxed.</span><span class="sxs-lookup"><span data-stu-id="30a54-111">With the exception of a boxed value type, you cannot convert a reference type to a value type.</span></span>

 <span data-ttu-id="30a54-112">Cette section présente également [void](void.md).</span><span class="sxs-lookup"><span data-stu-id="30a54-112">This section also introduces [void](void.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="30a54-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30a54-113">See also</span></span>

- [<span data-ttu-id="30a54-114">Référence C#</span><span class="sxs-lookup"><span data-stu-id="30a54-114">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="30a54-115">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="30a54-115">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="30a54-116">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="30a54-116">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="30a54-117">Tableaux de référence des types</span><span class="sxs-lookup"><span data-stu-id="30a54-117">Reference Tables for Types</span></span>](reference-tables-for-types.md)
- [<span data-ttu-id="30a54-118">Cast et conversions de types</span><span class="sxs-lookup"><span data-stu-id="30a54-118">Casting and Type Conversions</span></span>](../../programming-guide/types/casting-and-type-conversions.md)
- [<span data-ttu-id="30a54-119">Types</span><span class="sxs-lookup"><span data-stu-id="30a54-119">Types</span></span>](../../programming-guide/types/index.md)
