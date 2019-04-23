---
ms.openlocfilehash: 297af393e86c65e84ea7271d98eab36dbc6dbb0e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59774385"
---
### <a name="some-workflow-drag-and-drop-apis-are-obsolete"></a>Certaines API WorkFlow de glisser-déplacer sont obsolètes

|   |   |
|---|---|
|Détails|Cette API WorkFlow de glisser-déplacer est obsolète et génère des avertissements du compilateur si l’application est régénérée avec la version 4.5.|
|Suggestion|Utilisez à la place les nouvelles API <xref:System.Activities.Presentation.DragDropHelper?displayProperty=name> qui prennent en charge les opérations avec plusieurs objets. Vous pouvez également supprimer les avertissements de génération ou les éviter en utilisant un compilateur plus ancien. Ces API sont toujours prises en charge.|
|Portée|Mineur|
|Version|4.5|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Activities.Presentation.DragDropHelper.DoDragMove(System.Activities.Presentation.WorkflowViewElement,System.Windows.Point)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetCompositeView(System.Windows.DragEventArgs)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetDraggedModelItem(System.Windows.DragEventArgs)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetDroppedObject(System.Windows.DependencyObject,System.Windows.DragEventArgs,System.Activities.Presentation.EditingContext)?displayProperty=nameWithType></li></ul>|
