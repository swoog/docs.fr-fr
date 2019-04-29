---
title: 'Exceptions : try...with (expression)'
description: Découvrez comment utiliser le F# 'try... with' expression pour la gestion des exceptions.
ms.date: 05/16/2016
ms.openlocfilehash: 742e0b595525c69b83a55682c3c8b9b650326ac7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61945533"
---
# <a name="exceptions-the-trywith-expression"></a>Exceptions : try...with (expression)

Cette rubrique décrit la `try...with` expression, l’expression qui est utilisée pour la gestion des exceptions dans le F# langage.

## <a name="syntax"></a>Syntaxe

```fsharp
try
    expression1
with
| pattern1 -> expression2
| pattern2 -> expression3
...
```

## <a name="remarks"></a>Notes

Le `try...with` expression est utilisée pour gérer des exceptions dans F#. Elle est similaire à la `try...catch` instruction en langage c#. Dans la syntaxe précédente, le code dans *expression1* peut générer une exception. Le `try...with` expression retourne une valeur. Si aucune exception n’est levée, l’expression entière retourne la valeur de *expression1*. Si une exception est levée, chacun *modèle* est ensuite comparé avec l’exception et pour le premier modèle correspondant, correspondant *expression*, connu sous le *Gestionnaire d’exceptions*, pour cette branche est exécutée, et l’expression globale retourne la valeur de l’expression dans ce gestionnaire d’exceptions. Si aucun modèle ne correspond, l’exception se propage la pile des appels jusqu'à ce qu’un gestionnaire correspondant est trouvé. Les types des valeurs retournées de chaque expression dans les gestionnaires d’exceptions doivent correspondre au type retourné à partir de l’expression dans le `try` bloc.

Fréquemment, le fait qu’une erreur s’est produite également signifie qu’il n’existe aucune valeur valide qui peut être retournée par les expressions dans chaque gestionnaire d’exceptions. Un modèle fréquent consiste à avoir le type de l’expression à être un type d’option. L’exemple de code suivant illustre ce modèle.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet5601.fs)]

Les exceptions peuvent être des exceptions .NET, ou ils peuvent être F# exceptions. Vous pouvez définir F# exceptions à l’aide de la `exception` mot clé.

Vous pouvez utiliser divers modèles de filtrer sur le type d’exception et d’autres conditions ; les options sont résumées dans le tableau suivant.

|Motif|Description|
|-------|-----------|
|:? *exception-type*|Correspond au type d’exception .NET spécifié.|
|:? *type d’exception* comme *identificateur*|Correspond au type d’exception .NET spécifié, mais donne une valeur nommée à l’exception.|
|*exception-name*(*arguments*)|Correspond à un F# type d’exception et lie les arguments.|
|*identifier*|Correspond à n’importe quelle exception et lie le nom à l’objet exception. Équivalent à **: ? System.Exception comme**_identificateur_|
|*identificateur* lorsque *condition*|Correspond à une exception si la condition est vraie.|

## <a name="examples"></a>Exemples

Les exemples de code suivants illustrent l’utilisation des différents modèles de gestionnaire d’exception.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet5602.fs)]

> [!NOTE]
> Le `try...with` construction est une expression distincte à partir de la `try...finally` expression. Par conséquent, si votre code requiert à la fois un `with` bloc et un `finally` bloc, vous devez imbriquer les deux expressions.

> [!NOTE]
> Vous pouvez utiliser `try...with` dans les workflows asynchrones et autres expressions de calcul, dans lequel cas une version personnalisée de la `try...with` expression est utilisée. Pour plus d’informations, consultez [flux de travail asynchrones](../asynchronous-workflows.md), et [Expressions de calcul](../computation-expressions.md).

## <a name="see-also"></a>Voir aussi

- [Gestion des exceptions](index.md)
- [Types d'exceptions](exception-types.md)
- [Exceptions : Le `try...finally` Expression](the-try-finally-expression.md)