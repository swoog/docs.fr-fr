---
title: "Procédure pas à pas : hébergement d'un contrôle Windows Forms dans WPF avec XAML"
ms.date: 03/30/2017
helpviewer_keywords:
- hosting Windows Forms control in WPF [WPF]
ms.assetid: 1aef42cb-4cfb-44b4-9a7a-c02632d3d9c7
ms.openlocfilehash: b55a51a7ca16416b6963c57395da2f2a88a55648
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33548582"
---
# <a name="walkthrough-hosting-a-windows-forms-control-in-wpf-by-using-xaml"></a>Procédure pas à pas : hébergement d'un contrôle Windows Forms dans WPF avec XAML
[!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] fournit de nombreux contrôles avec un ensemble complet de fonctionnalités. Toutefois, vous souhaiterez parfois utiliser [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle sur votre [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] pages. Par exemple, avoir un investissement substantiel existant [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôles, ou vous pouvez avoir un [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle qui fournit des fonctionnalités uniques.  
  
 Cette procédure pas à pas vous montre comment héberger un Windows Forms <xref:System.Windows.Forms.MaskedTextBox?displayProperty=nameWithType> control sur un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] page à l’aide de [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)].  
  
 Pour l’intégralité du code des tâches illustrées dans cette procédure pas à pas, consultez [qui héberge un contrôle Windows Forms dans WPF à l’aide de XAML, exemple](http://go.microsoft.com/fwlink/?LinkID=160000).  
  
## <a name="prerequisites"></a>Prérequis  
 Pour exécuter cette procédure pas à pas, vous devez disposer des composants suivants :  
  
-   [!INCLUDE[vs_dev10_long](../../../../includes/vs-dev10-long-md.md)].  
  
## <a name="hosting-the-windows-forms-control"></a>Hébergement d’un contrôle Windows Forms  
  
#### <a name="to-host-the-maskedtextbox-control"></a>Pour héberger le contrôle MaskedTextBox  
  
1.  Créez un projet d’Application WPF nommé `HostingWfInWpfWithXaml`.  
  
2.  Ajoutez les références aux assemblys suivants.  
  
    -   WindowsFormsIntegration  
  
    -   System.Windows.Forms  
  
3.  Ouvrez MainWindow.xaml dans le [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)].  
  
4.  Dans la <xref:System.Windows.Window> élément, ajoutez le mappage d’espace de noms suivant. Le `wf` mappage d’espace de noms établit une référence à l’assembly qui contient le contrôle Windows Forms.  
  
    ```xaml  
    xmlns:wf="clr-namespace:System.Windows.Forms;assembly=System.Windows.Forms"  
    ```  
  
5.  Dans la <xref:System.Windows.Controls.Grid> élément Ajouter le code XAML suivant.  
  
     Le <xref:System.Windows.Forms.MaskedTextBox> contrôle est créé en tant qu’enfant de le <xref:System.Windows.Forms.Integration.WindowsFormsHost> contrôle.  
  
     [!code-xaml[HostingWfInWpfWithXaml#3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HostingWfInWpfWithXaml/CSharp/HostingWfInWpf/Window1.xaml#3)]  
  
6.  Appuyez sur F5 pour générer et exécuter l'application.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.Integration.ElementHost>  
 <xref:System.Windows.Forms.Integration.WindowsFormsHost>  
 [Concepteur WPF](http://msdn.microsoft.com/library/c6c65214-8411-4e16-b254-163ed4099c26)  
 [Procédure pas à pas : hébergement d’un contrôle Windows Forms dans WPF](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-windows-forms-control-in-wpf.md)  
 [Procédure pas à pas : hébergement d'un contrôle composite Windows Forms dans WPF](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-windows-forms-composite-control-in-wpf.md)  
 [Procédure pas à pas : Hébergement d'un contrôle composite WPF dans Windows Forms](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-wpf-composite-control-in-windows-forms.md)  
 [Contrôles Windows Forms et contrôles WPF équivalents](../../../../docs/framework/wpf/advanced/windows-forms-controls-and-equivalent-wpf-controls.md)  
 [Hébergement d’un contrôle Windows Forms dans WPF à l’aide de XAML, exemple](http://go.microsoft.com/fwlink/?LinkID=160000)
