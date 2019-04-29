---
title: 'Procédure : afficher un contrôle dans la boîte de dialogue Choisir des éléments de boîte à outils'
ms.date: 03/30/2017
helpviewer_keywords:
- global assembly cache [Windows Forms], Choose Toolbox Items dialog box
- AssemblyFoldersEx [Windows Forms], Choose Toolbox Items dialog box
- controls [Windows Forms], display in Choose Toolbox Items dialog box
- assembly folder registration [Windows Forms], Choose Toolbox Items dialog box
- Choose Toolbox Items dialog box [Windows Forms], display control
ms.assetid: 01ef6eba-d044-40f0-951d-78eff7ebd9a9
ms.openlocfilehash: d504ace9e5571246ae0e78e165a7ad2bc23fa481
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61954218"
---
# <a name="how-to-display-a-control-in-the-choose-toolbox-items-dialog-box"></a>Procédure : afficher un contrôle dans la boîte de dialogue Choisir des éléments de boîte à outils
Lorsque vous développez et distribuez des contrôles, vous souhaiterez peut-être ces contrôles s’affichent dans le **Choose Toolbox Items** boîte de dialogue qui s’affiche lorsque vous cliquez sur le **boîte à outils** et sélectionnez  **Choisir des éléments**. Vous pouvez activer votre contrôle s’affiche dans cette boîte de dialogue à l’aide de la procédure d’inscription AssemblyFoldersEx.  
  
### <a name="to-display-your-control-in-the-choose-toolbox-items-dialog-box"></a>Pour afficher votre contrôle dans la boîte de dialogue Choisir des éléments de boîte à outils  
  
- Installer votre assembly de contrôle dans le global assembly cache. Pour plus d'informations, voir [Procédure : installer un assembly dans le Global Assembly Cache](../../app-domains/how-to-install-an-assembly-into-the-gac.md)  
  
     - ou -  
  
- Inscrire votre contrôle et ses assemblys au moment du design associés à l’aide de la procédure d’inscription AssemblyFoldersEx. AssemblyFoldersEx est un emplacement de Registre où les fournisseurs tiers stockent les chemins de chaque version du framework pris en charge. La résolution au moment du design peut rechercher à cet emplacement de Registre pour rechercher des assemblys de référence. Le script de Registre peut spécifier les contrôles que vous souhaitez voir apparaître dans la boîte à outils. Pour plus d’informations, consultez [déploiement d’un contrôle personnalisé et les assemblys au moment du Design](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ee849818(v=vs.100)).  
  
## <a name="see-also"></a>Voir aussi

- [Choisir des éléments de boîte à outils, boîte de dialogue (Visual Studio)](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/dyca0t6t(v=vs.100))
- [Déploiement d’un contrôle personnalisé et les assemblys au moment du Design](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ee849818(v=vs.100))
- [Développement de contrôles Windows Forms au moment du design](developing-windows-forms-controls-at-design-time.md)
- [Guide pratique pour installer un assembly dans le Global Assembly Cache](../../app-domains/how-to-install-an-assembly-into-the-gac.md)
- [Procédure pas à pas : Remplissage automatique de la boîte à outils avec des composants personnalisés](walkthrough-automatically-populating-the-toolbox-with-custom-components.md)
