---
title: 'Procédure : Substituer la méthode OnRender de Panel'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
f1_keywords:
- overriding OnRender method
- Panel control, overriding OnRender method
- OnRender method
- controls, Panel, overriding OnRender method
helpviewer_keywords:
- overriding OnRender method of Panel control [WPF]
- OnRender method [WPF], overriding
- Panel control [WPF], overriding OnRender method
ms.assetid: 57397834-a085-4e36-90ab-416fad98f341
ms.openlocfilehash: c4539847368c1a5789e99ec92106d17077ed5943
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59102529"
---
# <a name="how-to-override-the-panel-onrender-method"></a>Procédure : Substituer la méthode OnRender de Panel
Cet exemple montre comment substituer la <xref:System.Windows.Controls.Panel.OnRender%2A> méthode de <xref:System.Windows.Controls.Panel> afin d’ajouter des effets graphiques personnalisés à un élément de disposition.  
  
## <a name="example"></a>Exemple  
 Utilisez le <xref:System.Windows.Controls.Panel.OnRender%2A> méthode afin d’ajouter des effets graphiques à un élément de panneau rendu. Par exemple, vous pouvez utiliser cette méthode pour ajouter une bordure personnalisée ou des effets d’arrière-plan. Un <xref:System.Windows.Media.DrawingContext> objet est passé en tant qu’argument, qui fournit des méthodes pour dessiner des formes, texte, images ou vidéos. Par conséquent, cette méthode est utile pour la personnalisation d’un objet de panneau.  
  
 [!code-csharp[LightWeightCustomPanel#1](~/samples/snippets/csharp/VS_Snippets_Wpf/LightWeightCustomPanel/CSharp/OffsetPanel.cs#1)]
 [!code-vb[LightWeightCustomPanel#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/LightWeightCustomPanel/visualbasic/offsetpanel.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.Panel>
- [Vue d’ensemble de Panel](panels-overview.md)
- [Exemple de panneau Radial personnalisé](https://go.microsoft.com/fwlink/?LinkID=159982)
- [Rubriques de guide pratique](panel-how-to-topics.md)
