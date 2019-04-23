---
ms.openlocfilehash: 63101fb127c84de21d165994bba85a2753e97344
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59236591"
---
### <a name="resizing-a-grid-can-hang"></a>Le redimensionnement d’une grille peut se bloquer

|   |   |
|---|---|
|Détails|Une boucle infinie peut se produire lors de la présentation d’une <code>T:System.Windows.Controls.Grid</code> dans les circonstances suivantes :<ul><li>Les définitions de ligne contiennent deux lignes *, toutes deux déclarant un MinHeight et un MaxHeight.</li><li>Le contenu des lignes * ne dépasse pas le MaxHeight correspondant</li><li>La hauteur disponible de la grille est dépassée par le premier MinHeight (plus les autres lignes fixes ou automatiques)</li><li>L’application cible .NET Framework 4.7 ou adhère à son algorithme d’allocation en définissant <code>Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=false</code></li></ul>La boucle se produit également avec plus de deux lignes, ou dans le cas analogue pour les colonnes. Le problème est résolu dans .NET Framework 4.7.1.|
|Suggestion|Mettre à niveau vers .NET Framework 4.7.1.  Si vous n’avez pas besoin de l’algorithme d’allocation de 4.7, vous pouvez aussi utiliser le paramètre de configuration suivant :<pre><code class="lang-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Portée|Microsoft Edge|
|Version|4.7|
|Type|Runtime|
