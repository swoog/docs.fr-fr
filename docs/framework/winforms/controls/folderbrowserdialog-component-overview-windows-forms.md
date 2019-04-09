---
title: Vue d’ensemble du composant FolderBrowserDialog (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- FolderBrowserDialog
helpviewer_keywords:
- FolderBrowserDialog component [Windows Forms], about FolderBrowserDialog
- directories [Windows Forms], enabling browsing in applications
- folders [Windows Forms], enabling browsing in applications
ms.assetid: 796b622c-3ba9-4356-93bb-e217fc52f2c7
ms.openlocfilehash: aae18167b29c71ad692cc6ba447457cd079374b4
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59074129"
---
# <a name="folderbrowserdialog-component-overview-windows-forms"></a><span data-ttu-id="e4102-102">Vue d’ensemble du composant FolderBrowserDialog (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="e4102-102">FolderBrowserDialog Component Overview (Windows Forms)</span></span>
<span data-ttu-id="e4102-103">Les formulaires Windows <xref:System.Windows.Forms.FolderBrowserDialog> composant est une boîte de dialogue modale qui est utilisée pour parcourir et sélectionner des dossiers.</span><span class="sxs-lookup"><span data-stu-id="e4102-103">The Windows Forms <xref:System.Windows.Forms.FolderBrowserDialog> component is a modal dialog box that is used for browsing and selecting folders.</span></span> <span data-ttu-id="e4102-104">Nouveaux dossiers peuvent également être créés depuis le <xref:System.Windows.Forms.FolderBrowserDialog> composant.</span><span class="sxs-lookup"><span data-stu-id="e4102-104">New folders can also be created from within the <xref:System.Windows.Forms.FolderBrowserDialog> component.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e4102-105">Pour sélectionner des fichiers, au lieu de dossiers, utilisez le [OpenFileDialog](openfiledialog-component-windows-forms.md) composant.</span><span class="sxs-lookup"><span data-stu-id="e4102-105">To select files, instead of folders, use the [OpenFileDialog](openfiledialog-component-windows-forms.md) component.</span></span>  
  
 <span data-ttu-id="e4102-106">Le <xref:System.Windows.Forms.FolderBrowserDialog> composant s’affiche au moment de l’exécution à l’aide du <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="e4102-106">The <xref:System.Windows.Forms.FolderBrowserDialog> component is displayed at run time using the <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> method.</span></span> <span data-ttu-id="e4102-107">Définir le <xref:System.Windows.Forms.FolderBrowserDialog.RootFolder%2A> propriété afin de déterminer le dossier supérieur et tous les sous-dossiers qui seront affichent dans l’arborescence de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e4102-107">Set the <xref:System.Windows.Forms.FolderBrowserDialog.RootFolder%2A> property to determine the top-most folder and any subfolders that will appear within the tree view of the dialog box.</span></span> <span data-ttu-id="e4102-108">Une fois que la boîte de dialogue a été affichée, vous pouvez utiliser le <xref:System.Windows.Forms.FolderBrowserDialog.SelectedPath%2A> propriété à obtenir le chemin d’accès du dossier qui a été sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e4102-108">Once the dialog box has been shown, you can use the <xref:System.Windows.Forms.FolderBrowserDialog.SelectedPath%2A> property to get the path of the folder that was selected.</span></span>  
  
 <span data-ttu-id="e4102-109">Lorsqu’il est ajouté à un formulaire, le <xref:System.Windows.Forms.FolderBrowserDialog> composant apparaît dans la barre d’état en bas du Concepteur Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="e4102-109">When it is added to a form, the <xref:System.Windows.Forms.FolderBrowserDialog> component appears in the tray at the bottom of the Windows Forms Designer.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e4102-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4102-110">See also</span></span>

- <xref:System.Windows.Forms.FolderBrowserDialog>
- [<span data-ttu-id="e4102-111">Procédure : choisir des dossiers avec le composant FolderBrowserDialog Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e4102-111">How to: Choose Folders with the Windows Forms FolderBrowserDialog Component</span></span>](how-to-choose-folders-with-the-windows-forms-folderbrowserdialog-component.md)
- [<span data-ttu-id="e4102-112">FolderBrowserDialog, composant</span><span class="sxs-lookup"><span data-stu-id="e4102-112">FolderBrowserDialog Component</span></span>](folderbrowserdialog-component-windows-forms.md)
