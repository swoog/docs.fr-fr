---
title: Composant BindingSource
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [Windows Forms], Windows Forms
- Windows Forms, data binding control
- BindingSource component [Windows Forms]
ms.assetid: 3e2faf4c-f5b8-4fa6-9fbc-f59c37ec2fb9
ms.openlocfilehash: 54639edb512a8bc6c5909282d5e4c210439e2a6e
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57717594"
---
# <a name="bindingsource-component"></a>Composant BindingSource
Encapsule une source de données pour la liaison à des contrôles.  
  
 Le composant <xref:System.Windows.Forms.BindingSource> remplit deux fonctions. Tout d'abord, il fournit une couche d'indirection lors de la liaison des contrôles sur un formulaire de données. Vous devez pour cela lier le composant <xref:System.Windows.Forms.BindingSource> à votre source de données, puis lier les contrôles sur votre formulaire au composant <xref:System.Windows.Forms.BindingSource>. Toute interaction supplémentaire avec les données, y compris la navigation, le tri, le filtrage et la mise à jour, est effectuée en appelant le composant <xref:System.Windows.Forms.BindingSource>.  
  
 Ensuite, le composant <xref:System.Windows.Forms.BindingSource> peut agir comme source de données fortement typée. L'ajout d'un type au composant <xref:System.Windows.Forms.BindingSource> avec la méthode <xref:System.Windows.Forms.BindingSource.Add%2A> crée une liste de ce type.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Vue d'ensemble du composant BindingSource](bindingsource-component-overview.md)  
 Présente les concepts généraux du composant <xref:System.Windows.Forms.BindingSource>, qui vous permet de lier une source de données à un contrôle.  
  
 [Guide pratique pour Lier des contrôles Windows Forms à des valeurs de base de données DBNull](how-to-bind-windows-forms-controls-to-dbnull-database-values.md)  
 Montre comment gérer une valeur <xref:System.DBNull> de la source de données à l'aide du composant <xref:System.Windows.Forms.BindingSource>.  
  
 [Guide pratique pour Trier et filtrer des données ADO.NET avec les Windows Forms composant BindingSource](sort-and-filter-ado-net-data-with-wf-bindingsource-component.md)  
 Illustre comment utiliser le composant <xref:System.Windows.Forms.BindingSource> pour appliquer des tris et des filtres aux données affichées.  
  
 [Guide pratique pour Lier à un Service Web à l’aide du BindingSource Windows Forms](how-to-bind-to-a-web-service-using-the-windows-forms-bindingsource.md)  
 Montre comment utiliser le composant <xref:System.Windows.Forms.BindingSource> pour établir une liaison à un service web.  
  
 [Guide pratique pour Gérer les erreurs et Exceptions qui se produisent avec Databinding](how-to-handle-errors-and-exceptions-that-occur-with-databinding.md)  
 Illustre comment utiliser le composant <xref:System.Windows.Forms.BindingSource> pour gérer correctement les erreurs qui se produisent dans une opération de liaison de données.  
  
 [Guide pratique pour Lier un contrôle de formulaires Windows à un Type](how-to-bind-a-windows-forms-control-to-a-type.md)  
 Montre comment utiliser un composant <xref:System.Windows.Forms.BindingSource> pour établir une liaison à un type.  
  
 [Guide pratique pour Lier un contrôle de formulaires Windows à un objet de fabrique](how-to-bind-a-windows-forms-control-to-a-factory-object.md)  
 Montre comment utiliser un composant <xref:System.Windows.Forms.BindingSource> pour établir une liaison à une méthode ou un objet de fabrique.  
  
 [Guide pratique pour Personnaliser l’ajout d’élément avec le BindingSource Windows Forms](how-to-customize-item-addition-with-the-windows-forms-bindingsource.md)  
 Montre comment utiliser un composant <xref:System.Windows.Forms.BindingSource> pour créer des éléments et les ajouter à une source de données.  
  
 [Guide pratique pour Déclencher des Notifications de modification à l’aide de la méthode ResetItem de BindingSource](how-to-raise-change-notifications-using-the-bindingsource-resetitem-method.md)  
 Montre comment utiliser un composant <xref:System.Windows.Forms.BindingSource> pour déclencher des événements de notifications de modifications pour les sources de données qui ne prennent pas en charge les notifications de modifications.  
  
 [Guide pratique pour Générer des Notifications de modification à l’aide d’un BindingSource et l’Interface INotifyPropertyChanged](raise-change-notifications--bindingsource.md)  
 Montre comment utiliser un type qui hérite de <xref:System.ComponentModel.INotifyPropertyChanged> avec un contrôle <xref:System.Windows.Forms.BindingSource>.  
  
 [Guide pratique pour Refléter les mises à jour de Source de données dans un contrôle de formulaire Windows avec le composant BindingSource](reflect-data-source-updates-in-a-wf-control-with-the-bindingsource.md)  
 Montre comment répondre aux modifications qui se produisent dans la source de données à l'aide du composant <xref:System.Windows.Forms.BindingSource>.  
  
 [Guide pratique pour Partager des données liées entre des formulaires à l’aide du composant BindingSource](how-to-share-bound-data-across-forms-using-the-bindingsource-component.md)  
 Montre comment utiliser <xref:System.Windows.Forms.BindingSource> pour lier plusieurs formulaires à la même source de données.  
  
## <a name="reference"></a>Référence  
 <xref:System.Windows.Forms.BindingSource>  
 Fournit la documentation de référence pour le composant <xref:System.Windows.Forms.BindingSource>.  
  
 <xref:System.Windows.Forms.BindingNavigator>  
 Fournit une documentation de référence pour le contrôle <xref:System.Windows.Forms.BindingNavigator>.  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Liaison de données Windows Forms](../windows-forms-data-binding.md)  
 Contient des liens vers des rubriques décrivant l’architecture de liaison de données Windows Forms.  
  
 Consultez également [Liaison de contrôles à des données dans Visual Studio](/visualstudio/data-tools/bind-controls-to-data-in-visual-studio).
