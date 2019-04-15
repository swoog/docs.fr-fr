---
ms.openlocfilehash: 39a329597ef28e002242103a247515d94761676a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59234715"
---
### <a name="resolveassemblyreference-task-now-warns-of-dependencies-with-the-wrong-architecture"></a>La tâche ResolveAssemblyReference avertit désormais en cas de dépendances avec une architecture incorrecte

|   |   |
|---|---|
|Détails|La tâche émet un avertissement, MSB3270, qui indique qu’une référence ou l’une de ses dépendances ne correspond pas à l’architecture de l’application. Cette situation se produit, par exemple, si une application qui a été compilée avec l'option <code>AnyCPU</code> inclut une référence x86. Ainsi, l'application peut échouer au moment de l'exécution (si l'application est déployée en tant que processus x64 dans notre exemple).|
|Suggestion|Deux domaines sont impactés :<ul><li>La recompilation génère des avertissements qui n'étaient pas apparus quand l'application avait été compilée sous une version antérieure de MSBuild. En revanche, étant donné que l'avertissement identifie une source potentielle d'échec du runtime, vous devez l'examiner et le traiter.</li><li>Si les avertissements sont considérés comme des erreurs, la compilation de l'application échouera.</li></ul>|
|Portée|Mineur|
|Version|4.5.1|
|Type|Reciblage|
