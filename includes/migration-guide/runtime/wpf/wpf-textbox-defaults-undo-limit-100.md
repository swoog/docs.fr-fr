---
ms.openlocfilehash: de79182e326082786c1e0691f8888e30cd410f5d
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235221"
---
### <a name="wpf-textbox-defaults-to-undo-limit-of-100"></a>Le nombre maximal d’annulations d’opérations pour une zone de texte WPF est de 100 par défaut

|   |   |
|---|---|
|Détails|Dans .NET Framework 4.5, le nombre maximal d’annulations d’opérations pour une zone de texte WPF est de 100 par défaut (dans .NET Framework 4.0, ce nombre était illimité).|
|Suggestion|Si une limite de 100 n’est pas suffisante, il est possible de définir explicitement cette valeur avec <xref:System.Windows.Controls.Primitives.TextBoxBase.UndoLimit>|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|
