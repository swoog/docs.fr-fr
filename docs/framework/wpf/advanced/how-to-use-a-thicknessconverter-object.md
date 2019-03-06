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
ms.openlocfilehash: 7dcac523ad105f074df11cdd74126536a60497b0
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57350695"
---
# <a name="how-to-use-a-thicknessconverter-object"></a>Procédure : Utiliser un objet ThicknessConverter
## <a name="example"></a>Exemple  
 Cet exemple montre comment créer une instance de <xref:System.Windows.ThicknessConverter> et l’utiliser pour modifier l’épaisseur d’une bordure.  
  
 L’exemple définit une méthode personnalisée nommée `changeThickness`; cette méthode convertit d’abord le contenu d’un <xref:System.Windows.Controls.ListBoxItem>, tel que défini dans une fonction [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] fichier, à une instance de <xref:System.Windows.Thickness>et plus tard convertit le contenu dans un <xref:System.String>. Cette méthode passe le <xref:System.Windows.Controls.ListBoxItem> à un <xref:System.Windows.ThicknessConverter> objet, qui convertit le <xref:System.Windows.Controls.ContentControl.Content%2A> d’un <xref:System.Windows.Controls.ListBoxItem> à une instance de <xref:System.Windows.Thickness>. Cette valeur est ensuite retournée comme la valeur de la <xref:System.Windows.Controls.Border.BorderThickness%2A> propriété de la <xref:System.Windows.Controls.Border>.  
  
 Cet exemple ne s’exécute pas.  
  
 [!code-csharp[ThicknessConverter#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ThicknessConverter/CSharp/Window1.xaml.cs#1)]
 [!code-vb[ThicknessConverter#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ThicknessConverter/VisualBasic/Window1.xaml.vb#1)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Thickness>
- <xref:System.Windows.ThicknessConverter>
- <xref:System.Windows.Controls.Border>
- [Guide pratique pour Modifier la propriété Margin](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms750561(v=vs.90))
- [Guide pratique pour Convertir un ListBoxItem en un nouveau Type de données](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms749147(v=vs.90))
- [Vue d’ensemble de Panel](../controls/panels-overview.md)
