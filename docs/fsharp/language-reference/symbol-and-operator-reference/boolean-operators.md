---
title: Opérateurs booléens (F#)
description: 'Obtenir des informations sur les opérateurs booléens sont disponibles dans le langage de programmation F #.'
ms.date: 05/16/2016
ms.openlocfilehash: f8516ceb531907400f98dc4226d2985d3119e9e9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33563426"
---
# <a name="boolean-operators"></a><span data-ttu-id="ba72b-103">Opérateurs booléens</span><span class="sxs-lookup"><span data-stu-id="ba72b-103">Boolean Operators</span></span>

<span data-ttu-id="ba72b-104">Cette rubrique décrit la prise en charge des opérateurs booléens dans le langage F #.</span><span class="sxs-lookup"><span data-stu-id="ba72b-104">This topic describes the support for Boolean operators in the F# language.</span></span>


## <a name="summary-of-boolean-operators"></a><span data-ttu-id="ba72b-105">Résumé des opérateurs booléens</span><span class="sxs-lookup"><span data-stu-id="ba72b-105">Summary of Boolean Operators</span></span>
<span data-ttu-id="ba72b-106">Le tableau suivant récapitule les opérateurs booléens sont disponibles dans le langage F #.</span><span class="sxs-lookup"><span data-stu-id="ba72b-106">The following table summarizes the Boolean operators that are available in the F# language.</span></span> <span data-ttu-id="ba72b-107">Le seul type pris en charge par ces opérateurs est le `bool` type.</span><span class="sxs-lookup"><span data-stu-id="ba72b-107">The only type supported by these operators is the `bool` type.</span></span>

|<span data-ttu-id="ba72b-108">Opérateur</span><span class="sxs-lookup"><span data-stu-id="ba72b-108">Operator</span></span>|<span data-ttu-id="ba72b-109">Description</span><span class="sxs-lookup"><span data-stu-id="ba72b-109">Description</span></span>|
|--------|-----------|
|`not`|<span data-ttu-id="ba72b-110">Négation booléenne</span><span class="sxs-lookup"><span data-stu-id="ba72b-110">Boolean negation</span></span>|
|<code>&#124;&#124;</code>|<span data-ttu-id="ba72b-111">Booléen OR</span><span class="sxs-lookup"><span data-stu-id="ba72b-111">Boolean OR</span></span>|
|`&&`|<span data-ttu-id="ba72b-112">Booléen AND</span><span class="sxs-lookup"><span data-stu-id="ba72b-112">Boolean AND</span></span>|

<span data-ttu-id="ba72b-113">Les opérateurs booléens AND et OR effectuent *l’évaluation de court-circuit*, autrement dit, elles évaluent l’expression à droite de l’opérateur uniquement lorsqu’il est nécessaire de déterminer le résultat global de l’expression.</span><span class="sxs-lookup"><span data-stu-id="ba72b-113">The Boolean AND and OR operators perform *short-circuit evaluation*, that is, they evaluate the expression on the right of the operator only when it is necessary to determine the overall result of the expression.</span></span> <span data-ttu-id="ba72b-114">La deuxième expression de la `&&` opérateur est évalué uniquement si la première expression a la valeur `true`; la deuxième expression de la `||` opérateur est évalué uniquement si la première expression a la valeur `false`.</span><span class="sxs-lookup"><span data-stu-id="ba72b-114">The second expression of the `&&` operator is evaluated only if the first expression evaluates to `true`; the second expression of the `||` operator is evaluated only if the first expression evaluates to `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="ba72b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba72b-115">See Also</span></span>
[<span data-ttu-id="ba72b-116">Opérateurs au niveau du bit</span><span class="sxs-lookup"><span data-stu-id="ba72b-116">Bitwise Operators</span></span>](bitwise-operators.md)

[<span data-ttu-id="ba72b-117">Opérateurs arithmétiques</span><span class="sxs-lookup"><span data-stu-id="ba72b-117">Arithmetic Operators</span></span>](arithmetic-operators.md)

[<span data-ttu-id="ba72b-118">Informations de référence des symboles et opérateurs</span><span class="sxs-lookup"><span data-stu-id="ba72b-118">Symbol and Operator Reference</span></span>](index.md)
