---
title: Limitations du composant Timer Windows Forms&#39;s propriété d’intervalle
ms.date: 03/30/2017
helpviewer_keywords:
- timers [Windows Forms], event intervals
- Interval property [Windows Forms], limitations
- timers [Windows Forms], Windows-based
- Timer component [Windows Forms], limitations of Interval property
ms.assetid: 7e5fb513-77e7-4046-a8e8-aab94e61ca0f
ms.openlocfilehash: e5b9e7e43369913f0cdc9c7f2111bd4fe58675e6
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43465653"
---
# <a name="limitations-of-the-windows-forms-timer-component39s-interval-property"></a><span data-ttu-id="3a42e-102">Limitations du composant Timer Windows Forms&#39;s propriété d’intervalle</span><span class="sxs-lookup"><span data-stu-id="3a42e-102">Limitations of the Windows Forms Timer Component&#39;s Interval Property</span></span>
<span data-ttu-id="3a42e-103">Les formulaires Windows <xref:System.Windows.Forms.Timer> composant possède un <xref:System.Windows.Forms.Timer.Interval%2A> propriété qui spécifie le nombre de millisecondes qui s’écouler entre deux événements de minuterie suivant.</span><span class="sxs-lookup"><span data-stu-id="3a42e-103">The Windows Forms <xref:System.Windows.Forms.Timer> component has an <xref:System.Windows.Forms.Timer.Interval%2A> property that specifies the number of milliseconds that pass between one timer event and the next.</span></span> <span data-ttu-id="3a42e-104">Sauf si le composant est désactivé, une minuterie continue à recevoir le <xref:System.Windows.Forms.Timer.Tick> événement à intervalles réguliers à peu près égales.</span><span class="sxs-lookup"><span data-stu-id="3a42e-104">Unless the component is disabled, a timer continues to receive the <xref:System.Windows.Forms.Timer.Tick> event at roughly equal intervals of time.</span></span>  
  
 <span data-ttu-id="3a42e-105">Ce composant est conçu pour un environnement Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="3a42e-105">This component is designed for a Windows Forms environment.</span></span> <span data-ttu-id="3a42e-106">Si vous avez besoin d’un minuteur adapté à un environnement de serveur, consultez l’article [Introduction aux minuteurs serveur](https://msdn.microsoft.com/library/adc0bc0a-a519-4812-bafc-fb9d1a5801fc).</span><span class="sxs-lookup"><span data-stu-id="3a42e-106">If you need a timer that is suitable for a server environment, see [Introduction to Server-Based Timers](https://msdn.microsoft.com/library/adc0bc0a-a519-4812-bafc-fb9d1a5801fc).</span></span>  
  
## <a name="the-interval-property"></a><span data-ttu-id="3a42e-107">La propriété d’intervalle</span><span class="sxs-lookup"><span data-stu-id="3a42e-107">The Interval Property</span></span>  
 <span data-ttu-id="3a42e-108">Le <xref:System.Windows.Forms.Timer.Interval%2A> propriété présente quelques limitations à prendre en compte lorsque vous programmez un <xref:System.Windows.Forms.Timer> composant :</span><span class="sxs-lookup"><span data-stu-id="3a42e-108">The <xref:System.Windows.Forms.Timer.Interval%2A> property has a few limitations to consider when you are programming a <xref:System.Windows.Forms.Timer> component:</span></span>  
  
-   <span data-ttu-id="3a42e-109">Si votre application ou une autre application effectue des demandes importantes sur le système, telles que les boucles longues, calculs complexes, ou le lecteur, réseau ou accès de port, votre application ne peut pas obtenir des événements de minuterie aussi souvent que le <xref:System.Windows.Forms.Timer.Interval%2A> propriété spécifie.</span><span class="sxs-lookup"><span data-stu-id="3a42e-109">If your application or another application is making heavy demands on the system — such as long loops, intensive calculations, or drive, network, or port access — your application may not get timer events as often as the <xref:System.Windows.Forms.Timer.Interval%2A> property specifies.</span></span>  
  
-   <span data-ttu-id="3a42e-110">L’intervalle n’est pas garanti s’écouler exactement le moment.</span><span class="sxs-lookup"><span data-stu-id="3a42e-110">The interval is not guaranteed to elapse exactly on time.</span></span> <span data-ttu-id="3a42e-111">Pour garantir l’exactitude, la minuterie doit vérifier l’horloge système en fonction des besoins, plutôt que d’essayer de suivre en interne le temps écoulé.</span><span class="sxs-lookup"><span data-stu-id="3a42e-111">To ensure accuracy, the timer should check the system clock as needed, rather than try to keep track of accumulated time internally.</span></span>  
  
-   <span data-ttu-id="3a42e-112">La précision de la <xref:System.Windows.Forms.Timer.Interval%2A> propriété est exprimée en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="3a42e-112">The precision of the <xref:System.Windows.Forms.Timer.Interval%2A> property is in milliseconds.</span></span> <span data-ttu-id="3a42e-113">Certains ordinateurs fournissent un compteur haute résolution qui a une résolution supérieure aux millisecondes.</span><span class="sxs-lookup"><span data-stu-id="3a42e-113">Some computers provide a high-resolution counter that has a resolution higher than milliseconds.</span></span> <span data-ttu-id="3a42e-114">La disponibilité de ce compteur varie selon le matériel de processeur de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3a42e-114">The availability of such a counter depends on the processor hardware of your computer.</span></span> <span data-ttu-id="3a42e-115">Pour plus d’informations, consultez l’article 172338, « Comment à utiliser QueryPerformanceCounter à temps Code », dans la Base de connaissances Microsoft à http://support.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="3a42e-115">For more information, see article 172338, "How To Use QueryPerformanceCounter to Time Code," in the Microsoft Knowledge Base at http://support.microsoft.com.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3a42e-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a42e-116">See Also</span></span>  
 <xref:System.Windows.Forms.Timer>  
 [<span data-ttu-id="3a42e-117">Timer, composant</span><span class="sxs-lookup"><span data-stu-id="3a42e-117">Timer Component</span></span>](../../../../docs/framework/winforms/controls/timer-component-windows-forms.md)  
 [<span data-ttu-id="3a42e-118">Vue d’ensemble du composant Timer</span><span class="sxs-lookup"><span data-stu-id="3a42e-118">Timer Component Overview</span></span>](../../../../docs/framework/winforms/controls/timer-component-overview-windows-forms.md)
