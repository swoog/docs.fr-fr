---
title: Développement de contrôles Windows Forms au moment du design
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms controls [Windows Forms]
- Windows Forms controls, creating
- controls [Windows Forms]
- controls [Windows Forms], creating
- user controls [Windows Forms]
- custom controls [Windows Forms]
ms.assetid: e5a8e088-7ec8-4fd9-bcb3-9078fd134829
ms.openlocfilehash: 641a6c1c99169c6836c33b3e84b2ae02aba298d2
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57707714"
---
# <a name="developing-windows-forms-controls-at-design-time"></a>Développement de contrôles Windows Forms au moment du design
Pour les auteurs de contrôles, le .NET Framework fournit une multitude de technologies de création de contrôles. Les auteurs ne sont plus contraints de concevoir des contrôles composites qui agissent en tant que collection de contrôles préexistants. À travers l’héritage, vous pouvez créer vos propres contrôles à partir de contrôles composites ou de contrôles Windows Forms préexistants. Vous pouvez également concevoir vos propres contrôles qui implémentent un dessin personnalisé. Ces options permettent une grande souplesse dans la conception et les fonctionnalités de l’interface visuelle. Pour tirer parti de ces fonctionnalités, vous devez bien connaître les concepts de la programmation orientée objet.  
  
> [!NOTE]
>  Il n’est pas nécessaire d’avoir une connaissance approfondie de l’héritage, mais il peut s’avérer utile pour faire référence à [fondamentaux de l’héritage (Visual Basic)](~/docs/visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md).  
  
 Si vous voulez créer des contrôle personnalisés à utiliser sur des Web Forms, consultez [Développement de contrôles serveur ASP.NET personnalisés](https://docs.microsoft.com/previous-versions/aspnet/zt27tfhy(v=vs.100)).  
  
## <a name="in-this-section"></a>Dans cette section  
 [Procédure pas à pas : Création d’un contrôle Composite avec Visual Basic](walkthrough-authoring-a-composite-control-with-visual-basic.md)  
 Montre comment créer un contrôle composite simple dans Visual Basic.  
  
 [Procédure pas à pas : Création d’un contrôle Composite avec VisualC#](walkthrough-authoring-a-composite-control-with-visual-csharp.md)  
 Montre comment créer un contrôle composite simple dans C#.  
  
 [Procédure pas à pas : Héritage d’un contrôle de formulaire Windows avec Visual Basic](walkthrough-inheriting-from-a-windows-forms-control-with-visual-basic.md)  
 Montre comment créer un contrôle Windows Forms simple à l’aide de l’héritage dans Visual Basic.  
  
 [Procédure pas à pas : Héritage d’un contrôle de formulaire Windows avec VisualC#](walkthrough-inheriting-from-a-windows-forms-control-with-visual-csharp.md)  
 Montre comment créer un contrôle Windows Forms simple à l’aide de l’héritage dans C#.  
  
 [Procédure pas à pas : Effectuer des tâches courantes à l’aide d’intelligent des balises sur Windows Forms contrôles](performing-common-tasks-using-smart-tags-on-wf-controls.md)  
 Montre comment utiliser la fonctionnalité de balise active sur les contrôles Windows Forms.  
  
 [Procédure pas à pas : Sérialisation des Collections de Types Standard avec DesignerSerializationVisibilityAttribute](serializing-collections-designerserializationvisibilityattribute.md)  
 Montre comment utiliser le <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute.Content?displayProperty=nameWithType> attribut pour sérialiser une collection.  
  
 [Procédure pas à pas : Débogage des contrôles Windows Forms personnalisés au moment du design](walkthrough-debugging-custom-windows-forms-controls-at-design-time.md)  
 Montre comment déboguer le comportement au moment du design de votre contrôle personnalisé.  
  
 [Procédure pas à pas : Création d’un contrôle de formulaire Windows qui tire parti des fonctionnalités au moment du Design de Visual Studio](creating-a-wf-control-design-time-features.md)  
 Montre comment intégrer étroitement un contrôle composite dans l’environnement de conception.  
  
 [Guide pratique pour Créer des contrôles pour les Windows Forms](how-to-author-controls-for-windows-forms.md)  
 Fournit une vue d’ensemble des considérations pour l’implémentation d’un contrôle Windows Forms.  
  
 [Guide pratique pour Créer des contrôles composites](how-to-author-composite-controls.md)  
 Montre comment créer un contrôle en héritant d’un contrôle composite.  
  
 [Guide pratique pour Hériter de la classe UserControl](how-to-inherit-from-the-usercontrol-class.md)  
 Fournit une vue d’ensemble de la procédure de création d’un contrôle composite.  
  
 [Guide pratique pour Windows existant hériter de contrôles de formulaires](how-to-inherit-from-existing-windows-forms-controls.md)  
 Montre comment créer un contrôle étendu en héritant de la <xref:System.Windows.Forms.Button> classe de contrôle.  
  
 [Guide pratique pour Héritez de la classe de contrôle](how-to-inherit-from-the-control-class.md)  
 Fournit une vue d’ensemble de la création d’un contrôle étendu.  
  
 [Guide pratique pour Aligner un contrôle sur les bords des formulaires au moment du Design](how-to-align-a-control-to-the-edges-of-forms-at-design-time.md)  
 Montre comment utiliser le <xref:System.Windows.Forms.Control.Dock%2A> propriété pour aligner votre contrôle sur le bord du formulaire qu’il occupe.  
  
 [Guide pratique pour Afficher un contrôle dans la boîte de dialogue de boîte à outils éléments choisir](how-to-display-a-control-in-the-choose-toolbox-items-dialog-box.md)  
 Montre la procédure d’installation de votre contrôle afin qu’il apparaisse dans la boîte de dialogue **Personnaliser la boîte à outils**.  
  
 [Guide pratique pour Fournir une Bitmap de boîte à outils pour un contrôle](how-to-provide-a-toolbox-bitmap-for-a-control.md)  
 Montre comment utiliser le <xref:System.Drawing.ToolboxBitmapAttribute> pour afficher une icône en regard de votre contrôle personnalisé dans le **boîte à outils**.  
  
 [Guide pratique pour Tester le comportement au moment de l’exécution d’un UserControl](how-to-test-the-run-time-behavior-of-a-usercontrol.md)  
 Montre comment utiliser le **conteneur de test UserControl** pour tester le comportement d’un contrôle composite.  
  
 [Erreurs au moment du design dans le Concepteur Windows Forms](design-time-errors-in-the-windows-forms-designer.md)  
 Explique la signification et l’utilisation de la liste d’erreurs au moment du design qui apparaît dans Microsoft Visual Studio en cas d’échec du chargement du Concepteur Windows Forms.  
  
 [Dépannage de la création de contrôles et de composants](troubleshooting-control-and-component-authoring.md)  
 Montre comment diagnostiquer et résoudre les problèmes courants qui peuvent se produire quand vous créez un composant ou un contrôle personnalisé.  
  
## <a name="reference"></a>Référence  
 <xref:System.Windows.Forms.Control?displayProperty=nameWithType>  
 Décrit cette classe et propose des liens vers tous ses membres.  
  
 <xref:System.Windows.Forms.UserControl?displayProperty=nameWithType>  
 Décrit cette classe et propose des liens vers tous ses membres.  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Développement de contrôles Windows Forms personnalisés avec le .NET Framework](developing-custom-windows-forms-controls.md)  
 Explique comment créer vos propres contrôles personnalisés avec le .NET Framework.  
  
 [Indépendance du langage et composants indépendants du langage](../../../standard/language-independence-and-language-independent-components.md)  
 Présente le common language runtime, qui est conçu pour simplifier la création et l’utilisation des composants. Un aspect important de cette simplification est l’interopérabilité améliorée entre les composants écrits à l’aide de différents langages de programmation. La Common Language Specification (CLS) permet de créer des outils et composants fonctionnant avec plusieurs langages de programmation.  
  
 [Procédure pas à pas : Remplissage automatique de la boîte à outils avec des composants personnalisés](walkthrough-automatically-populating-the-toolbox-with-custom-components.md)  
 Décrit comment activer l’affichage de votre composant ou de votre contrôle dans la boîte de dialogue **Personnaliser la boîte à outils**.
