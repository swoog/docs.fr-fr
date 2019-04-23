---
title: 'Procédure : réattribuer des contrôles existants à un autre parent'
ms.date: 03/30/2017
helpviewer_keywords:
- container controls [Windows Forms], Windows Forms
- layout [Windows Forms], resizing
- layout [Windows Forms], child controls
ms.assetid: 5a5723ff-34e0-4b6f-a57b-be4ebe35cb34
ms.openlocfilehash: 2639322707c1c7e378f6d389a1dec80fd619841c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59328216"
---
# <a name="how-to-reassign-existing-controls-to-a-different-parent"></a>Procédure : réattribuer des contrôles existants à un autre parent
Vous pouvez affecter des contrôles qui existent sur votre formulaire à un nouveau contrôle de conteneur.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-reassign-existing-controls-to-a-different-parent"></a>Pour réaffecter des contrôles existants à un autre parent  
  
1. Faites glisser trois contrôles <xref:System.Windows.Forms.Button> de la **Boîte à outils** vers le formulaire.  
  
     Disposez-les près les uns des autres en les laissant non alignés.  
  
2. Dans la **Boîte à outils**, cliquez sur l’icône de contrôle <xref:System.Windows.Forms.FlowLayoutPanel> .  
  
     Ne faites pas glisser l’icône vers le formulaire.  
  
3. Déplacez le pointeur de la souris près des trois contrôles <xref:System.Windows.Forms.Button> .  
  
     Le pointeur devient une croix à laquelle est attachée l’icône de contrôle <xref:System.Windows.Forms.FlowLayoutPanel> .  
  
4. Cliquez et maintenez le bouton de la souris enfoncé.  
  
5. Faites glisser le pointeur de la souris pour tracer le contour du contrôle <xref:System.Windows.Forms.FlowLayoutPanel> .  
  
6. Tracez le contour des trois contrôles <xref:System.Windows.Forms.Button> .  
  
7. Relâchez le bouton de la souris.  
  
     Les trois contrôles <xref:System.Windows.Forms.Button> sont maintenant insérés dans le contrôle <xref:System.Windows.Forms.FlowLayoutPanel> .  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.FlowLayoutPanel>
- <xref:System.Windows.Forms.TableLayoutPanel>
- [Disposition des contrôles dans les Windows Forms](arranging-controls-on-windows-forms.md)
- [Procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide d’un TableLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)
- [Procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide des lignes d’alignement](walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)
