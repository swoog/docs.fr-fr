---
title: F#guide de style
description: Découvrez les principes de cinq bonne F# code.
ms.date: 12/10/2018
ms.openlocfilehash: 9f47257626e04b09b546de2ae315d48d791678be
ms.sourcegitcommit: 3b9b7ae6771712337d40374d2fef6b25b0d53df6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/04/2019
ms.locfileid: "54030267"
---
# <a name="f-style-guide"></a>F#guide de style

Les articles suivants décrivent les instructions pour mettre en forme F# code et les conseils thématiques pour les fonctionnalités du langage et comment ils doivent être utilisés.

Ce guide a été formulé selon l’utilisation de F# dans des codes base volumineux avec un groupe diversifié des programmeurs. Ce guide conduit généralement à l’utilisation réussie de F# et réduit les frustrations lors de la configuration requise pour les programmes changer au fil du temps.

## <a name="five-principles-of-good-f-code"></a>Cinq principes bonne F# code

Gardez les principes suivants à l’esprit lorsque vous entrez F# code, en particulier dans les systèmes qui va changer au fil du temps. Chaque élément de conseils dans d’autres articles provient de ces cinq points.

1. **Bonne F# code est succinct, expressif et composable**

    F#possède de nombreuses fonctionnalités qui vous permettent d’exprimer des actions dans moins de lignes de code et de réutiliser les fonctionnalités génériques. Le F# bibliothèque principale contient également de nombreux types utiles et des fonctions pour travailler avec des collections de données courantes. Composition de vos propres fonctions et de celles figurant dans le F# bibliothèque principale (ou autres bibliothèques) fait partie de la routine IDIOMATIQUE F# de programmation. En règle générale, si une solution à un problème dans moins de lignes de code, vous pouvez exprimer des autres développeurs (ou votre self futures) sera développeurs. Il est également recommandé que vous utilisez une bibliothèque de FSharp.Core, le [des bibliothèques .NET vastes](../../../api/index.md) qui F# s’exécute, ou un package tiers sur [NuGet](https://www.nuget.org/) lorsque vous avez besoin effectuer une tâche non triviale.

2. **Bonne F# code est interopérable**

    L’interopérabilité peut prendre plusieurs formes, y compris la consommation du code dans différentes langues. Les limites de votre code qui interopèrent avec les autres appelants sont essentielles à coup, même si les appelants se trouvent également dans F#. Lors de l’écriture F#, vous devez toujours de penser sur la façon dont tout autre code appellera le code que vous écrivez, notamment s’ils le font à partir d’un autre langage tel que C#. Le [ F# les instructions de conception de composant](component-design-guidelines.md) décrivent l’interopérabilité en détail.

3. **Bonne F# code rend l’utilisation de la programmation de l’objet, pas l’objet orientation**

    F#a une prise en charge complète pour la programmation avec des objets dans .NET, y compris [classes](../language-reference/classes.md), [interfaces](../language-reference/interfaces.md), [modificateurs d’accès](../language-reference/access-control.md), [declassesabstraites](../language-reference/abstract-classes.md), et ainsi de suite. Pour le code fonctionnel plus complexe, tels que les fonctions qui doivent être sensibles au contexte, les objets peuvent encapsuler facilement des informations contextuelles de façons qui ne peut pas de fonctions. Fonctionnalités telles que [paramètres facultatifs](../language-reference/members/methods.md#optional-arguments) et usage modéré des [surcharge](../language-reference/members/methods.md#overloaded-methods) peut faciliter la consommation de cette fonctionnalité pour les appelants.

4. **Bonne F# code effectue également sans exposer de mutation**

    Il n’est aucun secret pour écrire du code de hautes performances, vous devez utiliser mutation. Il est ordinateurs fonctionnement, après tout. Ce code est souvent sujettes aux erreurs et difficile à réaliser correctement. Évitez d’exposer la mutation aux appelants. Au lieu de cela, [créer une interface fonctionnelle qui masque une implémentation basée sur une mutation](conventions.md#performance) lorsque la performance est critique.

5. **Bonne F# code est compatible avec les outils**

    Outils sont très utiles pour travailler dans les grandes bases de code, et vous pouvez écrire F# telles qu’il puisse être utilisé plus efficacement avec du code F# outils de langage. Un exemple consiste à s’assurer que vous ne pas abuser de cette possibilité avec un style libre de point de programmation, afin que les valeurs intermédiaires peuvent être inspectées avec un débogueur. À l’aide d’un autre exemple [commentaires de documentation XML](../language-reference/xml-documentation.md) décrivant les constructions telles que les info-bulles dans les éditeurs peuvent afficher ces commentaires sur le site d’appel. Envisagez toujours comment votre code est lu, cible de la navigation, de débogage et manipulé par d’autres programmeurs avec leurs outils.

## <a name="next-steps"></a>Étapes suivantes

Le [ F# code de mise en forme des lignes directrices](formatting.md) fournissent des conseils sur la mise en forme le code afin qu’il soit facile à lire.

Le [ F# conventions de codage](conventions.md) fournissent des conseils pour F# langages qui vous aide à la maintenance à long terme de la plus grande de programmation F# codes base.

Le [ F# les instructions de conception de composant](component-design-guidelines.md) fournissent des conseils pour la création de F# composants, tels que les bibliothèques.
