---
title: 'Procédure : fournir de l’aide dans une application Windows'
ms.date: 03/30/2017
helpviewer_keywords:
- Help [Windows Forms], Windows applications
- HTML Help [Windows Forms], Windows Forms
- Windows applications [Windows Forms], providing Help
- HelpProvider component [Windows Forms]
- forms [Windows Forms], providing Help
ms.assetid: 7c4e5cec-2bd2-4f0b-8d75-c2b88929bd61
ms.openlocfilehash: cbecb82acb22915af96fa26f08e441b4f6686c4a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61756544"
---
# <a name="how-to-provide-help-in-a-windows-application"></a>Procédure : fournir de l’aide dans une application Windows
Vous pouvez utiliser de la <xref:System.Windows.Forms.HelpProvider> composant pour attacher des rubriques d’aide d’un fichier d’aide à des contrôles spécifiques sur les Windows Forms. Le fichier d’aide peut être au format HTML, ou HTMLHelp 1.x ou ultérieur.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-provide-help"></a>Pour fournir une aide  
  
1. À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Forms.HelpProvider> à votre formulaire.  
  
     Le composant sera placé dans la barre d’état en bas du Concepteur Windows Forms.  
  
2. Dans le **propriétés** fenêtre, définissez le <xref:System.Windows.Forms.HelpProvider.HelpNamespace%2A> propriété au fichier d’aide .chm, .col ou .htm.  
  
3. Sélectionnez un autre contrôle dans votre formulaire, puis, dans le **propriétés** fenêtre, définissez le <xref:System.Windows.Forms.HelpProvider.SetHelpKeyword%2A> propriété.  
  
     Il s’agit la chaîne passée via le <xref:System.Windows.Forms.HelpProvider> composant à votre fichier d’aide pour appeler la rubrique d’aide appropriée.  
  
4. Dans le **propriétés** fenêtre, définissez la <xref:System.Windows.Forms.HelpProvider.SetHelpNavigator%2A> propriété une valeur de la <xref:System.Windows.Forms.HelpNavigator> énumération.  
  
     Ceci détermine la façon dont la propriété **HelpKeyword** est passée au système d’aide. Le tableau suivant montre les paramètres possibles et leur description.  
  
    |Nom du membre|Description|  
    |-----------------|-----------------|  
    |AssociateIndex|Spécifie que l’index d’une rubrique spécifiée est exécuté dans l’URL spécifiée.|  
    |Find|Spécifie que la page de recherche d’une URL spécifiée est affichée.|  
    |Index|Spécifie que l’index d’une URL spécifiée est affiché.|  
    |KeywordIndex|Spécifie un mot clé à rechercher et l’action à effectuer dans l’URL spécifiée.|  
    |TableOfContents|Spécifie que la table des matières du fichier d’aide HTML 1.0 est affiché.|  
    |Rubrique|Spécifie que la rubrique référencée par l’URL spécifiée est affichée.|  
  
 Au moment de l’exécution, en appuyant sur F1 lorsque le contrôle, pour lequel vous avez défini le **HelpKeyword** et **HelpNavigator** propriétés — a focus ouvre le fichier d’aide associé à ce <xref:System.Windows.Forms.HelpProvider> composant.  
  
 Actuellement, le **HelpNamespace** propriété prend en charge les fichiers d’aide dans les trois formats suivants : HTMLHelp 1.x, HTMLHelp 2.0 et HTML. Vous pouvez ainsi définir la propriété **HelpNamespace** sur une adresse http://, comme une page web. Dans ce cas, elle ouvre le navigateur par défaut à la page web avec la chaîne spécifiée dans la propriété **HelpKeyword** utilisée comme ancre. L’ancre est utilisée pour accéder à une partie spécifique d’une page HTML.  
  
> [!IMPORTANT]
>  Prenez soin de vérifier toutes les informations envoyées par un client avant de les utiliser dans votre application. Des utilisateurs malveillants peuvent tenter d’envoyer ou d’injecter un script exécutable, des instructions SQL ou un autre code. Avant d’afficher une entrée utilisateur, de la stocker dans une base de données ou de l’utiliser, vérifiez qu’elle ne contient pas d’informations potentiellement dangereuses. Une façon habituelle de le vérifier est d’utiliser une expression régulière pour rechercher des mots clés comme « SCRIPT » quand vous recevez une entrée d’un utilisateur.  
  
 Vous pouvez également utiliser le <xref:System.Windows.Forms.HelpProvider> composant pour afficher l’aide contextuelle, même si vous avez configuré pour afficher les fichiers d’aide pour les contrôles sur vos formulaires Windows. Pour plus d'informations, voir [Procédure : Afficher l’aide contextuelle](how-to-display-pop-up-help.md).  
  
## <a name="see-also"></a>Voir aussi

- [Guide pratique pour Afficher l’aide contextuelle](how-to-display-pop-up-help.md)
- [Affichage sous forme d’info-bulles de l’aide relative aux contrôles](control-help-using-tooltips.md)
- [Intégration de l’aide d’utilisateur dans les Windows Forms](integrating-user-help-in-windows-forms.md)
- [Windows Forms](../index.md)
