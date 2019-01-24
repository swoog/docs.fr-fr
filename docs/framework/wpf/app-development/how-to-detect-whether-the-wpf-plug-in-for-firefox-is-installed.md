---
title: 'Procédure : Détecter si le plug-in WPF de Firefox est installé'
ms.date: 03/30/2017
helpviewer_keywords:
- plug-in for Firefox [WPF]
- detecting Firefox installation [WPF]
- checking for the Firefox plug-in [WPF]
- Firefox [WPF], detecting installation
- detecting whether the WPF plug-in for Firefox is installed [WPF]
ms.assetid: 5f839373-e3fb-44f1-88ad-4a0761f02189
ms.openlocfilehash: f017aec8788d9ed38476262bba457f4621217519
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54677977"
---
# <a name="how-to-detect-whether-the-wpf-plug-in-for-firefox-is-installed"></a><span data-ttu-id="9cafe-102">Procédure : Détecter si le plug-in WPF de Firefox est installé</span><span class="sxs-lookup"><span data-stu-id="9cafe-102">How to: Detect Whether the WPF Plug-In for Firefox Is Installed</span></span>
<span data-ttu-id="9cafe-103">Windows Presentation Foundation (WPF) plug-in de Firefox permet [!INCLUDE[TLA#tla_xbap#plural](../../../../includes/tlasharptla-xbapsharpplural-md.md)] et perdre les fichiers XAML à exécuter dans le navigateur Mozilla Firefox.</span><span class="sxs-lookup"><span data-stu-id="9cafe-103">The Windows Presentation Foundation (WPF) plug-in for Firefox enables [!INCLUDE[TLA#tla_xbap#plural](../../../../includes/tlasharptla-xbapsharpplural-md.md)] and loose XAML files to run in the Mozilla Firefox browser.</span></span> <span data-ttu-id="9cafe-104">Cette rubrique fournit un script écrit en HTML et JavaScript, les administrateurs peuvent utiliser pour déterminer si le WPF plug-in de Firefox est installé.</span><span class="sxs-lookup"><span data-stu-id="9cafe-104">This topic provides a script written in HTML and JavaScript that administrators can use to determine whether the WPF plug-in for Firefox is installed.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="9cafe-105">Pour plus d’informations sur l’installation, déploiement et la détection du [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)], consultez [installer le .NET Framework pour les développeurs](../../../../docs/framework/install/guide-for-developers.md).</span><span class="sxs-lookup"><span data-stu-id="9cafe-105">For more information about installing, deploying, and detecting the [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)], see [Install the .NET Framework for developers](../../../../docs/framework/install/guide-for-developers.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="9cafe-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="9cafe-106">Example</span></span>  
 <span data-ttu-id="9cafe-107">Lorsque le [!INCLUDE[net_v35_short](../../../../includes/net-v35-short-md.md)] est installé, l’ordinateur client est configuré avec un plug-in WPF de Firefox.</span><span class="sxs-lookup"><span data-stu-id="9cafe-107">When the [!INCLUDE[net_v35_short](../../../../includes/net-v35-short-md.md)] is installed, the client computer is configured with a WPF plug-in for Firefox.</span></span> <span data-ttu-id="9cafe-108">L’exemple de script suivant vérifie le plug-in WPF de Firefox, puis affiche un message d’état approprié.</span><span class="sxs-lookup"><span data-stu-id="9cafe-108">The following example script checks for the WPF plug-in for Firefox and then displays an appropriate status message.</span></span>  
  
```  
<HTML>  
  
  <HEAD>  
    <TITLE>Test for the WPF plug-in for Firefox</TITLE>  
    <META HTTP-EQUIV="Content-Type" CONTENT="text/html; charset=utf-8" />  
    <SCRIPT type="text/javascript">  
    <!--  
    function OnLoad()  
    {  
  
       // Check for the WPF plug-in for Firefox and report  
       var msg = "The WPF plug-in for Firefox is ";  
       var wpfPlugin = navigator.plugins["Windows Presentation Foundation"];  
       if( wpfPlugin != null ) {  
          document.writeln(msg + " installed.");  
       }  
       else {  
          document.writeln(msg + " not installed. Please install or reinstall the .NET Framework 3.5.");  
       }  
    }  
    -->  
    </SCRIPT>  
  </HEAD>  
  
  <BODY onload="OnLoad()" />  
  
</HTML>  
```  
  
 <span data-ttu-id="9cafe-109">Si la vérification pour le plug-in WPF de Firefox est réussie, le message d’état suivant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="9cafe-109">If the check for the WPF plug-in for Firefox is successful, the following status message is displayed:</span></span>  
  
 `The WPF plug-in for Firefox is installed.`  
  
 <span data-ttu-id="9cafe-110">Sinon, le message d’état suivant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="9cafe-110">Otherwise, the following status message is displayed:</span></span>  
  
 `The WPF plug-in for Firefox is not installed. Please install or reinstall the .NET Framework 3.5.`  
  
## <a name="see-also"></a><span data-ttu-id="9cafe-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9cafe-111">See also</span></span>
- [<span data-ttu-id="9cafe-112">Détecter si .NET Framework 3.0 est installé</span><span class="sxs-lookup"><span data-stu-id="9cafe-112">Detect Whether the .NET Framework 3.0 Is Installed</span></span>](../../../../docs/framework/wpf/app-development/how-to-detect-whether-the-net-framework-3-0-is-installed.md)
- [<span data-ttu-id="9cafe-113">Détecter si .NET Framework 3.5 est installé</span><span class="sxs-lookup"><span data-stu-id="9cafe-113">Detect Whether the .NET Framework 3.5 Is Installed</span></span>](../../../../docs/framework/wpf/app-development/how-to-detect-whether-the-net-framework-3-5-is-installed.md)
- [<span data-ttu-id="9cafe-114">Vue d’ensemble des applications du navigateur XAML WPF</span><span class="sxs-lookup"><span data-stu-id="9cafe-114">WPF XAML Browser Applications Overview</span></span>](../../../../docs/framework/wpf/app-development/wpf-xaml-browser-applications-overview.md)
