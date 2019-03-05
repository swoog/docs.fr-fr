---
title: . opérateur - Référence C#
ms.custom: seodec18
ms.date: 02/25/2019
f1_keywords:
- ._CSharpKeyword
helpviewer_keywords:
- member access operator (.) [C#]
- . operator [C#]
- dot operator (.) [C#]
ms.assetid: a1f54b52-b686-4ae5-a48e-a2a9ebd0eb7b
ms.openlocfilehash: 2661676d53deb874c5e5a90b4443b301730e09df
ms.sourcegitcommit: bd28ff1e312eaba9718c4f7ea272c2d4781a7cac
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "56836459"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="dc07d-103">.</span><span class="sxs-lookup"><span data-stu-id="dc07d-103">.</span></span> <span data-ttu-id="dc07d-104">operator (référence C#)</span><span class="sxs-lookup"><span data-stu-id="dc07d-104">operator (C# Reference)</span></span>

<span data-ttu-id="dc07d-105">Le point, `.`, est en général utilisé pour l’accès aux membres.</span><span class="sxs-lookup"><span data-stu-id="dc07d-105">The dot, `.`, is typically used for member access.</span></span>

<span data-ttu-id="dc07d-106">Le jeton `.` sert à accéder à l’un des membres d’un espace de noms ou d’un type, comme le montrent les exemples suivants :</span><span class="sxs-lookup"><span data-stu-id="dc07d-106">You use the `.` token to access a member of a namespace or a type, as the following examples demonstrate:</span></span>

- <span data-ttu-id="dc07d-107">Utilisez `.` pour accéder à un espace de noms imbriqué dans un autre, comme le montre l’exemple suivant avec la [directive `using`](../keywords/using-directive.md) :</span><span class="sxs-lookup"><span data-stu-id="dc07d-107">Use `.` to access a nested namespace within a namespace, as the following example of a [`using` directive](../keywords/using-directive.md) shows:</span></span>

  [!code-csharp[nested namespaces](~/samples/snippets/csharp/language-reference/operators/MemberAccessExamples.cs#NestedNamespace)]

- <span data-ttu-id="dc07d-108">Utilisez `.` pour former un *nom qualifié* permettant d’accéder à un type dans un espace de noms, comme le montre le code suivant :</span><span class="sxs-lookup"><span data-stu-id="dc07d-108">Use `.` to form a *qualified name* to access a type within a namespace, as the following code shows:</span></span>

  [!code-csharp[qualified name](~/samples/snippets/csharp/language-reference/operators/MemberAccessExamples.cs#QualifiedName)]

  <span data-ttu-id="dc07d-109">Utiliser la [directive `using`](../keywords/using-directive.md) pour rendre facultative l’utilisation de noms qualifiés.</span><span class="sxs-lookup"><span data-stu-id="dc07d-109">Use the [`using` directive](../keywords/using-directive.md) to make the use of qualified names optional.</span></span>

- <span data-ttu-id="dc07d-110">Utilisez `.` pour accéder aux [membres de type](../../programming-guide/classes-and-structs/index.md#members), statiques et non statiques, comme le montre le code suivant :</span><span class="sxs-lookup"><span data-stu-id="dc07d-110">Use `.` to access [type members](../../programming-guide/classes-and-structs/index.md#members), static and non-static, as the following code shows:</span></span>

  [!code-csharp-interactive[type members](~/samples/snippets/csharp/language-reference/operators/MemberAccessExamples.cs#TypeMemberAccess)]

<span data-ttu-id="dc07d-111">Vous pouvez également utiliser `.` pour appeler une [méthode d’extension](../../programming-guide/classes-and-structs/extension-methods.md).</span><span class="sxs-lookup"><span data-stu-id="dc07d-111">You can also use `.` to invoke an [extension method](../../programming-guide/classes-and-structs/extension-methods.md).</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="dc07d-112">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="dc07d-112">Operator overloadability</span></span>

<span data-ttu-id="dc07d-113">L’opérateur `.` ne peut pas être surchargé.</span><span class="sxs-lookup"><span data-stu-id="dc07d-113">The operator `.` cannot be overloaded.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="dc07d-114">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="dc07d-114">C# language specification</span></span>

<span data-ttu-id="dc07d-115">Pour plus d’informations, voir la section [Accès au membre](~/_csharplang/spec/expressions.md#member-access) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="dc07d-115">For more information, see the [Member access](~/_csharplang/spec/expressions.md#member-access) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="dc07d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc07d-116">See also</span></span>

- [<span data-ttu-id="dc07d-117">Référence C#</span><span class="sxs-lookup"><span data-stu-id="dc07d-117">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="dc07d-118">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="dc07d-118">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="dc07d-119">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="dc07d-119">C# Operators</span></span>](index.md)
- <span data-ttu-id="dc07d-120">[Opérateurs ?. et ?[]](null-conditional-operators.md)</span><span class="sxs-lookup"><span data-stu-id="dc07d-120">[?. and ?[] operators](null-conditional-operators.md)</span></span>