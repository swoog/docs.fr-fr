---
title: 'Guide de style F #'
description: 'Découvrez les cinq principes du bon code F #.'
ms.date: 05/14/2018
ms.openlocfilehash: 6d8c1336ca991040a8f6e13290d209cb3b70054d
ms.sourcegitcommit: 78bcb629abdbdbde0e295b4e81f350a477864aba
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/08/2018
ms.locfileid: "34235903"
---
# <a name="f-style-guide"></a>Guide de style F #

Les articles suivants décrivent les instructions pour la mise en forme du code F # et thématique concernant les fonctionnalités du langage et comment ils doivent être utilisés.

Ce guide a été formulé selon l’utilisation de F # dans les grandes bases de code avec un groupe diversifié des programmeurs. En règle générale, ce guide conduit à une utilisation efficace de F # et réduit les frustrations lors de la configuration requise pour les programmes changer au fil du temps.

## <a name="five-principles-of-good-f-code"></a>Cinq principes du bon code F #

Vous devez conserver les principes suivants à l’esprit lorsque vous créez le code F #, en particulier dans les systèmes qui va changer au fil du temps. Chaque élément de conseils dans d’autres articles provient de ces cinq points.

1. **Bon code F # est succinctes et expressives**

    F # offre de nombreuses fonctionnalités qui vous permettent d’exprimer des actions dans moins de lignes de code et de réutiliser les fonctionnalités génériques. La bibliothèque principale F # contient également de nombreux types utiles et des fonctions pour travailler avec des collections de données courantes. En règle générale, si une solution à un problème dans moins de lignes de code, vous pouvez exprimer des autres développeurs (ou votre self futures) sera développeurs. Il est également recommandé que vous utilisez une bibliothèque de FSharp.Core, le [des bibliothèques .NET vastes](https://docs.microsoft.com/dotnet/api/) que F # s’exécute, ou un package tiers sur [NuGet](https://www.nuget.org/) lorsque vous avez besoin effectuer une tâche non triviale.

2. **Bon code F # est interopérable**

    L’interopérabilité peut prendre plusieurs formes, y compris la consommation du code dans différentes langues. Les limites de votre code qui interopèrent avec les autres appelants sont essentielles pour obtenir le droit. Lors de l’écriture de F #, vous devez toujours penser sur la façon dont tout autre code appellera le code que vous écrivez, notamment s’ils le font à partir d’un autre langage tel que c#. Le [instructions de conception de composant F #](component-design-guidelines.md) décrivent l’interopérabilité en détail.

3. **Bon code F # rend l’utilisation de la programmation de l’objet, pas l’objet orientation**

    F # offre une prise en charge complète pour la programmation avec des objets dans .NET, y compris [classes](../language-reference/classes.md), [interfaces](../language-reference/interfaces.md), [modificateurs d’accès](../language-reference/access-control.md), [declassesabstraites](../language-reference/abstract-classes.md), et ainsi de suite. Pour le code fonctionnel plus complexe, tels que les fonctions qui doivent être sensibles au contexte, les objets peuvent encapsuler facilement des informations contextuelles de façons qui ne peut pas de fonctions. Fonctionnalités telles que [paramètres facultatifs](../language-reference/members/methods.md#optional-arguments) et usage modéré des [surcharge](../language-reference/members/methods.md#overloaded-methods) peut faciliter la consommation de cette fonctionnalité pour les appelants.

4. **Bon code F # effectue également sans exposer de mutation**

    Il n’est aucun secret pour écrire du code de hautes performances, vous devez utiliser mutation. Il est ordinateurs fonctionnement, après tout. Ce code est souvent sujettes aux erreurs et difficile à réaliser correctement. Évitez d’exposer la mutation aux appelants. Au lieu de cela, [créer une interface fonctionnelle qui masque une implémentation basée sur une mutation](conventions.md#performance) lorsque la performance est critique.

5. **Bon code F # est compatible avec les outils**

    Outils sont très utiles pour travailler dans les grandes bases de code, et vous pouvez écrire du code F # tels qu’il puisse être utilisé plus efficacement avec les outils de langage F #. Un exemple consiste à s’assurer que vous ne pas abuser de cette possibilité avec un style libre de point de programmation, afin que les valeurs intermédiaires peuvent être inspectées avec un débogueur. À l’aide d’un autre exemple [commentaires de documentation XML](../language-reference/xml-documentation.md) décrivant les constructions telles que les info-bulles dans les éditeurs peuvent afficher ces commentaires sur le site d’appel. Envisagez toujours comment votre code est lu, cible de la navigation, de débogage et manipulé par d’autres programmeurs avec leurs outils.

## <a name="next-steps"></a>Étapes suivantes

Le [les instructions de mise en forme de code F #](formatting.md) fournissent des conseils sur la mise en forme le code afin qu’il soit facile à lire.

Le [F # conventions de codage](conventions.md) fournissent des conseils pour les langages qui vous aide à la maintenance à long terme de plus grande F # de programmation F # des codes base.

Le [instructions de conception de composant F #](component-design-guidelines.md) fournissent des conseils pour la création de composants F #, telles que les bibliothèques.
