---
title: 'Procédure : rechercher des éléments générés par ControlTemplate'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ControlTemplates [WPF], finding elements
- finding ControlTemplate elements [WPF]
ms.assetid: d7b25447-ceff-4bb4-9be5-fd7c40ef00af
ms.openlocfilehash: 426f6c93433711ac72fe67eff2ee3006aa4d9166
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62037138"
---
# <a name="how-to-find-controltemplate-generated-elements"></a>Procédure : rechercher des éléments générés par ControlTemplate
Cet exemple montre comment rechercher des éléments qui sont générés par un <xref:System.Windows.Controls.ControlTemplate>.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre un style qui crée un simple <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.Button> classe :  
  
 [!code-xaml[FindGeneratedItems#CT](~/samples/snippets/csharp/VS_Snippets_Wpf/FindGeneratedItems/CSharp/Window1.xaml#ct)]  
  
 Pour rechercher un élément dans le modèle une fois que le modèle a été appliqué, vous pouvez appeler la <xref:System.Windows.FrameworkTemplate.FindName%2A> méthode de la <xref:System.Windows.Controls.Control.Template%2A>. L’exemple suivant crée une boîte de message qui affiche la valeur de la largeur réelle de la <xref:System.Windows.Controls.Grid> dans le modèle de contrôle :  
  
 [!code-csharp[FindGeneratedItems#CTFindElement](~/samples/snippets/csharp/VS_Snippets_Wpf/FindGeneratedItems/CSharp/Window1.xaml.cs#ctfindelement)]
 [!code-vb[FindGeneratedItems#CTFindElement](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FindGeneratedItems/VisualBasic/Window1.xaml.vb#ctfindelement)]  
  
## <a name="see-also"></a>Voir aussi

- [Rechercher des éléments générés par DataTemplate](../data/how-to-find-datatemplate-generated-elements.md)
- [Application d’un style et création de modèles](styling-and-templating.md)
- [Portées de nom XAML WPF](../advanced/wpf-xaml-namescopes.md)
- [Arborescences dans WPF](../advanced/trees-in-wpf.md)
