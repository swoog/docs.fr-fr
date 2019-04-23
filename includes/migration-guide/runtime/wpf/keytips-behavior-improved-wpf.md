---
ms.openlocfilehash: 946096cb9510ca12bbd2cecd00099142308b072a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59803824"
---
### <a name="keytips-behavior-improved-in-wpf"></a>Amélioration du comportement des touches d’accès dans WPF

|   |   |
|---|---|
|Détails|Le comportement des touches d’accès a été modifié afin de correspondre au comportement de Microsoft Word et de l’Explorateur Windows. En vérifiant si l’état de la touche d’accès est activé ou non en cas de pression sur un <xref:System.Windows.Input.KeyEventArgs.SystemKey> (en particulier, <xref:System.Windows.Input.Key> ou <xref:System.Windows.Input.Key.F11>), WPF gère les touches KeyTip en conséquence. Les touches d’accès font maintenant disparaître un menu même quand il est ouvert par la souris.|
|Suggestion|N/A|
|Portée|Microsoft Edge|
|Version|4.7.2|
|Type|Runtime|
