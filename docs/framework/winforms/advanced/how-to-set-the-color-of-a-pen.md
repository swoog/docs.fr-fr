---
title: 'Procédure : définir la couleur d’un stylet'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- pens [Windows Forms], setting color
- colored pens
ms.assetid: a9df06f9-a6d5-4d9b-a2d1-583943540775
ms.openlocfilehash: ee2d3f8cdf6dd10ca2a9ff0dd3e66b164c84f21b
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64637000"
---
# <a name="how-to-set-the-color-of-a-pen"></a>Procédure : définir la couleur d’un stylet
Cet exemple modifie la couleur d’un préexistants <xref:System.Drawing.Pen> objet  
  
## <a name="example"></a>Exemple  
 [!code-cpp[System.Drawing.ConceptualHowTos#9](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#9)]
 [!code-csharp[System.Drawing.ConceptualHowTos#9](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#9)]
 [!code-vb[System.Drawing.ConceptualHowTos#9](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#9)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
- Un <xref:System.Drawing.Pen> objet nommé `myPen`.  
  
## <a name="robust-programming"></a>Programmation fiable  
 Vous devez appeler <xref:System.Drawing.Pen.Dispose%2A> sur les objets qui consomment des ressources système (telles que <xref:System.Drawing.Pen> objets) une fois que vous avez terminé.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Drawing.Pen>
- [Mise en route de la programmation graphique](getting-started-with-graphics-programming.md)
- [Guide pratique pour Créer un stylet](how-to-create-a-pen.md)
- [Utilisation d'un stylet pour dessiner des lignes et des formes](using-a-pen-to-draw-lines-and-shapes.md)
- [Stylets, lignes et rectangles dans GDI+](pens-lines-and-rectangles-in-gdi.md)
