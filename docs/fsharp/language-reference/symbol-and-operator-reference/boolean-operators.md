---
title: Opérateurs booléens (F#)
description: 'Obtenir des informations sur les opérateurs booléens sont disponibles dans le langage de programmation F #.'
ms.date: 05/16/2016
ms.openlocfilehash: f8516ceb531907400f98dc4226d2985d3119e9e9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="boolean-operators"></a>Opérateurs booléens

Cette rubrique décrit la prise en charge des opérateurs booléens dans le langage F #.


## <a name="summary-of-boolean-operators"></a>Résumé des opérateurs booléens
Le tableau suivant récapitule les opérateurs booléens sont disponibles dans le langage F #. Le seul type pris en charge par ces opérateurs est le `bool` type.

|Opérateur|Description|
|--------|-----------|
|`not`|Négation booléenne|
|<code>&#124;&#124;</code>|Booléen OR|
|`&&`|Booléen AND|

Les opérateurs booléens AND et OR effectuent *l’évaluation de court-circuit*, autrement dit, elles évaluent l’expression à droite de l’opérateur uniquement lorsqu’il est nécessaire de déterminer le résultat global de l’expression. La deuxième expression de la `&&` opérateur est évalué uniquement si la première expression a la valeur `true`; la deuxième expression de la `||` opérateur est évalué uniquement si la première expression a la valeur `false`.

## <a name="see-also"></a>Voir aussi
[Opérateurs au niveau du bit](bitwise-operators.md)

[Opérateurs arithmétiques](arithmetic-operators.md)

[Informations de référence des symboles et opérateurs](index.md)
