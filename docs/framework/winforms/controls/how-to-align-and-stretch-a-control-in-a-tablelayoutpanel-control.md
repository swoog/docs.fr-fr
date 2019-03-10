---
title: 'Procédure : Aligner et étirer un contrôle dans un contrôle TableLayoutPanel'
ms.date: 03/30/2017
f1_keywords:
- net.ComponentModel.StyleCollectionEditor.TLP.AlignStretchCtrl
helpviewer_keywords:
- TableLayoutPanel control [Windows Forms], stretching controls
- controls [Windows Forms], stretching
- controls [Windows Forms], aligning
ms.assetid: 7dc1a157-6fee-4995-8ebc-b65bdc0909a8
ms.openlocfilehash: 511ed20e63778b70355d1deb12e4256b4d2e9101
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57702917"
---
# <a name="how-to-align-and-stretch-a-control-in-a-tablelayoutpanel-control"></a>Procédure : Aligner et étirer un contrôle dans un contrôle TableLayoutPanel
Vous pouvez aligner et étirer des contrôles dans un <xref:System.Windows.Forms.TableLayoutPanel> avec la <xref:System.Windows.Forms.Control.Anchor%2A> et <xref:System.Windows.Forms.Control.Dock%2A> propriétés.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-align-and-stretch-a-control"></a>Pour aligner et étirer un contrôle  
  
1.  Faites glisser un contrôle <xref:System.Windows.Forms.TableLayoutPanel> de la **boîte à outils** vers le formulaire.  
  
2.  Faites glisser un <xref:System.Windows.Forms.Button> contrôler à partir de la **boîte à outils** dans la cellule supérieure gauche de la <xref:System.Windows.Forms.TableLayoutPanel> contrôle. Le <xref:System.Windows.Forms.Button> contrôle est centré dans la cellule.  
  
3.  Définissez la valeur de la <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Anchor%2A> propriété `Left,Right`. Le <xref:System.Windows.Forms.Button> contrôler s’étire pour correspondre à la largeur de la cellule.  
  
4.  Définissez la valeur de la <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Anchor%2A> propriété `Top,Bottom`. Le <xref:System.Windows.Forms.Button> contrôler s’étire pour correspondre à la hauteur de la cellule.  
  
5.  Définissez la valeur de la <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Dock%2A> propriété <xref:System.Windows.Forms.DockStyle.Fill>. Le <xref:System.Windows.Forms.Button> contrôle se développe pour remplir la cellule.  
  
6.  Définissez la valeur de la <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Dock%2A> propriété <xref:System.Windows.Forms.DockStyle.None>. Le <xref:System.Windows.Forms.Button> contrôle retourne à sa taille d’origine et se déplace vers l’angle supérieur gauche de la cellule. Le **Windows Forms Designer** a défini le <xref:System.Windows.Forms.Control.Anchor%2A> propriété `Top, Left`.  
  
7.  Définissez la valeur de la <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Anchor%2A> propriété `Bottom,Right`. Le <xref:System.Windows.Forms.Button> contrôle se déplace vers l’angle inférieur droit de la cellule.  
  
8.  Définissez la valeur de la <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Anchor%2A> propriété <xref:System.Windows.Forms.AnchorStyles.None>. Le <xref:System.Windows.Forms.Button> contrôle se déplace vers le centre de la cellule.  
  
## <a name="see-also"></a>Voir aussi
- [TableLayoutPanel, contrôle](tablelayoutpanel-control-windows-forms.md)
