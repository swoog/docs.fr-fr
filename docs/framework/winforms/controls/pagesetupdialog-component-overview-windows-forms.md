---
title: Vue d'ensemble du composant PageSetupDialog (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- PageSetupDialog
helpviewer_keywords:
- Page Setup dialog box [Windows Forms], displaying
- PageSetupDialog component
ms.assetid: 791caacb-a5ca-4fca-bad9-1a5721ad697c
ms.openlocfilehash: 989183b6152dfccb6167d89433317cea596d83c5
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211741"
---
# <a name="pagesetupdialog-component-overview-windows-forms"></a><span data-ttu-id="5530e-102">Vue d'ensemble du composant PageSetupDialog (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="5530e-102">PageSetupDialog Component Overview (Windows Forms)</span></span>

<span data-ttu-id="5530e-103">Les formulaires Windows <xref:System.Windows.Forms.PageSetupDialog> composant est une boîte de dialogue préconfigurée utilisée pour définir les détails de la page pour l’impression dans les applications Windows.</span><span class="sxs-lookup"><span data-stu-id="5530e-103">The Windows Forms <xref:System.Windows.Forms.PageSetupDialog> component is a pre-configured dialog box used to set page details for printing in Windows-based applications.</span></span> <span data-ttu-id="5530e-104">Utilisez-le dans votre application Windows comme une solution simple pour les utilisateurs pour définir les préférences de pages au lieu de configurer votre propre boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="5530e-104">Use it within your Windows-based application as a simple solution for users to set page preferences in lieu of configuring your own dialog box.</span></span> <span data-ttu-id="5530e-105">Vous pouvez autoriser les utilisateurs à définir la bordure et des marges, en-têtes et pieds de page et l’orientation portrait ou paysage.</span><span class="sxs-lookup"><span data-stu-id="5530e-105">You can enable users to set border and margin adjustments, headers and footers, and portrait or landscape orientation.</span></span> <span data-ttu-id="5530e-106">En vous appuyant sur des boîtes de dialogue Windows standard, vous pouvez créer des applications dont la fonction de base est immédiatement familière aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="5530e-106">By relying on standard Windows dialog boxes, you create applications whose basic functionality is immediately familiar to users.</span></span>

## <a name="key-properties-and-methods"></a><span data-ttu-id="5530e-107">Méthodes et propriétés de clé</span><span class="sxs-lookup"><span data-stu-id="5530e-107">Key Properties and Methods</span></span>

<span data-ttu-id="5530e-108">Utilisez le <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> méthode pour afficher la boîte de dialogue au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="5530e-108">Use the <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> method to display the dialog at run time.</span></span> <span data-ttu-id="5530e-109">Ce composant a vous pouvez définir les propriétés relatives à une seule page (<xref:System.Drawing.Printing.PrintDocument> classe) ou des documents (<xref:System.Drawing.Printing.PageSettings> classe).</span><span class="sxs-lookup"><span data-stu-id="5530e-109">This component has properties you can set that relate to either a single page (<xref:System.Drawing.Printing.PrintDocument> class) or any document (<xref:System.Drawing.Printing.PageSettings> class).</span></span> <span data-ttu-id="5530e-110">En outre, le <xref:System.Windows.Forms.PageSetupDialog> composant peut être utilisé pour déterminer les paramètres d’imprimante spécifiques, qui sont stockés dans le <xref:System.Drawing.Printing.PrinterSettings> classe.</span><span class="sxs-lookup"><span data-stu-id="5530e-110">Additionally, the <xref:System.Windows.Forms.PageSetupDialog> component can be used to determine specific printer settings, which are stored in the <xref:System.Drawing.Printing.PrinterSettings> class.</span></span>

<span data-ttu-id="5530e-111">Lorsqu’il est ajouté à un formulaire, le <xref:System.Windows.Forms.PageSetupDialog> composant apparaît dans la barre d’état en bas du Concepteur Windows Forms dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5530e-111">When it is added to a form, the <xref:System.Windows.Forms.PageSetupDialog> component appears in the tray at the bottom of the Windows Forms Designer in Visual Studio.</span></span>

## <a name="see-also"></a><span data-ttu-id="5530e-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5530e-112">See also</span></span>

- <xref:System.Windows.Forms.PageSetupDialog>
- [<span data-ttu-id="5530e-113">PageSetupDialog, composant</span><span class="sxs-lookup"><span data-stu-id="5530e-113">PageSetupDialog Component</span></span>](pagesetupdialog-component-windows-forms.md)
