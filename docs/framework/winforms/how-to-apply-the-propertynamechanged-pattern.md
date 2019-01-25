---
title: 'Procédure : Appliquer le modèle PropertyNameChanged'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- custom controls [Windows Forms], property changes (using code)
- data binding [Windows Forms], custom controls
- PropertyNameChanged pattern [Windows Forms], applying
ms.assetid: aa47ddf6-5223-40c4-833f-a78992194836
ms.openlocfilehash: 82856405ab3c9581b398f358e5bf9ecf989ce193
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54539764"
---
# <a name="how-to-apply-the-propertynamechanged-pattern"></a><span data-ttu-id="29f62-102">Procédure : Appliquer le modèle PropertyNameChanged</span><span class="sxs-lookup"><span data-stu-id="29f62-102">How to: Apply the PropertyNameChanged Pattern</span></span>
<span data-ttu-id="29f62-103">L’exemple de code suivant montre comment appliquer le *PropertyName*modèle a été modifié pour un contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="29f62-103">The following code example demonstrates how to apply the *PropertyName*Changed pattern to a custom control.</span></span> <span data-ttu-id="29f62-104">Appliquer ce modèle lorsque vous implémentez des contrôles personnalisés qui sont utilisés avec le moteur de liaison de données Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="29f62-104">Apply this pattern when you implement custom controls that are used with the Windows Forms data binding engine.</span></span>  
  
## <a name="example"></a><span data-ttu-id="29f62-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="29f62-105">Example</span></span>  
 [!code-csharp[System.Windows.Forms.ChangeNotification#3](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ChangeNotification/CS/Form1.cs#3)]
 [!code-vb[System.Windows.Forms.ChangeNotification#3](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ChangeNotification/VB/Form1.vb#3)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="29f62-106">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="29f62-106">Compiling the Code</span></span>  
 <span data-ttu-id="29f62-107">Pour compiler l’exemple de code précédent :</span><span class="sxs-lookup"><span data-stu-id="29f62-107">To compile the previous code example:</span></span>  
  
-   <span data-ttu-id="29f62-108">Collez le code dans un fichier de code vide.</span><span class="sxs-lookup"><span data-stu-id="29f62-108">Paste the code into an empty code file.</span></span> <span data-ttu-id="29f62-109">Vous devez utiliser le contrôle personnalisé dans un formulaire Windows qui contient un `Main` (méthode).</span><span class="sxs-lookup"><span data-stu-id="29f62-109">You must use the custom control on a Windows Form that contains a `Main` method.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="29f62-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29f62-110">See also</span></span>
- [<span data-ttu-id="29f62-111">Guide pratique pour Implémenter l’Interface INotifyPropertyChanged</span><span class="sxs-lookup"><span data-stu-id="29f62-111">How to: Implement the INotifyPropertyChanged Interface</span></span>](../../../docs/framework/winforms/how-to-implement-the-inotifypropertychanged-interface.md)
- [<span data-ttu-id="29f62-112">Notification de modifications dans la liaison de données Windows Forms</span><span class="sxs-lookup"><span data-stu-id="29f62-112">Change Notification in Windows Forms Data Binding</span></span>](../../../docs/framework/winforms/change-notification-in-windows-forms-data-binding.md)
- [<span data-ttu-id="29f62-113">Liaison de données Windows Forms</span><span class="sxs-lookup"><span data-stu-id="29f62-113">Windows Forms Data Binding</span></span>](../../../docs/framework/winforms/windows-forms-data-binding.md)
