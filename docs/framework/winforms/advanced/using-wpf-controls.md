---
title: Utilisation de contrôles WPF
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms Designer [Windows Forms], interoperability with WPF
- interoperability [WPF]
ms.assetid: 03c85dce-26ad-44cd-bc1d-8e0cb56de096
ms.openlocfilehash: be925bdceea3dd01c568d85fe025d6e037066454
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47170468"
---
# <a name="using-wpf-controls"></a>Utilisation de contrôles WPF
Vous pouvez utiliser des contrôles Windows Presentation Foundation (WPF) dans vos applications Windows Forms. Bien qu’il s’agit de deux technologies d’affichage différent, ils interagissent sans heurts.  
  
 Le Concepteur de formulaires Windows fournit un environnement de conception visuelle pour l’hébergement de contrôles Windows Presentation Foundation. Un contrôle WPF est hébergé par un contrôle Windows Forms spécial nommé <xref:System.Windows.Forms.Integration.ElementHost>. Ce contrôle permet le contrôle WPF à participer à la disposition du formulaire et de recevoir des messages de clavier et souris. Au moment du design, vous pouvez organiser les <xref:System.Windows.Forms.Integration.ElementHost> contrôler tout comme vous le feriez pour n’importe quel contrôle Windows Forms.  
  
 Vous pouvez également utiliser des contrôles Windows Forms dans vos applications WPF. Pour plus d’informations, consultez [XAML de conception dans Visual Studio](/visualstudio/designers/designing-xaml-in-visual-studio).  
  
## <a name="in-this-section"></a>Dans cette section  
 [Guide pratique pour copier et coller un contrôle ElementHost au moment du design](../../../../docs/framework/winforms/advanced/how-to-copy-and-paste-an-elementhost-control-at-design-time.md)  
 Montre comment copier un contrôle Windows Presentation Foundation sur un formulaire Windows.  
  
 [Procédure pas à pas : réorganisation du contenu WPF sur les Windows Forms au moment du design](../../../../docs/framework/winforms/advanced/walkthrough-arranging-wpf-content-on-windows-forms-at-design-time.md)  
 Montre comment utiliser les fonctionnalités de disposition Windows Forms, telles que l’ancrage et les lignes d’alignement, pour organiser les contrôles de Windows Presentation Foundation.
  
 [Procédure pas à pas : création de contenu WPF sur les Windows Forms au moment du design](../../../../docs/framework/winforms/advanced/walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md)  
 Montre comment créer un contrôle Windows Presentation Foundation pour une utilisation dans vos applications Windows Forms.
  
 [Procédure pas à pas : assignation du contenu WPF sur les Windows Forms au moment du design](../../../../docs/framework/winforms/advanced/walkthrough-assigning-wpf-content-on-windows-forms-at-design-time.md)  
 Montre comment sélectionner les types de contrôle Windows Presentation Foundation que vous souhaitez afficher sur votre formulaire.  
  
 [Procédure pas à pas : application de styles au contenu WPF](../../../../docs/framework/winforms/advanced/walkthrough-styling-wpf-content.md)  
 Affiche le workflow entre le Concepteur de formulaires Windows et le [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)] pour appliquer des styles à des contrôles Windows Presentation Foundation.  
  
## <a name="reference"></a>Référence  
 <xref:System.Windows.Forms.Integration.ElementHost>  
 Décrit une classe que vous pouvez utiliser pour héberger des contrôles Windows Presentation Foundation dans vos applications Windows Forms.  
  
 <xref:System.Windows.Forms.Integration.WindowsFormsHost>  
 Décrit une classe que vous pouvez utiliser pour héberger des contrôles Windows Forms dans votre application Windows Presentation Foundation.  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Migration et interopérabilité](../../../../docs/framework/wpf/advanced/migration-and-interoperability.md)  
 Décrit l’interopérabilité entre les technologies Windows Presentation Foundation et Windows Forms.  
  
 [Concevoir en XAML dans Visual Studio](/visualstudio/designers/designing-xaml-in-visual-studio)  
 Explique comment concevoir des contrôles Windows Presentation Foundation dans Visual Studio.
