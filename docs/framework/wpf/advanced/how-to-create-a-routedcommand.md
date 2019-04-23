---
title: 'Procédure : Créer un RoutedCommand'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- RoutedCommand class [WPF], creating
ms.assetid: aaf6979f-69ab-406f-979f-5766daa85fa0
ms.openlocfilehash: d433658a3039c262d2f682eff09df646d978018c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59109042"
---
# <a name="how-to-create-a-routedcommand"></a>Procédure : Créer un RoutedCommand
Cet exemple montre comment créer un personnalisé <xref:System.Windows.Input.RoutedCommand> et comment implémenter la commande personnalisée en créant un <xref:System.Windows.Input.ExecutedRoutedEventHandler> et un <xref:System.Windows.Input.CanExecuteRoutedEventHandler> et leur attachement à un <xref:System.Windows.Input.CommandBinding>.  Pour plus d’informations sur l’exécution de commandes, consultez le [vue d’ensemble des commandes](commanding-overview.md).  
  
## <a name="example"></a>Exemple  
 La première étape de création d’un <xref:System.Windows.Input.RoutedCommand> est la définition de la commande et l’instancier.  
  
 [!code-csharp[CommandingOverviewSnippets#CommandingOverviewCommandDefinition](~/samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml.cs#commandingoverviewcommanddefinition)]
 [!code-vb[CommandingOverviewSnippets#CommandingOverviewCommandDefinition](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CommandingOverviewSnippets/visualbasic/window1.xaml.vb#commandingoverviewcommanddefinition)]  
  
 Pour pouvoir utiliser la commande dans une application, les gestionnaires d’événements qui définissent ce que fait la commande doivent être créés  
  
 [!code-csharp[CommandingOverviewSnippets#CommandingOverviewExecuted](~/samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml.cs#commandingoverviewexecuted)]
 [!code-vb[CommandingOverviewSnippets#CommandingOverviewExecuted](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CommandingOverviewSnippets/visualbasic/window1.xaml.vb#commandingoverviewexecuted)]  
  
 [!code-csharp[CommandingOverviewSnippets#CommandingOverviewCanExecute](~/samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml.cs#commandingoverviewcanexecute)]
 [!code-vb[CommandingOverviewSnippets#CommandingOverviewCanExecute](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CommandingOverviewSnippets/visualbasic/window1.xaml.vb#commandingoverviewcanexecute)]  
  
 Ensuite, un <xref:System.Windows.Input.CommandBinding> est créé qui associe la commande avec les gestionnaires d’événements. Le <xref:System.Windows.Input.CommandBinding> est créé sur un objet spécifique.  Cet objet définit la portée de la <xref:System.Windows.Input.CommandBinding> dans l’arborescence d’éléments  
  
 [!code-xaml[CommandingOverviewSnippets#CommandingOverviewWindowCommandBindingXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml#commandingoverviewwindowcommandbindingxaml)]  
  
 [!code-csharp[CommandingOverviewSnippets#CommandingOverviewCustomCommandBindingCodeBehind](~/samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml.cs#commandingoverviewcustomcommandbindingcodebehind)]
 [!code-vb[CommandingOverviewSnippets#CommandingOverviewCustomCommandBindingCodeBehind](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CommandingOverviewSnippets/visualbasic/window1.xaml.vb#commandingoverviewcustomcommandbindingcodebehind)]  
  
 L’étape finale consiste à appeler la commande.  La première consiste à appeler une commande à associer à un <xref:System.Windows.Input.ICommandSource>, comme un <xref:System.Windows.Controls.Button>.  
  
 [!code-xaml[CommandingOverviewSnippets#CommandingOverviewCustomCommandSourceXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml#commandingoverviewcustomcommandsourcexaml)]  
  
 [!code-csharp[CommandingOverviewSnippets#CommandingOverviewCustomCommandSourceCodeBehind](~/samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml.cs#commandingoverviewcustomcommandsourcecodebehind)]
 [!code-vb[CommandingOverviewSnippets#CommandingOverviewCustomCommandSourceCodeBehind](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CommandingOverviewSnippets/visualbasic/window1.xaml.vb#commandingoverviewcustomcommandsourcecodebehind)]  
  
 Lorsque le bouton est activé, le <xref:System.Windows.Input.RoutedCommand.Execute%2A> méthode sur personnalisé <xref:System.Windows.Input.RoutedCommand> est appelée.  Le <xref:System.Windows.Input.RoutedCommand> déclenche le <xref:System.Windows.Input.CommandManager.PreviewExecuted> et <xref:System.Windows.Input.CommandManager.Executed> événements routés.  Ces événements parcourent l’arborescence d’éléments que vous recherchez un <xref:System.Windows.Input.CommandBinding> pour cette commande particulière.  Si un <xref:System.Windows.Input.CommandBinding> est trouvée, le <xref:System.Windows.Input.ExecutedRoutedEventHandler> associé <xref:System.Windows.Input.CommandBinding> est appelée.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Input.RoutedCommand>
- [Vue d’ensemble des commandes](commanding-overview.md)
