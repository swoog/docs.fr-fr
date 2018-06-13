---
title: 'Comment : configurer la notification de mises à jour de liaisons'
ms.date: 03/30/2017
helpviewer_keywords:
- notifications [WPF], binding updates
- data binding [WPF], notification of binding updates
- binding [WPF], updates [WPF], notifications of
ms.assetid: 5673073e-dbe1-49da-980a-484a88f9595a
ms.openlocfilehash: 896ce103361590dceecccf8534fd330aabe18086
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33555839"
---
# <a name="how-to-set-up-notification-of-binding-updates"></a>Comment : configurer la notification de mises à jour de liaisons
Cet exemple montre comment configurer l’envoi d’une notification lorsque la propriété de la cible de liaison (cible) ou de la source de liaison (source) d’une liaison a été mise à jour.  
  
## <a name="example"></a>Exemple  
 [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] déclenche un événement de mise à jour des données chaque fois que la source ou la cible de liaison a été mise à jour. En interne, cet événement est utilisé pour informer l’[!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] qu’elle doit se mettre à jour, car les données liées ont changé. Notez que pour ces événements fonctionnent et également pour la liaison unidirectionnelle ou bidirectionnelle fonctionne correctement, vous devez implémenter votre classe de données à l’aide du <xref:System.ComponentModel.INotifyPropertyChanged> interface. Pour plus d’informations, consultez [Implémenter la notification des modifications de propriétés](../../../../docs/framework/wpf/data/how-to-implement-property-change-notification.md).  
  
 Définir le <xref:System.Windows.Data.Binding.NotifyOnTargetUpdated%2A> ou <xref:System.Windows.Data.Binding.NotifyOnSourceUpdated%2A> propriété (ou les deux) à `true` dans la liaison. Le gestionnaire que vous fournissez pour écouter cet événement doit être directement attaché à l’élément sur lequel vous souhaitez être informé des modifications, ou au contexte de données global si vous souhaitez savoir que quelque chose dans le contexte a changé.  
  
 Voici un exemple qui montre comment configurer la notification lorsqu’une propriété cible a été mise à jour.  
  
 [!code-xaml[DirectionalBinding#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DirectionalBinding/CSharp/Page1.xaml#2)]  
  
 Vous pouvez ensuite affecter un gestionnaire basé sur le délégué EventHandler\<T >, *OnTargetUpdated* dans cet exemple, pour gérer l’événement :  
  
 [!code-csharp[DirectionalBinding#3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DirectionalBinding/CSharp/Page1.xaml.cs#3)]  
[!code-csharp[DirectionalBinding#EndEvent](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DirectionalBinding/CSharp/Page1.xaml.cs#endevent)]  
  
 Les paramètres de l’événement peuvent être utilisés pour déterminer les détails de la propriété qui ont changé (par exemple, le type ou l’élément spécifique si le même gestionnaire est attaché à plusieurs éléments), ce qui peut être utile si plusieurs propriétés sont liées sur un seul élément.  
  
## <a name="see-also"></a>Voir aussi  
 [Vue d’ensemble de la liaison de données](../../../../docs/framework/wpf/data/data-binding-overview.md)  
 [Rubriques de guide pratique](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
