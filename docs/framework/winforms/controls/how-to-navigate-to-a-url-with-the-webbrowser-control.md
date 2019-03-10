---
title: 'Procédure : Naviguer vers une URL avec le contrôle WebBrowser'
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
ms.openlocfilehash: 8d592aea972a95a582cc35ecb14227edec5860ce
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57707233"
---
# <a name="how-to-navigate-to-a-url-with-the-webbrowser-control"></a><span data-ttu-id="e994f-102">Procédure : Naviguer vers une URL avec le contrôle WebBrowser</span><span class="sxs-lookup"><span data-stu-id="e994f-102">How to: Navigate to a URL with the WebBrowser Control</span></span>
<span data-ttu-id="e994f-103">L’exemple de code suivant montre comment naviguer dans le <xref:System.Windows.Forms.WebBrowser> contrôle à une URL spécifique.</span><span class="sxs-lookup"><span data-stu-id="e994f-103">The following code example demonstrates how to navigate the <xref:System.Windows.Forms.WebBrowser> control to a specific URL.</span></span>  
  
 <span data-ttu-id="e994f-104">Pour déterminer quand le nouveau document est entièrement chargé, gérez le <xref:System.Windows.Forms.WebBrowser.DocumentCompleted> événement.</span><span class="sxs-lookup"><span data-stu-id="e994f-104">To determine when the new document is fully loaded, handle the <xref:System.Windows.Forms.WebBrowser.DocumentCompleted> event.</span></span> <span data-ttu-id="e994f-105">Pour une démonstration de cet événement, consultez [Comment : Impression avec un contrôle WebBrowser](how-to-print-with-a-webbrowser-control.md).</span><span class="sxs-lookup"><span data-stu-id="e994f-105">For a demonstration of this event, see [How to: Print with a WebBrowser Control](how-to-print-with-a-webbrowser-control.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="e994f-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="e994f-106">Example</span></span>  
  
```vb  
Me.webBrowser1.Navigate("http://www.microsoft.com")  
```  
  
```csharp  
this.webBrowser1.Navigate("http://www.microsoft.com");  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="e994f-107">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="e994f-107">Compiling the Code</span></span>  
 <span data-ttu-id="e994f-108">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="e994f-108">This example requires:</span></span>  
  
-   <span data-ttu-id="e994f-109">un contrôle <xref:System.Windows.Forms.WebBrowser> nommé `webBrowser1` ;</span><span class="sxs-lookup"><span data-stu-id="e994f-109">A <xref:System.Windows.Forms.WebBrowser> control named `webBrowser1`.</span></span>  
  
-   <span data-ttu-id="e994f-110">des références aux assemblys `System` et `System.Windows.Forms`.</span><span class="sxs-lookup"><span data-stu-id="e994f-110">References to the `System` and `System.Windows.Forms` assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e994f-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e994f-111">See also</span></span>
- <xref:System.Windows.Forms.WebBrowser>
- <xref:System.Windows.Forms.WebBrowser.DocumentCompleted?displayProperty=nameWithType>
- <xref:System.Windows.Forms.WebBrowser.Navigating?displayProperty=nameWithType>
- <xref:System.Windows.Forms.WebBrowser.Navigated?displayProperty=nameWithType>
- [<span data-ttu-id="e994f-112">WebBrowser, contrôle</span><span class="sxs-lookup"><span data-stu-id="e994f-112">WebBrowser Control</span></span>](webbrowser-control-windows-forms.md)
- [<span data-ttu-id="e994f-113">Guide pratique pour Imprimer avec un contrôle WebBrowser</span><span class="sxs-lookup"><span data-stu-id="e994f-113">How to: Print with a WebBrowser Control</span></span>](how-to-print-with-a-webbrowser-control.md)
