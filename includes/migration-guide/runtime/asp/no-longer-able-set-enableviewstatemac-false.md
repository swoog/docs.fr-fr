---
ms.openlocfilehash: dbe96abebdc61fae469f7727673e6fcb93cbc739
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59236642"
---
### <a name="no-longer-able-to-set-enableviewstatemac-to-false"></a>Il n’est plus possible de définir EnableViewStateMac sur false

|   |   |
|---|---|
|Détails|ASP.NET ne permet plus aux développeurs de spécifier <code>&lt;pages enableViewStateMac=&quot;false&quot;/&gt;</code> ou <code>&lt;@Page EnableViewStateMac=&quot;false&quot; %&gt;</code>. Le code d'authentification de message (code MAC) de l'état d'affichage est à présent appliqué à toutes les demandes avec état d'affichage intégré. Seules les applications qui définissent explicitement la propriété EnableViewStateMac sur <code>false</code> sont affectées.|
|Suggestion|Vous devez supposer que la propriété EnableViewStateMac a la valeur true. Les erreurs MAC résultantes doivent être résolues (comme expliqué dans [cette aide](https://support.microsoft.com/kb/2915218), qui contient plusieurs résolutions en fonction de l’origine des erreurs MAC).|
|Portée|Majeur|
|Version|4.5.2|
|Type|Runtime|
