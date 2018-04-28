---
title: Opérateurs booléens (F#)
description: 'Obtenir des informations sur les opérateurs booléens sont disponibles dans le langage de programmation F #.'
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: dotnet-fsharp
ms.devlang: fsharp
ms.openlocfilehash: 0b11b5133b02b6f507c7886b2fbaebf30abf46cb
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="boolean-operators"></a><span data-ttu-id="a344e-103">Opérateurs booléens</span><span class="sxs-lookup"><span data-stu-id="a344e-103">Boolean Operators</span></span>

<span data-ttu-id="a344e-104">Cette rubrique décrit la prise en charge des opérateurs booléens dans le langage F #.</span><span class="sxs-lookup"><span data-stu-id="a344e-104">This topic describes the support for Boolean operators in the F# language.</span></span>


## <a name="summary-of-boolean-operators"></a><span data-ttu-id="a344e-105">Résumé des opérateurs booléens</span><span class="sxs-lookup"><span data-stu-id="a344e-105">Summary of Boolean Operators</span></span>
<span data-ttu-id="a344e-106">Le tableau suivant récapitule les opérateurs booléens sont disponibles dans le langage F #.</span><span class="sxs-lookup"><span data-stu-id="a344e-106">The following table summarizes the Boolean operators that are available in the F# language.</span></span> <span data-ttu-id="a344e-107">Le seul type pris en charge par ces opérateurs est le `bool` type.</span><span class="sxs-lookup"><span data-stu-id="a344e-107">The only type supported by these operators is the `bool` type.</span></span>

|<span data-ttu-id="a344e-108">Opérateur</span><span class="sxs-lookup"><span data-stu-id="a344e-108">Operator</span></span>|<span data-ttu-id="a344e-109">Description</span><span class="sxs-lookup"><span data-stu-id="a344e-109">Description</span></span>|
|--------|-----------|
|`not`|<span data-ttu-id="a344e-110">Négation booléenne</span><span class="sxs-lookup"><span data-stu-id="a344e-110">Boolean negation</span></span>|
|<code>&#124;&#124;</code>|<span data-ttu-id="a344e-111">Booléen OR</span><span class="sxs-lookup"><span data-stu-id="a344e-111">Boolean OR</span></span>|
|`&&`|<span data-ttu-id="a344e-112">Booléen AND</span><span class="sxs-lookup"><span data-stu-id="a344e-112">Boolean AND</span></span>|

<span data-ttu-id="a344e-113">Les opérateurs booléens AND et OR effectuent *l’évaluation de court-circuit*, autrement dit, elles évaluent l’expression à droite de l’opérateur uniquement lorsqu’il est nécessaire de déterminer le résultat global de l’expression.</span><span class="sxs-lookup"><span data-stu-id="a344e-113">The Boolean AND and OR operators perform *short-circuit evaluation*, that is, they evaluate the expression on the right of the operator only when it is necessary to determine the overall result of the expression.</span></span> <span data-ttu-id="a344e-114">La deuxième expression de la `&&` opérateur est évalué uniquement si la première expression a la valeur `true`; la deuxième expression de la `||` opérateur est évalué uniquement si la première expression a la valeur `false`.</span><span class="sxs-lookup"><span data-stu-id="a344e-114">The second expression of the `&&` operator is evaluated only if the first expression evaluates to `true`; the second expression of the `||` operator is evaluated only if the first expression evaluates to `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="a344e-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a344e-115">See Also</span></span>
[<span data-ttu-id="a344e-116">Opérateurs au niveau du bit</span><span class="sxs-lookup"><span data-stu-id="a344e-116">Bitwise Operators</span></span>](bitwise-operators.md)

[<span data-ttu-id="a344e-117">Opérateurs arithmétiques</span><span class="sxs-lookup"><span data-stu-id="a344e-117">Arithmetic Operators</span></span>](arithmetic-operators.md)

[<span data-ttu-id="a344e-118">Informations de référence des symboles et opérateurs</span><span class="sxs-lookup"><span data-stu-id="a344e-118">Symbol and Operator Reference</span></span>](index.md)
