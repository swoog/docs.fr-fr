---
title: Vue d'ensemble du composant SaveFileDialog (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- SaveFileDialog
helpviewer_keywords:
- Save File dialog box [Windows Forms], displaying
- SaveFileDialog component [Windows Forms], about SaveFileDialog
ms.assetid: be7a625f-46fd-4d06-9985-b613dcbf9bd2
ms.openlocfilehash: b06c4d510cefdc7558944995594fd209b6121cb1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61904668"
---
# <a name="savefiledialog-component-overview-windows-forms"></a><span data-ttu-id="7dcd7-102">Vue d'ensemble du composant SaveFileDialog (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="7dcd7-102">SaveFileDialog Component Overview (Windows Forms)</span></span>
<span data-ttu-id="7dcd7-103">Le composant Windows Forms <xref:System.Windows.Forms.SaveFileDialog>  est une boîte de dialogue préconfigurée.</span><span class="sxs-lookup"><span data-stu-id="7dcd7-103">The Windows Forms <xref:System.Windows.Forms.SaveFileDialog> component is a pre-configured dialog box.</span></span> <span data-ttu-id="7dcd7-104">Il est identique à la norme **enregistrer le fichier** boîte de dialogue utilisée par Windows.</span><span class="sxs-lookup"><span data-stu-id="7dcd7-104">It is the same as the standard **Save File** dialog box used by Windows.</span></span> <span data-ttu-id="7dcd7-105">Il hérite de la classe <xref:System.Windows.Forms.CommonDialog>.</span><span class="sxs-lookup"><span data-stu-id="7dcd7-105">It inherits from the <xref:System.Windows.Forms.CommonDialog> class.</span></span>  
  
## <a name="working-with-the-savefiledialog-component"></a><span data-ttu-id="7dcd7-106">Utilisation du composant SaveFileDialog</span><span class="sxs-lookup"><span data-stu-id="7dcd7-106">Working with the SaveFileDialog Component</span></span>  
 <span data-ttu-id="7dcd7-107">Utilisez-la comme une solution simple pour permettre aux utilisateurs d’enregistrer des fichiers au lieu de configurer votre propre boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="7dcd7-107">Use it as a simple solution for enabling users to save files instead of configuring your own dialog box.</span></span> <span data-ttu-id="7dcd7-108">En vous appuyant sur les boîtes de dialogue Windows standards, les fonctionnalités de base des applications que vous créez sont immédiatement familière aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7dcd7-108">By relying on standard Windows dialog boxes, the basic functionality of applications you create is immediately familiar to users.</span></span> <span data-ttu-id="7dcd7-109">Cependant, sachez qu’au moment où à l’aide de la <xref:System.Windows.Forms.SaveFileDialog> composant, vous devez écrire votre propre logique d’enregistrement du fichier.</span><span class="sxs-lookup"><span data-stu-id="7dcd7-109">Be aware, however, that when using the <xref:System.Windows.Forms.SaveFileDialog> component, you must write your own file-saving logic.</span></span>  
  
 <span data-ttu-id="7dcd7-110">Vous pouvez utiliser la <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> méthode pour afficher la boîte de dialogue au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="7dcd7-110">You can use the <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> method to display the dialog box at run time.</span></span> <span data-ttu-id="7dcd7-111">Vous pouvez ouvrir un fichier en mode lecture/écriture à l’aide du <xref:System.Windows.Forms.SaveFileDialog.OpenFile%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="7dcd7-111">You can open a file in read/write mode using the <xref:System.Windows.Forms.SaveFileDialog.OpenFile%2A> method.</span></span>  
  
 <span data-ttu-id="7dcd7-112">Lorsqu’il est ajouté à un formulaire, le <xref:System.Windows.Forms.SaveFileDialog> composant apparaît dans la barre d’état en bas du Concepteur Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="7dcd7-112">When it is added to a form, the <xref:System.Windows.Forms.SaveFileDialog> component appears in the tray at the bottom of the Windows Forms Designer.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7dcd7-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7dcd7-113">See also</span></span>

- <xref:System.Windows.Forms.SaveFileDialog>
- [<span data-ttu-id="7dcd7-114">SaveFileDialog, composant</span><span class="sxs-lookup"><span data-stu-id="7dcd7-114">SaveFileDialog Component</span></span>](savefiledialog-component-windows-forms.md)
