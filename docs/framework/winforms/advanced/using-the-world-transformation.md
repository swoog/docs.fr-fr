---
title: Utilisation de la transformation universelle
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [Windows Forms], world transformation
- world transformation [Windows Forms], examples
ms.assetid: 1e717711-1361-448e-aa49-0f3ec43110c9
ms.openlocfilehash: ec232c92d32b91a7b334b237c869db8eb428eccc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54647606"
---
# <a name="using-the-world-transformation"></a>Utilisation de la transformation universelle
La transformation universelle est une propriété de la <xref:System.Drawing.Graphics> classe. Les nombres qui spécifient la transformation universelle sont stockés dans un <xref:System.Drawing.Drawing2D.Matrix> objet qui représente une matrice 3 x 3. Le <xref:System.Drawing.Drawing2D.Matrix> et <xref:System.Drawing.Graphics> classes disposent de plusieurs méthodes pour définir les nombres dans la matrice de transformation de monde.  
  
## <a name="different-types-of-transformations"></a>Différents Types de Transformations  
 Dans l’exemple suivant, le code crée un rectangle de 50 x 50 tout d’abord et situe à l’origine (0, 0). L’origine est dans l’angle supérieur gauche de la zone cliente.  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#11](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.MiscLegacyTopics#11](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#11)]  
  
 Le code suivant applique une transformation de mise à l’échelle qui développe le rectangle par un facteur de 1,75 dans la direction x et réduit le rectangle par un facteur de 0,5 dans la direction y :  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#12](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#12)]
 [!code-vb[System.Drawing.MiscLegacyTopics#12](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#12)]  
  
 Le résultat est un rectangle qui est plus longue dans la direction x et plus court sur l’axe y que l’original.  
  
 Pour faire pivoter le rectangle au lieu de la mise à l’échelle il, utilisez le code suivant :  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#13](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#13)]
 [!code-vb[System.Drawing.MiscLegacyTopics#13](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#13)]  
  
 Pour traduire le rectangle, utilisez le code suivant :  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#14](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#14)]
 [!code-vb[System.Drawing.MiscLegacyTopics#14](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#14)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Drawing.Drawing2D.Matrix>
- [Systèmes de coordonnées et transformations](../../../../docs/framework/winforms/advanced/coordinate-systems-and-transformations.md)
- [Utilisation des transformations dans GDI+ managé](../../../../docs/framework/winforms/advanced/using-transformations-in-managed-gdi.md)
