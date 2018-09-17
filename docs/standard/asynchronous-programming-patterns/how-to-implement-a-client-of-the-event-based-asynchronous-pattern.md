---
title: 'Comment : implémenter un client du modèle asynchrone basé sur des événements'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Event-based Asynchronous Pattern
- ProgressChangedEventArgs class
- BackgroundWorker component
- events [.NET Framework], asynchronous
- Asynchronous Pattern
- AsyncOperationManager class
- threading [.NET Framework], asynchronous features
- components [.NET Framework], asynchronous
- AsyncOperation class
- threading [Windows Forms], asynchronous features
- AsyncCompletedEventArgs class
ms.assetid: 21a858c1-3c99-4904-86ee-0d17b49804fa
ms.openlocfilehash: 4176d1a4cec91c5740b03c10d1a6d2cc263dba28
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45686282"
---
# <a name="how-to-implement-a-client-of-the-event-based-asynchronous-pattern"></a><span data-ttu-id="2cfdd-102">Comment : implémenter un client du modèle asynchrone basé sur des événements</span><span class="sxs-lookup"><span data-stu-id="2cfdd-102">How to: Implement a Client of the Event-based Asynchronous Pattern</span></span>
<span data-ttu-id="2cfdd-103">L’exemple de code suivant montre comment utiliser un composant conforme à la [vue d'ensemble du modèle asynchrone basé sur des événements](../../../docs/standard/asynchronous-programming-patterns/event-based-asynchronous-pattern-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2cfdd-103">The following code example demonstrates how to use a component that adheres to the [Event-based Asynchronous Pattern Overview](../../../docs/standard/asynchronous-programming-patterns/event-based-asynchronous-pattern-overview.md).</span></span> <span data-ttu-id="2cfdd-104">Le formulaire de cet exemple utilise le composant `PrimeNumberCalculator` décrit dans la rubrique [Comment : implémenter un composant qui prend en charge le modèle asynchrone basé sur des événements](../../../docs/standard/asynchronous-programming-patterns/component-that-supports-the-event-based-asynchronous-pattern.md).</span><span class="sxs-lookup"><span data-stu-id="2cfdd-104">The form for this example uses the `PrimeNumberCalculator` component described in [How to: Implement a Component That Supports the Event-based Asynchronous Pattern](../../../docs/standard/asynchronous-programming-patterns/component-that-supports-the-event-based-asynchronous-pattern.md).</span></span>  
  
 <span data-ttu-id="2cfdd-105">Quand vous exécutez un projet utilisant cet exemple, un formulaire « Calculatrice de nombres premiers » s’affiche avec une grille et deux boutons : **Démarrer une nouvelle tâche** et **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-105">When you run a project that uses this example, you will see a "Prime Number Calculator" form with a grid and two buttons: **Start New Task** and **Cancel**.</span></span> <span data-ttu-id="2cfdd-106">Si vous cliquez plusieurs fois de suite sur le bouton **Démarrer une nouvelle tâche**, à chaque clic, une opération asynchrone lance un calcul pour déterminer si un nombre test généré de manière aléatoire est un nombre premier.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-106">You can click the **Start New Task** button several times in succession, and for each click, an asynchronous operation will begin a computation to determine if a randomly generated test number is prime.</span></span> <span data-ttu-id="2cfdd-107">Le formulaire affiche régulièrement la progression et des résultats incrémentiels.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-107">The form will periodically display progress and incremental results.</span></span> <span data-ttu-id="2cfdd-108">Chaque opération est assignée à un ID de tâche unique.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-108">Each operation is assigned a unique task ID.</span></span> <span data-ttu-id="2cfdd-109">Le résultat du calcul est affiché dans la colonne **Résultat**. Si le nombre test n’est pas un nombre premier, il est étiqueté en tant que **Composite** et son premier diviseur est affiché.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-109">The result of the computation is displayed in the **Result** column; if the test number is not prime, it is labeled as **Composite,** and its first divisor is displayed.</span></span>  
  
 <span data-ttu-id="2cfdd-110">Toute opération en attente peut être annulée à l’aide du bouton **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-110">Any pending operation can be canceled with the **Cancel** button.</span></span> <span data-ttu-id="2cfdd-111">Il est possible d’effectuer des sélections multiples.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-111">Multiple selections can be made.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="2cfdd-112">La plupart des nombres ne seront pas des nombres premiers.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-112">Most numbers will not be prime.</span></span> <span data-ttu-id="2cfdd-113">Si aucun nombre premier n’a été trouvé après plusieurs opérations, démarrez simplement davantage de tâches jusqu’à trouver des nombres premiers.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-113">If you have not found a prime number after several completed operations, simply start more tasks, and eventually you will find some prime numbers.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2cfdd-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="2cfdd-114">Example</span></span>  
 [!code-csharp[System.ComponentModel.AsyncOperationManager#10](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.AsyncOperationManager/CS/primenumbercalculatormain.cs#10)]
 [!code-vb[System.ComponentModel.AsyncOperationManager#10](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.AsyncOperationManager/VB/primenumbercalculatormain.vb#10)]  
  
## <a name="see-also"></a><span data-ttu-id="2cfdd-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2cfdd-115">See also</span></span>

- <xref:System.ComponentModel.AsyncOperation>  
- <xref:System.ComponentModel.AsyncOperationManager>  
- <xref:System.Windows.Forms.WindowsFormsSynchronizationContext>
