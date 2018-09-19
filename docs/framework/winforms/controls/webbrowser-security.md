---
title: Sécurité WebBrowser
ms.date: 03/30/2017
helpviewer_keywords:
- WebBrowser control [Windows Forms], security
- security [Windows Forms], WebBrowser control
ms.assetid: 0968846e-48ee-485a-9797-65b5b9a622f8
ms.openlocfilehash: 683c6ad4cbc55a889f4a0c1d20ebe8e8a2669a13
ms.sourcegitcommit: f513a91160b3fec289dd06646d0d6f81f8fcf910
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46286537"
---
# <a name="webbrowser-security"></a><span data-ttu-id="66180-102">Sécurité WebBrowser</span><span class="sxs-lookup"><span data-stu-id="66180-102">WebBrowser Security</span></span>
<span data-ttu-id="66180-103">Le <xref:System.Windows.Forms.WebBrowser> contrôle est conçu pour fonctionner avec une confiance totale.</span><span class="sxs-lookup"><span data-stu-id="66180-103">The <xref:System.Windows.Forms.WebBrowser> control is designed to work in full trust only.</span></span> <span data-ttu-id="66180-104">Le contenu HTML affiché dans le contrôle peut provenir de serveurs Web externes et peut contenir du code non managé sous la forme de scripts ou de contrôles Web.</span><span class="sxs-lookup"><span data-stu-id="66180-104">The HTML content displayed in the control can come from external Web servers and may contain unmanaged code in the form of scripts or Web controls.</span></span> <span data-ttu-id="66180-105">Si vous utilisez le <xref:System.Windows.Forms.WebBrowser> contrôle dans ce cas, le contrôle n’est pas moins sécurisé qu’Internet Explorer serait, mais managé <xref:System.Windows.Forms.WebBrowser> contrôle n’empêche pas ce code non managé en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="66180-105">If you use the <xref:System.Windows.Forms.WebBrowser> control in this situation, the control is no less secure than Internet Explorer would be, but the managed <xref:System.Windows.Forms.WebBrowser> control does not prevent such unmanaged code from running.</span></span>  
  
 <span data-ttu-id="66180-106">Pour plus d’informations sur les problèmes de sécurité relatifs à ActiveX sous-jacent `WebBrowser` du contrôle, consultez [contrôle WebBrowser](https://go.microsoft.com/fwlink/?LinkId=198812).</span><span class="sxs-lookup"><span data-stu-id="66180-106">For more information about security issues relating to the underlying ActiveX `WebBrowser` control, see [WebBrowser Control](https://go.microsoft.com/fwlink/?LinkId=198812).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="66180-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66180-107">See Also</span></span>  
 <xref:System.Windows.Forms.WebBrowser>  
 [<span data-ttu-id="66180-108">Vue d’ensemble du contrôle WebBrowser</span><span class="sxs-lookup"><span data-stu-id="66180-108">WebBrowser Control Overview</span></span>](../../../../docs/framework/winforms/controls/webbrowser-control-overview.md)  
 [<span data-ttu-id="66180-109">WebBrowser, contrôle</span><span class="sxs-lookup"><span data-stu-id="66180-109">WebBrowser Control</span></span>](https://go.microsoft.com/fwlink/?LinkId=198812)
