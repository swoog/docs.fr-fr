---
ms.openlocfilehash: 6e5e90a4cfb862b3bfd74ac5a3715e97a736f598
ms.sourcegitcommit: 0aca6c5d166d7961a1e354c248495645b97a1dc5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2019
ms.locfileid: "58760438"
---
### <a name="workflow-now-throws-original-exception-instead-of-nullreferenceexception-in-some-cases"></a>Un workflow lève maintenant dans certains cas une exception d’origine au lieu d’une exception NullReferenceException

|   |   |
|---|---|
|Détails|Dans .NET Framework 4.6.2 et antérieur, quand la méthode Execute d’une activité de workflow lève une exception avec une valeur <code>null</code> pour la propriété <xref:System.Exception.Message>, l’exécution du workflow System.Activities lève une <xref:System.NullReferenceException?displayProperty=name>, masquant l’exception d’origine. Dans .NET Framework 4.7, l’exception précédemment masquée est levée.|
|Suggestion|Si votre code s’appuie sur la gestion de <xref:System.NullReferenceException?displayProperty=name>, modifiez-le afin d’intercepter les exceptions qui peuvent être levées depuis vos activités personnalisées.|
|Portée|Mineur|
|Version|4.7|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Activities.CodeActivity.Execute(System.Activities.CodeActivityContext)?displayProperty=nameWithType></li><li><xref:System.Activities.AsyncCodeActivity.BeginExecute(System.Activities.AsyncCodeActivityContext,System.AsyncCallback,System.Object)?displayProperty=nameWithType></li><li><xref:System.Activities.AsyncCodeActivity%601.BeginExecute(System.Activities.AsyncCodeActivityContext,System.AsyncCallback,System.Object)?displayProperty=nameWithType></li><li><xref:System.Activities.WorkflowInvoker.Invoke?displayProperty=nameWithType></li></ul>|

