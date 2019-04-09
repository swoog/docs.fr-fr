---
title: 'Procédure : Créer un style pour un en-tête de colonne GridView déplacé'
ms.date: 03/30/2017
helpviewer_keywords:
- ListView controls [WPF], styling
ms.assetid: 0b999645-0313-4b33-80b9-19ece08b5459
ms.openlocfilehash: dbcdd38e0397b8e637aff962420a2959f33203df
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59090093"
---
# <a name="how-to-create-a-style-for-a-dragged-gridview-column-header"></a>Procédure : Créer un style pour un en-tête de colonne GridView déplacé
Cet exemple montre comment modifier l’apparence d’un glissé <xref:System.Windows.Controls.GridViewColumnHeader> lorsque l’utilisateur modifie la position d’une colonne.  
  
## <a name="example"></a>Exemple  
 Lorsque vous faites glisser un en-tête de colonne vers un autre emplacement dans un <xref:System.Windows.Controls.ListView> qui utilise <xref:System.Windows.Controls.GridView> comme mode d’affichage, la colonne se déplace vers la nouvelle position. Lorsque vous faites glisser l’en-tête de colonne, une copie flottante de l’en-tête s’affiche en plus de l’en-tête d’origine. Un en-tête de colonne dans un <xref:System.Windows.Controls.GridView> est représenté par un <xref:System.Windows.Controls.GridViewColumnHeader> objet.  
  
 Pour personnaliser l’apparence des en-têtes flottants et d’origine, vous pouvez définir <xref:System.Windows.Controls.ControlTemplate.Triggers%2A> pour modifier la <xref:System.Windows.Controls.GridViewColumnHeader> <xref:System.Windows.Style>. Ces <xref:System.Windows.Controls.ControlTemplate.Triggers%2A> sont appliquées lorsque le <xref:System.Windows.Controls.Primitives.ButtonBase.IsPressed%2A> valeur de propriété est `true` et <xref:System.Windows.Controls.GridViewColumnHeader.Role%2A> valeur de propriété est <xref:System.Windows.Controls.GridViewColumnHeaderRole.Floating>.  
  
 Lorsque l’utilisateur appuie sur le bouton de la souris et le maintient enfoncé quand la souris s’arrête sur la <xref:System.Windows.Controls.GridViewColumnHeader>, le <xref:System.Windows.Controls.Primitives.ButtonBase.IsPressed%2A> modification de la valeur de propriété à `true`. De même, lorsque l’utilisateur commence l’opération glisser, la <xref:System.Windows.Controls.GridViewColumnHeader.Role%2A> modifications apportées aux propriétés <xref:System.Windows.Controls.GridViewColumnHeaderRole.Floating>.  
  
 L’exemple suivant montre comment définir <xref:System.Windows.Controls.ControlTemplate.Triggers%2A> pour modifier la <xref:System.Windows.Controls.Control.Foreground%2A> et <xref:System.Windows.Controls.Control.Background%2A> couleurs des en-têtes flottants et d’origine lorsque l’utilisateur fait glisser une colonne vers une nouvelle position.  
  
 [!code-xaml[ListViewHeaderRoleStyle#GVCHControlTemplateStart](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#gvchcontroltemplatestart)]  
[!code-xaml[ListViewHeaderRoleStyle#ControlTemplateTriggersStart](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#controltemplatetriggersstart)]  
[!code-xaml[ListViewHeaderRoleStyle#IsPressed](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#ispressed)]  
[!code-xaml[ListViewHeaderRoleStyle#Floating](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#floating)]  
[!code-xaml[ListViewHeaderRoleStyle#ControlTemplateTriggersEnd](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#controltemplatetriggersend)]  
[!code-xaml[ListViewHeaderRoleStyle#GVCHControlTemplateEnd](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#gvchcontroltemplateend)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.GridViewColumnHeader>
- <xref:System.Windows.Controls.GridViewColumnHeaderRole>
- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [Rubriques Comment](listview-how-to-topics.md)
- [Vue d'ensemble de ListView](listview-overview.md)
- [Vue d'ensemble de GridView](gridview-overview.md)
