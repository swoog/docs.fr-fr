---
title: 'Comment : affecter un arrière-plan transparent à votre contrôle'
ms.date: 03/30/2017
helpviewer_keywords:
- transparent backgrounds [Windows Forms], custom controls
- custom controls [Windows Forms], transparent background
- transparency [Windows Forms], Windows Forms custom controls
ms.assetid: 32433e63-f4e9-4305-9857-6de3edeb944a
ms.openlocfilehash: ad814c9179fd33955fe4df2666f8a47606bfbff0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-give-your-control-a-transparent-background"></a>Comment : affecter un arrière-plan transparent à votre contrôle
Dans les versions antérieures de .NET Framework, les contrôles ne prenaient pas en charge la définition de couleurs d’arrière-plan transparentes sans définition préalable de la méthode <xref:System.Windows.Forms.Control.SetStyle%2A> dans le constructeur du formulaire. Dans la version actuelle de l’infrastructure, vous pouvez affecter <xref:System.Drawing.Color.Transparent%2A> comme couleur d’arrière-plan de la plupart des contrôles  dans la fenêtre **Propriétés** au moment du design ou dans le code dans le constructeur du formulaire.  
  
> [!NOTE]
>  Les contrôles Windows Forms ne prennent pas en charge la véritable transparence. L’arrière-plan d’un contrôle Windows Forms transparent est peint par son parent.  
  
> [!NOTE]
>  Le contrôle <xref:System.Windows.Controls.Button> ne prend pas en charge une couleur d’arrière-plan transparente même quand la propriété <xref:System.Windows.Forms.ButtonBase.BackColor%2A> a la valeur <xref:System.Drawing.Color.Transparent%2A>.  
  
### <a name="to-give-your-control-a-transparent-backcolor"></a>Pour affecter un arrière-plan transparent à votre contrôle  
  
-   Dans la fenêtre Propriétés, choisissez la propriété <xref:System.Windows.Forms.ButtonBase.BackColor%2A> et affectez-lui la valeur <xref:System.Drawing.Color.Transparent%2A>.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Drawing.Color.FromArgb%2A>  
 [Développement de contrôles Windows Forms personnalisés avec le .NET Framework](../../../../docs/framework/winforms/controls/developing-custom-windows-forms-controls.md)  
 [Utilisation de classes graphiques managées](../../../../docs/framework/winforms/advanced/using-managed-graphics-classes.md)  
 [Guide pratique pour dessiner des lignes opaques et translucides](../../../../docs/framework/winforms/advanced/how-to-draw-opaque-and-semitransparent-lines.md)
