---
title: Vue d'ensemble du contrôle WebBrowser
ms.date: 03/30/2017
f1_keywords:
- WebBrowser
helpviewer_keywords:
- WebBrowser control [Windows Forms], about
- Web pages [Windows Forms], displaying in applications
ms.assetid: 6e3e1cc2-9c48-4136-9659-e99e4e60b7e9
ms.openlocfilehash: c75d0b348a2f3dd678f2bfb235bce2e4e227c4b6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59109433"
---
# <a name="webbrowser-control-overview"></a>Vue d'ensemble du contrôle WebBrowser
Le <xref:System.Windows.Forms.WebBrowser> contrôle fournit un wrapper managé pour le contrôle WebBrowser ActiveX. Le wrapper managé vous permet d’afficher des pages Web dans vos applications clientes Windows Forms. Vous pouvez utiliser la <xref:System.Windows.Forms.WebBrowser> contrôle dupliquer les fonctionnalités d’exploration de Web d’Internet Explorer dans votre application ou vous peut désactiver la fonctionnalité d’Internet Explorer par défaut et utiliser le contrôle comme une visionneuse de documents HTML simple. Vous pouvez également utiliser le contrôle pour ajouter des éléments d’interface utilisateur DHTML à votre formulaire et masquer le fait qu’ils sont hébergés dans le <xref:System.Windows.Forms.WebBrowser> contrôle. Cette approche vous permet de combiner de façon transparente les contrôles Web avec des contrôles Windows Forms dans une application unique.  
  
## <a name="frequently-used-properties-methods-and-events"></a>Propriétés fréquemment utilisées, méthodes et événements  
 Le <xref:System.Windows.Forms.WebBrowser> contrôle possède plusieurs propriétés, méthodes et événements que vous pouvez utiliser pour implémenter des contrôles dans Internet Explorer. Par exemple, vous pouvez utiliser la `Navigate` méthode pour implémenter une barre d’adresses et le `GoBack`, `GoForward`, `Stop`, et `Refresh` méthodes à implémenter des boutons de navigation sur une barre d’outils. Vous pouvez gérer le `Navigated` événement à mettre à jour de la barre d’adresses avec la valeur de la `Url` propriété et la barre de titre avec la valeur de la `DocumentTitle` propriété.  
  
 Si vous souhaitez générer votre propre contenu de page au sein de votre application, vous pouvez définir le `DocumentText` propriété. Si vous êtes familiarisé avec le modèle objet de document HTML (DOM), vous pouvez également manipuler le contenu de la page Web actuelle via la `Document` propriété. Avec cette propriété, vous pouvez stocker et modifier des documents en mémoire au lieu de naviguer parmi des fichiers.  
  
 Le `Document` propriété vous permet également d’appeler des méthodes implémentées dans du code à partir de votre code d’application cliente de script de page Web. Pour accéder à votre code d’application cliente à partir de votre code de script, définissez la `ObjectForScripting` propriété. L’objet que vous spécifiez est accessible par votre code de script en tant que le `window.external` objet.  
  
|Nom|Description|  
|----------|-----------------|  
|<xref:System.Windows.Forms.WebBrowser.Document%2A> propriété|Obtient un objet qui fournit l’accès managé pour le modèle objet de document HTML (DOM) de la page Web actuelle.|  
|<xref:System.Windows.Forms.WebBrowser.DocumentCompleted> événement|Se produit lorsqu’une page Web chargée.|  
|<xref:System.Windows.Forms.WebBrowser.DocumentText%2A> propriété|Obtient ou définit le code HTML contenu de la page Web actuelle.|  
|<xref:System.Windows.Forms.WebBrowser.DocumentTitle%2A> propriété|Obtient le titre de la page Web actuelle.|  
|<xref:System.Windows.Forms.WebBrowser.GoBack%2A> méthode|Navigue vers la page précédente dans l’historique.|  
|<xref:System.Windows.Forms.WebBrowser.GoForward%2A> méthode|Navigue vers la page suivante dans l’historique.|  
|<xref:System.Windows.Forms.WebBrowser.Navigate%2A> méthode|Navigue vers l’URL spécifiée.|  
|<xref:System.Windows.Forms.WebBrowser.Navigating> événement|Se produit avant le début de la navigation, l’activation de l’action doit être annulée.|  
|<xref:System.Windows.Forms.WebBrowser.ObjectForScripting%2A> propriété|Obtient ou définit un objet de code de script de page Web peuvent utiliser pour communiquer avec votre application.|  
|<xref:System.Windows.Forms.WebBrowser.Print%2A> méthode|Imprime la page Web actuelle.|  
|<xref:System.Windows.Forms.WebBrowser.Refresh%2A> méthode|Recharge la page Web actuelle.|  
|<xref:System.Windows.Forms.WebBrowser.Stop%2A> méthode|Arrête la navigation en cours et arrête les éléments de page dynamique tels que des sons et des animations.|  
|<xref:System.Windows.Forms.WebBrowser.Url%2A> propriété|Obtient ou définit l’URL de la page Web actuelle. Définition de cette propriété navigue le contrôle vers la nouvelle URL.|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.WebBrowser>
- <xref:System.Windows.Forms.WebBrowserDocumentCompletedEventArgs>
- <xref:System.Windows.Forms.WebBrowserDocumentCompletedEventHandler>
- <xref:System.Windows.Forms.WebBrowserEncryptionLevel>
- <xref:System.Windows.Forms.WebBrowserNavigatedEventArgs>
- <xref:System.Windows.Forms.WebBrowserNavigatedEventHandler>
- <xref:System.Windows.Forms.WebBrowserNavigatingEventArgs>
- <xref:System.Windows.Forms.WebBrowserNavigatingEventHandler>
- <xref:System.Windows.Forms.WebBrowserProgressChangedEventArgs>
- <xref:System.Windows.Forms.WebBrowserReadyState>
- <xref:System.Windows.Forms.WebBrowserRefreshOption>
- [Procédure : accéder à une URL avec le contrôle WebBrowser](how-to-navigate-to-a-url-with-the-webbrowser-control.md)
- [Procédure : imprimer avec un contrôle WebBrowser](how-to-print-with-a-webbrowser-control.md)
- [Procédure : ajouter des fonctionnalités de navigateur web à une application Windows Forms](how-to-add-web-browser-capabilities-to-a-windows-forms-application.md)
- [Procédure : créer une visionneuse de documents HTML dans une application Windows Forms](how-to-create-an-html-document-viewer-in-a-windows-forms-application.md)
- [Procédure : implémenter une communication bidirectionnelle entre le code DHTML et le code de l’application cliente](implement-two-way-com-between-dhtml-and-client.md)
- [Sécurité WebBrowser](webbrowser-security.md)
