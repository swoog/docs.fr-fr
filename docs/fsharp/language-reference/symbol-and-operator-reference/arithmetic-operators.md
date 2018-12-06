---
title: Opérateurs arithmétiques (F#)
description: En savoir plus sur les opérateurs arithmétiques qui sont disponibles dans le F# langage de programmation.
ms.date: 04/04/2018
ms.openlocfilehash: 2c0e2e25a4f79d00455d978e235e4bef16b52586
ms.sourcegitcommit: 6ae7cdd0437a32884556dd4826ca90e957b7a4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/06/2018
ms.locfileid: "45597426"
---
# <a name="arithmetic-operators"></a>Opérateurs arithmétiques

Cette rubrique décrit les opérateurs arithmétiques qui sont disponibles dans le F# langage.

## <a name="summary-of-binary-arithmetic-operators"></a>Résumé des opérateurs arithmétiques

Le tableau suivant récapitule les opérateurs arithmétiques sont disponibles pour les types intégraux et à virgule flottante unboxed.

|Opérateur binaire|Notes|
|---------------|-----|
|`+` (addition, ainsi que)|Elle est désactivée. Condition de dépassement possible lorsque les nombres sont ajoutés et la somme dépasse la valeur absolue maximale prise en charge par le type.|
|`-` (soustraction, moins)|Elle est désactivée. Condition de dépassement de capacité négatif possible lors de la soustrayant des types non signés, ou lorsque les valeurs à virgule flottante sont trop petits pour être représentée par le type.|
|`*` (multiplication, fois)|Elle est désactivée. Condition de dépassement de capacité possible lorsque les nombres sont multipliés et le produit dépasse la valeur absolue maximale prise en charge par le type.|
|`/` (division, divisé par)|Division par zéro provoque un <xref:System.DivideByZeroException> pour les types intégraux. Pour les types à virgule flottante, division par zéro vous donne les valeurs à virgule flottante spéciales `+Infinity` ou `-Infinity`. Il existe également une condition de dépassement de capacité négatif possible lorsqu’un nombre à virgule flottante est trop petit pour être représenté par le type.|
|`%` (reste, rem)|Retourne le reste d’une opération de division. Le signe du résultat est identique à celui du premier opérande.|
|`**` (élévation à la puissance de)|Condition de dépassement possible lorsque le résultat dépasse la valeur absolue maximale pour le type.<br /><br />L’opérateur d’élévation fonctionne uniquement avec les types à virgule flottante.|

## <a name="summary-of-unary-arithmetic-operators"></a>Résumé des opérateurs arithmétiques unaires

Le tableau suivant récapitule les opérateurs arithmétiques unaires qui sont disponibles pour les types intégraux et à virgule flottante.

|Opérateur unaire|Notes|
|--------------|-----|
|`+` (positif)|Peut être appliqué à n’importe quelle expression arithmétique. Ne modifie pas le signe de la valeur.|
|`-` (négation, négatif)|Peut être appliqué à n’importe quelle expression arithmétique. Change le signe de la valeur.|

Le comportement de dépassement de capacité positif ou négatif pour les types intégraux consiste à encapsuler. Cela entraîne un résultat incorrect. Dépassement sur les entiers est un problème potentiellement grave qui peut contribuer à des problèmes de sécurité lorsque le logiciel n’est pas écrite pour prendre en compte pour qu’il. S’il s’agit d’un critère important pour votre application, envisagez d’utiliser les opérateurs checked dans `Microsoft.FSharp.Core.Operators.Checked`.

## <a name="summary-of-binary-comparison-operators"></a>Résumé des opérateurs de comparaison binaires

Le tableau suivant répertorie les opérateurs de comparaison binaires qui sont disponibles pour les types intégraux et à virgule flottante. Ces opérateurs retournent des valeurs de type `bool`.

Nombres à virgule flottante doit jamais directement comparer l’égalité, étant donné que la représentation à virgule flottante IEEE ne prend pas en charge une opération d’égalité exacte. Deux nombres que vous pouvez facilement vérifier égal en examinant le code peut avoir réellement différentes représentations.

|Opérateur|Notes|
|--------|-----|
|`=` (égalité, égal à)|Ce n’est pas un opérateur d’assignation. Il est utilisé uniquement pour la comparaison. Il s’agit d’un opérateur générique.|
|`>` (supérieur à)|Il s’agit d’un opérateur générique.|
|`<` (inférieur à)|Il s’agit d’un opérateur générique.|
|`>=` (supérieur ou égal à)|Il s’agit d’un opérateur générique.|
|`<=` (inférieur ou égal à)|Il s’agit d’un opérateur générique.|
|`<>` (non égal)|Il s’agit d’un opérateur générique.|

## <a name="overloaded-and-generic-operators"></a>Opérateurs surchargés et génériques

Tous les opérateurs décrits dans cette rubrique sont définis dans le **Microsoft.FSharp.Core.Operators** espace de noms. Certains des opérateurs sont définis à l’aide des paramètres de type résolus statiquement. Cela signifie qu’il n’y a des définitions individuelles pour chaque type spécifique qui fonctionne avec cet opérateur. Tous les opérateurs unaires et binaires arithmétiques et au niveau du bit sont dans cette catégorie. Les opérateurs de comparaison sont génériques et par conséquent fonctionnent avec n’importe quel type, pas simplement primitifs types arithmétiques. Union discriminée et les types d’enregistrements ont leurs propres implémentations personnalisées qui sont générées par le F# compilateur. Types de classe utilisent la méthode <xref:System.Object.Equals%2A>.

Les opérateurs génériques sont personnalisables. Pour personnaliser les fonctions de comparaison, substituez <xref:System.Object.Equals%2A> pour fournir votre propre comparaison d’égalité personnalisée, puis implémentez <xref:System.IComparable>. Le <xref:System.IComparable?displayProperty=nameWithType> interface a une méthode unique, le <xref:System.IComparable.CompareTo%2A> (méthode).

## <a name="operators-and-type-inference"></a>Opérateurs et inférence de Type

L’utilisation d’un opérateur dans une expression contraint l’inférence de type sur cet opérateur. En outre, l’utilisation d’opérateurs empêche la généralisation automatique, car l’utilisation d’opérateurs implique un type arithmétique. En l’absence de toute autre information le F# compilateur déduit `int` comme type d’expressions arithmétiques. Vous pouvez remplacer ce comportement en spécifiant un autre type. Par conséquent les types d’arguments et le type de retour de `function1` dans le code suivant sont déduits pour être `int`, mais les types de `function2` sont déduits pour être `float`.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3501.fs)]

## <a name="see-also"></a>Voir aussi

- [Informations de référence des symboles et opérateurs](index.md)
- [Surcharge d'opérateur](../operator-overloading.md)
- [Opérateurs au niveau du bit](bitwise-operators.md)
- [Opérateurs booléens](boolean-operators.md)
