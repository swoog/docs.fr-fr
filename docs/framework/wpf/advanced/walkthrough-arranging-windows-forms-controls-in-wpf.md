---
title: 'Procédure pas à pas : organisation des contrôles Windows Forms dans WPF'
ms.date: 04/03/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- hybrid applications [WPF interoperability]
- arranging controls [WPF]
ms.assetid: a1db8049-15c7-45d6-ae3d-36a6735cb848
ms.openlocfilehash: 98b108be518a9fef03ee299d43ed591cf736f68f
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43484937"
---
# <a name="walkthrough-arranging-windows-forms-controls-in-wpf"></a>Procédure pas à pas : organisation des contrôles Windows Forms dans WPF
Cette procédure pas à pas vous montre comment utiliser [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] des fonctionnalités de disposition pour réorganiser [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôles dans une application hybride.  
  
 Cette procédure pas à pas décrit notamment les tâches suivantes :  
  
-   Création du projet  
  
-   Utilisation des paramètres de disposition par défaut  
  
-   Dimensionnement en fonction du contenu  
  
-   Utilisation du positionnement absolu  
  
-   Spécification explicite de la taille  
  
-   Définition des propriétés de disposition  
  
-   Présentation des limitations dans l’ordre de plan  
  
-   Ancrage  
  
-   Définition de la visibilité  
  
-   Hébergement d’un contrôle qui ne s’étire pas  
  
-   Mise à l’échelle  
  
-   Rotation  
  
-   Définition d’une marge intérieure et de marges  
  
-   Utilisation de conteneurs de présentation dynamiques  
  
 Pour l’intégralité du code des tâches illustrées dans cette procédure pas à pas, consultez [disposition de contrôles Windows Forms dans WPF, exemple](https://go.microsoft.com/fwlink/?LinkID=159971).  
  
 Lorsque vous avez terminé, vous aurez une compréhension de [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] des fonctionnalités de disposition dans [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]-en fonction des applications.  
  
## <a name="prerequisites"></a>Prérequis  
 Pour exécuter cette procédure pas à pas, vous devez disposer des composants suivants :  
  
-   [!INCLUDE[vs_dev10_long](../../../../includes/vs-dev10-long-md.md)].  
  
## <a name="creating-the-project"></a>Création du projet  
  
#### <a name="to-create-and-set-up-the-project"></a>Pour créer et configurer le projet  
  
1.  Créez un projet d’Application WPF nommé `WpfLayoutHostingWf`.  
  
2.  Dans l’Explorateur de solutions, ajoutez des références aux assemblys suivants.  
  
    -   WindowsFormsIntegration  
  
    -   System.Windows.Forms  
  
    -   System.Drawing  
  
3.  Double-cliquez sur MainWindow.xaml pour l’ouvrir dans la vue XAML.  
  
4.  Dans le <xref:System.Windows.Window> élément, ajoutez le code suivant [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] mappage d’espace de noms.  
  
    ```xaml  
    xmlns:wf="clr-namespace:System.Windows.Forms;assembly=System.Windows.Forms"  
    ```  
  
5.  Dans le <xref:System.Windows.Controls.Grid> élément défini le <xref:System.Windows.Controls.Grid.ShowGridLines%2A> propriété `true` et définissez cinq lignes et trois colonnes.  
  
     [!code-xaml[WpfLayoutHostingWfWithXaml#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#2)]  
  
## <a name="using-default-layout-settings"></a>Utilisation des paramètres de disposition par défaut  
 Par défaut, le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément gère la disposition pour hébergé [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle.  
  
#### <a name="to-use-default-layout-settings"></a>Pour utiliser les paramètres de disposition par défaut  
  
1.  Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.  
  
     [!code-xaml[WpfLayoutHostingWfWithXaml#3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#3)]  
  
2.  Appuyez sur F5 pour générer et exécuter l'application. Le [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] <xref:System.Windows.Forms.Button?displayProperty=nameWithType> contrôle s’affiche dans le <xref:System.Windows.Controls.Canvas>. Le contrôle hébergé est dimensionné selon son contenu et le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément est dimensionné selon le contrôle hébergé.  
  
## <a name="sizing-to-content"></a>Dimensionnement en fonction du contenu  
 Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément garantit que le contrôle hébergé est dimensionné pour afficher correctement son contenu.  
  
#### <a name="to-size-to-content"></a>Pour dimensionner en fonction du contenu  
  
1.  Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.  
  
     [!code-xaml[WpfLayoutHostingWfWithXaml#4](../../../../samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#4)]  
  
2.  Appuyez sur F5 pour générer et exécuter l'application. Les deux nouveaux contrôles bouton sont dimensionnés pour s’afficher correctement, la plus longue chaîne de texte et la taille de police et la <xref:System.Windows.Forms.Integration.WindowsFormsHost> éléments sont redimensionnés pour contenir les contrôles hébergés.  
  
## <a name="using-absolute-positioning"></a>Utilisation du positionnement absolu  
 Vous pouvez utiliser le positionnement absolu pour placer le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément n’importe où dans l’interface utilisateur (IU).  
  
#### <a name="to-use-absolute-positioning"></a>Pour utiliser le positionnement absolu  
  
1.  Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.  
  
     [!code-xaml[WpfLayoutHostingWfWithXaml#5](../../../../samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#5)]  
  
2.  Appuyez sur F5 pour générer et exécuter l'application. Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément est placé à 20 pixels du haut de la cellule de grille et 20 pixels à partir de la gauche.  
  
## <a name="specifying-size-explicitly"></a>Spécification explicite de la taille  
 Vous pouvez spécifier la taille de la <xref:System.Windows.Forms.Integration.WindowsFormsHost> à l’aide de l’élément le <xref:System.Windows.FrameworkElement.Width%2A> et <xref:System.Windows.FrameworkElement.Height%2A> propriétés.  
  
#### <a name="to-specify-size-explicitly"></a>Pour spécifier explicitement la taille  
  
1.  Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.  
  
     [!code-xaml[WpfLayoutHostingWfWithXaml#6](../../../../samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#6)]  
  
2.  Appuyez sur F5 pour générer et exécuter l'application. Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément a une taille de 50 pixels de large sur 70 pixels en hauteur, qui est plus petit que les paramètres de disposition par défaut. Le contenu de la [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle est réorganisé en conséquence.  
  
## <a name="setting-layout-properties"></a>Définition des propriétés de disposition  
 Toujours défini les propriétés relatives à la disposition sur le contrôle hébergé en utilisant les propriétés de la <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément. Si vous définissez les propriétés de disposition directement sur le contrôle hébergé, vous obtiendrez des résultats inattendus.  
  
 Définition des propriétés relatives à la disposition sur le contrôle hébergé dans [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] n’a aucun effet.  
  
#### <a name="to-see-the-effects-of-setting-properties-on-the-hosted-control"></a>Pour afficher les effets de la définition des propriétés sur le contrôle hébergé  
  
1.  Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.  
  
     [!code-xaml[WpfLayoutHostingWfWithXaml#7](../../../../samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#7)]  
  
2.  Dans l’Explorateur de solutions, double-cliquez sur MainWindow.xaml. vb ou MainWindow.xaml.cs pour l’ouvrir dans l’éditeur de code.  
  
3.  Copiez le code suivant dans le `MainWindow` définition de classe.  
  
     [!code-csharp[WpfLayoutHostingWfWithXaml#101](../../../../samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml.cs#101)]
     [!code-vb[WpfLayoutHostingWfWithXaml#101](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/VisualBasic/Window1.xaml.vb#101)]  
  
4.  Appuyez sur F5 pour générer et exécuter l'application.  
  
5.  Cliquez sur le **Click me** bouton. Le `button1_Click` Gestionnaire d’événements définit la <xref:System.Windows.Forms.Control.Top%2A> et <xref:System.Windows.Forms.Control.Left%2A> propriétés sur le contrôle hébergé. Le contrôle hébergé est ainsi repositionné dans le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément. L’hôte conserve la même zone d’écran, mais le contrôle hébergé est découpé. Au lieu de cela, le contrôle hébergé doit toujours remplir le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément.  
  
## <a name="understanding-z-order-limitations"></a>Présentation des limitations dans l’ordre de plan  
 Visible <xref:System.Windows.Forms.Integration.WindowsFormsHost> éléments sont toujours dessinés sur d’autres éléments WPF, et ils ne sont pas affectés par l’ordre de plan. Pour voir ce comportement de l’ordre de plan, procédez comme suit :

1.  Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.

     [!code-xaml[WpfLayoutHostingWfWithXaml#8](../../../../samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#8)]  
 
2.  Appuyez sur F5 pour générer et exécuter l'application. Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément est peint sur l’élément label.  


## <a name="docking"></a>Ancrage  
 <xref:System.Windows.Forms.Integration.WindowsFormsHost> prend en charge de l’élément [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] d’ancrage. Définir le <xref:System.Windows.Controls.DockPanel.Dock%2A> propriété jointe pour ancrer le contrôle hébergé dans un <xref:System.Windows.Controls.DockPanel> élément.  
  
#### <a name="to-dock-a-hosted-control"></a>Pour ancrer un contrôle hébergé  
  
1.  Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.  
  
     [!code-xaml[WpfLayoutHostingWfWithXaml#9](../../../../samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#9)]  
  
2.  Appuyez sur F5 pour générer et exécuter l'application. Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément est ancré à droite de la <xref:System.Windows.Controls.DockPanel> élément.  
  
## <a name="setting-visibility"></a>Définition de la visibilité  
 Vous pouvez rendre votre [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle invisible ou réduit en définissant le <xref:System.Windows.UIElement.Visibility%2A> propriété sur le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément. Quand un contrôle est invisible, il n’est pas affiché, mais il occupe l’espace de disposition. Quand un contrôle est réduit, il n’est pas affiché et n’occupe pas l’espace de disposition.  
  
#### <a name="to-set-the-visibility-of-a-hosted-control"></a>Pour définir la visibilité d’un contrôle hébergé  
  
1.  Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.  
  
     [!code-xaml[WpfLayoutHostingWfWithXaml#10](../../../../samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#10)]  
  
2.  Dans MainWindow.xaml.vb ou MainWindow.xaml.cs, copiez le code suivant dans la définition de classe.  
  
     [!code-csharp[WpfLayoutHostingWfWithXaml#102](../../../../samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml.cs#102)]
     [!code-vb[WpfLayoutHostingWfWithXaml#102](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/VisualBasic/Window1.xaml.vb#102)]  
  
3.  Appuyez sur F5 pour générer et exécuter l'application.  
  
4.  Cliquez sur le **cliquer pour rendre invisible** bouton pour rendre le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément invisible.  
  
5.  Cliquez sur le **cliquer pour réduire** bouton pour masquer la <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément à partir de la mise en page entièrement. Lorsque le [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle est réduit, les éléments voisins sont réorganisés pour occuper son espace.  
  
## <a name="hosting-a-control-that-does-not-stretch"></a>Hébergement d’un contrôle qui ne s’étire pas  
 Certains [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôles ont une taille fixe et ne s’étirent pas pour remplir l’espace disponible dans la disposition. Par exemple, le <xref:System.Windows.Forms.MonthCalendar> contrôle affiche un mois dans un espace fixe.  
  
#### <a name="to-host-a-control-that-does-not-stretch"></a>Pour héberger un contrôle qui ne s’étire pas  
  
1.  Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.  
  
     [!code-xaml[WpfLayoutHostingWfWithXaml#11](../../../../samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#11)]  
  
2.  Appuyez sur F5 pour générer et exécuter l'application. Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément est centré dans la ligne de grille, mais il n’est pas étiré pour remplir l’espace disponible. Si la fenêtre est suffisamment grande, vous pouvez voir deux mois ou plus affichées par hébergé <xref:System.Windows.Forms.MonthCalendar> contrôle, mais ils sont centrés dans la ligne. Le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] moteur de disposition centre les éléments qui ne peut pas être redimensionnés pour remplir l’espace disponible.  
  
## <a name="scaling"></a>Mise à l'échelle  
 Contrairement aux éléments WPF, la plupart des contrôles Windows Forms ne sont pas évolutives en continu. Pour fournir la mise à l’échelle personnalisée, vous substituez le <xref:System.Windows.Forms.Integration.WindowsFormsHost.ScaleChild%2A?displayProperty=nameWithType> (méthode). 
  
#### <a name="to-scale-a-hosted-control-by-using-the-default-behavior"></a>Pour mettre à l’échelle un contrôle hébergé selon le comportement par défaut  
  
1.  Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.  
  
     [!code-xaml[WpfLayoutHostingWfWithXaml#12](../../../../samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#12)]  
  
2.  Appuyez sur F5 pour générer et exécuter l'application. Le contrôle hébergé et ses éléments voisins sont mis à l’échelle par un facteur de 0,5. Toutefois, la police du contrôle hébergé n’est pas mise à l’échelle.

<!-- This could use an example of custom scaling. -->

## <a name="rotating"></a>Rotation  
 Contrairement aux éléments WPF, les contrôles Windows Forms ne gèrent pas de rotation. Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément ne pivote pas avec d’autres éléments WPF lorsqu’une transformation de rotation est appliquée. Toute valeur de rotation autre que 180 degrés déclenche le <xref:System.Windows.Forms.Integration.WindowsFormsHost.LayoutError> événement.
 
#### <a name="to-see-the-effect-of-rotation-in-a-hybrid-application"></a>Pour voir l’effet de la rotation dans une application hybride  
  
1.  Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.  
  
     [!code-xaml[WpfLayoutHostingWfWithXaml#13](../../../../samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#13)]  
  
2.  Appuyez sur F5 pour générer et exécuter l'application. Le contrôle hébergé ne pivote pas, mais ses éléments voisins subissent une rotation de 180 degrés. Vous devrez peut-être redimensionner la fenêtre pour apercevoir les éléments.  
 

## <a name="setting-padding-and-margins"></a>Définition d’une marge intérieure et de marges  
 Marge intérieure et marges dans [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] sont semblables aux marge intérieure et marges dans [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]. Il suffit de définir la <xref:System.Windows.Controls.Control.Padding%2A> et <xref:System.Windows.FrameworkElement.Margin%2A> propriétés sur le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément.  
  
#### <a name="to-set-padding-and-margins-for-a-hosted-control"></a>Pour définir la marge intérieure et les marges d’un contrôle hébergé  
  
1.  Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.  
  
     [!code-xaml[WpfLayoutHostingWfWithXaml#14](../../../../samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#14)]  
    [!code-xaml[WpfLayoutHostingWfWithXaml#15](../../../../samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#15)]  
  
2.  Appuyez sur F5 pour générer et exécuter l'application. Les paramètres de marge intérieure et marges sont appliqués à hébergé [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôles de la même façon qu’ils seraient appliqués dans [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)].  
  
## <a name="using-dynamic-layout-containers"></a>Utilisation de conteneurs de disposition dynamiques  
 [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] fournit deux conteneurs de disposition dynamique, <xref:System.Windows.Forms.FlowLayoutPanel> et <xref:System.Windows.Forms.TableLayoutPanel>. Vous pouvez également utiliser ces conteneurs dans [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] dispositions.  
  
#### <a name="to-use-a-dynamic-layout-container"></a>Pour utiliser un conteneur de disposition dynamique  
  
1.  Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.  
  
     [!code-xaml[WpfLayoutHostingWfWithXaml#16](../../../../samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#16)]  
  
2.  Dans MainWindow.xaml.vb ou MainWindow.xaml.cs, copiez le code suivant dans la définition de classe.  
  
     [!code-csharp[WpfLayoutHostingWfWithXaml#103](../../../../samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml.cs#103)]
     [!code-vb[WpfLayoutHostingWfWithXaml#103](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/VisualBasic/Window1.xaml.vb#103)]  
  
3.  Ajoutez un appel à la `InitializeFlowLayoutPanel` méthode dans le constructeur.  
  
     [!code-csharp[WpfLayoutHostingWfWithXaml#104](../../../../samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml.cs#104)]
     [!code-vb[WpfLayoutHostingWfWithXaml#104](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/VisualBasic/Window1.xaml.vb#104)]  
  
4.  Appuyez sur F5 pour générer et exécuter l'application. Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément remplit la <xref:System.Windows.Controls.DockPanel>, et <xref:System.Windows.Forms.FlowLayoutPanel> réorganise ses contrôles enfants dans la valeur par défaut <xref:System.Windows.Forms.FlowLayoutPanel.FlowDirection%2A>.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.Integration.ElementHost>  
 <xref:System.Windows.Forms.Integration.WindowsFormsHost>  
 [Concevoir en XAML dans Visual Studio](/visualstudio/designers/designing-xaml-in-visual-studio)  
 [Considérations sur la disposition de l’élément WindowsFormsHost](../../../../docs/framework/wpf/advanced/layout-considerations-for-the-windowsformshost-element.md)  
 [Organisation des Windows Forms contrôles dans WPF, exemple](https://go.microsoft.com/fwlink/?LinkID=159971)  
 [Procédure pas à pas : hébergement d'un contrôle composite Windows Forms dans WPF](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-windows-forms-composite-control-in-wpf.md)  
 [Procédure pas à pas : Hébergement d'un contrôle composite WPF dans Windows Forms](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-wpf-composite-control-in-windows-forms.md)
