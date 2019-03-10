---
title: 'Procédure : Étirer un ToolStripTextBox pour remplir la largeur restante d’un ToolStrip (Windows Forms)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text boxes [Windows Forms], stretching in ToolStrip control [Windows Forms]
- ToolStrip control [Windows Forms], stretching a text box
ms.assetid: 0e610fbf-85fe-414c-900c-9704a5dd5cc6
ms.openlocfilehash: 7a557a3d278c2b6d8d083b2ebf8c8129bc498afa
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57702761"
---
# <a name="how-to-stretch-a-toolstriptextbox-to-fill-the-remaining-width-of-a-toolstrip-windows-forms"></a>Procédure : Étirer un ToolStripTextBox pour remplir la largeur restante d’un ToolStrip (Windows Forms)
Lorsque vous définissez la <xref:System.Windows.Forms.ToolStrip.Stretch%2A> propriété d’un <xref:System.Windows.Forms.ToolStrip> le contrôle à `true`, le contrôle remplit son conteneur de bout en bout et se redimensionne quand son conteneur est redimensionné. Dans cette configuration, il peut s’avérer utile d’étirer un élément dans le contrôle, comme un <xref:System.Windows.Forms.ToolStripTextBox>, pour remplir l’espace disponible et redimensionner lorsque le contrôle est redimensionné. Cet étirement est utile, par exemple, si vous souhaitez obtenir une apparence et un comportement similaire à la barre d’adresses dans Microsoft® Internet Explorer.  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant fournit une classe dérivée de <xref:System.Windows.Forms.ToolStripTextBox> appelée `ToolStripSpringTextBox`. Cette classe substitue la <xref:System.Windows.Forms.ToolStripTextBox.GetPreferredSize%2A> méthode pour calculer la largeur disponible du parent <xref:System.Windows.Forms.ToolStrip> contrôler une fois que la largeur combinée de tous les autres éléments a été soustrait. Cet exemple de code fournit également un <xref:System.Windows.Forms.Form> classe et un `Program` pour illustrer le nouveau comportement.  
  
 [!code-csharp[ToolStripSpringTextBox#00](~/samples/snippets/csharp/VS_Snippets_Winforms/ToolStripSpringTextBox/cs/ToolStripSpringTextBox.cs#00)]
 [!code-vb[ToolStripSpringTextBox#00](~/samples/snippets/visualbasic/VS_Snippets_Winforms/ToolStripSpringTextBox/vb/ToolStripSpringTextBox.vb#00)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   Références aux assemblys System, System.Drawing et System.Windows.Forms.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStrip.Stretch%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.ToolStripTextBox>
- <xref:System.Windows.Forms.ToolStripTextBox.GetPreferredSize%2A?displayProperty=nameWithType>
- [Architecture du contrôle ToolStrip](toolstrip-control-architecture.md)
- [Guide pratique pour Utiliser la propriété Spring dans un StatusStrip de manière interactive](how-to-use-the-spring-property-interactively-in-a-statusstrip.md)
