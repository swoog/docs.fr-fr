---
title: "Procédure : Implémenter de manière explicite des membres d'interface - Guide de programmation C#"
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- interfaces [C#], explicitly implementing
ms.assetid: 514cde76-f981-474e-8b40-9493619f899c
ms.openlocfilehash: 8cef6c840bf6afff8ccbf7d02012990e11d47991
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64595369"
---
# <a name="how-to-explicitly-implement-interface-members-c-programming-guide"></a><span data-ttu-id="2d9a2-102">Procédure : Implémenter de manière explicite des membres d'interface (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="2d9a2-102">How to: Explicitly Implement Interface Members (C# Programming Guide)</span></span>
<span data-ttu-id="2d9a2-103">Cet exemple déclare une [interface](../../../csharp/language-reference/keywords/interface.md), `IDimensions` et une classe `Box`, qui implémente de manière explicite les membres d’interface `getLength` et `getWidth`.</span><span class="sxs-lookup"><span data-stu-id="2d9a2-103">This example declares an [interface](../../../csharp/language-reference/keywords/interface.md), `IDimensions`, and a class, `Box`, which explicitly implements the interface members `getLength` and `getWidth`.</span></span> <span data-ttu-id="2d9a2-104">Les membres sont accessibles via l’instance d’interface `dimensions`.</span><span class="sxs-lookup"><span data-stu-id="2d9a2-104">The members are accessed through the interface instance `dimensions`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2d9a2-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="2d9a2-105">Example</span></span>  
 [!code-csharp[csProgGuideInheritance#8](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideInheritance/CS/Inheritance.cs#8)]  
  
## <a name="robust-programming"></a><span data-ttu-id="2d9a2-106">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="2d9a2-106">Robust Programming</span></span>  
  
- <span data-ttu-id="2d9a2-107">Notez que les lignes suivantes de la méthode `Main` sont commentées car elles produiraient des erreurs de compilation.</span><span class="sxs-lookup"><span data-stu-id="2d9a2-107">Notice that the following lines, in the `Main` method, are commented out because they would produce compilation errors.</span></span> <span data-ttu-id="2d9a2-108">Un membre d’interface qui est implémenté de façon explicite n’est pas accessible à partir d’une instance de [classe](../../../csharp/language-reference/keywords/class.md) :</span><span class="sxs-lookup"><span data-stu-id="2d9a2-108">An interface member that is explicitly implemented cannot be accessed from a [class](../../../csharp/language-reference/keywords/class.md) instance:</span></span>  
  
     [!code-csharp[csProgGuideInheritance#45](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideInheritance/CS/Inheritance.cs#45)]  
  
- <span data-ttu-id="2d9a2-109">Notez également que les lignes suivantes de la méthode `Main` impriment correctement les dimensions de la zone, car les méthodes sont appelées à partir d’une instance de l’interface :</span><span class="sxs-lookup"><span data-stu-id="2d9a2-109">Notice also that the following lines, in the `Main` method, successfully print out the dimensions of the box because the methods are being called from an instance of the interface:</span></span>  
  
     [!code-csharp[csProgGuideInheritance#46](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideInheritance/CS/Inheritance.cs#46)]  
  
## <a name="see-also"></a><span data-ttu-id="2d9a2-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d9a2-110">See also</span></span>

- [<span data-ttu-id="2d9a2-111">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="2d9a2-111">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="2d9a2-112">Classes et structs</span><span class="sxs-lookup"><span data-stu-id="2d9a2-112">Classes and Structs</span></span>](../../../csharp/programming-guide/classes-and-structs/index.md)
- [<span data-ttu-id="2d9a2-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="2d9a2-113">Interfaces</span></span>](../../../csharp/programming-guide/interfaces/index.md)
- [<span data-ttu-id="2d9a2-114">Guide pratique pour implémenter de manière explicite des membres de deux interfaces</span><span class="sxs-lookup"><span data-stu-id="2d9a2-114">How to: Explicitly Implement Members of Two Interfaces</span></span>](../../../csharp/programming-guide/interfaces/how-to-explicitly-implement-members-of-two-interfaces.md)
