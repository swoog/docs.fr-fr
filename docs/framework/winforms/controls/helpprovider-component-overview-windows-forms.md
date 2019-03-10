---
title: Vue d'ensemble du composant HelpProvider (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- HelpProvider
helpviewer_keywords:
- HelpProvider component [Windows Forms], about HelpProvider component
- Help [Windows Forms], adding to Windows applications
- F1 Help [Windows Forms], adding to Windows Forms
- dialog boxes [Windows Forms], context-sensitive Help
- Windows Forms, context-sensitive Help
ms.assetid: 6b10c2cc-c577-4cb5-9669-e37b33416af9
ms.openlocfilehash: f9cf0c165c6c64186eff53676c8b1b06f74361fc
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57708377"
---
# <a name="helpprovider-component-overview-windows-forms"></a>Vue d'ensemble du composant HelpProvider (Windows Forms)
Les formulaires Windows [HelpProvider](helpprovider-component-windows-forms.md) composant est utilisé pour associer un fichier d’aide HTML Help 1.x (fichier .chm généré par HTML Help Workshop ou fichier .htm) à votre application Windows. Vous pouvez fournir une aide de plusieurs façons :  
  
-   Fournir une aide contextuelle pour les contrôles Windows Forms.  
  
-   Fournir une aide contextuelle sur une boîte de dialogue particulier ou de contrôles spécifiques sur une boîte de dialogue.  
  
-   Ouvrez un fichier d’aide à des zones spécifiques, telles que la page principale d’une Table des matières, l’Index ou une fonction de recherche.  
  
## <a name="using-the-help-provider"></a>L’utilisation du fournisseur d’aide  
 Ajout d’un <xref:System.Windows.Forms.HelpProvider> composant à votre formulaire Windows permet aux autres contrôles sur le formulaire pour exposer les propriétés de l’aide de la <xref:System.Windows.Forms.HelpProvider> composant. Cela vous permet de fournir une aide pour les contrôles sur votre formulaire Windows. Vous pouvez associer un fichier d’aide avec le <xref:System.Windows.Forms.HelpProvider> à l’aide du composant le <xref:System.Windows.Forms.HelpProvider.HelpNamespace%2A> propriété. Vous spécifiez le type d’aide fourni en appelant <xref:System.Windows.Forms.HelpProvider.SetHelpNavigator%2A> et en fournissant une valeur comprise entre le <xref:System.Windows.Forms.HelpNavigator> énumération pour le contrôle spécifié. Vous fournissez le mot clé ou une rubrique d’aide en appelant le <xref:System.Windows.Forms.HelpProvider.SetHelpKeyword%2A> (méthode).  
  
 Si vous le souhaitez, pour associer une chaîne d’aide spécifique à un autre contrôle, utilisez le <xref:System.Windows.Forms.HelpProvider.SetHelpString%2A> (méthode). La chaîne que vous associez à un contrôle à l’aide de cette méthode est affichée dans une fenêtre contextuelle lorsque l’utilisateur appuie sur la touche F1 pendant que le contrôle a le focus.  
  
 Si <xref:System.Windows.Forms.HelpProvider.HelpNamespace%2A> n’a pas été défini, vous devez utiliser <xref:System.Windows.Forms.HelpProvider.SetHelpString%2A> pour fournir le texte d’aide. Si vous avez défini les deux <xref:System.Windows.Forms.HelpProvider.HelpNamespace%2A> et la chaîne d’aide, l’aide basée sur <xref:System.Windows.Forms.HelpProvider.HelpNamespace%2A> est prioritaire.  
  
> [!NOTE]
>  Vous pouvez rencontrer des problèmes à l’aide du chemin d’accès relatif lorsque vous spécifiez le chemin d’accès au fichier d’aide dans le <xref:System.Windows.Forms.Help.ShowHelp%2A> méthode ou <xref:System.Windows.Forms.HelpProvider.HelpNamespace%2A> propriété de la <xref:System.Windows.Forms.HelpProvider> contrôle. Par conséquent, veillez à utiliser le chemin d’accès absolu pour spécifier le fichier d’aide.  
  
## <a name="see-also"></a>Voir aussi
- [Systèmes d’aide dans les applications Windows Forms](../advanced/help-systems-in-windows-forms-applications.md)
