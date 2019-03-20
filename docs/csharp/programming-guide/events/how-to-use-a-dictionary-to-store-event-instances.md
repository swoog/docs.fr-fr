---
title: 'Guide pratique : Utiliser un dictionnaire pour stocker des instances d’événements – Guide de programmation C#'
ms.custom: seodec18
ms.date: 03/11/2019
helpviewer_keywords:
- events [C#], storing instances in a Dictionary
ms.assetid: 9512c64d-5aaf-40cd-b941-ca2a592f0064
ms.openlocfilehash: f8522e499887398402f63c7788bbc6c6c4f57782
ms.sourcegitcommit: 16aefeb2d265e69c0d80967580365fabf0c5d39a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2019
ms.locfileid: "57845270"
---
# <a name="how-to-use-a-dictionary-to-store-event-instances-c-programming-guide"></a><span data-ttu-id="1cf24-102">Guide pratique : Utiliser un dictionnaire pour stocker des instances d’événements (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="1cf24-102">How to: use a dictionary to store event instances (C# Programming Guide)</span></span>

<span data-ttu-id="1cf24-103">Les accesseurs d’événements personnalisés `add` et `remove` peuvent notamment servir à exposer un grand nombre d’événements sans allouer de champ à chacun, mais en utilisant une instance <xref:System.Collections.Generic.Dictionary%602> pour stocker les instances d’événements, comme le montre l’exemple ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="1cf24-103">One use for the `add` and `remove` custom event accessors is to expose many events without allocating a field for each event, but instead using a <xref:System.Collections.Generic.Dictionary%602> instance to store the event instances, as the example below demonstrates.</span></span> <span data-ttu-id="1cf24-104">Cette méthode n’est utile que si le site comporte de nombreux événements, dont la plupart ne seront probablement pas souscrits.</span><span class="sxs-lookup"><span data-stu-id="1cf24-104">This is only useful if a type has many events, but you expect that most of the events will not be subscribed to.</span></span>

[!code-csharp[csProgGuideEvents#9](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideEvents/CS/Events.cs#9)]

<span data-ttu-id="1cf24-105">Cette implémentation est conforme au comportement [d’ajout et de suppression de délégués](~/_csharplang/spec/delegates.md#delegate-invocation) de la spécification du langage C#.</span><span class="sxs-lookup"><span data-stu-id="1cf24-105">This implementation conforms to the behavior for [adding and removing delegates](~/_csharplang/spec/delegates.md#delegate-invocation) in the C# language specification.</span></span>

<span data-ttu-id="1cf24-106">Vous remarquerez que l’instruction [lock](../../language-reference/keywords/lock-statement.md) ne sert qu’à *accéder* au dictionnaire comportant les gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="1cf24-106">Note that the [lock](../../language-reference/keywords/lock-statement.md) statement is used only to *access* the dictionary with event handlers.</span></span> <span data-ttu-id="1cf24-107">N’appelez pas un gestionnaire d’événements se trouvant dans le corps de l’instruction `lock`, car cela pourrait entraîner des blocages ou une contention de verrouillage.</span><span class="sxs-lookup"><span data-stu-id="1cf24-107">Don't invoke an event handler inside the body of the `lock` statement, as it could lead to deadlocks or lock contention.</span></span>

## <a name="see-also"></a><span data-ttu-id="1cf24-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cf24-108">See also</span></span>

- [<span data-ttu-id="1cf24-109">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="1cf24-109">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="1cf24-110">Événements</span><span class="sxs-lookup"><span data-stu-id="1cf24-110">Events</span></span>](../../../csharp/programming-guide/events/index.md)
- [<span data-ttu-id="1cf24-111">Délégués</span><span class="sxs-lookup"><span data-stu-id="1cf24-111">Delegates</span></span>](../../../csharp/programming-guide/delegates/index.md)
