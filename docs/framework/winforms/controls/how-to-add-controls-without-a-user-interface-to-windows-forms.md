---
title: 'Procédure : ajouter des contrôles sans interface utilisateur à des Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- NonVisualSelection
helpviewer_keywords:
- invisible controls [Windows Forms]
- Windows Forms controls, adding to form
- controls [Windows Forms], nonvisual
- Windows Forms controls, nonvisual
- nonvisual controls [Windows Forms]
ms.assetid: 52134d9c-cff6-4eed-8e2b-3d5eb3bd494e
ms.openlocfilehash: 0768f811653543b3370310ccc0b59890273baf52
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59330101"
---
# <a name="how-to-add-controls-without-a-user-interface-to-windows-forms"></a>Procédure : ajouter des contrôles sans interface utilisateur à des Windows Forms
Un contrôle non visuel (ou un composant) fournit des fonctionnalités à votre application. Contrairement à d’autres contrôles, composants ne fournissent pas d’une interface utilisateur à l’utilisateur et n’avez donc pas besoin doit être affiché sur l’aire du Concepteur de formulaires Windows. Lorsqu’un composant est ajouté à un formulaire, le Concepteur de formulaires Windows affiche une barre d’état redimensionnable en bas de l’écran où tous les composants sont affichés. Une fois qu’un contrôle a été ajouté à la barre d’état du composant, vous pouvez sélectionner le composant et définissez ses propriétés comme vous le feriez pour tout autre contrôle sur le formulaire.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-add-a-component-to-a-windows-form"></a>Pour ajouter un composant à un formulaire Windows  
  
1. Ouvrez le formulaire. Pour plus d’informations, consultez [Guide pratique pour Afficher des Windows Forms dans le concepteur](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/w5yd62ts(v=vs.100)).  
  
2. Dans le **boîte à outils**, cliquez sur un composant et faites-le glisser vers votre formulaire.  
  
     Votre composant s’affiche dans la barre d’état du composant.  
  
 En outre, les composants peuvent être ajoutés à un formulaire au moment de l’exécution. Il s’agit d’un scénario courant, notamment parce que les composants n’ont pas une expression visual, contrairement aux contrôles qui ont une interface utilisateur. Dans l’exemple ci-dessous, un <xref:System.Windows.Forms.Timer> composant est ajouté au moment de l’exécution. (Notez que Visual Studio contient un nombre de différents minuteurs ; dans ce cas, utiliser des formulaires Windows <xref:System.Windows.Forms.Timer> composant. Pour plus d’informations sur les différents minuteurs dans Visual Studio, consultez [Introduction aux minuteurs serveur](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/tb9yt5e6(v=vs.90)).)  
  
> [!CAUTION]
>  Composants possèdent souvent des propriétés spécifiques au contrôle qui doivent être définies pour le composant de fonctionner efficacement. Dans le cas de la <xref:System.Windows.Forms.Timer> composant ci-dessous, vous définissez le `Interval` propriété. Veillez, lorsque vous ajoutez des composants à votre projet, définissez les propriétés nécessaires pour ce composant.  
  
#### <a name="to-add-a-component-to-a-windows-form-programmatically"></a>Pour ajouter un composant à un formulaire Windows par programmation  
  
1. Créez une instance de la <xref:System.Windows.Forms.Timer> classe dans le code.  
  
2. Définir le `Interval` propriété afin de déterminer la durée séparant les graduations de la minuterie.  
  
3. Configurer toutes les propriétés nécessaires pour votre composant.  
  
     Le code suivant illustre la création d’un <xref:System.Windows.Forms.Timer> avec son `Interval` jeu de propriétés.  
  
    ```vb  
    Public Sub CreateTimer()  
       Dim timerKeepTrack As New System.Windows.Forms.Timer  
       timerKeepTrack.Interval = 1000  
    End Sub  
    ```  
  
    ```csharp  
    public void createTimer()  
    {  
       System.Windows.Forms.Timer timerKeepTrack = new  
           System.Windows.Forms.Timer();  
       timerKeepTrack.Interval = 1000;  
    }  
    ```  
  
    ```cpp  
    public:  
       void createTimer()  
       {  
          System::Windows::Forms::Timer^ timerKeepTrack = gcnew  
             System::Windows::Forms::Timer();  
          timerKeepTrack->Interval = 1000;  
       }  
    ```  
  
    > [!IMPORTANT]
    >  Vous pouvez exposer votre ordinateur local à un risque de sécurité via le réseau en référençant un UserControl malveillant. Il s’agit uniquement d’un problème dans le cas d’une personne malveillante, création d’un contrôle personnalisé causer des dommages, que vous suivi par inadvertance l’ajout à votre projet.  
  
## <a name="see-also"></a>Voir aussi

- [Contrôles Windows Forms](index.md)
- [Guide pratique pour Ajouter des contrôles aux Windows Forms](how-to-add-controls-to-windows-forms.md)
- [Guide pratique pour Ajouter des contrôles ActiveX aux Windows Forms](how-to-add-activex-controls-to-windows-forms.md)
- [Guide pratique pour Copier des contrôles entre des Windows Forms](how-to-copy-controls-between-windows-forms.md)
- [Placement de contrôles dans les Windows Forms](putting-controls-on-windows-forms.md)
- [Création d'étiquettes et de raccourcis pour les contrôles Windows Forms](labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
- [Contrôles à utiliser dans les Windows Forms](controls-to-use-on-windows-forms.md)
- [Classement par fonction des contrôles Windows Forms](windows-forms-controls-by-function.md)
