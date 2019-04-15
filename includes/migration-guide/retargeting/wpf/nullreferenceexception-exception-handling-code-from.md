---
ms.openlocfilehash: e4cf139d308a1c12425d966a84d59a0c3bb89712
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59236388"
---
### <a name="nullreferenceexception-in-exception-handling-code-from-imagesourceconverterconvertfrom"></a>NullReferenceException dans le code de gestion des exceptions à partir de ImageSourceConverter.ConvertFrom

|   |   |
|---|---|
|Détails|Une erreur dans le code de gestion des exceptions <xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)> a provoqué la levée d’une exception <xref:System.NullReferenceException?displayProperty=name> incorrecte au lieu de l’exception prévue (par exemple, <xref:System.IO.DirectoryNotFoundException?displayProperty=name> ou <xref:System.IO.FileNotFoundException?displayProperty=name>). Ce changement corrige cette erreur pour que la méthode lève la bonne exception. <p/>Par défaut, toutes les applications ciblant .NET Framework 4.6.2 et antérieur continuent à lever <xref:System.NullReferenceException?displayProperty=name> pour assurer la compatibilité. Les développeurs ciblant .NET Framework 4.7 et ultérieur devraient voir les bonnes exceptions.|
|Suggestion|Les développeurs qui ciblent le .NET Framework 4.7 et qui préfèrent obtenir l’exception <xref:System.NullReferenceException?displayProperty=name> peuvent ajouter/fusionner les éléments suivants dans le fichier App.config de leur application :<pre><code class="lang-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Media.ImageSourceConverter.OverrideExceptionWithNullReferenceException=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Portée|Microsoft Edge|
|Version|4.7|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)?displayProperty=nameWithType></li></ul>|
