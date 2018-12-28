---
title: 'Gestion des ressources : L’utilisation du mot clé'
description: En savoir plus sur les F# mot clé 'use' et la fonction 'using', qui permettre contrôler l’initialisation et la libération de ressources.
ms.date: 05/16/2016
ms.openlocfilehash: 127877a3823faade9bc3c6aefea655c86cc348e7
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53613087"
---
# <a name="resource-management-the-use-keyword"></a>Gestion des ressources : L’utilisation du mot clé

Cette rubrique décrit le mot clé `use` et `using` (fonction), qui peut contrôler l’initialisation et la libération de ressources.

## <a name="resources"></a>Ressources

Le terme *ressource* est utilisé dans plusieurs façons. Oui, les ressources peuvent être des données par une application, telles que des chaînes, des graphiques et autres, mais dans ce contexte, *ressources* fait référence aux ressources de système d’exploitation ou des logiciels, telles que les contextes de périphérique de graphiques, les descripteurs de fichiers réseau base de données et connexions, les objets d’accès concurrentiel tels que les handles d’attente et ainsi de suite. L’utilisation de ces ressources par les applications implique l’acquisition de la ressource à partir du système d’exploitation ou d’autres fournisseurs de ressources, suivie de la libération de la ressource pour le pool afin qu’elle peut être fournie à une autre application. Problèmes se produisent lorsque les applications ne libèrent pas de ressources vers le pool commun.

## <a name="managing-resources"></a>Gestion des ressources

Pour gérer les ressources dans une application efficacement et de façon responsable, vous devez libérer les ressources rapidement et de manière prévisible. Le .NET Framework vous permet de faire en fournissant le `System.IDisposable` interface. Un type qui implémente `System.IDisposable` a le `System.IDisposable.Dispose` (méthode), ce qui libère les ressources correctement. Applications bien écrites garantissent que `System.IDisposable.Dispose` est appelé rapidement lorsqu’un objet qui contient une ressource limitée n’est plus nécessaire. Heureusement, la plupart des langages .NET prennent en charge pour simplifier ce processus, et F# ne fait pas exception. Il existe deux constructions de langage utiles qui prennent en charge le modèle de suppression : le `use` liaison et le `using` (fonction).

## <a name="use-binding"></a>Utiliser la liaison

Le `use` mot clé a une forme semblable à celle de la `let` liaison :

Utilisez *valeur* = *expression*

Il fournit les mêmes fonctionnalités qu’un `let` de liaison, mais ajoute un appel à `Dispose` sur la valeur lorsque la valeur est hors de portée. Notez que le compilateur insère une vérification de valeur null sur la valeur, afin que si la valeur est `null`, l’appel à `Dispose` n’est pas tentée.

L’exemple suivant montre comment fermer automatiquement un fichier à l’aide de la `use` mot clé.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6301.fs)]

> [!NOTE]
> Vous pouvez utiliser `use` dans les expressions de calcul, auquel cas une version personnalisée de la `use` expression est utilisée. Pour plus d’informations, consultez [séquences](sequences.md), [flux de travail asynchrones](asynchronous-workflows.md), et [Expressions de calcul](computation-expressions.md).

## <a name="using-function"></a>à l’aide de la fonction

Le `using` fonction a la forme suivante :

`using` (*expression1*) *-ou-lambda function*

Dans un `using` expression, *expression1* crée l’objet qui doit être supprimée. Le résultat de *expression1* (l’objet qui doit être supprimé) devienne un argument, *valeur*à *lambda function ou*, qui est soit une fonction qui attend un seul restant argument d’un type qui correspond à la valeur produite par *expression1*, ou une expression lambda qui attend un argument de ce type. À la fin de l’exécution de la fonction, le runtime appelle `Dispose` et libère les ressources (sauf si la valeur est `null`, auquel cas l’appel à Dispose n’est pas tentée).

L’exemple suivant montre le `using` expression avec une expression lambda.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6302.fs)]

L’exemple suivant montre le `using` expression avec une fonction.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6303.fs)]

Notez que la fonction peut être une fonction qui a des arguments déjà appliqués. L'exemple de code suivant illustre cette tâche. Elle crée un fichier qui contient la chaîne `XYZ`.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6304.fs)]

Le `using` (fonction) et le `use` liaison sont presque différentes façons d’accomplir la même chose. Le `using` mot clé fournit davantage de contrôle sur quand `Dispose` est appelée. Lorsque vous utilisez `using`, `Dispose` est appelée à la fin de la fonction ou une expression lambda ; lorsque vous utilisez le `use` mot clé, `Dispose` est appelée à la fin du bloc de code contenant. En règle générale, vous préférez utiliser `use` au lieu du `using` (fonction).

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)