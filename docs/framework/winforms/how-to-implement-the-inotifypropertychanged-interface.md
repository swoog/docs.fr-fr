---
title: 'Procédure : Implémenter l’Interface INotifyPropertyChanged'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- INotifyPropertyChanged interface [Windows Forms], implementing
ms.assetid: eac428af-b43b-46ac-80d9-1a5f88658725
ms.openlocfilehash: 51c0b1fa535921b7b33a16f55bdc8b76d6125e72
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57704087"
---
# <a name="how-to-implement-the-inotifypropertychanged-interface"></a><span data-ttu-id="7e9e8-102">Procédure : Implémenter l’Interface INotifyPropertyChanged</span><span class="sxs-lookup"><span data-stu-id="7e9e8-102">How to: Implement the INotifyPropertyChanged Interface</span></span>
<span data-ttu-id="7e9e8-103">L’exemple de code suivant montre comment implémenter la <xref:System.ComponentModel.INotifyPropertyChanged> interface.</span><span class="sxs-lookup"><span data-stu-id="7e9e8-103">The following code example demonstrates how to implement the <xref:System.ComponentModel.INotifyPropertyChanged> interface.</span></span> <span data-ttu-id="7e9e8-104">Implémentez cette interface sur les objets métier qui sont utilisés dans la liaison de données Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="7e9e8-104">Implement this interface on business objects that are used in Windows Forms data binding.</span></span> <span data-ttu-id="7e9e8-105">En cas d’implémentation, l’interface communique à un contrôle dépendant les modifications des propriétés sur un objet métier.</span><span class="sxs-lookup"><span data-stu-id="7e9e8-105">When implemented, the interface  communicates to a bound control the property changes on a business object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7e9e8-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="7e9e8-106">Example</span></span>  
 [!code-csharp[System.ComponentModel.IPropertyChangeExample#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.IPropertyChangeExample/CS/Form1.cs#1)]
 [!code-vb[System.ComponentModel.IPropertyChangeExample#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.IPropertyChangeExample/VB/Form1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="7e9e8-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e9e8-107">See also</span></span>
- [<span data-ttu-id="7e9e8-108">Guide pratique pour Appliquer le modèle PropertyNameChanged</span><span class="sxs-lookup"><span data-stu-id="7e9e8-108">How to: Apply the PropertyNameChanged Pattern</span></span>](how-to-apply-the-propertynamechanged-pattern.md)
- [<span data-ttu-id="7e9e8-109">Liaison de données Windows Forms</span><span class="sxs-lookup"><span data-stu-id="7e9e8-109">Windows Forms Data Binding</span></span>](windows-forms-data-binding.md)
- [<span data-ttu-id="7e9e8-110">Guide pratique pour Générer des Notifications de modification à l’aide d’un BindingSource et l’Interface INotifyPropertyChanged</span><span class="sxs-lookup"><span data-stu-id="7e9e8-110">How to: Raise Change Notifications Using a BindingSource and the INotifyPropertyChanged Interface</span></span>](./controls/raise-change-notifications--bindingsource.md)
- [<span data-ttu-id="7e9e8-111">Notification de modifications dans la liaison de données Windows Forms</span><span class="sxs-lookup"><span data-stu-id="7e9e8-111">Change Notification in Windows Forms Data Binding</span></span>](change-notification-in-windows-forms-data-binding.md)
