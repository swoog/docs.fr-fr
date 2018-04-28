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
