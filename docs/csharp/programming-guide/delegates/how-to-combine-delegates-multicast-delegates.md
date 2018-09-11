---
title: 'Comment : combiner des délégués (délégués multicast) (Guide de programmation C#)'
ms.date: 07/20/2015
helpviewer_keywords:
- delegates [C#], combining
- multicast delegates [C#]
ms.assetid: 4e689450-6d0c-46de-acfd-f961018ae5dd
ms.openlocfilehash: e3cc3f9082bd86004a7821b64c01253408c07641
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44083275"
---
# <a name="how-to-combine-delegates-multicast-delegatesc-programming-guide"></a><span data-ttu-id="2c52e-102">Comment : combiner des délégués (délégués multicast) (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="2c52e-102">How to: Combine Delegates (Multicast Delegates)(C# Programming Guide)</span></span>
<span data-ttu-id="2c52e-103">Cet exemple explique comment créer des délégués multicast.</span><span class="sxs-lookup"><span data-stu-id="2c52e-103">This example demonstrates how to create multicast delegates.</span></span> <span data-ttu-id="2c52e-104">Une propriété utile des objets [délégués](../../../csharp/language-reference/keywords/delegate.md) est que plusieurs objets peuvent être assignés à une instance de délégué à l’aide de l’opérateur `+`.</span><span class="sxs-lookup"><span data-stu-id="2c52e-104">A useful property of [delegate](../../../csharp/language-reference/keywords/delegate.md) objects is that multiple objects can be assigned to one delegate instance by using the `+` operator.</span></span> <span data-ttu-id="2c52e-105">Le délégué multicast contient une liste des délégués assignés.</span><span class="sxs-lookup"><span data-stu-id="2c52e-105">The multicast delegate contains a list of the assigned delegates.</span></span> <span data-ttu-id="2c52e-106">Quand le délégué multicast est appelé, il appelle les délégués dans la liste, dans l’ordre.</span><span class="sxs-lookup"><span data-stu-id="2c52e-106">When the multicast delegate is called, it invokes the delegates in the list, in order.</span></span> <span data-ttu-id="2c52e-107">Seuls des délégués de même type peuvent être combinés.</span><span class="sxs-lookup"><span data-stu-id="2c52e-107">Only delegates of the same type can be combined.</span></span>  
  
 <span data-ttu-id="2c52e-108">Vous pouvez utiliser l’opérateur `-` pour supprimer un délégué de composant d’un délégué multicast.</span><span class="sxs-lookup"><span data-stu-id="2c52e-108">The `-` operator can be used to remove a component delegate from a multicast delegate.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2c52e-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="2c52e-109">Example</span></span>  
 [!code-csharp[csProgGuideDelegates#11](../../../csharp/programming-guide/delegates/codesnippet/CSharp/how-to-combine-delegates-multicast-delegates_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="2c52e-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c52e-110">See Also</span></span>

- <xref:System.MulticastDelegate>  
- [<span data-ttu-id="2c52e-111">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="2c52e-111">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="2c52e-112">Événements</span><span class="sxs-lookup"><span data-stu-id="2c52e-112">Events</span></span>](../../../csharp/programming-guide/events/index.md)
