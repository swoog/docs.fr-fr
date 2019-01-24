---
title: 'Procédure : Activer des Styles visuels dans une Application hybride'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- hybrid applications [WPF interoperability]
- visual styles [Windows Forms]
ms.assetid: 95de9b9c-d804-405c-b2d1-49a88c1e0fe1
ms.openlocfilehash: 03ac17816e071299307c03ffebb363fe0ddde9c7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54616184"
---
# <a name="how-to-enable-visual-styles-in-a-hybrid-application"></a><span data-ttu-id="42213-102">Procédure : Activer des Styles visuels dans une Application hybride</span><span class="sxs-lookup"><span data-stu-id="42213-102">How to: Enable Visual Styles in a Hybrid Application</span></span>
<span data-ttu-id="42213-103">Cette rubrique montre comment activer [!INCLUDE[TLA#tla_winxp](../../../../includes/tlasharptla-winxp-md.md)] styles visuels sur un [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle hébergé dans un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]-application basée sur.</span><span class="sxs-lookup"><span data-stu-id="42213-103">This topic shows how to enable [!INCLUDE[TLA#tla_winxp](../../../../includes/tlasharptla-winxp-md.md)] visual styles on a [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] control hosted in a [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]-based application.</span></span>  
  
 <span data-ttu-id="42213-104">Si votre application appelle la <xref:System.Windows.Forms.Application.EnableVisualStyles%2A> (méthode), la plupart de vos [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôles utiliseront automatiquement les styles visuels quand votre application est exécutée sur [!INCLUDE[TLA#tla_winxp](../../../../includes/tlasharptla-winxp-md.md)].</span><span class="sxs-lookup"><span data-stu-id="42213-104">If your application calls the <xref:System.Windows.Forms.Application.EnableVisualStyles%2A> method, most of your [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] controls will automatically use visual styles when your application is run on [!INCLUDE[TLA#tla_winxp](../../../../includes/tlasharptla-winxp-md.md)].</span></span> <span data-ttu-id="42213-105">Pour plus d’informations, consultez [rendu des contrôles avec les Styles visuels](../../../../docs/framework/winforms/controls/rendering-controls-with-visual-styles.md).</span><span class="sxs-lookup"><span data-stu-id="42213-105">For more information, see [Rendering Controls with Visual Styles](../../../../docs/framework/winforms/controls/rendering-controls-with-visual-styles.md).</span></span>  
  
 <span data-ttu-id="42213-106">Pour l’intégralité du code des tâches illustrées dans cette rubrique, consultez [activation des Styles visuels dans une Application hybride, exemple](https://go.microsoft.com/fwlink/?LinkID=159986).</span><span class="sxs-lookup"><span data-stu-id="42213-106">For a complete code listing of the tasks illustrated in this topic, see [Enabling Visual Styles in a Hybrid Application Sample](https://go.microsoft.com/fwlink/?LinkID=159986).</span></span>  
  
## <a name="enabling-windows-forms-visual-styles"></a><span data-ttu-id="42213-107">Activation de styles visuels Windows Forms</span><span class="sxs-lookup"><span data-stu-id="42213-107">Enabling Windows Forms Visual Styles</span></span>  
  
#### <a name="to-enable-windows-forms-visual-styles"></a><span data-ttu-id="42213-108">Pour activer les styles visuels Windows Forms</span><span class="sxs-lookup"><span data-stu-id="42213-108">To enable Windows Forms visual styles</span></span>  
  
1.  <span data-ttu-id="42213-109">Créer un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] projet d’Application nommé `HostingWfWithVisualStyles`.</span><span class="sxs-lookup"><span data-stu-id="42213-109">Create a [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] Application project named `HostingWfWithVisualStyles`.</span></span>  
  
2.  <span data-ttu-id="42213-110">Dans l’Explorateur de solutions, ajoutez des références aux assemblys suivants.</span><span class="sxs-lookup"><span data-stu-id="42213-110">In Solution Explorer, add references to the following assemblies.</span></span>  
  
    -   <span data-ttu-id="42213-111">WindowsFormsIntegration</span><span class="sxs-lookup"><span data-stu-id="42213-111">WindowsFormsIntegration</span></span>  
  
    -   <span data-ttu-id="42213-112">System.Windows.Forms</span><span class="sxs-lookup"><span data-stu-id="42213-112">System.Windows.Forms</span></span>  
  
3.  <span data-ttu-id="42213-113">Dans la boîte à outils, double-cliquez sur le <xref:System.Windows.Controls.Grid> icône pour placer un <xref:System.Windows.Controls.Grid> élément sur l’aire de conception.</span><span class="sxs-lookup"><span data-stu-id="42213-113">In the Toolbox, double-click the <xref:System.Windows.Controls.Grid> icon to place a <xref:System.Windows.Controls.Grid> element on the design surface.</span></span>  
  
4.  <span data-ttu-id="42213-114">Dans la fenêtre Propriétés, définissez les valeurs de la <xref:System.Windows.FrameworkElement.Height%2A> et <xref:System.Windows.FrameworkElement.Width%2A> propriétés à **automatique**.</span><span class="sxs-lookup"><span data-stu-id="42213-114">In the Properties window, set the values of the <xref:System.Windows.FrameworkElement.Height%2A> and <xref:System.Windows.FrameworkElement.Width%2A> properties to **Auto**.</span></span>  
  
5.  <span data-ttu-id="42213-115">Dans le mode Création ou XAML, sélectionnez le <xref:System.Windows.Window>.</span><span class="sxs-lookup"><span data-stu-id="42213-115">In Design view or XAML view, select the <xref:System.Windows.Window>.</span></span>  
  
6.  <span data-ttu-id="42213-116">Dans la fenêtre Propriétés, cliquez sur le **événements** onglet.</span><span class="sxs-lookup"><span data-stu-id="42213-116">In the Properties window, click the **Events** tab.</span></span>  
  
7.  <span data-ttu-id="42213-117">Double-cliquez sur le <xref:System.Windows.FrameworkElement.Loaded> événement.</span><span class="sxs-lookup"><span data-stu-id="42213-117">Double-click the <xref:System.Windows.FrameworkElement.Loaded> event.</span></span>
  
8.  <span data-ttu-id="42213-118">Dans MainWindow.xaml.vb ou MainWindow.xaml.cs, insérez le code suivant pour gérer les <xref:System.Windows.FrameworkElement.Loaded> événement.</span><span class="sxs-lookup"><span data-stu-id="42213-118">In MainWindow.xaml.vb or MainWindow.xaml.cs, insert the following code to handle the <xref:System.Windows.FrameworkElement.Loaded> event.</span></span>  
  
     [!code-csharp[HostingWfWithVisualStyles#11](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HostingWfWithVisualStyles/CSharp/HostingWfWithVisualStyles/Window1.xaml.cs#11)]
     [!code-vb[HostingWfWithVisualStyles#11](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HostingWfWithVisualStyles/VisualBasic/HostingWfWithVisualStyles/Window1.xaml.vb#11)]  
  
9. <span data-ttu-id="42213-119">Appuyez sur F5 pour générer et exécuter l'application.</span><span class="sxs-lookup"><span data-stu-id="42213-119">Press F5 to build and run the application.</span></span>  
  
     <span data-ttu-id="42213-120">Le [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle est peint avec des styles visuels.</span><span class="sxs-lookup"><span data-stu-id="42213-120">The [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] control is painted with visual styles.</span></span>  
  
## <a name="disabling-windows-forms-visual-styles"></a><span data-ttu-id="42213-121">Désactivation de styles visuels Windows Forms</span><span class="sxs-lookup"><span data-stu-id="42213-121">Disabling Windows Forms Visual Styles</span></span>  
 <span data-ttu-id="42213-122">Pour désactiver les styles visuels, supprimez simplement l’appel à la <xref:System.Windows.Forms.Application.EnableVisualStyles%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="42213-122">To disable visual styles, simply remove the call to the <xref:System.Windows.Forms.Application.EnableVisualStyles%2A> method.</span></span>  
  
#### <a name="to-disable-windows-forms-visual-styles"></a><span data-ttu-id="42213-123">Pour désactiver les styles visuels Windows Forms</span><span class="sxs-lookup"><span data-stu-id="42213-123">To disable Windows Forms visual styles</span></span>  
  
1.  <span data-ttu-id="42213-124">Ouvrez MainWindow.xaml.vb ou MainWindow.xaml.cs dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="42213-124">Open MainWindow.xaml.vb or MainWindow.xaml.cs in the Code Editor.</span></span>  
  
2.  <span data-ttu-id="42213-125">Commentez l’appel à la <xref:System.Windows.Forms.Application.EnableVisualStyles%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="42213-125">Comment out the call to the <xref:System.Windows.Forms.Application.EnableVisualStyles%2A> method.</span></span>  
  
3.  <span data-ttu-id="42213-126">Appuyez sur F5 pour générer et exécuter l'application.</span><span class="sxs-lookup"><span data-stu-id="42213-126">Press F5 to build and run the application.</span></span>  
  
     <span data-ttu-id="42213-127">Le [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle est peint avec le style par défaut du système.</span><span class="sxs-lookup"><span data-stu-id="42213-127">The [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] control is painted with the default system style.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="42213-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42213-128">See also</span></span>
- <xref:System.Windows.Forms.Application.EnableVisualStyles%2A>
- <xref:System.Windows.Forms.VisualStyles>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [<span data-ttu-id="42213-129">Rendu des contrôles avec les styles visuels</span><span class="sxs-lookup"><span data-stu-id="42213-129">Rendering Controls with Visual Styles</span></span>](../../../../docs/framework/winforms/controls/rendering-controls-with-visual-styles.md)
- [<span data-ttu-id="42213-130">Procédure pas à pas : Hébergement d’un contrôle de formulaires Windows dans WPF</span><span class="sxs-lookup"><span data-stu-id="42213-130">Walkthrough: Hosting a Windows Forms Control in WPF</span></span>](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-windows-forms-control-in-wpf.md)
