---
title: 'Procédure : Gérer manuellement des graphiques mis en mémoire tampon'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- flicker [Windows Forms], reducing by manually managing graphics
- graphics [Windows Forms], managing buffered
ms.assetid: 4c2a90ee-bbbe-4ff6-9170-1b06c195c918
ms.openlocfilehash: b27a013d2cf66fb12365bffc35a07ed32bc25a2e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54554489"
---
# <a name="how-to-manually-manage-buffered-graphics"></a>Procédure : Gérer manuellement des graphiques mis en mémoire tampon
Pour des scénarios de double mise en mémoire tampon plus avancés, vous pouvez utiliser le [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] classes pour implémenter votre propre logique de double tampon. La classe responsable de l’allocation et la gestion des mémoires tampon de graphiques individuelles est la <xref:System.Drawing.BufferedGraphicsContext> classe. Chaque application a sa propre valeur par défaut <xref:System.Drawing.BufferedGraphicsContext> qui gère toute la double mise en mémoire tampon pour l’application de la valeur par défaut. Vous pouvez récupérer une référence à cette instance en appelant le <xref:System.Drawing.BufferedGraphicsManager.Current%2A>.  
  
### <a name="to-obtain-a-reference-to-the-default-bufferedgraphicscontext"></a>Pour obtenir une référence à la valeur par défaut BufferedGraphicsContext  
  
-   Définir le <xref:System.Drawing.BufferedGraphicsManager.Current%2A> propriété, comme indiqué dans l’exemple de code suivant.  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#11](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#11)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#11](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#11)]  
  
    > [!NOTE]
    >  Vous n’avez pas besoin d’appeler le `Dispose` méthode sur le <xref:System.Drawing.BufferedGraphicsContext> référence que vous recevez à partir de la <xref:System.Drawing.BufferedGraphicsManager> classe. Le <xref:System.Drawing.BufferedGraphicsManager> traite l’intégralité de l’allocation de mémoire et la distribution par défaut <xref:System.Drawing.BufferedGraphicsContext> instances.  
  
     Pour les applications gourmandes en ressources graphiques telles que l’animation, vous pouvez parfois améliorer les performances en utilisant un dédié <xref:System.Drawing.BufferedGraphicsContext> au lieu du <xref:System.Drawing.BufferedGraphicsContext> fournie par le <xref:System.Drawing.BufferedGraphicsManager>. Cela vous permet de créer et gérer les mémoires tampons de graphiques individuellement, sans subir la surcharge de performances de la gestion de tous les autres mises en mémoire tampon graphiques associés à votre application, même si la mémoire consommée par l’application sera supérieure.  
  
### <a name="to-create-a-dedicated-bufferedgraphicscontext"></a>Pour créer un BufferedGraphicsContext dédié  
  
-   Déclarez et créez une nouvelle instance de la <xref:System.Drawing.BufferedGraphicsContext> classe, comme indiqué dans l’exemple de code suivant.  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#12](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#12)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#12](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#12)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Drawing.BufferedGraphicsContext>
- [Graphiques mis deux fois en mémoire tampon](../../../../docs/framework/winforms/advanced/double-buffered-graphics.md)
- [Guide pratique pour Restituer manuellement des graphiques mis en mémoire tampon](../../../../docs/framework/winforms/advanced/how-to-manually-render-buffered-graphics.md)
