---
title: Vue d'ensemble du composant OpenFileDialog (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- OpenFileDialog
helpviewer_keywords:
- OpenFileDialog component [Windows Forms], about OpenFileDialog
- Open File dialog box [Windows Forms], displaying in Windows Forms
ms.assetid: cd717300-46b6-4f82-8207-b218fa7fa407
ms.openlocfilehash: 24327ded50ac927642e2687b40b1f10de9bdf41e
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211707"
---
# <a name="openfiledialog-component-overview-windows-forms"></a><span data-ttu-id="9c642-102">Vue d'ensemble du composant OpenFileDialog (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="9c642-102">OpenFileDialog Component Overview (Windows Forms)</span></span>

<span data-ttu-id="9c642-103">Le composant Windows Forms <xref:System.Windows.Forms.OpenFileDialog>  est une boîte de dialogue préconfigurée.</span><span class="sxs-lookup"><span data-stu-id="9c642-103">The Windows Forms <xref:System.Windows.Forms.OpenFileDialog> component is a pre-configured dialog box.</span></span> <span data-ttu-id="9c642-104">Il est identique à **ouvrir un fichier** boîte de dialogue exposée par le système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="9c642-104">It is the same **Open File** dialog box exposed by the Windows operating system.</span></span> <span data-ttu-id="9c642-105">Il hérite de la classe <xref:System.Windows.Forms.CommonDialog>.</span><span class="sxs-lookup"><span data-stu-id="9c642-105">It inherits from the <xref:System.Windows.Forms.CommonDialog> class.</span></span>

## <a name="use-this-component"></a><span data-ttu-id="9c642-106">Utilisez ce composant</span><span class="sxs-lookup"><span data-stu-id="9c642-106">Use this component</span></span>

<span data-ttu-id="9c642-107">Utiliser ce composant dans votre application Windows comme une solution simple pour la sélection de fichier au lieu de configurer votre propre boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="9c642-107">Use this component within your Windows-based application as a simple solution for file selection in lieu of configuring your own dialog box.</span></span> <span data-ttu-id="9c642-108">En vous appuyant sur des boîtes de dialogue Windows standard, vous pouvez créer des applications dont la fonction de base est immédiatement familière aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9c642-108">By relying on standard Windows dialog boxes, you create applications whose basic functionality is immediately familiar to users.</span></span> <span data-ttu-id="9c642-109">Cependant, sachez qu’au moment où à l’aide de la <xref:System.Windows.Forms.OpenFileDialog> composant, vous devez écrire votre propre logique d’ouverture de fichier.</span><span class="sxs-lookup"><span data-stu-id="9c642-109">Be aware, however, that when using the <xref:System.Windows.Forms.OpenFileDialog> component, you must write your own file-opening logic.</span></span>

<span data-ttu-id="9c642-110">Utilisez le <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> méthode pour afficher la boîte de dialogue au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="9c642-110">Use the <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> method to display the dialog at run time.</span></span> <span data-ttu-id="9c642-111">Vous pouvez autoriser les utilisateurs à sélectionner plusieurs fichiers à ouvrir avec le <xref:System.Windows.Forms.OpenFileDialog.Multiselect%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="9c642-111">You can enable users to multi-select files to be opened with the <xref:System.Windows.Forms.OpenFileDialog.Multiselect%2A> property.</span></span> <span data-ttu-id="9c642-112">En outre, vous pouvez utiliser le <xref:System.Windows.Forms.OpenFileDialog.ShowReadOnly%2A> propriété afin de déterminer si une case à cocher en lecture seule s’affiche dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="9c642-112">Additionally, you can use the <xref:System.Windows.Forms.OpenFileDialog.ShowReadOnly%2A> property to determine if a read-only check box appears in the dialog box.</span></span> <span data-ttu-id="9c642-113">Le <xref:System.Windows.Forms.OpenFileDialog.ReadOnlyChecked%2A> propriété indique si la case à cocher en lecture seule est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="9c642-113">The <xref:System.Windows.Forms.OpenFileDialog.ReadOnlyChecked%2A> property indicates whether the read-only check box is selected.</span></span> <span data-ttu-id="9c642-114">Enfin, le <xref:System.Windows.Forms.FileDialog.Filter%2A> propriété définit la chaîne de filtre du nom de fichier actuel, qui détermine les choix qui s’affichent dans la zone « Fichiers de type » dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="9c642-114">Finally, the <xref:System.Windows.Forms.FileDialog.Filter%2A> property sets the current file name filter string, which determines the choices that appear in the "Files of type" box in the dialog box.</span></span>

<span data-ttu-id="9c642-115">Lorsqu’il est ajouté à un formulaire, le <xref:System.Windows.Forms.OpenFileDialog> composant apparaît dans la barre d’état en bas du Concepteur Windows Forms dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9c642-115">When it is added to a form, the <xref:System.Windows.Forms.OpenFileDialog> component appears in the tray at the bottom of the Windows Forms Designer in Visual Studio.</span></span>

## <a name="see-also"></a><span data-ttu-id="9c642-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c642-116">See also</span></span>

- <xref:System.Windows.Forms.OpenFileDialog>
- [<span data-ttu-id="9c642-117">OpenFileDialog, composant</span><span class="sxs-lookup"><span data-stu-id="9c642-117">OpenFileDialog Component</span></span>](openfiledialog-component-windows-forms.md)
