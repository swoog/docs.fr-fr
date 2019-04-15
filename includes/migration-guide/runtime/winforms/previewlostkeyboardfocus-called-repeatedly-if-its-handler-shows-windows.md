---
ms.openlocfilehash: addfd55fd01b13e9088e4706ff846fc624aafa68
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235362"
---
### <a name="previewlostkeyboardfocus-is-called-repeatedly-if-its-handler-shows-a-windows-forms-message-box"></a>PreviewLostKeyboardFocus est appelé de façon répétée si son gestionnaire affiche une boîte de message Windows Forms

|   |   |
|---|---|
|Détails|À compter de la version 4.5 du .NET Framework, quand vous appelez <xref:System.Windows.Forms.MessageBox.Show%2A?displayProperty=nameWithType> à partir d’un gestionnaire <xref:System.Windows.UIElement.PreviewLostKeyboardFocus>, le gestionnaire est redéclenché quand la boîte de message est fermée, ce qui peut aboutir à une boucle infinie de boîtes de message.|
|Suggestion|Il existe deux options pour contourner ce problème :<ol><li>Vous pouvez appeler <xref:System.Windows.MessageBox.Show%2A?displayProperty=nameWithType> au lieu de <xref:System.Windows.Forms.MessageBox.Show%2A?displayProperty=nameWithType>.</li><li>Vous pouvez afficher la boîte de message à partir d’un gestionnaire d’événements <xref:System.Windows.UIElement.LostKeyboardFocus?displayProperty=nameWithType> (au lieu du gestionnaire d’événements <xref:System.Windows.UIElement.PreviewLostKeyboardFocus?displayProperty=name>).</li></ol>|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.ContentElement.PreviewLostKeyboardFocus?displayProperty=nameWithType></li><li><xref:System.Windows.IInputElement.PreviewLostKeyboardFocus?displayProperty=nameWithType></li><li><xref:System.Windows.UIElement.PreviewLostKeyboardFocus?displayProperty=nameWithType></li><li><xref:System.Windows.UIElement3D.PreviewLostKeyboardFocus?displayProperty=nameWithType></li></ul>|
