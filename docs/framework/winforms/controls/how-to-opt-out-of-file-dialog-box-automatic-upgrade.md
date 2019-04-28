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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61913642"
---
# <a name="how-to-opt-out-of-file-dialog-box-automatic-upgrade"></a>Procédure : refuser la mise à niveau automatique des boîtes de dialogue Fichier
Lorsque le <xref:System.Windows.Forms.OpenFileDialog> et <xref:System.Windows.Forms.SaveFileDialog> classes sont utilisées dans une application, leur apparence et leur comportement dépendent de la version de Windows, l’application est en cours d’exécution. Lorsqu’une application qui a été créée sur le [!INCLUDE[dnprdnext](../../../../includes/dnprdnext-md.md)] ou antérieur est affichée sur [!INCLUDE[wiprlhext](../../../../includes/wiprlhext-md.md)], <xref:System.Windows.Forms.OpenFileDialog> et <xref:System.Windows.Forms.SaveFileDialog> sont affichées automatiquement avec le [!INCLUDE[wiprlhext](../../../../includes/wiprlhext-md.md)] apparence et le comportement. À compter de la [!INCLUDE[net_v30_short](../../../../includes/net-v30-short-md.md)], vous pouvez refuser la mise à niveau automatique pour afficher le <xref:System.Windows.Forms.OpenFileDialog> et <xref:System.Windows.Forms.SaveFileDialog> avec un [!INCLUDE[winxp](../../../../includes/winxp-md.md)]-apparence et le comportement.  
  
### <a name="to-opt-out-of-file-dialog-box-automatic-upgrade"></a>Pour refuser la mise à niveau automatique de la boîte de dialogue Fichier  
  
1. Définir le <xref:System.Windows.Forms.FileDialog.AutoUpgradeEnabled%2A> propriété du <xref:System.Windows.Forms.OpenFileDialog> ou <xref:System.Windows.Forms.SaveFileDialog> à `false` avant d’afficher la boîte de dialogue.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.FileDialog>
