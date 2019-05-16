---
title: Opérateurs booléens
description: En savoir plus sur les opérateurs booléens sont disponibles dans le F# langage de programmation.
ms.date: 05/16/2016
ms.openlocfilehash: ad4bdd1121389f7e280647dbe0c4d0098ffb17df
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65641901"
---
# <a name="boolean-operators"></a><span data-ttu-id="5c66d-103">Opérateurs booléens</span><span class="sxs-lookup"><span data-stu-id="5c66d-103">Boolean Operators</span></span>

<span data-ttu-id="5c66d-104">Cette rubrique décrit la prise en charge pour les opérateurs booléens dans les F# langage.</span><span class="sxs-lookup"><span data-stu-id="5c66d-104">This topic describes the support for Boolean operators in the F# language.</span></span>

## <a name="summary-of-boolean-operators"></a><span data-ttu-id="5c66d-105">Résumé des opérateurs booléens</span><span class="sxs-lookup"><span data-stu-id="5c66d-105">Summary of Boolean Operators</span></span>

<span data-ttu-id="5c66d-106">Le tableau suivant récapitule les opérateurs booléens sont disponibles dans le F# langage.</span><span class="sxs-lookup"><span data-stu-id="5c66d-106">The following table summarizes the Boolean operators that are available in the F# language.</span></span> <span data-ttu-id="5c66d-107">Le seul type pris en charge par ces opérateurs est le `bool` type.</span><span class="sxs-lookup"><span data-stu-id="5c66d-107">The only type supported by these operators is the `bool` type.</span></span>

|<span data-ttu-id="5c66d-108">Opérateur</span><span class="sxs-lookup"><span data-stu-id="5c66d-108">Operator</span></span>|<span data-ttu-id="5c66d-109">Description</span><span class="sxs-lookup"><span data-stu-id="5c66d-109">Description</span></span>|
|--------|-----------|
|`not`|<span data-ttu-id="5c66d-110">Négation booléenne</span><span class="sxs-lookup"><span data-stu-id="5c66d-110">Boolean negation</span></span>|
|<code>&#124;&#124;</code>|<span data-ttu-id="5c66d-111">Booléen OR</span><span class="sxs-lookup"><span data-stu-id="5c66d-111">Boolean OR</span></span>|
|`&&`|<span data-ttu-id="5c66d-112">Booléen AND</span><span class="sxs-lookup"><span data-stu-id="5c66d-112">Boolean AND</span></span>|

<span data-ttu-id="5c66d-113">Les opérateurs booléens AND et OR effectuent *l’évaluation de court-circuit*, autrement dit, ils évaluent l’expression à droite de l’opérateur uniquement lorsqu’il est nécessaire déterminer le résultat global de l’expression.</span><span class="sxs-lookup"><span data-stu-id="5c66d-113">The Boolean AND and OR operators perform *short-circuit evaluation*, that is, they evaluate the expression on the right of the operator only when it is necessary to determine the overall result of the expression.</span></span> <span data-ttu-id="5c66d-114">La deuxième expression de la `&&` opérateur est évalué uniquement si la première expression a la valeur `true`; la deuxième expression de la `||` opérateur est évalué uniquement si la première expression a la valeur `false`.</span><span class="sxs-lookup"><span data-stu-id="5c66d-114">The second expression of the `&&` operator is evaluated only if the first expression evaluates to `true`; the second expression of the `||` operator is evaluated only if the first expression evaluates to `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="5c66d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c66d-115">See also</span></span>

- [<span data-ttu-id="5c66d-116">Opérateurs au niveau du bit</span><span class="sxs-lookup"><span data-stu-id="5c66d-116">Bitwise Operators</span></span>](bitwise-operators.md)
- [<span data-ttu-id="5c66d-117">Opérateurs arithmétiques</span><span class="sxs-lookup"><span data-stu-id="5c66d-117">Arithmetic Operators</span></span>](arithmetic-operators.md)
- [<span data-ttu-id="5c66d-118">Informations de référence des symboles et opérateurs</span><span class="sxs-lookup"><span data-stu-id="5c66d-118">Symbol and Operator Reference</span></span>](index.md)
