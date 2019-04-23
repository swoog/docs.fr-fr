---
title: 'Procédure : réduire le scintillement des graphismes avec double mise en mémoire tampon pour les formulaires et contrôles'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- flicker [Windows Forms], reducing in Windows Forms
- graphics [Windows Forms], reducing double-buffered flicker
ms.assetid: 91083d3a-653f-4f15-a467-0f37b2aa39d6
ms.openlocfilehash: ef05b72b33d3f28d1811389dfae65554a1567d43
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59096951"
---
# <a name="how-to-reduce-graphics-flicker-with-double-buffering-for-forms-and-controls"></a>Procédure : réduire le scintillement des graphismes avec double mise en mémoire tampon pour les formulaires et contrôles
La double mise en mémoire tampon utilise une mémoire tampon pour résoudre les problèmes de scintillement associés aux opérations de dessin multiples. Quand la double mise en mémoire tampon est activée, toutes les opérations de dessin sont d’abord rendues dans une mémoire tampon au lieu de l’être sur la surface de dessin à l’écran. Une fois que toutes les opérations de dessin sont terminées, la mémoire tampon est copiée directement sur la surface de dessin qui y est associée. Étant donné que les graphiques qu’une seule opération sur l’écran, le scintillement de l’image associé aux opérations de dessin complexes est éliminé. Pour la plupart des applications, le double tampon par défaut fourni par le [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] fournira les meilleurs résultats. Contrôles Windows Forms standard sont double mise en mémoire tampon par défaut. Vous pouvez activer la double mise en mémoire tampon dans vos formulaires et contrôles de deux manières créés. Vous pouvez soit définir le <xref:System.Windows.Forms.Control.DoubleBuffered%2A> propriété `true`, ou vous pouvez appeler la <xref:System.Windows.Forms.Control.SetStyle%2A> méthode pour définir le <xref:System.Windows.Forms.ControlStyles.OptimizedDoubleBuffer> indicateur `true`. Les deux méthodes seront activer double tampon par défaut pour votre formulaire ou contrôle et fournir un rendu graphique sans scintillement. Appel de la <xref:System.Windows.Forms.Control.SetStyle%2A> méthode est recommandée uniquement pour les contrôles personnalisés pour lequel vous avez écrit tout le code de rendu.  
  
 Pour les scénarios double mise en mémoire tampon plus avancés, tels que l’animation ou la gestion avancée de la mémoire, vous pouvez implémenter votre propre logique de mise en mémoire tampon double. Pour plus d'informations, voir [Procédure : Gérer manuellement des graphiques mis en mémoire tampon](how-to-manually-manage-buffered-graphics.md).  
  
### <a name="to-reduce-flicker"></a>Pour réduire le scintillement  
  
-   Affectez à la propriété <xref:System.Windows.Forms.Control.DoubleBuffered%2A> la valeur `true`.  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#31)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#31)]  
  
 \- ou -  
  
-   Appelez le <xref:System.Windows.Forms.Control.SetStyle%2A> méthode pour définir le <xref:System.Windows.Forms.ControlStyles.OptimizedDoubleBuffer> indicateur `true`.  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#32](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#32)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#32](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#32)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Control.DoubleBuffered%2A>
- <xref:System.Windows.Forms.Control.SetStyle%2A>
- [Graphiques mis deux fois en mémoire tampon](double-buffered-graphics.md)
- [Graphiques et dessins dans Windows Forms](graphics-and-drawing-in-windows-forms.md)
