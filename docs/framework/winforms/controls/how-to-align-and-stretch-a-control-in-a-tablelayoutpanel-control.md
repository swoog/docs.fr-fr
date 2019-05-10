---
title: 'Procédure : aligner et étirer un contrôle dans un contrôle TableLayoutPanel'
ms.date: 03/30/2017
f1_keywords:
- net.ComponentModel.StyleCollectionEditor.TLP.AlignStretchCtrl
helpviewer_keywords:
- TableLayoutPanel control [Windows Forms], stretching controls
- controls [Windows Forms], stretching
- controls [Windows Forms], aligning
ms.assetid: 7dc1a157-6fee-4995-8ebc-b65bdc0909a8
ms.openlocfilehash: fd32593bcad9e3f3ef93edee8aa2659d423f9feb
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65210362"
---
# <a name="how-to-align-and-stretch-a-control-in-a-tablelayoutpanel-control"></a>Procédure : aligner et étirer un contrôle dans un contrôle TableLayoutPanel

Vous pouvez aligner et étirer des contrôles dans un <xref:System.Windows.Forms.TableLayoutPanel> avec la <xref:System.Windows.Forms.Control.Anchor%2A> et <xref:System.Windows.Forms.Control.Dock%2A> propriétés.

## <a name="align-and-stretch-a-control"></a>Aligner et étirer un contrôle

1. Dans Visual Studio, faites glisser un <xref:System.Windows.Forms.TableLayoutPanel> contrôle depuis la **boîte à outils** vers votre formulaire.

2. Faites glisser un <xref:System.Windows.Forms.Button> contrôler à partir de la **boîte à outils** dans la cellule supérieure gauche de la <xref:System.Windows.Forms.TableLayoutPanel> contrôle. Le <xref:System.Windows.Forms.Button> contrôle est centré dans la cellule.

3. Définissez la valeur de la <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Anchor%2A> propriété `Left,Right`. Le <xref:System.Windows.Forms.Button> contrôler s’étire pour correspondre à la largeur de la cellule.

4. Définissez la valeur de la <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Anchor%2A> propriété `Top,Bottom`. Le <xref:System.Windows.Forms.Button> contrôler s’étire pour correspondre à la hauteur de la cellule.

5. Définissez la valeur de la <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Dock%2A> propriété <xref:System.Windows.Forms.DockStyle.Fill>. Le <xref:System.Windows.Forms.Button> contrôle se développe pour remplir la cellule.

6. Définissez la valeur de la <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Dock%2A> propriété <xref:System.Windows.Forms.DockStyle.None>. Le <xref:System.Windows.Forms.Button> contrôle retourne à sa taille d’origine et se déplace vers l’angle supérieur gauche de la cellule. Le **Windows Forms Designer** a défini le <xref:System.Windows.Forms.Control.Anchor%2A> propriété `Top, Left`.

7. Définissez la valeur de la <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Anchor%2A> propriété `Bottom,Right`. Le <xref:System.Windows.Forms.Button> contrôle se déplace vers l’angle inférieur droit de la cellule.

8. Définissez la valeur de la <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Anchor%2A> propriété <xref:System.Windows.Forms.AnchorStyles.None>. Le <xref:System.Windows.Forms.Button> contrôle se déplace vers le centre de la cellule.

## <a name="see-also"></a>Voir aussi

- [TableLayoutPanel, contrôle](tablelayoutpanel-control-windows-forms.md)
