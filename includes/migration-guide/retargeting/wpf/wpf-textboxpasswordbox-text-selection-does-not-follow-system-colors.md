---
ms.openlocfilehash: 649e4456ef6a11903ab1b390baf56583f31f5562
ms.sourcegitcommit: 0aca6c5d166d7961a1e354c248495645b97a1dc5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2019
ms.locfileid: "58760841"
---
### <a name="wpf-textboxpasswordbox-text-selection-does-not-follow-system-colors"></a>La sélection de texte WPF TextBox/PasswordBox ne suit pas les couleurs système

|   |   |
|---|---|
|Détails|Dans .NET Framework 4.7.1 et versions antérieures, WPF <code>System.Windows.Controls.TextBox</code> et <code>System.Windows.Controls.PasswordBox</code> pouvaient afficher une sélection de texte uniquement dans la couche Ornement. Dans certains thèmes système, cela occultait le texte, au point de le rendre difficile à lire.  Dans .NET Framework 4.7.2 et ultérieur, les développeurs ont la possibilité d’activer un schéma de rendu de sélection non basée sur la couche Ornement qui atténue ce problème.|
|Suggestion|Un développeur qui souhaite utiliser cette modification doit définir l’indicateur AppContext suivant de façon appropriée.  Vous ne pouvez utiliser cette fonctionnalité que si vous avez installé .NET Framework version 4.7.2 ou ultérieure. Pour activer la sélection non basée sur un ornement, utilisez l’indicateur AppContext suivant.<pre><code class="lang-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.Text.UseAdornerForTextboxSelectionRendering=false&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Portée|Microsoft Edge|
|Version|4.7.2|
|Type|Reciblage|

