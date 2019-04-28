---
title: Opérations glisser-déposer et prise en charge du Presse-papiers
ms.date: 03/30/2017
helpviewer_keywords:
- drag and drop [Windows Forms]
- drag and drop [Windows Forms], Windows Forms
- Clipboard [Windows Forms], Windows Forms
ms.assetid: 7cce79b6-5835-46fd-b690-73f12ad368b2
ms.openlocfilehash: 5e7bb75b648163dab7e410a159d55ebbb75f1b0a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61756427"
---
# <a name="drag-and-drop-operations-and-clipboard-support"></a><span data-ttu-id="aa670-102">Opérations glisser-déposer et prise en charge du Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="aa670-102">Drag-and-Drop Operations and Clipboard Support</span></span>
<span data-ttu-id="aa670-103">Vous pouvez activer les opérations de glisser-déplacer dans une application Windows en gérant une série d'événements, notamment <xref:System.Windows.Forms.Control.DragEnter>, <xref:System.Windows.Forms.Control.DragLeave>, et <xref:System.Windows.Forms.Control.DragDrop> .</span><span class="sxs-lookup"><span data-stu-id="aa670-103">You can enable user drag-and-drop operations within a Windows-based application by handling a series of events, most notably the <xref:System.Windows.Forms.Control.DragEnter>, <xref:System.Windows.Forms.Control.DragLeave>, and <xref:System.Windows.Forms.Control.DragDrop> events.</span></span>  
  
 <span data-ttu-id="aa670-104">Vous pouvez aussi implémenter la prise en charge des opérations couper/copier/coller par l'utilisateur et le transfert de données par l'utilisateur dans le Presse-papiers dans vos applications Windows à l'aide de simples appels de méthode.</span><span class="sxs-lookup"><span data-stu-id="aa670-104">You can also implement user cut/copy/paste support and user data transfer to the Clipboard within your Windows-based applications by using simple method calls.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="aa670-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="aa670-105">In This Section</span></span>  
 [<span data-ttu-id="aa670-106">Procédure pas à pas : Exécution d’une opération de glisser-déplacer dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="aa670-106">Walkthrough: Performing a Drag-and-Drop Operation in Windows Forms</span></span>](walkthrough-performing-a-drag-and-drop-operation-in-windows-forms.md)  
 <span data-ttu-id="aa670-107">Explique comment démarrer une opération de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="aa670-107">Explains how to start a drag-and-drop operation.</span></span>  
  
 [<span data-ttu-id="aa670-108">Guide pratique pour Effectuer des opérations de glisser-déplacer entre les Applications</span><span class="sxs-lookup"><span data-stu-id="aa670-108">How to: Perform Drag-and-Drop Operations Between Applications</span></span>](how-to-perform-drag-and-drop-operations-between-applications.md)  
 <span data-ttu-id="aa670-109">Montre comment effectuer des opérations de glisser-déplacer entre des applications.</span><span class="sxs-lookup"><span data-stu-id="aa670-109">Illustrates how to accomplish drag-and-drop operations across applications.</span></span>  
  
 [<span data-ttu-id="aa670-110">Guide pratique pour Ajouter des données dans le Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="aa670-110">How to: Add Data to the Clipboard</span></span>](how-to-add-data-to-the-clipboard.md)  
 <span data-ttu-id="aa670-111">Décrit un moyen d'insérer des informations dans le Presse-papiers par programmation.</span><span class="sxs-lookup"><span data-stu-id="aa670-111">Describes a way to programmatically insert information on the Clipboard.</span></span>  
  
 [<span data-ttu-id="aa670-112">Guide pratique pour Récupérer des données à partir du Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="aa670-112">How to: Retrieve Data from the Clipboard</span></span>](how-to-retrieve-data-from-the-clipboard.md)  
 <span data-ttu-id="aa670-113">Décrit comment accéder aux données stockées dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="aa670-113">Describes how to access the data stored on the Clipboard.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="aa670-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aa670-114">Related Sections</span></span>  
 [<span data-ttu-id="aa670-115">Fonctionnalité de glisser-déposer dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="aa670-115">Drag-and-Drop Functionality in Windows Forms</span></span>](../drag-and-drop-functionality-in-windows-forms.md)  
 <span data-ttu-id="aa670-116">Décrit les méthodes, les événements et les classes utilisés pour implémenter le comportement de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="aa670-116">Describes the methods, events, and classes used to implement drag-and-drop behavior.</span></span>  
  
 <xref:System.Windows.Forms.Control.QueryContinueDrag>  
 <span data-ttu-id="aa670-117">Décrit les complexités de l'événement qui demande l'autorisation de continuer l'opération glisser.</span><span class="sxs-lookup"><span data-stu-id="aa670-117">Describes the intricacies of the event that asks permission to continue the drag operation.</span></span>  
  
 <xref:System.Windows.Forms.Control.DoDragDrop%2A>  
 <span data-ttu-id="aa670-118">Décrit les complexités de la méthode qui est centrale au démarrage d'une opération glisser.</span><span class="sxs-lookup"><span data-stu-id="aa670-118">Describes the intricacies of the method that is central to beginning a drag operation.</span></span>  
  
 <xref:System.Windows.Forms.Clipboard>  
 <span data-ttu-id="aa670-119">Voir également [Guide pratique pour Envoyer des données à l’enfant MDI actif](how-to-send-data-to-the-active-mdi-child.md).</span><span class="sxs-lookup"><span data-stu-id="aa670-119">Also see [How to: Send Data to the Active MDI Child](how-to-send-data-to-the-active-mdi-child.md).</span></span>
