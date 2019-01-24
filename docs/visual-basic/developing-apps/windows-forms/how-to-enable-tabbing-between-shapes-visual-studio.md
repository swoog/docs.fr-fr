---
title: 'Procédure : Activer la tabulation entre les formes (Visual Studio)'
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Line control [Visual Basic], implementing tabbing
- Shape control [Visual Basic], implementing tabbing
ms.assetid: 09731b34-3900-4fcb-a9df-ce5280328433
ms.openlocfilehash: c47d94317008af57907b747e53bd13ae7ca229f5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54498279"
---
# <a name="how-to-enable-tabbing-between-shapes-visual-studio"></a>Procédure : Activer la tabulation entre les formes (Visual Studio)
Contrôles Line et shape n’ont pas `TabStop` ou `TabIndex` propriétés, mais vous pouvez toujours activer la tabulation entre eux. Dans l’exemple suivant, en appuyant sur la touche CTRL et les touches TAB sera onglet entre les formes. uniquement la touche TAB sera onglet entre les boutons.  
  
> [!NOTE]
>  Il est possible que pour certains des éléments de l’interface utilisateur de Visual Studio, votre ordinateur affiche des noms ou des emplacements différents de ceux indiqués dans les instructions suivantes. L’édition de Visual Studio dont vous disposez et les paramètres que vous utilisez déterminent ces éléments. Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
## <a name="to-enable-tabbing-among-shapes"></a>Pour activer la tabulation entre les formes  
  
1.  Faites glisser trois <xref:Microsoft.VisualBasic.PowerPacks.RectangleShape> contrôles et deux <xref:System.Windows.Forms.Button> des contrôles de la **boîte à outils** à un formulaire.  
  
2.  Dans le **éditeur de Code**, ajoutez un `Imports` ou `using` instruction en haut du module :  
  
```vb  
Imports Microsoft.VisualBasic.PowerPacks  
```  
  
```csharp  
using Microsoft.VisualBasic.PowerPacks;  
```  

3.  Dans une procédure événementielle, ajoutez le code suivant :  
  
[!code-csharp[VbPowerPacksTabbing#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-enable-tabbing-between-shapes-visual-studio_1.cs)]
[!code-vb[VbPowerPacksTabbing#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-enable-tabbing-between-shapes-visual-studio_1.vb)]  
  
4.  Ajoutez le code suivant dans le `Button1_PreviewKeyDown` procédure événementielle :  
  
[!code-csharp[VbPowerPacksTabbing#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-enable-tabbing-between-shapes-visual-studio_2.cs)]
[!code-vb[VbPowerPacksTabbing#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-enable-tabbing-between-shapes-visual-studio_2.vb)]  
  
## <a name="see-also"></a>Voir aussi
- [Guide pratique pour Dessiner des formes avec les contrôles OvalShape et RectangleShape](../../../visual-basic/developing-apps/windows-forms/how-to-draw-shapes-with-the-ovalshape-and-rectangleshape-controls.md)
- [Guide pratique pour Dessiner des lignes avec le contrôle LineShape](../../../visual-basic/developing-apps/windows-forms/how-to-draw-lines-with-the-lineshape-control-visual-studio.md)
- [Introduction aux contrôles Line et Shape](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-line-and-shape-controls-visual-studio.md)
