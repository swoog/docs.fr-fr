---
title: 'Procédure : créer une visionneuse de documents HTML dans une application Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WebBrowser control [Windows Forms], creating an HTML document viewer
- document viewers
- Windows Forms, creating document viewers
ms.assetid: 6a6338fe-f7ee-4f5e-9d8f-0465c57e9039
ms.openlocfilehash: 99609e4bf5a352c436986e0773375d1c8e15e790
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61746972"
---
# <a name="how-to-create-an-html-document-viewer-in-a-windows-forms-application"></a>Procédure : créer une visionneuse de documents HTML dans une application Windows Forms
Vous pouvez utiliser la <xref:System.Windows.Forms.WebBrowser> contrôle pour afficher et imprimer des documents HTML sans fournir toutes les fonctionnalités d’un navigateur Internet. Cela est utile lorsque vous souhaitez tirer parti des fonctionnalités de mise en forme du code HTML, mais ne souhaitez pas que vos utilisateurs pour charger des pages Web arbitraires qui peuvent contenir des contrôles Web non approuvés ou un script potentiellement malveillant. Vous souhaiterez peut-être limiter la capacité de la <xref:System.Windows.Forms.WebBrowser> contrôle de cette manière, par exemple, pour l’utiliser comme une visionneuse de courrier électronique HTML ou fournir une aide au format HTML dans votre application.  
  
### <a name="to-create-an-html-document-viewer"></a>Pour créer une visionneuse de document HTML  
  
1. Définir le <xref:System.Windows.Forms.WebBrowser.AllowWebBrowserDrop%2A> propriété `false` pour empêcher le <xref:System.Windows.Forms.WebBrowser> contrôle à partir de l’ouverture des fichiers déposés sur lui.  
  
     [!code-csharp[WebBrowserMisc#20](~/samples/snippets/csharp/VS_Snippets_Winforms/WebBrowserMisc/CS/WebBrowserMisc.cs#20)]
     [!code-vb[WebBrowserMisc#20](~/samples/snippets/visualbasic/VS_Snippets_Winforms/WebBrowserMisc/vb/WebBrowserMisc.vb#20)]  
  
2. Définir le <xref:System.Windows.Forms.WebBrowser.Url%2A> propriété à l’emplacement du fichier initial à afficher.  
  
     [!code-csharp[WebBrowserMisc#21](~/samples/snippets/csharp/VS_Snippets_Winforms/WebBrowserMisc/CS/WebBrowserMisc.cs#21)]
     [!code-vb[WebBrowserMisc#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/WebBrowserMisc/vb/WebBrowserMisc.vb#21)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
- un contrôle <xref:System.Windows.Forms.WebBrowser> nommé `webBrowser1` ;  
  
- des références aux assemblys `System` et `System.Windows.Forms`.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.WebBrowser>
- <xref:System.Windows.Forms.WebBrowser.AllowWebBrowserDrop%2A>
- <xref:System.Windows.Forms.WebBrowser.Url%2A>
- [Vue d’ensemble du contrôle WebBrowser](webbrowser-control-overview.md)
- [Sécurité WebBrowser](webbrowser-security.md)
- [Guide pratique pour Naviguer vers une URL avec le contrôle WebBrowser](how-to-navigate-to-a-url-with-the-webbrowser-control.md)
- [Guide pratique pour Imprimer avec un contrôle WebBrowser](how-to-print-with-a-webbrowser-control.md)
