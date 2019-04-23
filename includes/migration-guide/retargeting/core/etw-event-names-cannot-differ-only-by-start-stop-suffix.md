---
ms.openlocfilehash: 71c81cf188fa4c2300661f10eb87e7ae00e031f6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59803882"
---
### <a name="etw-event-names-cannot-differ-only-by-a-start-or-stop-suffix"></a>Les noms d’événements ETW ne peuvent pas différer uniquement par le suffixe « Start » ou « Stop »

|   |   |
|---|---|
|Détails|Dans .NET Framework 4.6 et 4.6.1, le runtime lève un <xref:System.ArgumentException> quand deux noms d’événements ETW (Event Tracing for Windows) diffèrent uniquement par le suffixe &quot;Start&quot; ou &quot;Stop&quot; (comme quand un événement est nommé <code>LogUser</code> et un autre <code>LogUserStart</code>). Dans ce cas, le runtime ne peut pas construire la source d’événements, qui ne peut pas émettre de journalisation.|
|Suggestion|Pour empêcher cette exception, vérifiez qu’aucun des deux noms d’événement ne diffère uniquement par un suffixe &quot;Start&quot; ou &quot;Stop&quot;. À compter de .NET Framework 4.6.2, cette vérification n’est plus nécessaire. Le runtime est désormais capable de lever l’ambiguïté des noms d’événements qui diffèrent uniquement par le suffixe &quot;Start&quot; et &quot;Stop&quot;.|
|Portée|Microsoft Edge|
|Version|4.6|
|Type|Reciblage|
