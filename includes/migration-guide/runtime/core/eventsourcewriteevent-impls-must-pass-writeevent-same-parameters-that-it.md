---
ms.openlocfilehash: 47d0aa554d88726caca35fa6bebe4d863fdc0695
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235230"
---
### <a name="eventsourcewriteevent-impls-must-pass-writeevent-the-same-parameters-that-it-received-plus-id"></a>Les implémentations d’EventSource.WriteEvent doivent passer à WriteEvent les mêmes paramètres qu’il a reçus (plus l’ID)

|   |   |
|---|---|
|Détails|Le runtime applique à présent le contrat qui spécifie la condition suivante : une classe dérivée de <xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> qui définit une méthode d’événement ETW doit appeler la méthode <code>EventSource.WriteEvent</code> de la classe de base avec l’ID d’événement suivi des arguments passés à la méthode d’événement ETW.|
|Suggestion|Une exception <xref:System.IndexOutOfRangeException?displayProperty=name> est levée si un <xref:System.Diagnostics.Tracing.EventListener?displayProperty=name> lit des données <xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> dans le processus pour une source d'événement qui ne respecte pas ce contrat.|
|Portée|Mineur|
|Version|4.5.1|
|Type|Runtime|
