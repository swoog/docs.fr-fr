---
title: 'Comment : créer un RoutedCommand'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- RoutedCommand class [WPF], creating
ms.assetid: aaf6979f-69ab-406f-979f-5766daa85fa0
ms.openlocfilehash: 75e6c435516fe2a174cf991bd41f24e1b30a212a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33544106"
---
# <a name="how-to-create-a-routedcommand"></a>Comment : créer un RoutedCommand
Cet exemple montre comment créer un personnalisé <xref:System.Windows.Input.RoutedCommand> et comment implémenter la commande personnalisée en créant un <xref:System.Windows.Input.ExecutedRoutedEventHandler> et un <xref:System.Windows.Input.CanExecuteRoutedEventHandler> et les joindre à un <xref:System.Windows.Input.CommandBinding>.  Pour plus d’informations sur l’exécution des commandes, consultez le [vue d’ensemble de l’exécution des commandes](../../../../docs/framework/wpf/advanced/commanding-overview.md).  
  
## <a name="example"></a>Exemple  
 La première étape de création d’un <xref:System.Windows.Input.RoutedCommand> est la définition de la commande et l’instancier.  
  
 [!code-csharp[CommandingOverviewSnippets#CommandingOverviewCommandDefinition](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml.cs#commandingoverviewcommanddefinition)]
 [!code-vb[CommandingOverviewSnippets#CommandingOverviewCommandDefinition](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/CommandingOverviewSnippets/visualbasic/window1.xaml.vb#commandingoverviewcommanddefinition)]  
  
 Pour utiliser la commande dans une application, les gestionnaires d’événements qui définissent ce que fait la commande doivent être créées.  
  
 [!code-csharp[CommandingOverviewSnippets#CommandingOverviewExecuted](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml.cs#commandingoverviewexecuted)]
 [!code-vb[CommandingOverviewSnippets#CommandingOverviewExecuted](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/CommandingOverviewSnippets/visualbasic/window1.xaml.vb#commandingoverviewexecuted)]  
  
 [!code-csharp[CommandingOverviewSnippets#CommandingOverviewCanExecute](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml.cs#commandingoverviewcanexecute)]
 [!code-vb[CommandingOverviewSnippets#CommandingOverviewCanExecute](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/CommandingOverviewSnippets/visualbasic/window1.xaml.vb#commandingoverviewcanexecute)]  
  
 Ensuite, un <xref:System.Windows.Input.CommandBinding> est créé qui associe la commande avec les gestionnaires d’événements. Le <xref:System.Windows.Input.CommandBinding> est créé sur un objet spécifique.  Cet objet définit l’étendue de la <xref:System.Windows.Input.CommandBinding> dans l’arborescence d’éléments  
  
 [!code-xaml[CommandingOverviewSnippets#CommandingOverviewWindowCommandBindingXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml#commandingoverviewwindowcommandbindingxaml)]  
  
 [!code-csharp[CommandingOverviewSnippets#CommandingOverviewCustomCommandBindingCodeBehind](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml.cs#commandingoverviewcustomcommandbindingcodebehind)]
 [!code-vb[CommandingOverviewSnippets#CommandingOverviewCustomCommandBindingCodeBehind](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/CommandingOverviewSnippets/visualbasic/window1.xaml.vb#commandingoverviewcustomcommandbindingcodebehind)]  
  
 L’étape finale consiste à appeler la commande.  La première consiste à appeler une commande à associer à un <xref:System.Windows.Input.ICommandSource>, comme un <xref:System.Windows.Controls.Button>.  
  
 [!code-xaml[CommandingOverviewSnippets#CommandingOverviewCustomCommandSourceXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml#commandingoverviewcustomcommandsourcexaml)]  
  
 [!code-csharp[CommandingOverviewSnippets#CommandingOverviewCustomCommandSourceCodeBehind](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml.cs#commandingoverviewcustomcommandsourcecodebehind)]
 [!code-vb[CommandingOverviewSnippets#CommandingOverviewCustomCommandSourceCodeBehind](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/CommandingOverviewSnippets/visualbasic/window1.xaml.vb#commandingoverviewcustomcommandsourcecodebehind)]  
  
 Lorsque le bouton est activé, le <xref:System.Windows.Input.RoutedCommand.Execute%2A> méthode personnalisée <xref:System.Windows.Input.RoutedCommand> est appelée.  Le <xref:System.Windows.Input.RoutedCommand> déclenche le <xref:System.Windows.Input.CommandManager.PreviewExecuted> et <xref:System.Windows.Input.CommandManager.Executed> les événements routés.  Ces événements parcourent l’arborescence d’éléments recherchant un <xref:System.Windows.Input.CommandBinding> pour cette commande particulière.  Si un <xref:System.Windows.Input.CommandBinding> est trouvée, le <xref:System.Windows.Input.ExecutedRoutedEventHandler> associés <xref:System.Windows.Input.CommandBinding> est appelée.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Input.RoutedCommand>  
 [Vue d’ensemble des commandes](../../../../docs/framework/wpf/advanced/commanding-overview.md)
