---
title: 'Comment : utiliser le découpage avec une région'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- regions [Windows Forms], clipping
- regions [Windows Forms], restricting drawing surface
ms.assetid: 43d121b4-e14c-4901-b25c-2d6c25ba4e29
ms.openlocfilehash: bfc40d985ec12a30b73935ace7ef034aadbd5385
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-use-clipping-with-a-region"></a>Comment : utiliser le découpage avec une région
Une des propriétés de la <xref:System.Drawing.Graphics> classe est la zone de découpage. Tout le dessin effectué un donné <xref:System.Drawing.Graphics> objet est limité à la zone de découpage de ce <xref:System.Drawing.Graphics> objet. Vous pouvez définir la zone de découpage en appelant le <xref:System.Drawing.Graphics.SetClip%2A> (méthode).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant construit un chemin d’accès qui se compose d’un polygone unique. Le code crée ensuite une région, en fonction de ce chemin d’accès. La région est passée à la <xref:System.Drawing.Graphics.SetClip%2A> méthode d’un <xref:System.Drawing.Graphics> objet, puis les deux chaînes sont dessinées.  
  
 L’illustration suivante montre les chaînes découpées.  
  
 ![Élément](../../../../docs/framework/winforms/advanced/media/clip1.png "1 sur")  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#41](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#41)]
 [!code-vb[System.Drawing.MiscLegacyTopics#41](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#41)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.  
  
## <a name="see-also"></a>Voir aussi  
 [Régions dans GDI+](../../../../docs/framework/winforms/advanced/regions-in-gdi.md)  
 [Utilisation de régions](../../../../docs/framework/winforms/advanced/using-regions.md)
