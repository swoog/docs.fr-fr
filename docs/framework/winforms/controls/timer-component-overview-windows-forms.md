---
title: Vue d'ensemble du composant Timer (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- Timer
helpviewer_keywords:
- Timer component [Windows Forms], about Timer components
- timers [Windows Forms], about timers
ms.assetid: e672c05b-a8b6-4b26-9e4d-9223aa9e3873
ms.openlocfilehash: 6e453f6b7718c6c5be3109f51153a3f5e4b5b6f4
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44136457"
---
# <a name="timer-component-overview-windows-forms"></a><span data-ttu-id="ac5f5-102">Vue d'ensemble du composant Timer (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="ac5f5-102">Timer Component Overview (Windows Forms)</span></span>
<span data-ttu-id="ac5f5-103"><xref:System.Windows.Forms.Timer> est un composant Windows Forms qui déclenche un événement à intervalles réguliers.</span><span class="sxs-lookup"><span data-stu-id="ac5f5-103">The Windows Forms <xref:System.Windows.Forms.Timer> is a component that raises an event at regular intervals.</span></span> <span data-ttu-id="ac5f5-104">Ce composant est conçu pour un environnement Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="ac5f5-104">This component is designed for a Windows Forms environment.</span></span> <span data-ttu-id="ac5f5-105">Si vous avez besoin d’un minuteur adapté à un environnement de serveur, consultez l’article [Introduction aux minuteurs serveur](https://msdn.microsoft.com/library/adc0bc0a-a519-4812-bafc-fb9d1a5801fc).</span><span class="sxs-lookup"><span data-stu-id="ac5f5-105">If you need a timer that is suitable for a server environment, see [Introduction to Server-Based Timers](https://msdn.microsoft.com/library/adc0bc0a-a519-4812-bafc-fb9d1a5801fc).</span></span>  
  
## <a name="key-properties-methods-and-events"></a><span data-ttu-id="ac5f5-106">Événements, méthodes et propriétés de clé</span><span class="sxs-lookup"><span data-stu-id="ac5f5-106">Key Properties, Methods, and Events</span></span>  
 <span data-ttu-id="ac5f5-107">La durée des intervalles est définie par le <xref:System.Windows.Forms.Timer.Interval%2A> propriété, dont la valeur est exprimée en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="ac5f5-107">The length of the intervals is defined by the <xref:System.Windows.Forms.Timer.Interval%2A> property, whose value is in milliseconds.</span></span> <span data-ttu-id="ac5f5-108">Lorsque le composant est activé, le <xref:System.Windows.Forms.Timer.Tick> événement est déclenché chaque intervalle.</span><span class="sxs-lookup"><span data-stu-id="ac5f5-108">When the component is enabled, the <xref:System.Windows.Forms.Timer.Tick> event is raised every interval.</span></span> <span data-ttu-id="ac5f5-109">Voici où vous devez ajouter le code qui doit être exécuté.</span><span class="sxs-lookup"><span data-stu-id="ac5f5-109">This is where you would add code to be executed.</span></span> <span data-ttu-id="ac5f5-110">Pour plus d’informations, consultez [Comment : exécuter des procédures à intervalles de définir avec le composant Timer Windows Forms](../../../../docs/framework/winforms/controls/run-procedures-at-set-intervals-with-wf-timer-component.md).</span><span class="sxs-lookup"><span data-stu-id="ac5f5-110">For more information, see [How to: Run Procedures at Set Intervals with the Windows Forms Timer Component](../../../../docs/framework/winforms/controls/run-procedures-at-set-intervals-with-wf-timer-component.md).</span></span> <span data-ttu-id="ac5f5-111">Les principales méthodes de la <xref:System.Windows.Forms.Timer> composant sont <xref:System.Windows.Forms.Timer.Start%2A> et <xref:System.Windows.Forms.Timer.Stop%2A>, lequel activer le minuteur et désactiver.</span><span class="sxs-lookup"><span data-stu-id="ac5f5-111">The key methods of the <xref:System.Windows.Forms.Timer> component are <xref:System.Windows.Forms.Timer.Start%2A> and <xref:System.Windows.Forms.Timer.Stop%2A>, which turn the timer on and off.</span></span> <span data-ttu-id="ac5f5-112">Lorsque la minuterie est désactivée, elle est réinitialisée ; Il n’existe aucun moyen pour suspendre un <xref:System.Windows.Forms.Timer> composant.</span><span class="sxs-lookup"><span data-stu-id="ac5f5-112">When the timer is switched off, it resets; there is no way to pause a <xref:System.Windows.Forms.Timer> component.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ac5f5-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac5f5-113">See Also</span></span>  
 <xref:System.Windows.Forms.Timer>  
 [<span data-ttu-id="ac5f5-114">Timer, composant</span><span class="sxs-lookup"><span data-stu-id="ac5f5-114">Timer Component</span></span>](../../../../docs/framework/winforms/controls/timer-component-windows-forms.md)  
 [<span data-ttu-id="ac5f5-115">Restrictions relatives à la propriété Interval du composant Timer Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ac5f5-115">Limitations of the Windows Forms Timer Component's Interval Property</span></span>](../../../../docs/framework/winforms/controls/limitations-of-the-timer-component-interval-property.md)
