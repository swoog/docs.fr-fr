---
title: Opérateurs booléens (F#)
description: 'En savoir plus sur les opérateurs booléens sont disponibles dans le langage de programmation F #.'
ms.date: 05/16/2016
ms.openlocfilehash: faa181090efa7c4064a30b42d83afa4888e98b82
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44172727"
---
# <a name="boolean-operators"></a><span data-ttu-id="5d368-103">Opérateurs booléens</span><span class="sxs-lookup"><span data-stu-id="5d368-103">Boolean Operators</span></span>

<span data-ttu-id="5d368-104">Cette rubrique décrit la prise en charge pour les opérateurs booléens dans le langage F #.</span><span class="sxs-lookup"><span data-stu-id="5d368-104">This topic describes the support for Boolean operators in the F# language.</span></span>

## <a name="summary-of-boolean-operators"></a><span data-ttu-id="5d368-105">Résumé des opérateurs booléens</span><span class="sxs-lookup"><span data-stu-id="5d368-105">Summary of Boolean Operators</span></span>

<span data-ttu-id="5d368-106">Le tableau suivant récapitule les opérateurs booléens sont disponibles dans le langage F #.</span><span class="sxs-lookup"><span data-stu-id="5d368-106">The following table summarizes the Boolean operators that are available in the F# language.</span></span> <span data-ttu-id="5d368-107">Le seul type pris en charge par ces opérateurs est le `bool` type.</span><span class="sxs-lookup"><span data-stu-id="5d368-107">The only type supported by these operators is the `bool` type.</span></span>

|<span data-ttu-id="5d368-108">Opérateur</span><span class="sxs-lookup"><span data-stu-id="5d368-108">Operator</span></span>|<span data-ttu-id="5d368-109">Description</span><span class="sxs-lookup"><span data-stu-id="5d368-109">Description</span></span>|
|--------|-----------|
|`not`|<span data-ttu-id="5d368-110">Négation booléenne</span><span class="sxs-lookup"><span data-stu-id="5d368-110">Boolean negation</span></span>|
|<code>&#124;&#124;</code>|<span data-ttu-id="5d368-111">Booléen OR</span><span class="sxs-lookup"><span data-stu-id="5d368-111">Boolean OR</span></span>|
|`&&`|<span data-ttu-id="5d368-112">Booléen AND</span><span class="sxs-lookup"><span data-stu-id="5d368-112">Boolean AND</span></span>|

<span data-ttu-id="5d368-113">Les opérateurs booléens AND et OR effectuent *l’évaluation de court-circuit*, autrement dit, ils évaluent l’expression à droite de l’opérateur uniquement lorsqu’il est nécessaire déterminer le résultat global de l’expression.</span><span class="sxs-lookup"><span data-stu-id="5d368-113">The Boolean AND and OR operators perform *short-circuit evaluation*, that is, they evaluate the expression on the right of the operator only when it is necessary to determine the overall result of the expression.</span></span> <span data-ttu-id="5d368-114">La deuxième expression de la `&&` opérateur est évalué uniquement si la première expression a la valeur `true`; la deuxième expression de la `||` opérateur est évalué uniquement si la première expression a la valeur `false`.</span><span class="sxs-lookup"><span data-stu-id="5d368-114">The second expression of the `&&` operator is evaluated only if the first expression evaluates to `true`; the second expression of the `||` operator is evaluated only if the first expression evaluates to `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="5d368-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d368-115">See also</span></span>

- [<span data-ttu-id="5d368-116">Opérateurs au niveau du bit</span><span class="sxs-lookup"><span data-stu-id="5d368-116">Bitwise Operators</span></span>](bitwise-operators.md)
- [<span data-ttu-id="5d368-117">Opérateurs arithmétiques</span><span class="sxs-lookup"><span data-stu-id="5d368-117">Arithmetic Operators</span></span>](arithmetic-operators.md)
- [<span data-ttu-id="5d368-118">Informations de référence des symboles et opérateurs</span><span class="sxs-lookup"><span data-stu-id="5d368-118">Symbol and Operator Reference</span></span>](index.md)
