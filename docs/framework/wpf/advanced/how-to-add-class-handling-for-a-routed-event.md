---
title: 'Procédure : Ajouter la gestion de classe d’un événement routé'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- routed events [WPF], class handlers
- task_core_add_class_handling_routed_properties [WPF]
- class handlers [WPF], routed events
ms.assetid: 15b7b06c-9112-4ee5-b30a-65d10c5c5df6
ms.openlocfilehash: 7b897954cbdab461dc0305c6290e67c1af5282c3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59224267"
---
# <a name="how-to-add-class-handling-for-a-routed-event"></a>Procédure : Ajouter la gestion de classe d’un événement routé
Les événements routés peuvent être gérés par les gestionnaires de classe ou gestionnaires d’instance sur n’importe quel nœud donné dans l’itinéraire. Gestionnaires de classe sont effectués en premier et utilisable par les implémentations de classe pour supprimer des événements de gestion d’instances ou d’introduire d’autres comportements spécifiques des événements sur les événements qui sont détenus par les classes de base. Cet exemple illustre deux techniques étroitement liées pour l’implémentation des gestionnaires de classe.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise une classe personnalisée selon la <xref:System.Windows.Controls.Canvas> Panneau de configuration. Le principe fondamental de l’application est que la classe personnalisée introduit des comportements sur ses éléments enfants, y compris l’interception clique sur un bouton de gauche de la souris et leur marquage comme gérés, avant de la classe d’élément enfant ou les gestionnaires d’instance sur ce dernier seront appelés.  
  
 Le <xref:System.Windows.UIElement> classe expose une méthode virtuelle qui permet la gestion de classe sur le <xref:System.Windows.UIElement.PreviewMouseLeftButtonDown> événement, en remplaçant simplement l’événement. Il s’agit de la façon la plus simple pour implémenter la gestion de classe si cette méthode virtuelle est disponible quelque part dans la hiérarchie de votre classe. Le code suivant illustre la <xref:System.Windows.UIElement.OnPreviewMouseLeftButtonDown%2A> mise en œuvre dans le « MyEditContainer » qui est dérivé de <xref:System.Windows.Controls.Canvas>. L’implémentation marque l’événement comme géré dans les arguments, puis ajoute du code pour donner à l’élément source à une modification visible de base.  
  
 [!code-csharp[ClassHandling#OnStarClassHandler](~/samples/snippets/csharp/VS_Snippets_Wpf/ClassHandling/CSharp/SDKSampleLibrary/class1.cs#onstarclasshandler)]
 [!code-vb[ClassHandling#OnStarClassHandler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ClassHandling/visualbasic/sdksamplelibrary/class1.vb#onstarclasshandler)]  
  
 Si aucun élément virtuel n’est disponible sur les classes de base ou pour cette méthode particulière, gestion de classe peut être ajoutée directement à l’aide d’une méthode d’utilitaire de la <xref:System.Windows.EventManager> (classe), <xref:System.Windows.EventManager.RegisterClassHandler%2A>. Cette méthode doit uniquement être appelée au sein de l’initialisation statique des classes qui ajoutent la gestion de classe. Cet exemple ajoute un autre gestionnaire pour <xref:System.Windows.UIElement.PreviewMouseLeftButtonDown> , et dans ce cas la classe inscrite est la classe personnalisée. En revanche, lorsque vous utilisez les méthodes virtuelles, la classe inscrite correspond réellement le <xref:System.Windows.UIElement> classe de base. Dans les cas où les classes de base et les sous-classes inscrivent la gestion de classe, les gestionnaires de sous-classe sont effectués en premier. Le comportement dans une application serait que ce gestionnaire affiche tout d’abord sa boîte de message et puis sont affiché le plus grand changement dans le Gestionnaire de la méthode virtuelle.  
  
 [!code-csharp[ClassHandling#StaticAndRegisterClassHandler](~/samples/snippets/csharp/VS_Snippets_Wpf/ClassHandling/CSharp/SDKSampleLibrary/class1.cs#staticandregisterclasshandler)]
 [!code-vb[ClassHandling#StaticAndRegisterClassHandler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ClassHandling/visualbasic/sdksamplelibrary/class1.vb#staticandregisterclasshandler)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.EventManager>
- [Marquage des événements routés comme étant gérés et gestion de classe](marking-routed-events-as-handled-and-class-handling.md)
- [Gérer un événement routé](how-to-handle-a-routed-event.md)
- [Vue d'ensemble des événements routés](routed-events-overview.md)
