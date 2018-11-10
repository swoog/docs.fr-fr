---
title: Opérateurs booléens (F#)
description: En savoir plus sur les opérateurs booléens sont disponibles dans le langage de programmation F#.
ms.date: 05/16/2016
ms.openlocfilehash: faa181090efa7c4064a30b42d83afa4888e98b82
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "45638478"
---
# <a name="boolean-operators"></a>Opérateurs booléens

Cette rubrique décrit la prise en charge pour les opérateurs booléens dans le langage F#.

## <a name="summary-of-boolean-operators"></a>Résumé des opérateurs booléens

Le tableau suivant récapitule les opérateurs booléens sont disponibles dans le langage F#. Le seul type pris en charge par ces opérateurs est le `bool` type.

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
