---
ms.openlocfilehash: 6c1740df66ead271afa5f97dc125587810946bc6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235236"
---
### <a name="flowdocument-may-show-an-extra-line-of-text"></a>FlowDocument peut afficher une ligne de texte supplémentaire

|   |   |
|---|---|
|Détails|Dans certains cas, un élément <xref:System.Windows.Documents.FlowDocument> affiche une ligne de texte supplémentaire lors de l’exécution sur .NET Framework 4.5 par rapport à la façon dont il s’affichait lors de l’exécution sur .NET Framework 4.0. Il n’existe aucun cas connu où ce changement provoquerait un affichage incorrect ou illisible du texte, mais il peut avoir comme conséquence que du texte qui était omis dans la vue de <xref:System.Windows.Documents.FlowDocument> désormais apparaisse.|
|Suggestion|Dans certains cas, la diminution d’une unité de la valeur de la propriété PageHeight pour l’élément d’un affichage peut rétablir le nombre précédent de lignes affichées.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Documents.FlowDocument.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Documents.FlowDocument.%23ctor(System.Windows.Documents.Block)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentReader.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentPageViewer.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.DocumentPageView.%23ctor?displayProperty=nameWithType></li></ul>|
