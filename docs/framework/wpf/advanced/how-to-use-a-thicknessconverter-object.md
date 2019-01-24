---
title: 'Procédure : Utiliser un objet ThicknessConverter'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- border thickness [WPF]
- ThicknessConverter objects [WPF]
ms.assetid: 52682194-d7fd-499c-8005-73fcc84e7b2c
ms.openlocfilehash: 22215a155f4a204e3edeebc464413d5718290bb4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54577069"
---
# <a name="how-to-use-a-thicknessconverter-object"></a>Procédure : Utiliser un objet ThicknessConverter
## <a name="example"></a>Exemple  
 Cet exemple montre comment créer une instance de <xref:System.Windows.ThicknessConverter> et l’utiliser pour modifier l’épaisseur d’une bordure.  
  
 L’exemple définit une méthode personnalisée nommée `changeThickness`; cette méthode convertit d’abord le contenu d’un <xref:System.Windows.Controls.ListBoxItem>, tel que défini dans une fonction [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] fichier, à une instance de <xref:System.Windows.Thickness>et plus tard convertit le contenu dans un <xref:System.String>. Cette méthode passe le <xref:System.Windows.Controls.ListBoxItem> à un <xref:System.Windows.ThicknessConverter> objet, qui convertit le <xref:System.Windows.Controls.ContentControl.Content%2A> d’un <xref:System.Windows.Controls.ListBoxItem> à une instance de <xref:System.Windows.Thickness>. Cette valeur est ensuite retournée comme la valeur de la <xref:System.Windows.Controls.Border.BorderThickness%2A> propriété de la <xref:System.Windows.Controls.Border>.  
  
 Cet exemple ne s’exécute pas.  
  
 [!code-csharp[ThicknessConverter#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ThicknessConverter/CSharp/Window1.xaml.cs#1)]
 [!code-vb[ThicknessConverter#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ThicknessConverter/VisualBasic/Window1.xaml.vb#1)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Thickness>
- <xref:System.Windows.ThicknessConverter>
- <xref:System.Windows.Controls.Border>
- [Guide pratique pour Modifier la propriété Margin](https://msdn.microsoft.com/library/8a313efd-5f99-4097-b4c1-8fa49d8379a2)
- [Guide pratique pour Convertir un ListBoxItem en un nouveau Type de données](https://msdn.microsoft.com/library/7a080b88-184e-4b27-bb61-d42bafba9727)
- [Vue d’ensemble de Panel](../../../../docs/framework/wpf/controls/panels-overview.md)
