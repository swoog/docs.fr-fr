---
ms.openlocfilehash: 3bde64b80e5dcfe98bbf598700b6d7004e3c3c9d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59774039"
---
### <a name="keyboard-focus-now-moves-correctly-across-multiple-layers-of-winformswpf-hosting"></a>Le focus clavier se déplace désormais correctement entre plusieurs couches d’hébergement WinForms/WPF

|   |   |
|---|---|
|Détails|Imaginez une application WPF qui héberge un contrôle WinForms hébergeant à son tour des contrôles WPF. Les utilisateurs peuvent être dans l’impossibilité de quitter la couche WinForms au moyen de la touche Tab si le premier ou dernier contrôle dans cette couche est le contrôle WPF <code>System.Windows.Forms.Integration.ElementHost</code>. Ce changement résout ce problème, et les utilisateurs peuvent désormais quitter la couche WinForms au moyen de la touche Tab. Les applications automatisées pour lesquelles il est indispensable que le focus ne quitte jamais la couche WinForms pourraient ne plus fonctionner comme prévu.|
|Suggestion|Un développeur qui souhaite utiliser ce changement tout en ciblant une version du .NET Framework antérieure à la version 4.7.2 peut définir l’ensemble suivant d’indicateurs AppContext sur false pour activer la modification.<pre><code class="lang-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.UseLegacyAccessibilityFeatures=false;Switch.UseLegacyAccessibilityFeatures.2=false&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>Les applications WPF doivent accepter toutes les améliorations d’accessibilité antérieures pour obtenir les dernières améliorations. En d’autres termes, les deux commutateurs <code>Switch.UseLegacyAccessibilityFeatures</code> et <code>Switch.UseLegacyAccessibilityFeatures.2</code> doivent être définis. Un développeur qui a besoin des fonctionnalités antérieures tout en ciblant .NET 4.7.2 ou version ultérieure peut définir l’indicateur AppContext suivant sur la valeur true pour activer la modification.<pre><code class="lang-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.UseLegacyAccessibilityFeatures.2=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Portée|Microsoft Edge|
|Version|4.7.2|
|Type|Reciblage|
