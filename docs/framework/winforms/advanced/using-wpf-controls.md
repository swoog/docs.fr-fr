---
title: Utilisation de contrôles WPF
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms Designer [Windows Forms], interoperability with WPF
- interoperability [WPF]
ms.assetid: 03c85dce-26ad-44cd-bc1d-8e0cb56de096
ms.openlocfilehash: 24b88e456628c5a0bdc3cded60b0e52a92057851
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57713798"
---
# <a name="using-wpf-controls"></a>Utilisation de contrôles WPF
Vous pouvez utiliser des contrôles Windows Presentation Foundation (WPF) dans vos applications Windows Forms. Bien qu’il s’agit de deux technologies d’affichage différent, ils interagissent sans heurts.  
  
 Le Concepteur de formulaires Windows fournit un environnement de conception visuelle pour l’hébergement de contrôles Windows Presentation Foundation. Un contrôle WPF est hébergé par un contrôle Windows Forms spécial nommé <xref:System.Windows.Forms.Integration.ElementHost>. Ce contrôle permet le contrôle WPF à participer à la disposition du formulaire et de recevoir des messages de clavier et souris. Au moment du design, vous pouvez organiser les <xref:System.Windows.Forms.Integration.ElementHost> contrôler tout comme vous le feriez pour n’importe quel contrôle Windows Forms.  
  
 Vous pouvez également utiliser des contrôles Windows Forms dans vos applications WPF. Pour plus d’informations, consultez [XAML de conception dans Visual Studio](/visualstudio/designers/designing-xaml-in-visual-studio).  
  
## <a name="in-this-section"></a>Dans cette section  
 [Guide pratique pour Copiez et collez un contrôle ElementHost au moment du Design](how-to-copy-and-paste-an-elementhost-control-at-design-time.md)  
 Montre comment copier un contrôle Windows Presentation Foundation sur un formulaire Windows.  
  
 [Procédure pas à pas : Réorganisation du contenu WPF dans les Windows Forms au moment du Design](walkthrough-arranging-wpf-content-on-windows-forms-at-design-time.md)  
 Montre comment utiliser les fonctionnalités de disposition Windows Forms, telles que l’ancrage et les lignes d’alignement, pour organiser les contrôles de Windows Presentation Foundation.
  
 [Procédure pas à pas : Création de contenu WPF dans les Windows Forms au moment du Design](walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md)  
 Montre comment créer un contrôle Windows Presentation Foundation pour une utilisation dans vos applications Windows Forms.
  
 [Procédure pas à pas : Assignation du contenu WPF dans les Windows Forms au moment du Design](walkthrough-assigning-wpf-content-on-windows-forms-at-design-time.md)  
 Montre comment sélectionner les types de contrôle Windows Presentation Foundation que vous souhaitez afficher sur votre formulaire.  
  
 [Procédure pas à pas : Contenu WPF de style](walkthrough-styling-wpf-content.md)  
 Affiche le workflow entre le Concepteur de formulaires Windows et le [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)] pour appliquer des styles à des contrôles Windows Presentation Foundation.  
  
## <a name="reference"></a>Référence  
 <xref:System.Windows.Forms.Integration.ElementHost>  
 Décrit une classe que vous pouvez utiliser pour héberger des contrôles Windows Presentation Foundation dans vos applications Windows Forms.  
  
 <xref:System.Windows.Forms.Integration.WindowsFormsHost>  
 Décrit une classe que vous pouvez utiliser pour héberger des contrôles Windows Forms dans votre application Windows Presentation Foundation.  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Migration et interopérabilité](../../wpf/advanced/migration-and-interoperability.md)  
 Décrit l’interopérabilité entre les technologies Windows Presentation Foundation et Windows Forms.  
  
 [Concevoir en XAML dans Visual Studio](/visualstudio/designers/designing-xaml-in-visual-studio)  
 Explique comment concevoir des contrôles Windows Presentation Foundation dans Visual Studio.
