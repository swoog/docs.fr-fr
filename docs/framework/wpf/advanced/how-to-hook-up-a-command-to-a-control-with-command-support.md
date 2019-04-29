---
title: 'Procédure : Accrocher une commande à un contrôle avec prise en charge de la commande'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Control class [WPF], attaching a RoutedCommand
- classes [WPF], Control [WPF], attaching a RoutedCommand
- RoutedCommand class [WPF], attaching to a Control
- classes [WPF], RoutedCommand [WPF], attaching to a Control
ms.assetid: 8d8592ae-0c91-469e-a1cd-d179c4544548
ms.openlocfilehash: 981fecf33b60c76ecab760185db7dab4bbb254d7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61757246"
---
# <a name="how-to-hook-up-a-command-to-a-control-with-command-support"></a>Procédure : Accrocher une commande à un contrôle avec prise en charge de la commande
L’exemple suivant montre comment raccorder <xref:System.Windows.Input.RoutedCommand> à un <xref:System.Windows.Controls.Control> qui a une prise en charge intégrée de la commande.  Pour obtenir un exemple complet qui raccorde des commandes à plusieurs sources, consultez l’exemple [Créer un exemple RoutedCommand personnalisé](https://github.com/Microsoft/WPF-Samples/tree/master/Input%20and%20Commands/CustomRoutedCommand).  
  
## <a name="example"></a>Exemple  
 [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] fournit une bibliothèque de commandes courantes que les programmeurs d’applications rencontrent régulièrement.  Les classes qui constituent la bibliothèque de commandes sont : <xref:System.Windows.Input.ApplicationCommands>, <xref:System.Windows.Input.ComponentCommands>, <xref:System.Windows.Input.NavigationCommands>, <xref:System.Windows.Input.MediaCommands> et <xref:System.Windows.Documents.EditingCommands>.  
  
 Les objets statiques <xref:System.Windows.Input.RoutedCommand> qui composent ces classes ne fournissent pas de logique de commande.  La logique de la commande est associée à la commande avec <xref:System.Windows.Input.CommandBinding>.  Certains contrôles ont un CommandBindings intégré pour certaines commandes.  Ce mécanisme permet à la sémantique d’une commande de rester la même, tandis que l’implémentation réelle peut changer.  <xref:System.Windows.Controls.TextBox>, par exemple, gère la commande <xref:System.Windows.Input.ApplicationCommands.Paste%2A> différemment d’un contrôle conçu pour prendre en charge les images. Toutefois, le principe de base relatif au collage reste le même.  La logique de commande ne peut pas être fournie par la commande. Elle doit plutôt être fournie par le contrôle ou l’application.  
  
 De nombreux contrôles dans [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] offrent une prise en charge intégrée de certaines commandes de la bibliothèque de commandes.  <xref:System.Windows.Controls.TextBox>, par exemple, prend en charge de nombreuses commandes d’édition de l’application, par exemple <xref:System.Windows.Input.ApplicationCommands.Paste%2A>, <xref:System.Windows.Input.ApplicationCommands.Copy%2A>, <xref:System.Windows.Input.ApplicationCommands.Cut%2A>, <xref:System.Windows.Input.ApplicationCommands.Redo%2A> et <xref:System.Windows.Input.ApplicationCommands.Undo%2A>.  Le développeur d’application n’a aucune action spéciale à effectuer pour que ces commandes fonctionnent avec ces contrôles.  Si <xref:System.Windows.Controls.TextBox> est la cible de commande au moment de l’exécution de la commande, il gère la commande à l’aide de <xref:System.Windows.Input.CommandBinding>, qui est intégré au contrôle.  
  
 L’exemple suivant montre comment utiliser <xref:System.Windows.Controls.MenuItem> en tant que source de commande pour la commande <xref:System.Windows.Input.ApplicationCommands.Paste%2A>, où <xref:System.Windows.Controls.TextBox> est la cible de la commande.  Toute la logique qui définit la façon dont <xref:System.Windows.Controls.TextBox> effectue le collage est intégrée dans le contrôle <xref:System.Windows.Controls.TextBox>.  
  
 <xref:System.Windows.Controls.MenuItem> est créé, et sa propriété <xref:System.Windows.Controls.MenuItem.Command%2A> a la valeur de la commande <xref:System.Windows.Input.ApplicationCommands.Paste%2A>.  <xref:System.Windows.Controls.MenuItem.CommandTarget%2A> n’est pas explicitement défini en fonction de l’objet <xref:System.Windows.Controls.TextBox>.  Quand <xref:System.Windows.Controls.MenuItem.CommandTarget%2A> n’est pas défini, la cible de la commande est l’élément qui a le focus clavier.  Si l’élément qui a le focus clavier ne prend pas en charge la commande <xref:System.Windows.Input.ApplicationCommands.Paste%2A> ou ne peut pas exécuter la commande de collage (le Presse-papiers est vide, par exemple), <xref:System.Windows.Controls.MenuItem> est grisé.  
  
 [!code-xaml[MenuItemCommandTask_XAML#MenuItemCommanding](~/samples/snippets/csharp/VS_Snippets_Wpf/MenuItemCommandTask_XAML/CS/Window1.xaml#menuitemcommanding)]  
  
 [!code-csharp[MenuItemCommandTask#MenuItemCommandingCodeBehind](~/samples/snippets/csharp/VS_Snippets_Wpf/MenuItemCommandTask/CSharp/Window1.xaml.cs#menuitemcommandingcodebehind)]
 [!code-vb[MenuItemCommandTask#MenuItemCommandingCodeBehind](~/samples/snippets/visualbasic/VS_Snippets_Wpf/MenuItemCommandTask/VisualBasic/Window1.xaml.vb#menuitemcommandingcodebehind)]  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble des commandes](commanding-overview.md)
- [Raccorder une commande à un contrôle sans prise en charge de commande](how-to-hook-up-a-command-to-a-control-with-no-command-support.md)
