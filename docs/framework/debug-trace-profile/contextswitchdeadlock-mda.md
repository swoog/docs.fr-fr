---
title: Assistant Débogage managé contextSwitchDeadlock
ms.date: 03/30/2017
helpviewer_keywords:
- deadlocks [.NET Framework]
- pumping messages
- STA message pumping
- single-threaded COM components
- MDAs (managed debugging assistants), context switching deadlocks
- managed debugging assistants (MDAs), context switching deadlocks
- ContextSwitchDeadlock MDA
- message pumping
- context switching deadlocks
ms.assetid: 26dfaa15-9ddb-4b0a-b6da-999bba664fa6
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c1a0e2a6c7851b261baa3e02f6431e7a4ff697e4
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64660321"
---
# <a name="contextswitchdeadlock-mda"></a>Assistant Débogage managé contextSwitchDeadlock

L'Assistant Débogage managé `contextSwitchDeadlock` est activé quand un interblocage est détecté pendant une tentative de transition de contexte COM.

## <a name="symptoms"></a>Symptômes

Le symptôme le plus courant est l'absence de retour suite à un appel sur un composant COM non managé à partir d'un code managé.  Un autre symptôme est l'augmentation de l'utilisation de la mémoire dans le temps.

## <a name="cause"></a>Cause

La cause la plus probable est qu'un thread cloisonné ne pompe pas les messages. Soit le thread cloisonné attend sans pomper les messages, soit il effectue des opérations de longue durée qui empêchent le pompage de la file d'attente des messages.

L'augmentation de l'utilisation de la mémoire dans le temps est due au fait que le thread du finaliseur appelle `Release` sur un composant COM non managé qui ne répond pas à cet appel.  Dans cette situation, le finaliseur ne peut pas récupérer d'autres objets.

Par défaut, le modèle de thread du thread principal des applications console Visual Basic est le modèle cloisonné. Cet Assistant Débogage managé est activé si un thread cloisonné utilise l'interopérabilité COM soit directement, soit indirectement par le biais du Common Language Runtime ou d'un contrôle tiers.  Pour éviter d'activer cet Assistant Débogage managé dans une application console Visual Basic, appliquez l'attribut <xref:System.MTAThreadAttribute> à la méthode principale ou modifiez l'application pour qu'elle pompe les messages.

Il est possible que cet Assistant Débogage managé soit faussement activé quand toutes les conditions suivantes sont réunies :

- Une application crée des composants COM à partir de threads cloisonnés soit directement, soit indirectement par le biais de bibliothèques.

- L'application a été arrêtée dans le débogueur et l'utilisateur a continué d'exécuter l'application ou a effectué une opération pas à pas.

- Le débogage non managé n'est pas activé.

Pour déterminer si l'Assistant Débogage managé est faussement activé, désactivez tous les points d'arrêt, redémarrez l'application et laissez-la s'exécuter sans l'interrompre. Si l'Assistant Débogage managé n'est pas activé, l'activation initiale était probablement fausse. Dans ce cas, désactivez l'Assistant Débogage managé pour éviter des interférences avec la session de débogage.

> [!NOTE]
> Cet Assistant Débogage MANAGÉ est dans l’ensemble par défaut de Visual Studio. Pour plus d’informations sur la désactivation des Assistants Débogage managé, consultez [diagnostic d’erreurs avec les Assistants Débogage managé](../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md#enable-and-disable-mdas).

## <a name="resolution"></a>Résolution

Appliquez les règles COM relatives au pompage des messages de thread cloisonné.

## <a name="effect-on-the-runtime"></a>Effet sur le runtime

Cet Assistant Débogage managé n'a aucun effet sur le CLR. Il fournit uniquement des informations sur les contextes COM.

## <a name="output"></a>Sortie

Message décrivant le contexte actuel et le contexte cible.

## <a name="configuration"></a>Configuration

```xml
<mdaConfig>
  <assistants>
    <contextSwitchDeadlock />
  </assistants>
</mdaConfig>
```

## <a name="see-also"></a>Voir aussi

- <xref:System.Runtime.InteropServices.MarshalAsAttribute>
- [Diagnostic d’erreurs avec les Assistants Débogage managé](../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
- [Marshaling d'interopérabilité](../../../docs/framework/interop/interop-marshaling.md)
