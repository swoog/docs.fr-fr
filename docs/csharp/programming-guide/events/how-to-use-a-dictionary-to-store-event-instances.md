---
title: "Comment : utiliser un dictionnaire pour stocker des instances d'événements (Guide de programmation C#)"
ms.date: 07/20/2015
helpviewer_keywords:
- events [C#], storing instances in a Dictionary
ms.assetid: 9512c64d-5aaf-40cd-b941-ca2a592f0064
ms.openlocfilehash: c3a804ce1bf1f5ac8db47f0f0c1f37d1ca5f781b
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44213171"
---
# <a name="how-to-use-a-dictionary-to-store-event-instances-c-programming-guide"></a><span data-ttu-id="0dce1-102">Comment : utiliser un dictionnaire pour stocker des instances d'événements (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="0dce1-102">How to: Use a Dictionary to Store Event Instances (C# Programming Guide)</span></span>
<span data-ttu-id="0dce1-103">Une des façons d’utiliser `accessor-declarations` consiste à exposer un grand nombre d’événements sans allouer de champ à chaque événement, mais en utilisant à la place un dictionnaire pour stocker les instances d’événements.</span><span class="sxs-lookup"><span data-stu-id="0dce1-103">One use for `accessor-declarations` is to expose many events without allocating a field for each event, but instead using a Dictionary to store the event instances.</span></span> <span data-ttu-id="0dce1-104">Cette méthode n’est utile qu’en présence d’un grand nombre d’événements dont la plupart ne seront pas implémentés.</span><span class="sxs-lookup"><span data-stu-id="0dce1-104">This is only useful if you have many events, but you expect most of the events will not be implemented.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0dce1-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="0dce1-105">Example</span></span>  
 [!code-csharp[csProgGuideEvents#9](../../../csharp/programming-guide/events/codesnippet/CSharp/how-to-use-a-dictionary-to-store-event-instances_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="0dce1-106">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0dce1-106">See Also</span></span>

- [<span data-ttu-id="0dce1-107">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="0dce1-107">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="0dce1-108">Événements</span><span class="sxs-lookup"><span data-stu-id="0dce1-108">Events</span></span>](../../../csharp/programming-guide/events/index.md)  
- [<span data-ttu-id="0dce1-109">Délégués</span><span class="sxs-lookup"><span data-stu-id="0dce1-109">Delegates</span></span>](../../../csharp/programming-guide/delegates/index.md)
