---
title: 'Comment : naviguer vers une URL avec un contrôle WebBrowser'
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
ms.openlocfilehash: f34577d45ddfbd2445fd4558c5694facf3f1aa29
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33531883"
---
# <a name="how-to-navigate-to-a-url-with-the-webbrowser-control"></a><span data-ttu-id="f08dd-102">Comment : naviguer vers une URL avec un contrôle WebBrowser</span><span class="sxs-lookup"><span data-stu-id="f08dd-102">How to: Navigate to a URL with the WebBrowser Control</span></span>
<span data-ttu-id="f08dd-103">L’exemple de code suivant montre comment parcourir le <xref:System.Windows.Forms.WebBrowser> contrôle vers une URL spécifique.</span><span class="sxs-lookup"><span data-stu-id="f08dd-103">The following code example demonstrates how to navigate the <xref:System.Windows.Forms.WebBrowser> control to a specific URL.</span></span>  
  
 <span data-ttu-id="f08dd-104">Pour déterminer quand le nouveau document est complètement chargé, gérez le <xref:System.Windows.Forms.WebBrowser.DocumentCompleted> événement.</span><span class="sxs-lookup"><span data-stu-id="f08dd-104">To determine when the new document is fully loaded, handle the <xref:System.Windows.Forms.WebBrowser.DocumentCompleted> event.</span></span> <span data-ttu-id="f08dd-105">Pour une démonstration de cet événement, consultez [Comment : imprimer avec un contrôle WebBrowser](../../../../docs/framework/winforms/controls/how-to-print-with-a-webbrowser-control.md).</span><span class="sxs-lookup"><span data-stu-id="f08dd-105">For a demonstration of this event, see [How to: Print with a WebBrowser Control](../../../../docs/framework/winforms/controls/how-to-print-with-a-webbrowser-control.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="f08dd-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="f08dd-106">Example</span></span>  
  
```vb  
Me.webBrowser1.Navigate("http://www.microsoft.com")  
```  
  
```csharp  
this.webBrowser1.Navigate("http://www.microsoft.com");  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="f08dd-107">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="f08dd-107">Compiling the Code</span></span>  
 <span data-ttu-id="f08dd-108">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="f08dd-108">This example requires:</span></span>  
  
-   <span data-ttu-id="f08dd-109">un contrôle <xref:System.Windows.Forms.WebBrowser> nommé `webBrowser1` ;</span><span class="sxs-lookup"><span data-stu-id="f08dd-109">A <xref:System.Windows.Forms.WebBrowser> control named `webBrowser1`.</span></span>  
  
-   <span data-ttu-id="f08dd-110">des références aux assemblys `System` et `System.Windows.Forms`.</span><span class="sxs-lookup"><span data-stu-id="f08dd-110">References to the `System` and `System.Windows.Forms` assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f08dd-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f08dd-111">See Also</span></span>  
 <xref:System.Windows.Forms.WebBrowser>  
 <xref:System.Windows.Forms.WebBrowser.DocumentCompleted?displayProperty=nameWithType>  
 <xref:System.Windows.Forms.WebBrowser.Navigating?displayProperty=nameWithType>  
 <xref:System.Windows.Forms.WebBrowser.Navigated?displayProperty=nameWithType>  
 [<span data-ttu-id="f08dd-112">WebBrowser, contrôle</span><span class="sxs-lookup"><span data-stu-id="f08dd-112">WebBrowser Control</span></span>](../../../../docs/framework/winforms/controls/webbrowser-control-windows-forms.md)  
 [<span data-ttu-id="f08dd-113">Guide pratique pour imprimer avec un contrôle WebBrowser</span><span class="sxs-lookup"><span data-stu-id="f08dd-113">How to: Print with a WebBrowser Control</span></span>](../../../../docs/framework/winforms/controls/how-to-print-with-a-webbrowser-control.md)
