---
title: Restrictions relatives à la propriété Interval du composant Timer Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- timers [Windows Forms], event intervals
- Interval property [Windows Forms], limitations
- timers [Windows Forms], Windows-based
- Timer component [Windows Forms], limitations of Interval property
ms.assetid: 7e5fb513-77e7-4046-a8e8-aab94e61ca0f
ms.openlocfilehash: 54782c4e0460ba1ba9b8a870b8f60f08a76340b3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59125170"
---
# <a name="limitations-of-the-windows-forms-timer-components-interval-property"></a><span data-ttu-id="01fd6-102">Restrictions relatives à la propriété Interval du composant Timer Windows Forms</span><span class="sxs-lookup"><span data-stu-id="01fd6-102">Limitations of the Windows Forms Timer Component's Interval Property</span></span>
<span data-ttu-id="01fd6-103">Les formulaires Windows <xref:System.Windows.Forms.Timer> composant possède un <xref:System.Windows.Forms.Timer.Interval%2A> propriété qui spécifie le nombre de millisecondes qui s’écouler entre deux événements de minuterie suivant.</span><span class="sxs-lookup"><span data-stu-id="01fd6-103">The Windows Forms <xref:System.Windows.Forms.Timer> component has an <xref:System.Windows.Forms.Timer.Interval%2A> property that specifies the number of milliseconds that pass between one timer event and the next.</span></span> <span data-ttu-id="01fd6-104">Sauf si le composant est désactivé, une minuterie continue à recevoir le <xref:System.Windows.Forms.Timer.Tick> événement à intervalles réguliers à peu près égales.</span><span class="sxs-lookup"><span data-stu-id="01fd6-104">Unless the component is disabled, a timer continues to receive the <xref:System.Windows.Forms.Timer.Tick> event at roughly equal intervals of time.</span></span>  
  
 <span data-ttu-id="01fd6-105">Ce composant est conçu pour un environnement Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="01fd6-105">This component is designed for a Windows Forms environment.</span></span> <span data-ttu-id="01fd6-106">Si vous avez besoin d’un minuteur adapté à un environnement de serveur, consultez l’article [Introduction aux minuteurs serveur](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/tb9yt5e6(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="01fd6-106">If you need a timer that is suitable for a server environment, see [Introduction to Server-Based Timers](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/tb9yt5e6(v=vs.90)).</span></span>  
  
## <a name="the-interval-property"></a><span data-ttu-id="01fd6-107">La propriété d’intervalle</span><span class="sxs-lookup"><span data-stu-id="01fd6-107">The Interval Property</span></span>  
 <span data-ttu-id="01fd6-108">Le <xref:System.Windows.Forms.Timer.Interval%2A> propriété présente quelques limitations à prendre en compte lorsque vous programmez un <xref:System.Windows.Forms.Timer> composant :</span><span class="sxs-lookup"><span data-stu-id="01fd6-108">The <xref:System.Windows.Forms.Timer.Interval%2A> property has a few limitations to consider when you are programming a <xref:System.Windows.Forms.Timer> component:</span></span>  
  
-   <span data-ttu-id="01fd6-109">Si votre application ou une autre application effectue des demandes importantes sur le système, telles que les boucles longues, calculs complexes, ou le lecteur, réseau ou accès de port, votre application ne peut pas obtenir des événements de minuterie aussi souvent que le <xref:System.Windows.Forms.Timer.Interval%2A> propriété spécifie.</span><span class="sxs-lookup"><span data-stu-id="01fd6-109">If your application or another application is making heavy demands on the system — such as long loops, intensive calculations, or drive, network, or port access — your application may not get timer events as often as the <xref:System.Windows.Forms.Timer.Interval%2A> property specifies.</span></span>  
  
-   <span data-ttu-id="01fd6-110">L’intervalle n’est pas garanti s’écouler exactement le moment.</span><span class="sxs-lookup"><span data-stu-id="01fd6-110">The interval is not guaranteed to elapse exactly on time.</span></span> <span data-ttu-id="01fd6-111">Pour garantir l’exactitude, la minuterie doit vérifier l’horloge système en fonction des besoins, plutôt que d’essayer de suivre en interne le temps écoulé.</span><span class="sxs-lookup"><span data-stu-id="01fd6-111">To ensure accuracy, the timer should check the system clock as needed, rather than try to keep track of accumulated time internally.</span></span>  
  
-   <span data-ttu-id="01fd6-112">La précision de la <xref:System.Windows.Forms.Timer.Interval%2A> propriété est exprimée en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="01fd6-112">The precision of the <xref:System.Windows.Forms.Timer.Interval%2A> property is in milliseconds.</span></span> <span data-ttu-id="01fd6-113">Certains ordinateurs fournissent un compteur haute résolution qui a une résolution supérieure aux millisecondes.</span><span class="sxs-lookup"><span data-stu-id="01fd6-113">Some computers provide a high-resolution counter that has a resolution higher than milliseconds.</span></span> <span data-ttu-id="01fd6-114">La disponibilité de ce compteur varie selon le matériel de processeur de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="01fd6-114">The availability of such a counter depends on the processor hardware of your computer.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="01fd6-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01fd6-115">See also</span></span>

- <xref:System.Windows.Forms.Timer>
- [<span data-ttu-id="01fd6-116">Timer, composant</span><span class="sxs-lookup"><span data-stu-id="01fd6-116">Timer Component</span></span>](timer-component-windows-forms.md)
- [<span data-ttu-id="01fd6-117">Vue d’ensemble du composant Timer</span><span class="sxs-lookup"><span data-stu-id="01fd6-117">Timer Component Overview</span></span>](timer-component-overview-windows-forms.md)
