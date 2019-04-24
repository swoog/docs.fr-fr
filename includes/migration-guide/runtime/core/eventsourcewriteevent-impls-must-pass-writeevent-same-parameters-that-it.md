---
ms.openlocfilehash: 47d0aa554d88726caca35fa6bebe4d863fdc0695
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59803898"
---
### <a name="eventsourcewriteevent-impls-must-pass-writeevent-the-same-parameters-that-it-received-plus-id"></a><span data-ttu-id="8ba36-101">Les implémentations d’EventSource.WriteEvent doivent passer à WriteEvent les mêmes paramètres qu’il a reçus (plus l’ID)</span><span class="sxs-lookup"><span data-stu-id="8ba36-101">EventSource.WriteEvent impls must pass WriteEvent the same parameters that it received (plus ID)</span></span>

|   |   |
|---|---|
|<span data-ttu-id="8ba36-102">Détails</span><span class="sxs-lookup"><span data-stu-id="8ba36-102">Details</span></span>|<span data-ttu-id="8ba36-103">Le runtime applique à présent le contrat qui spécifie la condition suivante : une classe dérivée de <xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> qui définit une méthode d’événement ETW doit appeler la méthode <code>EventSource.WriteEvent</code> de la classe de base avec l’ID d’événement suivi des arguments passés à la méthode d’événement ETW.</span><span class="sxs-lookup"><span data-stu-id="8ba36-103">The runtime now enforces the contract that specifies the following: A class derived from <xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> that defines an ETW event method must call the base class <code>EventSource.WriteEvent</code> method with the event ID followed by the same arguments that the ETW event method was passed.</span></span>|
|<span data-ttu-id="8ba36-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="8ba36-104">Suggestion</span></span>|<span data-ttu-id="8ba36-105">Une exception <xref:System.IndexOutOfRangeException?displayProperty=name> est levée si un <xref:System.Diagnostics.Tracing.EventListener?displayProperty=name> lit des données <xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> dans le processus pour une source d'événement qui ne respecte pas ce contrat.</span><span class="sxs-lookup"><span data-stu-id="8ba36-105">An <xref:System.IndexOutOfRangeException?displayProperty=name> exception is thrown if an <xref:System.Diagnostics.Tracing.EventListener?displayProperty=name> reads <xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> data in process for an event source that violates this contract.</span></span>|
|<span data-ttu-id="8ba36-106">Portée</span><span class="sxs-lookup"><span data-stu-id="8ba36-106">Scope</span></span>|<span data-ttu-id="8ba36-107">Mineur</span><span class="sxs-lookup"><span data-stu-id="8ba36-107">Minor</span></span>|
|<span data-ttu-id="8ba36-108">Version</span><span class="sxs-lookup"><span data-stu-id="8ba36-108">Version</span></span>|<span data-ttu-id="8ba36-109">4.5.1</span><span class="sxs-lookup"><span data-stu-id="8ba36-109">4.5.1</span></span>|
|<span data-ttu-id="8ba36-110">Type</span><span class="sxs-lookup"><span data-stu-id="8ba36-110">Type</span></span>|<span data-ttu-id="8ba36-111">Runtime</span><span class="sxs-lookup"><span data-stu-id="8ba36-111">Runtime</span></span>|
