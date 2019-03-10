---
title: 'Procédure : Ajouter des contrôles ActiveX aux Windows Forms'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms controls, ActiveX controls
- forms [Windows Forms], adding ActiveX controls
- ActiveX controls [Windows Forms], adding
ms.assetid: 54a61e5b-555e-4887-b41e-6244fed271eb
ms.openlocfilehash: 68e25cb2cd7e1f1c63954b20d24f028a49431553
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57707987"
---
# <a name="how-to-add-activex-controls-to-windows-forms"></a>Procédure : Ajouter des contrôles ActiveX aux Windows Forms
Alors que le Concepteur de formulaires Windows est optimisé pour héberger des contrôles Windows Forms, vous pouvez également placer des contrôles ActiveX sur Windows Forms.  
  
> [!CAUTION]
>  Il existe des limitations de performances pour les Windows Forms lorsque des contrôles ActiveX leur sont ajoutés.  
  
 Avant d’ajouter des contrôles ActiveX à votre formulaire, vous devez les ajouter à la boîte à outils. Pour plus d’informations, consultez [des composants COM, boîte de dialogue Personnaliser la boîte à outils](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/cby6tzh5(v=vs.100)).  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier ces paramètres, cliquez sur **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-add-an-activex-control-to-your-windows-form"></a>Pour ajouter un contrôle ActiveX à votre formulaire Windows  
  
-   Double-cliquez sur le contrôle sur la boîte à outils.  
  
     Visual Studio ajoute toutes les références au contrôle dans votre projet. Pour plus d’informations sur les éléments à prendre en compte lors de l’utilisation de contrôles ActiveX sur Windows Forms, consultez [considérations sur l’hébergement d’un contrôle ActiveX sur un formulaire Windows](considerations-when-hosting-an-activex-control-on-a-windows-form.md).  
  
    > [!NOTE]
    >  Windows Forms ActiveX Control Importer (AxImp.exe) crée des arguments d’événement d’un type différent que prévu lors de l’importation de bibliothèques de liens dynamiques ActiveX. Les arguments créés par AxImp.exe sont semblables à ce qui suit : `Invoke(object sender, DWebBrowserEvents2_ProgressChangeEvent e)`, lorsque `Invoke(object sender, DWebBrowserEvents2_ProgressChangeEventArgs e)` est attendu. N’oubliez pas que cette anomalie n’empêche pas le code de fonctionner normalement. Pour plus d’informations, consultez [Windows Forms ActiveX Control Importer (Aximp.exe)](../../tools/aximp-exe-windows-forms-activex-control-importer.md).  
  
## <a name="see-also"></a>Voir aussi
- [Contrôles Windows Forms](index.md)
- [Comparaison des contrôles et des objets programmables dans divers langages et bibliothèques](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/0061wezk(v=vs.100))
- [Guide pratique pour Ajouter des contrôles aux Windows Forms](how-to-add-controls-to-windows-forms.md)
- [Disposition des contrôles dans les Windows Forms](arranging-controls-on-windows-forms.md)
- [Création d'étiquettes et de raccourcis pour les contrôles Windows Forms](labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
- [Contrôles à utiliser dans les Windows Forms](controls-to-use-on-windows-forms.md)
- [Classement par fonction des contrôles Windows Forms](windows-forms-controls-by-function.md)
