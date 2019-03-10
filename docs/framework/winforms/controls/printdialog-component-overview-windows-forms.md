---
title: Vue d'ensemble du composant PrintDialog (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- PrintDialog
helpviewer_keywords:
- Print dialog box [Windows Forms], displaying
- PrintDialog component [Windows Forms], about PrintDialog component
ms.assetid: 8327b8ac-1017-4b5e-a88b-fea9dd56999c
ms.openlocfilehash: dfd6979c596f47fbc9bf68e3866f7fbc9d1dc21c
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57723359"
---
# <a name="printdialog-component-overview-windows-forms"></a><span data-ttu-id="6367e-102">Vue d'ensemble du composant PrintDialog (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="6367e-102">PrintDialog Component Overview (Windows Forms)</span></span>
<span data-ttu-id="6367e-103">Les formulaires Windows [PrintDialog](printdialog-component-windows-forms.md) composant est une boîte de dialogue préconfigurée utilisée pour sélectionner une imprimante, choisir les pages à imprimer et déterminer les autres paramètres d’impression dans les applications Windows.</span><span class="sxs-lookup"><span data-stu-id="6367e-103">The Windows Forms [PrintDialog](printdialog-component-windows-forms.md) component is a pre-configured dialog box used to select a printer, choose the pages to print, and determine other print-related settings in Windows-based applications.</span></span> <span data-ttu-id="6367e-104">Utilisez-le comme un moyen simple de sélectionner une imprimante ou des paramètres d'impression au lieu de configurer votre propre boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="6367e-104">Use it as a simple solution for printer and print-related settings selection in lieu of configuring your own dialog box.</span></span> <span data-ttu-id="6367e-105">Vous pouvez autoriser les utilisateurs à imprimer de nombreuses parties de leurs documents : imprimer tout, imprimer une plage de pages sélectionnées ou imprimer une sélection.</span><span class="sxs-lookup"><span data-stu-id="6367e-105">You can enable users to print many parts of their documents: print all, print a selected page range, or print a selection.</span></span> <span data-ttu-id="6367e-106">En vous appuyant sur des boîtes de dialogue Windows standard, vous pouvez créer des applications dont la fonction de base est immédiatement familière aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="6367e-106">By relying on standard Windows dialog boxes, you create applications whose basic functionality is immediately familiar to users.</span></span> <span data-ttu-id="6367e-107">Le <xref:System.Windows.Forms.PrintDialog> composant hérite de la <xref:System.Windows.Forms.CommonDialog> classe.</span><span class="sxs-lookup"><span data-stu-id="6367e-107">The <xref:System.Windows.Forms.PrintDialog> component inherits from the <xref:System.Windows.Forms.CommonDialog> class.</span></span>  
  
## <a name="working-with-the-component"></a><span data-ttu-id="6367e-108">Utilisation du composant</span><span class="sxs-lookup"><span data-stu-id="6367e-108">Working with the Component</span></span>  
 <span data-ttu-id="6367e-109">Utilisez le <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> méthode pour afficher la boîte de dialogue au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="6367e-109">Use the <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> method to display the dialog box at run time.</span></span> <span data-ttu-id="6367e-110">Ce composant possède des propriétés relatives à un seul travail d’impression (<xref:System.Drawing.Printing.PrintDocument> classe) ou les paramètres d’une imprimante spécifique (<xref:System.Drawing.Printing.PrinterSettings> classe).</span><span class="sxs-lookup"><span data-stu-id="6367e-110">This component has properties that relate to either a single print job (<xref:System.Drawing.Printing.PrintDocument> class) or the settings of an individual printer (<xref:System.Drawing.Printing.PrinterSettings> class).</span></span> <span data-ttu-id="6367e-111">Dans ce cas, peut à son tour, être partagé par plusieurs imprimantes.</span><span class="sxs-lookup"><span data-stu-id="6367e-111">Either of these, in turn, may be shared by multiple printers.</span></span>  
  
 <span data-ttu-id="6367e-112">Lorsqu’il est ajouté à un formulaire, le <xref:System.Windows.Forms.PrintDialog> composant apparaît dans la barre d’état en bas du Concepteur Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="6367e-112">When it is added to a form, the <xref:System.Windows.Forms.PrintDialog> component appears in the tray at the bottom of the Windows Forms Designer.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6367e-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6367e-113">See also</span></span>
- <xref:System.Windows.Forms.PrintDialog>
- [<span data-ttu-id="6367e-114">PrintDialog, composant</span><span class="sxs-lookup"><span data-stu-id="6367e-114">PrintDialog Component</span></span>](printdialog-component-windows-forms.md)
