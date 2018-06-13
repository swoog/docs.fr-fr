---
title: "Comment : utiliser un dictionnaire pour stocker des instances d'événements (Guide de programmation C#)"
ms.date: 07/20/2015
helpviewer_keywords:
- events [C#], storing instances in a Dictionary
ms.assetid: 9512c64d-5aaf-40cd-b941-ca2a592f0064
ms.openlocfilehash: 97a7b0f168e4a1c81ec396f42b731dabb45b3516
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33327214"
---
# <a name="how-to-use-a-dictionary-to-store-event-instances-c-programming-guide"></a><span data-ttu-id="f30ff-102">Comment : utiliser un dictionnaire pour stocker des instances d'événements (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="f30ff-102">How to: Use a Dictionary to Store Event Instances (C# Programming Guide)</span></span>
<span data-ttu-id="f30ff-103">Une des façons d’utiliser `accessor-declarations` consiste à exposer un grand nombre d’événements sans allouer de champ à chaque événement, mais en utilisant à la place un dictionnaire pour stocker les instances d’événements.</span><span class="sxs-lookup"><span data-stu-id="f30ff-103">One use for `accessor-declarations` is to expose many events without allocating a field for each event, but instead using a Dictionary to store the event instances.</span></span> <span data-ttu-id="f30ff-104">Cette méthode n’est utile qu’en présence d’un grand nombre d’événements dont la plupart ne seront pas implémentés.</span><span class="sxs-lookup"><span data-stu-id="f30ff-104">This is only useful if you have many events, but you expect most of the events will not be implemented.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f30ff-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="f30ff-105">Example</span></span>  
 [!code-csharp[csProgGuideEvents#9](../../../csharp/programming-guide/events/codesnippet/CSharp/how-to-use-a-dictionary-to-store-event-instances_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="f30ff-106">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f30ff-106">See Also</span></span>  
 [<span data-ttu-id="f30ff-107">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="f30ff-107">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="f30ff-108">Événements</span><span class="sxs-lookup"><span data-stu-id="f30ff-108">Events</span></span>](../../../csharp/programming-guide/events/index.md)  
 [<span data-ttu-id="f30ff-109">Délégués</span><span class="sxs-lookup"><span data-stu-id="f30ff-109">Delegates</span></span>](../../../csharp/programming-guide/delegates/index.md)
