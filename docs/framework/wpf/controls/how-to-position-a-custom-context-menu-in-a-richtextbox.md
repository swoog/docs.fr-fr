---
title: 'Procédure : Positionner un menu contextuel personnalisé dans un RichTextBox'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- custom context menus [WPF], positioning
- positioning custom context menus [WPF]
- RichTextBox control [WPF], positioning custom context menus
- context menus [WPF], positioning
ms.assetid: bf77c930-a546-4573-9a56-9af345ba189a
ms.openlocfilehash: f9407f59c3daafd09fa5b84006f33ef2f3ebd31f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59209422"
---
# <a name="how-to-position-a-custom-context-menu-in-a-richtextbox"></a>Procédure : Positionner un menu contextuel personnalisé dans un RichTextBox
Cet exemple montre comment positionner un menu contextuel personnalisé pour un <xref:System.Windows.Controls.RichTextBox>.  
  
 Lorsque vous implémentez un menu contextuel personnalisé pour un **RichTextBox**, il vous appartient de gérer le positionnement du menu contextuel.  Par défaut, un menu contextuel personnalisé s’ouvre au centre du **RichTextBox**.  
  
## <a name="example"></a>Exemple  
 Pour remplacer le comportement de positionnement par défaut, ajoutez un écouteur pour le <xref:System.Windows.FrameworkContentElement.ContextMenuOpening> événement.  L’exemple suivant montre comment procéder par programme.  
  
 [!code-csharp[RichTextBox_ContextMenu#_AddListener](~/samples/snippets/csharp/VS_Snippets_Wpf/RichTextBox_ContextMenu/CSharp/app.xaml.cs#_addlistener)]
 [!code-vb[RichTextBox_ContextMenu#_AddListener](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RichTextBox_ContextMenu/VisualBasic/app.xaml.vb#_addlistener)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant illustre une implémentation correspondante <xref:System.Windows.FrameworkContentElement.ContextMenuOpening> écouteur d’événements.  
  
 [!code-csharp[RichTextBox_ContextMenu#_ListenerBody](~/samples/snippets/csharp/VS_Snippets_Wpf/RichTextBox_ContextMenu/CSharp/app.xaml.cs#_listenerbody)]
 [!code-vb[RichTextBox_ContextMenu#_ListenerBody](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RichTextBox_ContextMenu/VisualBasic/app.xaml.vb#_listenerbody)]  
  
## <a name="see-also"></a>Voir aussi

- [Vue d'ensemble de RichTextBox](richtextbox-overview.md)
- [Vue d'ensemble de TextBox](textbox-overview.md)
