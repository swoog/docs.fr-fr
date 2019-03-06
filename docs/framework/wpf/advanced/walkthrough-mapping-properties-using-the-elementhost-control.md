---
title: 'Procédure pas à pas : Mappage de propriétés à l’aide du contrôle ElementHost'
ms.date: 08/18/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- mapping properties [WPF]
- ElementHost control [WPF], mapping properties
ms.assetid: bccd6e0d-2272-4924-9107-ff8ed58b88aa
ms.openlocfilehash: 3fe3f00950fdfdf92c3f95dc42b27cc9110e0c95
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57371682"
---
# <a name="walkthrough-mapping-properties-using-the-elementhost-control"></a>Procédure pas à pas : Mappage de propriétés à l’aide du contrôle ElementHost

Cette procédure pas à pas vous montre comment utiliser le <xref:System.Windows.Forms.Integration.ElementHost.PropertyMap%2A> propriété à mapper [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] propriétés aux propriétés correspondantes dans un hébergé [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] élément.

Cette procédure pas à pas décrit notamment les tâches suivantes :

-   Création du projet

-   Définition d’un nouveau mappage de propriété.

-   Suppression d’un mappage de propriété par défaut.

-   Extension d’un mappage de propriété par défaut.

Pour l’intégralité du code des tâches illustrées dans cette procédure pas à pas, consultez [propriétés de mappage à l’aide de l’exemple de contrôle ElementHost](https://go.microsoft.com/fwlink/?LinkID=160018).

Lorsque vous avez terminé, vous serez en mesure de mapper [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] propriétés correspondant [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] propriétés sur un élément hébergé.

## <a name="prerequisites"></a>Prérequis

Pour exécuter cette procédure pas à pas, vous devez disposer des composants suivants :

-   Visual Studio 2017

## <a name="creating-the-project"></a>Création du projet

### <a name="to-create-the-project"></a>Pour créer le projet

1.  Créer un **Windows Forms application** projet nommé `PropertyMappingWithElementHost`.

2.  Dans **l’Explorateur de solutions**, ajoutez des références à ce qui suit [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] assemblys.

    -   PresentationCore

    -   PresentationFramework

    -   WindowsBase

    -   WindowsFormsIntegration

3.  Copiez le code suivant en haut de la `Form1` fichier de code.

     [!code-csharp[PropertyMappingWithElementHost#10](~/samples/snippets/csharp/VS_Snippets_Wpf/PropertyMappingWithElementHost/CSharp/PropertyMappingWithElementHost/Form1.cs#10)]
     [!code-vb[PropertyMappingWithElementHost#10](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PropertyMappingWithElementHost/VisualBasic/PropertyMappingWithElementHost/Form1.vb#10)]

4.  Ouvrez `Form1` dans le Concepteur Windows Forms. Double-cliquez sur le formulaire pour ajouter un gestionnaire d’événements pour le <xref:System.Windows.Forms.Form.Load> événement.

5.  Revenez au Concepteur Windows Forms et ajouter un gestionnaire d’événements pour le formulaire <xref:System.Windows.Forms.Control.Resize> événement. Pour plus d'informations, voir [Procédure : Créer des gestionnaires d’événements à l’aide du concepteur](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/zwwsdtbk(v=vs.100)).

6.  Déclarez un <xref:System.Windows.Forms.Integration.ElementHost> champ dans le `Form1` classe.

     [!code-csharp[PropertyMappingWithElementHost#16](~/samples/snippets/csharp/VS_Snippets_Wpf/PropertyMappingWithElementHost/CSharp/PropertyMappingWithElementHost/Form1.cs#16)]
     [!code-vb[PropertyMappingWithElementHost#16](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PropertyMappingWithElementHost/VisualBasic/PropertyMappingWithElementHost/Form1.vb#16)]

## <a name="defining-new-property-mappings"></a>Définition de nouveaux mappages de propriété

Le <xref:System.Windows.Forms.Integration.ElementHost> contrôle fournit par défaut plusieurs mappages de propriété. Vous ajoutez un nouveau mappage de propriété en appelant le <xref:System.Windows.Forms.Integration.PropertyMap.Add%2A> méthode sur le <xref:System.Windows.Forms.Integration.ElementHost> du contrôle <xref:System.Windows.Forms.Integration.ElementHost.PropertyMap%2A>.

### <a name="to-define-new-property-mappings"></a>Pour définir de nouveaux mappages de propriété

1.  Copiez le code suivant dans la définition de la `Form1` classe.

     [!code-csharp[PropertyMappingWithElementHost#12](~/samples/snippets/csharp/VS_Snippets_Wpf/PropertyMappingWithElementHost/CSharp/PropertyMappingWithElementHost/Form1.cs#12)]
     [!code-vb[PropertyMappingWithElementHost#12](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PropertyMappingWithElementHost/VisualBasic/PropertyMappingWithElementHost/Form1.vb#12)]

     Le `AddMarginMapping` méthode ajoute un nouveau mappage pour le <xref:System.Windows.Forms.Control.Margin%2A> propriété.

     Le `OnMarginChange` méthode se traduit par la <xref:System.Windows.Forms.Control.Margin%2A> propriété le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.FrameworkElement.Margin%2A> propriété.

2.  Copiez le code suivant dans la définition de la `Form1` classe.

     [!code-csharp[PropertyMappingWithElementHost#14](~/samples/snippets/csharp/VS_Snippets_Wpf/PropertyMappingWithElementHost/CSharp/PropertyMappingWithElementHost/Form1.cs#14)]
     [!code-vb[PropertyMappingWithElementHost#14](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PropertyMappingWithElementHost/VisualBasic/PropertyMappingWithElementHost/Form1.vb#14)]

     Le `AddRegionMapping` méthode ajoute un nouveau mappage pour le <xref:System.Windows.Forms.Control.Region%2A> propriété.

     Le `OnRegionChange` méthode se traduit par la <xref:System.Windows.Forms.Control.Region%2A> propriété le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.UIElement.Clip%2A> propriété.

     Le `Form1_Resize` méthode gère le formulaire <xref:System.Windows.Forms.Control.Resize> événements et de la taille de la zone de découpage pour s’ajuster à l’élément hébergé.

## <a name="removing-a-default-property-mapping"></a>Suppression d’un mappage de propriété par défaut

Supprimer un mappage de propriété par défaut en appelant le <xref:System.Windows.Forms.Integration.PropertyMap.Remove%2A> méthode sur le <xref:System.Windows.Forms.Integration.ElementHost> du contrôle <xref:System.Windows.Forms.Integration.ElementHost.PropertyMap%2A>.

### <a name="to-remove-a-default-property-mapping"></a>Pour supprimer un mappage de propriété par défaut

-   Copiez le code suivant dans la définition de la `Form1` classe.

     [!code-csharp[PropertyMappingWithElementHost#13](~/samples/snippets/csharp/VS_Snippets_Wpf/PropertyMappingWithElementHost/CSharp/PropertyMappingWithElementHost/Form1.cs#13)]
     [!code-vb[PropertyMappingWithElementHost#13](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PropertyMappingWithElementHost/VisualBasic/PropertyMappingWithElementHost/Form1.vb#13)]

     Le `RemoveCursorMapping` méthode supprime le mappage par défaut pour le <xref:System.Windows.Forms.Control.Cursor%2A> propriété.

## <a name="extending-a-default-property-mapping"></a>Extension d’un mappage de propriété par défaut

Vous pouvez utiliser un mappage de propriété par défaut et l’étendre avec votre propre mappage.

### <a name="to-extend-a-default-property-mapping"></a>Pour étendre un mappage de propriété par défaut

-   Copiez le code suivant dans la définition de la `Form1` classe.

     [!code-csharp[PropertyMappingWithElementHost#15](~/samples/snippets/csharp/VS_Snippets_Wpf/PropertyMappingWithElementHost/CSharp/PropertyMappingWithElementHost/Form1.cs#15)]
     [!code-vb[PropertyMappingWithElementHost#15](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PropertyMappingWithElementHost/VisualBasic/PropertyMappingWithElementHost/Form1.vb#15)]

     Le `ExtendBackColorMapping` méthode ajoute un traducteur de propriété personnalisée à l’objet existant <xref:System.Windows.Forms.Control.BackColor%2A> mappage de propriété.

     Le `OnBackColorChange` méthode assigne une image spécifique du contrôle hébergé <xref:System.Windows.Controls.Control.Background%2A> propriété. Le `OnBackColorChange` méthode est appelée une fois que le mappage de propriété par défaut est appliqué.

## <a name="initialize-your-property-mappings"></a>Initialiser vos mappages de propriétés

1.  Copiez le code suivant dans la définition de la `Form1` classe.

     [!code-csharp[PropertyMappingWithElementHost#11](~/samples/snippets/csharp/VS_Snippets_Wpf/PropertyMappingWithElementHost/CSharp/PropertyMappingWithElementHost/Form1.cs#11)]
     [!code-vb[PropertyMappingWithElementHost#11](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PropertyMappingWithElementHost/VisualBasic/PropertyMappingWithElementHost/Form1.vb#11)]

     Le `Form1_Load` méthode gère le <xref:System.Windows.Forms.Form.Load> événement et effectue l’initialisation suivante.

    -   Crée un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.Button> élément.

    -   Appelle les méthodes que vous avez définies précédemment dans la procédure pas à pas pour configurer les mappages de propriétés.

    -   Assigne les valeurs initiales aux propriétés mappées.

2.  Appuyez sur F5 pour générer et exécuter l'application.

## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Integration.ElementHost.PropertyMap%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost.PropertyMap%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [Mappage de propriétés Windows Forms et WPF](windows-forms-and-wpf-property-mapping.md)
- [Concevoir en XAML dans Visual Studio](/visualstudio/designers/designing-xaml-in-visual-studio)
- [Procédure pas à pas : Hébergement d’un contrôle Composite WPF dans les Windows Forms](walkthrough-hosting-a-wpf-composite-control-in-windows-forms.md)