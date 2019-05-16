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
# <a name="boolean-operators"></a>Opérateurs booléens

Cette rubrique décrit la prise en charge pour les opérateurs booléens dans les F# langage.

## <a name="summary-of-boolean-operators"></a>Résumé des opérateurs booléens

Le tableau suivant récapitule les opérateurs booléens sont disponibles dans le F# langage. Le seul type pris en charge par ces opérateurs est le `bool` type.

|Opérateur|Description|
|--------|-----------|
|`not`|Négation booléenne|
|<code>&#124;&#124;</code>|Booléen OR|
|`&&`|Booléen AND|

Les opérateurs booléens AND et OR effectuent *l’évaluation de court-circuit*, autrement dit, ils évaluent l’expression à droite de l’opérateur uniquement lorsqu’il est nécessaire déterminer le résultat global de l’expression. La deuxième expression de la `&&` opérateur est évalué uniquement si la première expression a la valeur `true`; la deuxième expression de la `||` opérateur est évalué uniquement si la première expression a la valeur `false`.

## <a name="see-also"></a>Voir aussi

- [Opérateurs au niveau du bit](bitwise-operators.md)
- [Opérateurs arithmétiques](arithmetic-operators.md)
- [Informations de référence des symboles et opérateurs](index.md)
