---
title: 'Procédure : Afficher un contrôle dans la boîte de dialogue de boîte à outils éléments choisir'
ms.date: 03/30/2017
helpviewer_keywords:
- global assembly cache [Windows Forms], Choose Toolbox Items dialog box
- AssemblyFoldersEx [Windows Forms], Choose Toolbox Items dialog box
- controls [Windows Forms], display in Choose Toolbox Items dialog box
- assembly folder registration [Windows Forms], Choose Toolbox Items dialog box
- Choose Toolbox Items dialog box [Windows Forms], display control
ms.assetid: 01ef6eba-d044-40f0-951d-78eff7ebd9a9
ms.openlocfilehash: 56dad16b7a0bd8f0e7423b4a70e7173578150cbe
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54520449"
---
# <a name="how-to-display-a-control-in-the-choose-toolbox-items-dialog-box"></a>Procédure : Afficher un contrôle dans la boîte de dialogue de boîte à outils éléments choisir
Lorsque vous développez et distribuez des contrôles, vous souhaiterez peut-être ces contrôles s’affichent dans le **Choose Toolbox Items** boîte de dialogue qui s’affiche lorsque vous cliquez sur le **boîte à outils** et sélectionnez  **Choisir des éléments**. Vous pouvez activer votre contrôle s’affiche dans cette boîte de dialogue à l’aide de la procédure d’inscription AssemblyFoldersEx.  
  
### <a name="to-display-your-control-in-the-choose-toolbox-items-dialog-box"></a>Pour afficher votre contrôle dans la boîte de dialogue Choisir des éléments de boîte à outils  
  
-   Installer votre assembly de contrôle dans le global assembly cache. Pour plus d'informations, voir [Procédure : Installer un Assembly dans le Global Assembly Cache](../../../../docs/framework/app-domains/how-to-install-an-assembly-into-the-gac.md)  
  
     ou  
  
-   Inscrire votre contrôle et ses assemblys au moment du design associés à l’aide de la procédure d’inscription AssemblyFoldersEx. AssemblyFoldersEx est un emplacement de Registre où les fournisseurs tiers stockent les chemins de chaque version du framework pris en charge. La résolution au moment du design peut rechercher à cet emplacement de Registre pour rechercher des assemblys de référence. Le script de Registre peut spécifier les contrôles que vous souhaitez voir apparaître dans la boîte à outils. Pour plus d’informations, consultez [déploiement d’un contrôle personnalisé et des assemblys au moment du Design (Visual Studio 2013)](https://msdn.microsoft.com/library/96158eb0-b691-4ae1-9e7b-3c65a1b798cb).  
  
## <a name="see-also"></a>Voir aussi
- [Choisir des éléments de boîte à outils, boîte de dialogue (Visual Studio)](https://msdn.microsoft.com/library/bd07835f-18a8-433e-bccc-7141f65263bb)
- [Déploiement d’un contrôle personnalisé et des assemblys au moment du Design (Visual Studio 2013)](https://msdn.microsoft.com/library/96158eb0-b691-4ae1-9e7b-3c65a1b798cb)
- [Développement de contrôles Windows Forms au moment du design](../../../../docs/framework/winforms/controls/developing-windows-forms-controls-at-design-time.md)
- [Guide pratique pour Installer un Assembly dans le Global Assembly Cache](../../../../docs/framework/app-domains/how-to-install-an-assembly-into-the-gac.md)
- [Procédure pas à pas : Remplissage automatique de la boîte à outils avec des composants personnalisés](../../../../docs/framework/winforms/controls/walkthrough-automatically-populating-the-toolbox-with-custom-components.md)
