---
title: Opérations glisser-déposer et prise en charge du Presse-papiers
ms.date: 03/30/2017
helpviewer_keywords:
- drag and drop [Windows Forms]
- drag and drop [Windows Forms], Windows Forms
- Clipboard [Windows Forms], Windows Forms
ms.assetid: 7cce79b6-5835-46fd-b690-73f12ad368b2
ms.openlocfilehash: c2bb3c24298ffe5308af03c5af5bae697a22c33b
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43528612"
---
# <a name="drag-and-drop-operations-and-clipboard-support"></a><span data-ttu-id="50c21-102">Opérations glisser-déposer et prise en charge du Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="50c21-102">Drag-and-Drop Operations and Clipboard Support</span></span>
<span data-ttu-id="50c21-103">Vous pouvez activer les opérations de glisser-déplacer dans une application Windows en gérant une série d'événements, notamment <xref:System.Windows.Forms.Control.DragEnter>, <xref:System.Windows.Forms.Control.DragLeave>, et <xref:System.Windows.Forms.Control.DragDrop> .</span><span class="sxs-lookup"><span data-stu-id="50c21-103">You can enable user drag-and-drop operations within a Windows-based application by handling a series of events, most notably the <xref:System.Windows.Forms.Control.DragEnter>, <xref:System.Windows.Forms.Control.DragLeave>, and <xref:System.Windows.Forms.Control.DragDrop> events.</span></span>  
  
 <span data-ttu-id="50c21-104">Vous pouvez aussi implémenter la prise en charge des opérations couper/copier/coller par l'utilisateur et le transfert de données par l'utilisateur dans le Presse-papiers dans vos applications Windows à l'aide de simples appels de méthode.</span><span class="sxs-lookup"><span data-stu-id="50c21-104">You can also implement user cut/copy/paste support and user data transfer to the Clipboard within your Windows-based applications by using simple method calls.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="50c21-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="50c21-105">In This Section</span></span>  
 [<span data-ttu-id="50c21-106">Procédure pas à pas : exécution d’opérations de glisser-déposer dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="50c21-106">Walkthrough: Performing a Drag-and-Drop Operation in Windows Forms</span></span>](../../../../docs/framework/winforms/advanced/walkthrough-performing-a-drag-and-drop-operation-in-windows-forms.md)  
 <span data-ttu-id="50c21-107">Explique comment démarrer une opération de glisser-déposer.</span><span class="sxs-lookup"><span data-stu-id="50c21-107">Explains how to start a drag-and-drop operation.</span></span>  
  
 [<span data-ttu-id="50c21-108">Guide pratique pour exécuter des opérations de glisser-déposer entre des applications</span><span class="sxs-lookup"><span data-stu-id="50c21-108">How to: Perform Drag-and-Drop Operations Between Applications</span></span>](../../../../docs/framework/winforms/advanced/how-to-perform-drag-and-drop-operations-between-applications.md)  
 <span data-ttu-id="50c21-109">Montre comment effectuer des opérations de glisser-déposer entre des applications.</span><span class="sxs-lookup"><span data-stu-id="50c21-109">Illustrates how to accomplish drag-and-drop operations across applications.</span></span>  
  
 [<span data-ttu-id="50c21-110">Guide pratique pour ajouter des données au Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="50c21-110">How to: Add Data to the Clipboard</span></span>](../../../../docs/framework/winforms/advanced/how-to-add-data-to-the-clipboard.md)  
 <span data-ttu-id="50c21-111">Décrit un moyen d'insérer des informations dans le Presse-papiers par programmation.</span><span class="sxs-lookup"><span data-stu-id="50c21-111">Describes a way to programmatically insert information on the Clipboard.</span></span>  
  
 [<span data-ttu-id="50c21-112">Guide pratique pour récupérer des données du Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="50c21-112">How to: Retrieve Data from the Clipboard</span></span>](../../../../docs/framework/winforms/advanced/how-to-retrieve-data-from-the-clipboard.md)  
 <span data-ttu-id="50c21-113">Décrit comment accéder aux données stockées dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="50c21-113">Describes how to access the data stored on the Clipboard.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="50c21-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="50c21-114">Related Sections</span></span>  
 [<span data-ttu-id="50c21-115">Fonctionnalité de glisser-déposer dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="50c21-115">Drag-and-Drop Functionality in Windows Forms</span></span>](../../../../docs/framework/winforms/drag-and-drop-functionality-in-windows-forms.md)  
 <span data-ttu-id="50c21-116">Décrit les méthodes, les événements et les classes utilisés pour implémenter le comportement de glisser-déposer.</span><span class="sxs-lookup"><span data-stu-id="50c21-116">Describes the methods, events, and classes used to implement drag-and-drop behavior.</span></span>  
  
 <xref:System.Windows.Forms.Control.QueryContinueDrag>  
 <span data-ttu-id="50c21-117">Décrit les complexités de l'événement qui demande l'autorisation de continuer l'opération glisser.</span><span class="sxs-lookup"><span data-stu-id="50c21-117">Describes the intricacies of the event that asks permission to continue the drag operation.</span></span>  
  
 <xref:System.Windows.Forms.Control.DoDragDrop%2A>  
 <span data-ttu-id="50c21-118">Décrit les complexités de la méthode qui est centrale au démarrage d'une opération glisser.</span><span class="sxs-lookup"><span data-stu-id="50c21-118">Describes the intricacies of the method that is central to beginning a drag operation.</span></span>  
  
 <xref:System.Windows.Forms.Clipboard>  
 <span data-ttu-id="50c21-119">Consultez également [Comment : envoyer des données à l’enfant MDI actif](https://msdn.microsoft.com/library/y0hkh2c8\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="50c21-119">Also see [How to: Send Data to the Active MDI Child](https://msdn.microsoft.com/library/y0hkh2c8\(v=vs.110\)).</span></span>
