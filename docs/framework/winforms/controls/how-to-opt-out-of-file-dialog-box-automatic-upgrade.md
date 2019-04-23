---
title: 'Procédure : refuser la mise à niveau automatique des boîtes de dialogue Fichier'
ms.date: 03/30/2017
helpviewer_keywords:
- OpenFileDialog [Windows Forms], opt out of automatic upgrade
- file dialog box [Windows Forms], opt out of automatic upgrade
- Windows Vista file dialog box [Windows Forms], opt out of automatic upgrade
- SaveFileDialog [Windows Forms], opt out of automatic upgrade
- AutoUpgradeEnabled property
ms.assetid: 522e482e-cc01-48b1-8d59-9617dc2c4ac1
ms.openlocfilehash: a4be35617e8be1c6c83ac6f2d06e03b6cbb2977f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59769409"
---
# <a name="how-to-opt-out-of-file-dialog-box-automatic-upgrade"></a><span data-ttu-id="fd88e-102">Procédure : refuser la mise à niveau automatique des boîtes de dialogue Fichier</span><span class="sxs-lookup"><span data-stu-id="fd88e-102">How To: Opt Out of File Dialog Box Automatic Upgrade</span></span>
<span data-ttu-id="fd88e-103">Lorsque le <xref:System.Windows.Forms.OpenFileDialog> et <xref:System.Windows.Forms.SaveFileDialog> classes sont utilisées dans une application, leur apparence et leur comportement dépendent de la version de Windows, l’application est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="fd88e-103">When the <xref:System.Windows.Forms.OpenFileDialog> and <xref:System.Windows.Forms.SaveFileDialog> classes are used in an application, their appearance and behavior depend on the version of Windows the application is running on.</span></span> <span data-ttu-id="fd88e-104">Lorsqu’une application qui a été créée sur le [!INCLUDE[dnprdnext](../../../../includes/dnprdnext-md.md)] ou antérieur est affichée sur [!INCLUDE[wiprlhext](../../../../includes/wiprlhext-md.md)], <xref:System.Windows.Forms.OpenFileDialog> et <xref:System.Windows.Forms.SaveFileDialog> sont affichées automatiquement avec le [!INCLUDE[wiprlhext](../../../../includes/wiprlhext-md.md)] apparence et le comportement.</span><span class="sxs-lookup"><span data-stu-id="fd88e-104">When an application that was created on the [!INCLUDE[dnprdnext](../../../../includes/dnprdnext-md.md)] or earlier is displayed on [!INCLUDE[wiprlhext](../../../../includes/wiprlhext-md.md)], <xref:System.Windows.Forms.OpenFileDialog> and <xref:System.Windows.Forms.SaveFileDialog> are automatically displayed with the [!INCLUDE[wiprlhext](../../../../includes/wiprlhext-md.md)] appearance and behavior.</span></span> <span data-ttu-id="fd88e-105">À compter de la [!INCLUDE[net_v30_short](../../../../includes/net-v30-short-md.md)], vous pouvez refuser la mise à niveau automatique pour afficher le <xref:System.Windows.Forms.OpenFileDialog> et <xref:System.Windows.Forms.SaveFileDialog> avec un [!INCLUDE[winxp](../../../../includes/winxp-md.md)]-apparence et le comportement.</span><span class="sxs-lookup"><span data-stu-id="fd88e-105">Starting in the [!INCLUDE[net_v30_short](../../../../includes/net-v30-short-md.md)], you can opt out of the automatic upgrade to display the <xref:System.Windows.Forms.OpenFileDialog> and <xref:System.Windows.Forms.SaveFileDialog> with a [!INCLUDE[winxp](../../../../includes/winxp-md.md)]-style appearance and behavior.</span></span>  
  
### <a name="to-opt-out-of-file-dialog-box-automatic-upgrade"></a><span data-ttu-id="fd88e-106">Pour refuser la mise à niveau automatique de la boîte de dialogue Fichier</span><span class="sxs-lookup"><span data-stu-id="fd88e-106">To opt out of file dialog box automatic upgrade</span></span>  
  
1. <span data-ttu-id="fd88e-107">Définir le <xref:System.Windows.Forms.FileDialog.AutoUpgradeEnabled%2A> propriété du <xref:System.Windows.Forms.OpenFileDialog> ou <xref:System.Windows.Forms.SaveFileDialog> à `false` avant d’afficher la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="fd88e-107">Set the <xref:System.Windows.Forms.FileDialog.AutoUpgradeEnabled%2A> property of <xref:System.Windows.Forms.OpenFileDialog> or <xref:System.Windows.Forms.SaveFileDialog> to `false` before you display the dialog box.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fd88e-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd88e-108">See also</span></span>

- <xref:System.Windows.Forms.FileDialog>
