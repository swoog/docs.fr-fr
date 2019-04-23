---
ms.openlocfilehash: 921baed7381fad363cc832c6b6af69068c2c8f43
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59236048"
---
### <a name="ribbongroup-background-is-set-to-transparent-in-localized-builds"></a>L’arrière-plan de RibbonGroup est défini sur Transparent dans les versions localisées

|   |   |
|---|---|
|Détails|<xref:System.Windows.Controls.Ribbon.RibbonGroup?displayProperty=name> L’arrière-plan sur les versions localisées était toujours dessiné avec le pinceau Transparent, ce qui offrait une expérience assez pauvre dans l’interface utilisateur. Ce point est résolu dans le correctif de .NET Framework 4.7 WPF par le biais d’une mise à jour des ressources localisées pour <xref:System.Windows.Controls.Ribbon.RibbonGroup?displayProperty=name>, qui à son tour garantit que le bon pinceau est sélectionné.|
|Suggestion|Mettre à niveau vers .NET Framework 4.7|
|Portée|Microsoft Edge|
|Version|4.6.2|
|Type|Runtime|
