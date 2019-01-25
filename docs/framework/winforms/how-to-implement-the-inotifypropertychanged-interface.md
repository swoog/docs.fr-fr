---
title: 'Procédure : Implémenter l’Interface INotifyPropertyChanged'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- INotifyPropertyChanged interface [Windows Forms], implementing
ms.assetid: eac428af-b43b-46ac-80d9-1a5f88658725
ms.openlocfilehash: c92406899cffa56a1001f50f89cb53303df5da39
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54560072"
---
# <a name="how-to-implement-the-inotifypropertychanged-interface"></a><span data-ttu-id="caad8-102">Procédure : Implémenter l’Interface INotifyPropertyChanged</span><span class="sxs-lookup"><span data-stu-id="caad8-102">How to: Implement the INotifyPropertyChanged Interface</span></span>
<span data-ttu-id="caad8-103">L’exemple de code suivant montre comment implémenter la <xref:System.ComponentModel.INotifyPropertyChanged> interface.</span><span class="sxs-lookup"><span data-stu-id="caad8-103">The following code example demonstrates how to implement the <xref:System.ComponentModel.INotifyPropertyChanged> interface.</span></span> <span data-ttu-id="caad8-104">Implémentez cette interface sur les objets métier qui sont utilisés dans la liaison de données Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="caad8-104">Implement this interface on business objects that are used in Windows Forms data binding.</span></span> <span data-ttu-id="caad8-105">En cas d’implémentation, l’interface communique à un contrôle dépendant les modifications des propriétés sur un objet métier.</span><span class="sxs-lookup"><span data-stu-id="caad8-105">When implemented, the interface  communicates to a bound control the property changes on a business object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="caad8-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="caad8-106">Example</span></span>  
 [!code-csharp[System.ComponentModel.IPropertyChangeExample#1](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.IPropertyChangeExample/CS/Form1.cs#1)]
 [!code-vb[System.ComponentModel.IPropertyChangeExample#1](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.IPropertyChangeExample/VB/Form1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="caad8-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="caad8-107">See also</span></span>
- [<span data-ttu-id="caad8-108">Guide pratique pour Appliquer le modèle PropertyNameChanged</span><span class="sxs-lookup"><span data-stu-id="caad8-108">How to: Apply the PropertyNameChanged Pattern</span></span>](../../../docs/framework/winforms/how-to-apply-the-propertynamechanged-pattern.md)
- [<span data-ttu-id="caad8-109">Liaison de données Windows Forms</span><span class="sxs-lookup"><span data-stu-id="caad8-109">Windows Forms Data Binding</span></span>](../../../docs/framework/winforms/windows-forms-data-binding.md)
- [<span data-ttu-id="caad8-110">Guide pratique pour Générer des Notifications de modification à l’aide d’un BindingSource et l’Interface INotifyPropertyChanged</span><span class="sxs-lookup"><span data-stu-id="caad8-110">How to: Raise Change Notifications Using a BindingSource and the INotifyPropertyChanged Interface</span></span>](../../../docs/framework/winforms/controls/raise-change-notifications--bindingsource.md)
- [<span data-ttu-id="caad8-111">Notification de modifications dans la liaison de données Windows Forms</span><span class="sxs-lookup"><span data-stu-id="caad8-111">Change Notification in Windows Forms Data Binding</span></span>](../../../docs/framework/winforms/change-notification-in-windows-forms-data-binding.md)
