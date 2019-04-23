---
title: 'Procédure : créer des boutons bascule dans des contrôles ToolStrip'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toggle buttons [Windows Forms], creating
- examples [Windows Forms], toolbars
- ToolStrip control [Windows Forms], creating toggle buttons
ms.assetid: d9c197df-4c65-43f2-beee-b68b52b2befc
ms.openlocfilehash: e688e9a220e6c82caa2d107589b5ca9a1e59e72b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59091250"
---
# <a name="how-to-create-toggle-buttons-in-toolstrip-controls"></a>Procédure : créer des boutons bascule dans des contrôles ToolStrip
Quand un utilisateur clique sur un bouton bascule, il apparaît enfoncé et garde cette apparence jusqu'à ce que l’utilisateur clique sur le bouton Nouveau.  
  
### <a name="to-create-a-toggling-toolstripbutton"></a>Pour créer un ToolStripButton  
  
-   Utilisez le code comme dans l’exemple de code suivant. Ce code suppose que votre formulaire contienne un <xref:System.Windows.Forms.ToolStrip> contrôle et que son <xref:System.Windows.Forms.ToolStrip.Items%2A> collection contient un <xref:System.Windows.Forms.ToolStripButton> appelée `toolStripButton1`. Il suppose également que vous disposez d’un gestionnaire d’événements appelé `toolStripButton1_CheckedChanged`.  
  
    ```vb  
    toolStripButton1.CheckOnClick = True  
    toolStripButton1.CheckedChanged AddressOf _  
    EventHandler(toolStripButton1_CheckedChanged);  
    ```  
  
    ```csharp  
    toolStripButton1.CheckOnClick = true;  
    toolStripButton1.CheckedChanged += new _  
    EventHandler(toolStripButton1_CheckedChanged);  
    ```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.ToolStripButton>
- [Vue d’ensemble du contrôle ToolStrip](toolstrip-control-overview-windows-forms.md)
