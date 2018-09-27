---
title: Assertions (F#)
description: 'Découvrez comment utiliser l’expression « déclarer » comme une fonctionnalité de débogage pour le test des expressions dans le langage de programmation F #.'
ms.date: 05/16/2016
ms.openlocfilehash: 85b1e839bfd19bada48b7f1821d15ddd8fa77754
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47233237"
---
# <a name="assertions"></a><span data-ttu-id="1f08d-103">Assertions</span><span class="sxs-lookup"><span data-stu-id="1f08d-103">Assertions</span></span>

<span data-ttu-id="1f08d-104">Le `assert` expression est une fonctionnalité de débogage que vous pouvez utiliser pour tester une expression.</span><span class="sxs-lookup"><span data-stu-id="1f08d-104">The `assert` expression is a debugging feature that you can use to test an expression.</span></span> <span data-ttu-id="1f08d-105">En cas d’échec en mode débogage, une assertion génère une boîte de dialogue d’erreur système.</span><span class="sxs-lookup"><span data-stu-id="1f08d-105">Upon failure in Debug mode, an assertion generates a system error dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f08d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f08d-106">Syntax</span></span>

```fsharp
assert condition
```

## <a name="remarks"></a><span data-ttu-id="1f08d-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1f08d-107">Remarks</span></span>

<span data-ttu-id="1f08d-108">Le `assert` expression a le type `bool -> unit`.</span><span class="sxs-lookup"><span data-stu-id="1f08d-108">The `assert` expression has type `bool -> unit`.</span></span>

<span data-ttu-id="1f08d-109">Dans la syntaxe précédente, *condition* représente une expression booléenne qui doit être testée.</span><span class="sxs-lookup"><span data-stu-id="1f08d-109">In the previous syntax, *condition* represents a Boolean expression that is to be tested.</span></span> <span data-ttu-id="1f08d-110">Si l’expression prend la valeur `true`, l’exécution se poursuit normalement.</span><span class="sxs-lookup"><span data-stu-id="1f08d-110">If the expression evaluates to `true`, execution continues unaffected.</span></span> <span data-ttu-id="1f08d-111">Si elle a la valeur `false`, une boîte de dialogue d’erreur système est générée.</span><span class="sxs-lookup"><span data-stu-id="1f08d-111">If it evaluates to `false`, a system error dialog box is generated.</span></span> <span data-ttu-id="1f08d-112">La boîte de dialogue d’erreur comprend une légende qui contient la chaîne **Échec de l’Assertion**.</span><span class="sxs-lookup"><span data-stu-id="1f08d-112">The error dialog box has a caption that contains the string **Assertion Failed**.</span></span> <span data-ttu-id="1f08d-113">La boîte de dialogue contient une trace de pile qui indique où l’échec d’assertion s’est produite.</span><span class="sxs-lookup"><span data-stu-id="1f08d-113">The dialog box contains a stack trace that indicates where the assertion failure occurred.</span></span>

<span data-ttu-id="1f08d-114">Vérification de l’assertion est activée uniquement lorsque vous compilez en mode débogage ; Autrement dit, si la constante `DEBUG` est défini.</span><span class="sxs-lookup"><span data-stu-id="1f08d-114">Assertion checking is enabled only when you compile in Debug mode; that is, if the constant `DEBUG` is defined.</span></span> <span data-ttu-id="1f08d-115">Dans le système de projet, par défaut, le `DEBUG` constante n’est définie dans la configuration Debug, mais pas dans la configuration Release.</span><span class="sxs-lookup"><span data-stu-id="1f08d-115">In the project system, by default, the `DEBUG` constant is defined in the Debug configuration but not in the Release configuration.</span></span>

<span data-ttu-id="1f08d-116">L’erreur d’échec d’assertion ne peut pas être interceptée à l’aide de la gestion des exceptions F #.</span><span class="sxs-lookup"><span data-stu-id="1f08d-116">The assertion failure error cannot be caught by using F# exception handling.</span></span>

>[!NOTE]
<span data-ttu-id="1f08d-117">Le `assert` fonction se résout en <xref:System.Diagnostics.Debug.Assert*?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="1f08d-117">The `assert` function resolves to <xref:System.Diagnostics.Debug.Assert*?displayProperty=nameWithType>.</span></span>

## <a name="example"></a><span data-ttu-id="1f08d-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="1f08d-118">Example</span></span>

<span data-ttu-id="1f08d-119">L’exemple de code suivant illustre l’utilisation de la `assert` expression.</span><span class="sxs-lookup"><span data-stu-id="1f08d-119">The following code example illustrates the use of the `assert` expression.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5401.fs)]

## <a name="see-also"></a><span data-ttu-id="1f08d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f08d-120">See also</span></span>

- [<span data-ttu-id="1f08d-121">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="1f08d-121">F# Language Reference</span></span>](index.md)
