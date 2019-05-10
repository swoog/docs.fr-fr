---
title: 'Procédure : accéder à une URL avec le contrôle WebBrowser'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
f1_keywords:
- WebBrowser.Navigate
helpviewer_keywords:
- WebBrowser control [Windows Forms], examples
- URLs [Windows Forms], navigating to
- WebBrowser control [Windows Forms], navigating to URLs
- examples [Windows Forms], WebBrowser control
ms.assetid: b3ec38cb-f509-4d0b-bd79-9f3611259c62
ms.openlocfilehash: bee16a388d823f74bc9c88bc34b510d2a5907393
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64649224"
---
# <a name="how-to-navigate-to-a-url-with-the-webbrowser-control"></a>Procédure : accéder à une URL avec le contrôle WebBrowser
L’exemple de code suivant montre comment naviguer dans le <xref:System.Windows.Forms.WebBrowser> contrôle à une URL spécifique.  
  
 Pour déterminer quand le nouveau document est entièrement chargé, gérez le <xref:System.Windows.Forms.WebBrowser.DocumentCompleted> événement. Pour une démonstration de cet événement, consultez [Comment : Impression avec un contrôle WebBrowser](how-to-print-with-a-webbrowser-control.md).  
  
## <a name="example"></a>Exemple  
  
```vb  
Me.webBrowser1.Navigate("http://www.microsoft.com")  
```  
  
```csharp  
this.webBrowser1.Navigate("http://www.microsoft.com");  
```  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
- un contrôle <xref:System.Windows.Forms.WebBrowser> nommé `webBrowser1` ;  
  
- des références aux assemblys `System` et `System.Windows.Forms`.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.WebBrowser>
- <xref:System.Windows.Forms.WebBrowser.DocumentCompleted?displayProperty=nameWithType>
- <xref:System.Windows.Forms.WebBrowser.Navigating?displayProperty=nameWithType>
- <xref:System.Windows.Forms.WebBrowser.Navigated?displayProperty=nameWithType>
- [WebBrowser, contrôle](webbrowser-control-windows-forms.md)
- [Guide pratique pour Imprimer avec un contrôle WebBrowser](how-to-print-with-a-webbrowser-control.md)
