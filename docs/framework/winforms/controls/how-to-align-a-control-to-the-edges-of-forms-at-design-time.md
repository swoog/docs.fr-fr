---
title: 'Procédure : aligner un contrôle sur les bords des formulaires au moment du design'
ms.date: 03/30/2017
helpviewer_keywords:
- custom controls [Windows Forms], docking using designer
- Dock property [Windows Forms], aligning controls (using designer)
ms.assetid: 51f08998-5e3b-4330-be58-a4edd0eb60f4
ms.openlocfilehash: b08e01eb9adb984a32a8fc435cf1f3b93b159a14
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65210381"
---
# <a name="how-to-align-a-control-to-the-edges-of-forms-at-design-time"></a>Procédure : aligner un contrôle sur les bords des formulaires au moment du design

Vous pouvez aligner un contrôle sur le bord de vos formulaires en définissant la valeur de la <xref:System.Windows.Forms.Control.Dock%2A> propriété. Cette propriété désigne l’emplacement de votre contrôle dans le formulaire. La propriété <xref:System.Windows.Forms.Control.Dock%2A> peut avoir les valeurs suivantes :

|Paramètre|Effet sur le contrôle|
|-------------|----------------------------|
|<xref:System.Windows.Forms.DockStyle.Bottom>|S'ancre en bas du formulaire.|
|<xref:System.Windows.Forms.DockStyle.Fill>|Remplit tout l'espace restant dans le formulaire.|
|<xref:System.Windows.Forms.DockStyle.Left>|S'ancre sur le côté gauche du formulaire.|
|<xref:System.Windows.Forms.DockStyle.None>|Ne s’ancre en tout lieu et il s’affiche à l’emplacement spécifié par son <xref:System.Windows.Forms.Control.Location%2A>.|
|<xref:System.Windows.Forms.DockStyle.Right>|S'ancre sur le côté droit du formulaire.|
|<xref:System.Windows.Forms.DockStyle.Top>|S'ancre en haut du formulaire.|

Ces valeurs peuvent également être définies dans le code. Pour plus d'informations, voir [Procédure : Aligner un contrôle sur les bords des formulaires](how-to-align-a-control-to-the-edges-of-forms.md).

## <a name="set-the-dock-property-for-your-control-at-design-time"></a>Définir la propriété Dock de votre contrôle au moment du design

1. Dans le Concepteur de formulaires Windows dans Visual Studio, sélectionnez votre contrôle.

2. Dans le **propriétés** , cliquez sur la liste déroulante située en regard du <xref:System.Windows.Forms.Control.Dock%2A> propriété.

     Une interface graphique représentant les six possibles <xref:System.Windows.Forms.Control.Dock%2A> paramètres s’affiche.

3. Choisissez le paramètre approprié.

4. Votre contrôle s’ancre maintenant de la manière spécifiée par le paramètre.

## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Control.Dock%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.Anchor%2A?displayProperty=nameWithType>
- [Guide pratique pour Aligner un contrôle sur les bords des formulaires](how-to-align-a-control-to-the-edges-of-forms.md)
- [Procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide des lignes d’alignement](walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)
- [Guide pratique pour Ancrer les contrôles aux Windows Forms](how-to-anchor-controls-on-windows-forms.md)
- [Guide pratique pour Ancrer et arrimer des contrôles enfants dans un contrôle TableLayoutPanel](how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)
- [Guide pratique pour Ancrer et arrimer des contrôles enfants dans un contrôle FlowLayoutPanel](how-to-anchor-and-dock-child-controls-in-a-flowlayoutpanel-control.md)
- [Procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide d’un TableLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)
- [Procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide d’un FlowLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md)
- [Développement de contrôles Windows Forms au moment du design](developing-windows-forms-controls-at-design-time.md)
