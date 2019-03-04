---
title: "Procédure : Utiliser un dictionnaire pour stocker des instances d'événements - Guide de programmation C#"
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- events [C#], storing instances in a Dictionary
ms.assetid: 9512c64d-5aaf-40cd-b941-ca2a592f0064
ms.openlocfilehash: f3b8e313bd0b1bd3973102caebb9bbc9da620ae6
ms.sourcegitcommit: 41c0637e894fbcd0713d46d6ef1866f08dc321a2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/01/2019
ms.locfileid: "57203030"
---
# <a name="how-to-use-a-dictionary-to-store-event-instances-c-programming-guide"></a><span data-ttu-id="c3659-102">Procédure : Utiliser un dictionnaire pour stocker des instances d'événements (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="c3659-102">How to: Use a Dictionary to Store Event Instances (C# Programming Guide)</span></span>
<span data-ttu-id="c3659-103">Une des façons d’utiliser `accessor-declarations` consiste à exposer un grand nombre d’événements sans allouer de champ à chaque événement, mais en utilisant à la place un dictionnaire pour stocker les instances d’événements.</span><span class="sxs-lookup"><span data-stu-id="c3659-103">One use for `accessor-declarations` is to expose many events without allocating a field for each event, but instead using a Dictionary to store the event instances.</span></span> <span data-ttu-id="c3659-104">Cette méthode n’est utile qu’en présence d’un grand nombre d’événements dont la plupart ne seront pas implémentés.</span><span class="sxs-lookup"><span data-stu-id="c3659-104">This is only useful if you have many events, but you expect most of the events will not be implemented.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c3659-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="c3659-105">Example</span></span>  
 [!code-csharp[csProgGuideEvents#9](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideEvents/CS/Events.cs#9)]  
  
## <a name="see-also"></a><span data-ttu-id="c3659-106">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3659-106">See also</span></span>

- [<span data-ttu-id="c3659-107">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="c3659-107">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="c3659-108">Événements</span><span class="sxs-lookup"><span data-stu-id="c3659-108">Events</span></span>](../../../csharp/programming-guide/events/index.md)
- [<span data-ttu-id="c3659-109">Délégués</span><span class="sxs-lookup"><span data-stu-id="c3659-109">Delegates</span></span>](../../../csharp/programming-guide/delegates/index.md)
