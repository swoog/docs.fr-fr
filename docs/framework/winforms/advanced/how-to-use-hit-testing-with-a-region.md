---
title: 'Procédure : Utiliser avec une région de test de positionnement'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- hit tests [Windows Forms], using regions
- regions [Windows Forms], hit testing
ms.assetid: 3a4c07cb-a40a-4d14-ad35-008f531910a8
ms.openlocfilehash: 1866810b875063271e206da1fe5d6fc06f7b5de0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54564303"
---
# <a name="how-to-use-hit-testing-with-a-region"></a>Procédure : Utiliser avec une région de test de positionnement
L’objectif du test de positionnement consiste à déterminer si le curseur se trouve sur un objet donné, tel qu’une icône ou un bouton.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée une région en forme de plus par l’union de deux régions rectangulaires. Supposons que la variable `point` contient l’emplacement du clic plus récent. Le code vérifie si `point` se trouve dans la région en forme de plus. Si le point se trouve dans la région (une atteinte), la région est remplie avec un pinceau rouge opaque. Sinon, la région est remplie avec un pinceau rouge translucide.  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#31](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.MiscLegacyTopics#31](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Drawing.Region>
- [Régions dans GDI+](../../../../docs/framework/winforms/advanced/regions-in-gdi.md)
- [Guide pratique pour Utiliser le découpage avec une région](../../../../docs/framework/winforms/advanced/how-to-use-clipping-with-a-region.md)
