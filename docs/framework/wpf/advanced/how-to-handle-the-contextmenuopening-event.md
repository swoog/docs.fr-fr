---
title: 'Procédure : Gérer l’événement ContextMenuOpening'
ms.date: 03/30/2017
helpviewer_keywords:
- ContextMenuOpening properties [WPF]
ms.assetid: 789652fb-1951-4217-934a-7843e355adf4
ms.openlocfilehash: 65a1e34d5b078c49bf59c2d9787812940c9a7494
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59340397"
---
# <a name="how-to-handle-the-contextmenuopening-event"></a>Procédure : Gérer l’événement ContextMenuOpening
Le <xref:System.Windows.FrameworkElement.ContextMenuOpening> événement peut être géré dans une application pour ajuster un menu contextuel existant avant son pour afficher ou pour supprimer un menu qui serait affiché en définissant le <xref:System.Windows.RoutedEventArgs.Handled%2A> propriété `true` dans les données d’événement. La justification habituelle d’un paramètre <xref:System.Windows.RoutedEventArgs.Handled%2A> à `true` de l’événement données consiste à remplacer le menu entièrement par un nouveau <xref:System.Windows.Controls.ContextMenu> de l’objet, qui requiert parfois l’annulation de l’opération et le démarrage d’un nouveau ouvert. Si vous écrivez des gestionnaires pour les <xref:System.Windows.FrameworkElement.ContextMenuOpening> événement, vous devez être conscient des problèmes de synchronisation entre un <xref:System.Windows.Controls.ContextMenu> contrôle et le service qui est chargé d’ouvrir et de positionner des menus contextuels pour les contrôles en général. Cette rubrique illustre quelques-unes des techniques de codage pour le menu contextuel de différents scénarios d’ouverture et illustre un cas où le problème de synchronisation entre en jeu.  
  
 Il existe plusieurs scénarios pour gérer la <xref:System.Windows.FrameworkElement.ContextMenuOpening> événement :  
  
-   Ajuster les éléments de menu avant l’affichage.  
  
-   En remplaçant l’intégralité du menu avant l’affichage.  
  
-   Complètement supprimer un menu contextuel existant et ne rien afficher.  
  
## <a name="example"></a>Exemple  
  
## <a name="adjusting-the-menu-items-before-display"></a>Ajuster les éléments de Menu avant l’affichage  
 Ajuster les éléments de menu existant est relativement simple et est probablement le scénario le plus courant. Vous pouvez procéder ainsi afin d’ajouter ou soustraire des options du menu contextuel en réponse à des informations d’état actuel dans votre application ou les informations d’état particulier qui est disponibles en tant que propriété sur l’objet dans lequel le menu contextuel est demandé.  
  
 La technique générale consiste à obtenir la source de l’événement, qui est le contrôle qui a été clic droit sur, et le <xref:System.Windows.FrameworkElement.ContextMenu%2A> propriété à partir de celui-ci. Vous souhaitez généralement vérifier les <xref:System.Windows.Controls.ItemsControl.Items%2A> collection pour afficher les éléments de menu contextuel existent dans le menu, déjà et puis ajoutez ou supprimez approprié nouveau <xref:System.Windows.Controls.MenuItem> éléments vers ou à partir de la collection.  
  
 [!code-csharp[ContextMenuOpeningHandlers#AddItemNoHandle](~/samples/snippets/csharp/VS_Snippets_Wpf/ContextMenuOpeningHandlers/CSharp/Pane1.xaml.cs#additemnohandle)]  
  
## <a name="replacing-the-entire-menu-before-display"></a>En remplaçant l’intégralité du Menu avant l’affichage  
 Un autre scénario est si vous souhaitez remplacer l’intégralité du menu contextuel. Vous pouvez utiliser bien sûr également une variation du code précédent, pour supprimer chaque élément d’un menu contextuel existant et ajouter de nouveaux, en commençant par l’élément zéro. Mais l’approche la plus intuitive pour remplacer tous les éléments dans le menu contextuel consiste à créer un nouveau <xref:System.Windows.Controls.ContextMenu>, remplir avec des éléments, puis définissez le <xref:System.Windows.FrameworkElement.ContextMenu%2A?displayProperty=nameWithType> propriété d’un contrôle pour être la nouvelle <xref:System.Windows.Controls.ContextMenu>.  
  
 Voici le code de gestionnaire simple pour remplacer un <xref:System.Windows.Controls.ContextMenu>. Le code fait référence à un personnalisé `BuildMenu` (méthode), qui est distinct, car elle est appelée par plusieurs des exemples de gestionnaires.  
  
 [!code-csharp[ContextMenuOpeningHandlers#ReplaceNoReopen](~/samples/snippets/csharp/VS_Snippets_Wpf/ContextMenuOpeningHandlers/CSharp/Pane1.xaml.cs#replacenoreopen)]  
  
 [!code-csharp[ContextMenuOpeningHandlers#BuildMenu](~/samples/snippets/csharp/VS_Snippets_Wpf/ContextMenuOpeningHandlers/CSharp/Pane1.xaml.cs#buildmenu)]  
  
 Toutefois, si vous utilisez ce style de gestionnaire pour <xref:System.Windows.FrameworkElement.ContextMenuOpening>, vous pouvez exposer un problème de synchronisation si l’objet dans lequel vous définissez la <xref:System.Windows.Controls.ContextMenu> n’a pas de menu contextuel préexistant. Quand un utilisateur clique sur un contrôle, <xref:System.Windows.FrameworkElement.ContextMenuOpening> est déclenché même si existant <xref:System.Windows.Controls.ContextMenu> est vide ou null. Mais dans ce cas, quel que soit de nouveau <xref:System.Windows.Controls.ContextMenu> vous définissez sur la source élément arrive trop tard pour être affiché. En outre, si l’utilisateur se produit avec le bouton droit une deuxième fois, cette fois, votre nouvelle <xref:System.Windows.Controls.ContextMenu> s’affiche, la valeur est non null, votre gestionnaire remplacer correctement et afficher le menu lorsque le gestionnaire s’exécute une deuxième fois. Cela suggère deux solutions de contournement possibles :  
  
1. Veillez à ce que <xref:System.Windows.FrameworkElement.ContextMenuOpening> gestionnaires s’exécutent toujours sur les contrôles qui ont au moins un espace réservé <xref:System.Windows.Controls.ContextMenu> disponible, auquel vous souhaitez remplacer par le code du gestionnaire. Dans ce cas, vous pouvez toujours utiliser le gestionnaire indiqué dans l’exemple précédent, mais vous souhaiterez généralement affecter un espace réservé <xref:System.Windows.Controls.ContextMenu> dans la balise initiale :  
  
     [!code-xaml[ContextMenuOpeningHandlers#XAMLWithInitCM](~/samples/snippets/csharp/VS_Snippets_Wpf/ContextMenuOpeningHandlers/CSharp/Pane1.xaml#xamlwithinitcm)]  
  
2. Supposons que la première <xref:System.Windows.Controls.ContextMenu> valeur peut être null, selon une logique préliminaire. Vous pouvez vérifier la présence <xref:System.Windows.Controls.ContextMenu> pour valeur null ou utiliser un indicateur dans votre code pour vérifier si votre gestionnaire a été exécuté au moins une fois. Comme vous supposez que le <xref:System.Windows.Controls.ContextMenu> à propos d’être affiché, votre gestionnaire puis définit <xref:System.Windows.RoutedEventArgs.Handled%2A> à `true` dans les données d’événement. Pour le <xref:System.Windows.Controls.ContextMenuService> qui est chargée de l’affichage du menu contextuel, un `true` valeur pour <xref:System.Windows.RoutedEventArgs.Handled%2A> de l’événement données représentent une demande d’annulation de l’affichage du menu contextuel combinaison / contrôle qui a déclenché l’événement.  
  
 Maintenant que vous avez supprimé le menu contextuel potentiellement suspect, l’étape suivante consiste à fournir un nouveau, puis l’afficher. Définition de la nouvelle est fondamentalement identique à celle du gestionnaire précédent : vous générez un nouveau <xref:System.Windows.Controls.ContextMenu> et définir la source de contrôle <xref:System.Windows.FrameworkElement.ContextMenu%2A?displayProperty=nameWithType> propriété avec lui. L’étape supplémentaire est que vous devez maintenant forcer l’affichage du menu contextuel, car vous avez supprimé la première tentative. Pour forcer l’affichage, vous définissez le <xref:System.Windows.Controls.Primitives.Popup.IsOpen%2A?displayProperty=nameWithType> propriété `true` dans le gestionnaire. Soyez prudent lorsque vous effectuez cette opération, car l’ouverture du menu contextuel dans le gestionnaire déclenche le <xref:System.Windows.FrameworkElement.ContextMenuOpening> événement à nouveau. Si vous entrez à nouveau votre gestionnaire, il devient à l’infini récursive. C’est pourquoi vous devez toujours vérifier pour `null` ou utiliser un indicateur si vous ouvrez un menu contextuel à partir d’un <xref:System.Windows.FrameworkElement.ContextMenuOpening> Gestionnaire d’événements.  
  
## <a name="suppressing-any-existing-context-menu-and-displaying-no-context-menu"></a>Suppression d’un Menu contextuel existant et ne rien afficher  
 Le dernier scénario, en écrivant un gestionnaire qui supprime un menu totalement, est rare. Si un contrôle donné n’est pas censé pour afficher un menu contextuel, il existe probablement plus appropriés des moyens qu’en supprimant le menu uniquement quand un utilisateur le demande. Mais si vous souhaitez utiliser le gestionnaire pour supprimer un menu contextuel et ne rien afficher, votre gestionnaire doit simplement définir <xref:System.Windows.RoutedEventArgs.Handled%2A> à `true` dans les données d’événement. Le <xref:System.Windows.Controls.ContextMenuService> qui est chargée pour afficher un menu contextuel vérifie les données d’événement de l’événement, il est déclenché sur le contrôle. Si l’événement a été marqué comme <xref:System.Windows.RoutedEventArgs.Handled%2A> n’importe où sur l’itinéraire, puis l’action menu contextuel ouvert qui a initié l’événement est supprimée.  
  
 [!code-csharp[ContextMenuOpeningHandlers#ReplaceReopen](~/samples/snippets/csharp/VS_Snippets_Wpf/ContextMenuOpeningHandlers/CSharp/Pane1.xaml.cs#replacereopen)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.ContextMenu>
- <xref:System.Windows.FrameworkElement.ContextMenu%2A?displayProperty=nameWithType>
- [Vue d’ensemble des éléments de base](base-elements-overview.md)
- [Vue d’ensemble de ContextMenu](../controls/contextmenu-overview.md)
