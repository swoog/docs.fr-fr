---
title: 'Procédure : Spécifier si un lien hypertexte est souligné ou non'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Hyperlink control type [WPF]
ms.assetid: 3996cfe6-1dac-4835-aeb3-c719ce9cfee5
ms.openlocfilehash: 5718912e24a0697f209669b0ab4e7f4df1765ed3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59076313"
---
# <a name="how-to-specify-whether-a-hyperlink-is-underlined"></a>Procédure : Spécifier si un lien hypertexte est souligné ou non
Le <xref:System.Windows.Documents.Hyperlink> objet est un élément de contenu de flux inline qui permet d’héberger des liens hypertexte dans le contenu de flux. Par défaut, <xref:System.Windows.Documents.Hyperlink> utilise un <xref:System.Windows.TextDecoration> objet pour afficher un trait de soulignement. <xref:System.Windows.TextDecoration> les objets peuvent être des performances, en particulier si vous disposez de nombreuses <xref:System.Windows.Documents.Hyperlink> objets. Si vous utilisez beaucoup de <xref:System.Windows.Documents.Hyperlink> éléments, vous souhaiterez afficher un soulignement uniquement lors du déclenchement d’un événement, tel que le <xref:System.Windows.ContentElement.MouseEnter> événement.  
  
 Dans l’exemple suivant, le trait de soulignement pour le lien « Mon MSN » est dynamique, autrement dit, elle s’affiche uniquement lorsque le <xref:System.Windows.ContentElement.MouseEnter> est déclenché.  
  
  ![Liens hypertexte affichant TextDecorations](./media/how-to-specify-whether-a-hyperlink-is-underlined/text-decorations-hyperlinks.png)  

## <a name="example"></a>Exemple  
 L’exemple de balisage suivant montre un <xref:System.Windows.Documents.Hyperlink> défini avec et sans soulignement :  
  
 [!code-xaml[Performance#PerformanceSnippet11](~/samples/snippets/csharp/VS_Snippets_Wpf/Performance/CSharp/Hyperlink.xaml#performancesnippet11)]  
  
 L’exemple de code suivant montre comment créer un trait de soulignement pour le <xref:System.Windows.Documents.Hyperlink> sur le <xref:System.Windows.ContentElement.MouseEnter> événement et le supprimer sur le <xref:System.Windows.ContentElement.MouseLeave> événement.  
  
 [!code-csharp[Performance#PerformanceSnippet15](~/samples/snippets/csharp/VS_Snippets_Wpf/Performance/CSharp/Hyperlink.xaml.cs#performancesnippet15)]
 [!code-vb[Performance#PerformanceSnippet15](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Performance/visualbasic/hyperlink.xaml.vb#performancesnippet15)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.TextDecoration>
- <xref:System.Windows.Documents.Hyperlink>
- [Optimisation des performances des applications WPF](optimizing-wpf-application-performance.md)
- [Créer une décoration de texte](how-to-create-a-text-decoration.md)
