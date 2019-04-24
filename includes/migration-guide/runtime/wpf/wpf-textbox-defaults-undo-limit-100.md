---
ms.openlocfilehash: de79182e326082786c1e0691f8888e30cd410f5d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59235221"
---
### <a name="wpf-textbox-defaults-to-undo-limit-of-100"></a>Le nombre maximal d’annulations d’opérations pour une zone de texte WPF est de 100 par défaut

|   |   |
|---|---|
|Détails|Dans .NET Framework 4.5, le nombre maximal d’annulations d’opérations pour une zone de texte WPF est de 100 par défaut (dans .NET Framework 4.0, ce nombre était illimité).|
|Suggestion|Si ce nombre n’est pas suffisant, vous pouvez définir explicitement cette valeur avec <xref:System.Windows.Controls.Primitives.TextBoxBase.UndoLimit>|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|
