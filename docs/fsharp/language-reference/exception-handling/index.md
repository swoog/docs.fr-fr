---
title: Gestion des exceptions
description: Découvrez les principes fondamentaux de la gestion des exceptions dans F# et découvrez des liens vers les expressions et fonctions de gestion des exceptions.
ms.date: 05/16/2016
ms.openlocfilehash: 187236ca380c7de0b3714160f6c3703f8fb93d5a
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53614439"
---
# <a name="exception-handling"></a>Gestion des exceptions

Cette section contient des informations sur la prise en charge de la gestion des exceptions en langage F#.

## <a name="exception-handling-basics"></a>Concepts de base de la gestion des exceptions
La gestion des exceptions constitue le moyen standard de gérer les conditions d’erreur dans le .NET Framework. Par conséquent, tout langage .NET doit prendre en charge ce mécanisme, notamment F#. Une *exception* est un objet qui encapsule des informations sur une erreur. Quand des erreurs se produisent, des exceptions sont déclenchées et l’exécution normale s’arrête. Le runtime recherche alors un gestionnaire approprié pour l’exception. La recherche démarre dans la fonction active et remonte dans la pile en passant par les couches d’appelants jusqu’à ce qu’un gestionnaire correspondant soit trouvé. Le gestionnaire est ensuite exécuté.

De plus, à mesure que la pile est déroulée, le runtime exécute le code présent dans les blocs `finally` pour garantir que les objets sont nettoyés correctement pendant le processus de déroulement.

## <a name="related-topics"></a>Rubriques connexes

|Titre|Description|
|-----|-----------|
|[Types d'exceptions](exception-types.md)|Décrit comment déclarer un type d’exception.|
|[Exceptions : Le `try...with` Expression](the-try-with-expression.md)|Décrit la construction de langage qui prend en charge la gestion des exceptions.|
|[Exceptions : Le `try...finally` Expression](the-try-finally-expression.md)|Décrit la construction de langage qui vous permet d’exécuter du code de nettoyage à mesure que la pile se déroule quand une exception est levée.|
|[Exceptions : fonction `raise`](the-raise-Function.md)|Décrit comment lever un objet exception.|
|[Exceptions : Le `failwith` (fonction)](the-failwith-function.md)|Décrit comment générer une exception F# générale.|
|[Exceptions : Le `invalidArg` (fonction)](the-invalidArg-function.md)|Décrit comment générer une exception d’argument non valide.|