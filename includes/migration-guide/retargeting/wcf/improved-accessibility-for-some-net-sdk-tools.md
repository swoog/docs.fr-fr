---
ms.openlocfilehash: 0b087fca59d60a086a9ea8b2bb19c09f646c3dfd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59803888"
---
### <a name="improved-accessibility-for-some-net-sdk-tools"></a>Amélioration de l’accessibilité pour certains outils du SDK .NET

|   |   |
|---|---|
|Détails|Dans le kit .NET Framework SDK 4.7.1, les outils SvcConfigEditor.exe et SvcTraceViewer.exe ont été améliorés en corrigeant différents problèmes d’accessibilité. La plupart étaient des petits problèmes comme un nom non défini ou certains modèles d’automatisation de l’interface utilisateur non implémentés correctement. Alors que de nombreux utilisateurs n’ont pas connaissance de ces valeurs incorrectes, les clients qui utilisent des technologies d’assistance comme les lecteurs d’écran trouveront ces outils de SDK plus accessibles. Il est évident que ces correctifs changent certains comportements précédents, comme l’ordre de focus clavier. Pour obtenir tous les correctifs liés à l’accessibilité dans ces outils, vous pouvez ajouter ce qui suit à votre fichier app.config :<pre><code class="lang-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.UseLegacyAccessibilityFeatures=false&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Portée|Microsoft Edge|
|Version|4.7.1|
|Type|Reciblage|
