---
title: "Procédure : Utiliser un dictionnaire pour stocker des instances d'événements - Guide de programmation C#"
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- events [C#], storing instances in a Dictionary
ms.assetid: 9512c64d-5aaf-40cd-b941-ca2a592f0064
ms.openlocfilehash: 819c81aed3a6f09a20e51285058dcc77749dd33a
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53245140"
---
# <a name="how-to-use-a-dictionary-to-store-event-instances-c-programming-guide"></a><span data-ttu-id="ff47a-102">Procédure : Utiliser un dictionnaire pour stocker des instances d'événements (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="ff47a-102">How to: Use a Dictionary to Store Event Instances (C# Programming Guide)</span></span>
<span data-ttu-id="ff47a-103">Une des façons d’utiliser `accessor-declarations` consiste à exposer un grand nombre d’événements sans allouer de champ à chaque événement, mais en utilisant à la place un dictionnaire pour stocker les instances d’événements.</span><span class="sxs-lookup"><span data-stu-id="ff47a-103">One use for `accessor-declarations` is to expose many events without allocating a field for each event, but instead using a Dictionary to store the event instances.</span></span> <span data-ttu-id="ff47a-104">Cette méthode n’est utile qu’en présence d’un grand nombre d’événements dont la plupart ne seront pas implémentés.</span><span class="sxs-lookup"><span data-stu-id="ff47a-104">This is only useful if you have many events, but you expect most of the events will not be implemented.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ff47a-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="ff47a-105">Example</span></span>  
 [!code-csharp[csProgGuideEvents#9](../../../csharp/programming-guide/events/codesnippet/CSharp/how-to-use-a-dictionary-to-store-event-instances_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="ff47a-106">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff47a-106">See Also</span></span>

- [<span data-ttu-id="ff47a-107">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="ff47a-107">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="ff47a-108">Événements</span><span class="sxs-lookup"><span data-stu-id="ff47a-108">Events</span></span>](../../../csharp/programming-guide/events/index.md)  
- [<span data-ttu-id="ff47a-109">Délégués</span><span class="sxs-lookup"><span data-stu-id="ff47a-109">Delegates</span></span>](../../../csharp/programming-guide/delegates/index.md)
