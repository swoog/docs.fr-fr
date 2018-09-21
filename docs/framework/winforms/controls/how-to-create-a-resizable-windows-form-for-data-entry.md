---
title: "Comment : créer un Windows Form redimensionnable pour l'entrée de données"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- TableLayoutPanel control [Windows Forms]
- layout [Windows Forms], resizing
- forms [Windows Forms], creating resizable
- Windows Forms, resizable
ms.assetid: babdf198-404c-485d-a914-ed370c6ecd99
ms.openlocfilehash: a319fba43c6735cd5552dd71d1fb614a6192da97
ms.sourcegitcommit: 2350a091ef6459f0fcfd894301242400374d8558
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/21/2018
ms.locfileid: "46541013"
---
# <a name="how-to-create-a-resizable-windows-form-for-data-entry"></a>Comment : créer un Windows Form redimensionnable pour l'entrée de données
Une bonne disposition répond correctement aux modifications des dimensions de son formulaire parent. Vous pouvez utiliser le contrôle <xref:System.Windows.Forms.TableLayoutPanel> pour organiser la disposition de votre formulaire afin de redimensionner et de positionner vos contrôles de façon cohérente à mesure que les dimensions du formulaire changent. Le contrôle <xref:System.Windows.Forms.TableLayoutPanel> est également utile quand des modifications du contenu de vos contrôles entraîne une modification de la disposition. Vous pouvez effectuer les tâches décrites dans cette procédure dans l'environnement Visual Studio.  Consultez également [Procédure pas à pas : création d’un Windows Form redimensionnable pour l’entrée de données](https://msdn.microsoft.com/library/991eahec\(v=vs.110\)).  
  
## <a name="example"></a>Exemple  
 L'exemple suivant montre comment utiliser un contrôle <xref:System.Windows.Forms.TableLayoutPanel> pour générer une disposition qui répond correctement quand l'utilisateur redimensionne le formulaire. Il illustre également une disposition qui répond correctement à la localisation.  
  
 [!code-cpp[System.Windows.Forms.TableLayoutPanel.DataEntryForm#1](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.DataEntryForm/cpp/basicdataentryform.cpp#1)]
 [!code-csharp[System.Windows.Forms.TableLayoutPanel.DataEntryForm#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.DataEntryForm/CS/basicdataentryform.cs#1)]
 [!code-vb[System.Windows.Forms.TableLayoutPanel.DataEntryForm#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.DataEntryForm/VB/basicdataentryform.vb#1)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   Références aux assemblys System, System.Data, System.Drawing et System.Windows.Forms.  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  Consultez également [Guide pratique pour compiler et exécuter un exemple complet de code Windows Forms à l’aide de Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.FlowLayoutPanel>  
 <xref:System.Windows.Forms.TableLayoutPanel>  
 [Guide pratique pour ancrer et arrimer des contrôles enfants dans un contrôle TableLayoutPanel](../../../../docs/framework/winforms/controls/how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)  
 [Guide pratique pour créer une présentation Windows Forms qui répond bien à la localisation](../../../../docs/framework/winforms/controls/how-to-design-a-windows-forms-layout-that-responds-well-to-localization.md)  
 [Expérience utilisateur Microsoft Windows, Recommandations officielles à destination des développeurs et des concepteurs d’interfaces utilisateur. Redmond, WA: Microsoft Press, 1999. (USBN : 0-7356-0566-1)](https://www.microsoft.com/mspress/southpacific/books/book11588.htm)
