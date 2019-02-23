---
title: 'Procédure : Définir un modèle GroupBox'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], GroupBox
- GroupBox control [WPF], creating templates
ms.assetid: 85a4d1a7-4753-4f4a-b26d-14fa10c1ddb5
ms.openlocfilehash: 6294a52d5914b52d191b564330f904e6a865c283
ms.sourcegitcommit: 8f95d3a37e591963ebbb9af6e90686fd5f3b8707
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "56745196"
---
# <a name="how-to-define-a-groupbox-template"></a>Procédure : Définir un modèle GroupBox
Cet exemple montre comment créer un modèle pour un <xref:System.Windows.Controls.GroupBox> contrôle.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant définit un <xref:System.Windows.Controls.GroupBox> modèle de contrôle à l’aide un <xref:System.Windows.Controls.Grid> contrôle de disposition. Le modèle utilise un <xref:System.Windows.Controls.BorderGapMaskConverter> pour définir la bordure de la <xref:System.Windows.Controls.GroupBox> afin que la bordure ne masque pas le <xref:System.Windows.Controls.HeaderedContentControl.Header%2A> contenu.  
  
 [!code-xaml[GroupBoxSnippet#GroupBoxTemplate](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GroupBoxSnippet/CS/Window1.xaml#groupboxtemplate)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Controls.GroupBox>
- [Guide pratique pour Créer un contrôle GroupBox](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms748321(v=vs.90))
