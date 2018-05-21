---
title: 'Guide de style F #'
description: 'Découvrez les principes de cinq du bon code F #.'
ms.date: 05/14/2018
ms.openlocfilehash: 6d8c1336ca991040a8f6e13290d209cb3b70054d
ms.sourcegitcommit: 22c3c8f74eaa138dbbbb02eb7d720fce87fc30a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2018
---
# <a name="f-style-guide"></a>Guide de style F #

Les articles suivants décrivent les instructions pour la mise en forme du code F # et conseils applique des fonctionnalités du langage et comment ils doivent être utilisées.

Ce guide a été formulé en fonction de l’utilisation de F # dans les grandes bases de code avec un large éventail de programmeurs. En règle générale, ce guide entraîne l’utilisation réussie de F # et réduit les frustrations lors de la configuration requise pour les programmes changer au fil du temps.

## <a name="five-principles-of-good-f-code"></a>Cinq principes du bon code F #

Vous devez conserver les principes suivants à l’esprit lorsque vous entrez un code F #, notamment dans les systèmes qui changent au fil du temps. Chaque partie du guide dans les autres articles provient de ces cinq points.

1. **Bon code F # est succinctes et expressives**

    F # propose de nombreuses fonctionnalités qui vous permettent de désignent des actions dans moins de lignes de code et de réutiliser les fonctionnalités génériques. La bibliothèque principale F # contient également de nombreux types utiles et fonctions permettant de travailler avec des collections de données courantes. En règle générale, si vous pouvez exprimer une solution à un problème dans moins de lignes de code, les autres développeurs (ou votre self futures) sera appreciative. Il est également recommandé que vous utilisez une bibliothèque, par exemple FSharp.Core, le [grandes bibliothèques .NET](https://docs.microsoft.com/dotnet/api/) fonctionnant F #, ou un package tiers sur [NuGet](https://www.nuget.org/) lorsque vous devez effectuer une tâche non triviale.

2. **Bon code F # est interopérable**

    Interopérabilité peut prendre plusieurs formes, y compris la consommation du code dans des langages différents. Les limites de votre code qui interopèrent avec les autres appelants sont essentielles pour obtenir le droit. Lorsque vous écrivez F #, vous devez toujours penser sur comment d’autres code appelle le code que vous écrivez, notamment s’ils le font à partir d’un autre langage comme c#. Le [règles de conception du composant F #](component-design-guidelines.md) décrivent l’interopérabilité en détail.

3. **Bon code F # rend utilisent de la programmation de l’objet, pas l’objet l’orientation**

    F # prend totalement en charge la programmation avec des objets dans .NET, y compris [classes](../language-reference/classes.md), [interfaces](../language-reference/interfaces.md), [les modificateurs d’accès](../language-reference/access-control.md), [declassesabstraites](../language-reference/abstract-classes.md), et ainsi de suite. Pour le code fonctionnel plus complexe, tels que les fonctions qui doivent être sensibles au contexte, les objets peuvent encapsuler facilement les informations contextuelles d’une manière qui ne peut pas de fonctions. Fonctionnalités, telles que [paramètres facultatifs](../language-reference/members/methods.md#optional-arguments) et [surcharge](../language-reference/members/methods.md#overloaded-methods) aident également la consommation de cette fonctionnalité pour les appelants.

4. **Bon code F # exécute également sans exposer mutation**

    Il n’est pas secret pour écrire du code de hautes performances, vous devez utiliser mutation. Il s’agit de fonctionnement des ordinateurs, une fois toutes les. Ce code est souvent difficile d’obtenir le droit et sujette à erreurs. Évitez d’exposer la mutation aux appelants. Recherche d’une interface fonctionnelle sur une implémentation basée sur une mutation.

5. **Bon code F # est compatible avec les outils**

    Outils sont très utiles pour l’utilisation de grandes bases de code, vous pouvez écrire du code F # tel qu’il peut être utilisé plus efficacement avec les outils de langage F #. Un exemple consiste à s’assurer, que vous n’abuser avec un style exempt de point de programmation, afin que les valeurs intermédiaires peuvent être inspectées avec un débogueur. Utilisation d’un autre exemple [les commentaires de documentation XML](../language-reference/xml-documentation.md) décrivant les constructions telles que les info-bulles dans les éditeurs peuvent afficher les commentaires sur le site d’appel. Pensez toujours comment votre code est en lecture, accédé, de débogage et manipulé par d’autres programmeurs avec leurs outils.

## <a name="next-steps"></a>Étapes suivantes

Le [les instructions de mise en forme de code F #](formatting.md) fournissent des conseils sur la mise en forme le code afin qu’il soit facile à lire.

Le [F # conventions de codage](conventions.md) fournissent des conseils pour les langages qui vous aide à la maintenance à long terme de plus grande F # de programmation F # codebases.

Le [règles de conception du composant F #](component-design-guidelines.md) fournissent des conseils pour la création de composants F #, telles que des bibliothèques.
