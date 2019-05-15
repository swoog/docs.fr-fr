---
title: 'Procédure : implémenter un formulaire qui utilise une opération en arrière-plan'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- threading [Windows Forms], forms
- BackgroundWorker component
- background tasks
- forms [Windows Forms], multithreading
- components [Windows Forms], asynchronous
- forms [Windows Forms], background operations
- background threads
- threading [Windows Forms], background operations
- background operations
ms.assetid: 9f483f93-1613-4be1-a021-b4934e9c78f3
ms.openlocfilehash: df7c6caf7b23824a596e94e1bd62205907b0b56a
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65592413"
---
# <a name="how-to-implement-a-form-that-uses-a-background-operation"></a><span data-ttu-id="bba71-102">Procédure : implémenter un formulaire qui utilise une opération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="bba71-102">How to: Implement a Form That Uses a Background Operation</span></span>
<span data-ttu-id="bba71-103">L'exemple de programme suivant crée un formulaire qui calcule les nombres de Fibonacci.</span><span class="sxs-lookup"><span data-stu-id="bba71-103">The following example program creates a form that calculates Fibonacci numbers.</span></span> <span data-ttu-id="bba71-104">Le calcul s'exécute sur un thread distinct du thread d'interface utilisateur, pour que l'interface utilisateur continue de s'exécuter sans délai lors du calcul.</span><span class="sxs-lookup"><span data-stu-id="bba71-104">The calculation runs on a thread that is separate from the user interface thread, so the user interface continues to run without delays as the calculation proceeds.</span></span>  
  
 <span data-ttu-id="bba71-105">Cette tâche est très bien prise en charge dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="bba71-105">There is extensive support for this task in Visual Studio.</span></span>  
  
 <span data-ttu-id="bba71-106">Consultez également [procédure pas à pas : Implémentation d’un formulaire qui utilise une opération d’arrière-plan](walkthrough-implementing-a-form-that-uses-a-background-operation.md).</span><span class="sxs-lookup"><span data-stu-id="bba71-106">Also see [Walkthrough: Implementing a Form That Uses a Background Operation](walkthrough-implementing-a-form-that-uses-a-background-operation.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="bba71-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="bba71-107">Example</span></span>  
 [!code-cpp[System.ComponentModel.BackgroundWorker#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CPP/fibonacciform.cpp#1)]
 [!code-csharp[System.ComponentModel.BackgroundWorker#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CS/fibonacciform.cs#1)]
 [!code-vb[System.ComponentModel.BackgroundWorker#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/VB/fibonacciform.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="bba71-108">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="bba71-108">Compiling the Code</span></span>  
 <span data-ttu-id="bba71-109">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="bba71-109">This example requires:</span></span>  
  
- <span data-ttu-id="bba71-110">Références aux assemblys System, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="bba71-110">References to the System, System.Drawing, and System.Windows.Forms assemblies.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="bba71-111">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="bba71-111">Robust Programming</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="bba71-112">Quand vous utilisez le multithreading, vous vous exposez potentiellement à des bogues très sérieux et complexes.</span><span class="sxs-lookup"><span data-stu-id="bba71-112">When using multithreading of any sort, you potentially expose yourself to very serious and complex bugs.</span></span> <span data-ttu-id="bba71-113">Consultez les [Meilleures pratiques pour le threading managé](../../../standard/threading/managed-threading-best-practices.md) avant d’implémenter une solution qui utilise le multithreading.</span><span class="sxs-lookup"><span data-stu-id="bba71-113">Consult the [Managed Threading Best Practices](../../../standard/threading/managed-threading-best-practices.md) before implementing any solution that uses multithreading.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bba71-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bba71-114">See also</span></span>

- <xref:System.ComponentModel.BackgroundWorker>
- <xref:System.ComponentModel.DoWorkEventArgs>
- [<span data-ttu-id="bba71-115">Vue d’ensemble du modèle asynchrone basé sur les événements</span><span class="sxs-lookup"><span data-stu-id="bba71-115">Event-based Asynchronous Pattern Overview</span></span>](../../../standard/asynchronous-programming-patterns/event-based-asynchronous-pattern-overview.md)
- [<span data-ttu-id="bba71-116">Bonnes pratiques de threading géré</span><span class="sxs-lookup"><span data-stu-id="bba71-116">Managed Threading Best Practices</span></span>](../../../standard/threading/managed-threading-best-practices.md)
