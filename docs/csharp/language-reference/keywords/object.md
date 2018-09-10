---
title: object (référence C#)
ms.date: 07/20/2015
f1_keywords:
- object_CSharpKeyword
- object
helpviewer_keywords:
- object keyword [C#]
ms.assetid: 93f60c0b-e17a-40a9-9362-cca5fb77b0e7
ms.openlocfilehash: b36703828e6027a89297ac88edaf2b55ec18f42e
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44191805"
---
# <a name="object-c-reference"></a><span data-ttu-id="4303c-102">object (référence C#)</span><span class="sxs-lookup"><span data-stu-id="4303c-102">object (C# Reference)</span></span>

<span data-ttu-id="4303c-103">Le type `object` est un alias de <xref:System.Object> dans .NET.</span><span class="sxs-lookup"><span data-stu-id="4303c-103">The `object` type is an alias for <xref:System.Object> in .NET.</span></span> <span data-ttu-id="4303c-104">Dans le système de type unifié de C#, tous les types (les types référence et valeur, prédéfinis ou définis par l’utilisateur) héritent directement ou indirectement du type <xref:System.Object>.</span><span class="sxs-lookup"><span data-stu-id="4303c-104">In the unified type system of C#, all types, predefined and user-defined, reference types and value types, inherit directly or indirectly from <xref:System.Object>.</span></span> <span data-ttu-id="4303c-105">Vous pouvez assigner des valeurs de tout type aux variables de type `object`.</span><span class="sxs-lookup"><span data-stu-id="4303c-105">You can assign values of any type to variables of type `object`.</span></span> <span data-ttu-id="4303c-106">Quand une variable d’un type valeur est convertie en type objet, elle est dite *boxed*.</span><span class="sxs-lookup"><span data-stu-id="4303c-106">When a variable of a value type is converted to object, it is said to be *boxed*.</span></span> <span data-ttu-id="4303c-107">Quand une variable de type objet est convertie en type valeur, elle est dite *unboxed*.</span><span class="sxs-lookup"><span data-stu-id="4303c-107">When a variable of type object is converted to a value type, it is said to be *unboxed*.</span></span> <span data-ttu-id="4303c-108">Pour plus d’informations, consultez [Boxing et unboxing](../../../csharp/programming-guide/types/boxing-and-unboxing.md).</span><span class="sxs-lookup"><span data-stu-id="4303c-108">For more information, see [Boxing and Unboxing](../../../csharp/programming-guide/types/boxing-and-unboxing.md).</span></span>

## <a name="example"></a><span data-ttu-id="4303c-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="4303c-109">Example</span></span>

<span data-ttu-id="4303c-110">L’exemple suivant montre comment les variables de type `object` acceptent des valeurs de tout type de données et comment les variables de type `object` utilisent des méthodes d’<xref:System.Object> du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="4303c-110">The following sample shows how variables of type `object` can accept values of any data type and how variables of type `object` can use methods on <xref:System.Object> from the .NET Framework.</span></span>

[!code-csharp[csrefKeywordsTypes#16](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#16)]

## <a name="c-language-specification"></a><span data-ttu-id="4303c-111">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="4303c-111">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="4303c-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4303c-112">See also</span></span>

- [<span data-ttu-id="4303c-113">Référence C#</span><span class="sxs-lookup"><span data-stu-id="4303c-113">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="4303c-114">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="4303c-114">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="4303c-115">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="4303c-115">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="4303c-116">Types référence</span><span class="sxs-lookup"><span data-stu-id="4303c-116">Reference Types</span></span>](reference-types.md)
- [<span data-ttu-id="4303c-117">Types valeur</span><span class="sxs-lookup"><span data-stu-id="4303c-117">Value Types</span></span>](value-types.md)