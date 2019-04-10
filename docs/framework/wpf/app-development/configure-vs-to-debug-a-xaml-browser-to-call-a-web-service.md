---
title: 'Procédure : Configurer Visual Studio pour déboguer une application de navigateur XAML et appeler un service web'
ms.date: 03/30/2017
helpviewer_keywords:
- debugging XBAPs that call a Web service [WPF]
- debugging security exceptions for XBAPs [WPF]
- security exception for XBAPs [WPF], debugging
- configuring Visual Studio to debug XAML browser applications [WPF]
- configuring Visual Studio to debug XBAPs [WPF]
ms.assetid: fd1db082-a7bb-4c4b-9331-6ad74a0682d0
ms.openlocfilehash: dcaabf9ecd47bc88095e92aa8ed28ad5f13fd1dc
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59314371"
---
# <a name="how-to-configure-visual-studio-to-debug-a-xaml-browser-application-to-call-a-web-service"></a><span data-ttu-id="3700c-102">Procédure : Configurer Visual Studio pour déboguer une application de navigateur XAML et appeler un service web</span><span class="sxs-lookup"><span data-stu-id="3700c-102">How to: Configure Visual Studio to Debug a XAML Browser Application to Call a Web Service</span></span>
[!INCLUDE[TLA#tla_xbap#plural](../../../../includes/tlasharptla-xbapsharpplural-md.md)] <span data-ttu-id="3700c-103">s’exécutent dans un bac à sable de sécurité de confiance partielle qui est limité au jeu de la zone Internet d’autorisations.</span><span class="sxs-lookup"><span data-stu-id="3700c-103">run within a partial-trust security sandbox that is restricted to the Internet zone set of permissions.</span></span> <span data-ttu-id="3700c-104">Ce jeu d’autorisations restreint les appels de service Web seulement services Web qui sont trouvent dans le [!INCLUDE[TLA2#tla_xbap](../../../../includes/tla2sharptla-xbap-md.md)] site de l’application d’origine.</span><span class="sxs-lookup"><span data-stu-id="3700c-104">This permission set restricts Web service calls to only Web services that are located at the [!INCLUDE[TLA2#tla_xbap](../../../../includes/tla2sharptla-xbap-md.md)] application's site of origin.</span></span> <span data-ttu-id="3700c-105">Quand un [!INCLUDE[TLA2#tla_xbap](../../../../includes/tla2sharptla-xbap-md.md)] du débogage à partir de Visual Studio 2005, cependant, il n'est pas considérée comme ayant le même site d’origine que le service Web il références.</span><span class="sxs-lookup"><span data-stu-id="3700c-105">When an [!INCLUDE[TLA2#tla_xbap](../../../../includes/tla2sharptla-xbap-md.md)] is debugged from Visual Studio 2005, though, it is not considered to have the same site of origin as the Web service it references.</span></span> <span data-ttu-id="3700c-106">Cette causes des exceptions de sécurité à déclencher lorsque la [!INCLUDE[TLA2#tla_xbap](../../../../includes/tla2sharptla-xbap-md.md)] tente d’appeler le service Web.</span><span class="sxs-lookup"><span data-stu-id="3700c-106">This causes security exceptions to be raised when the [!INCLUDE[TLA2#tla_xbap](../../../../includes/tla2sharptla-xbap-md.md)] attempts to call the Web service.</span></span> <span data-ttu-id="3700c-107">Toutefois, un Visual Studio 2005 [!INCLUDE[TLA#tla_wpfbrowserappproj](../../../../includes/tlasharptla-wpfbrowserappproj-md.md)] projet peut être configuré pour simuler le même site d’origine que le service Web qu’elle appelle pendant le débogage.</span><span class="sxs-lookup"><span data-stu-id="3700c-107">However, a Visual Studio 2005 [!INCLUDE[TLA#tla_wpfbrowserappproj](../../../../includes/tlasharptla-wpfbrowserappproj-md.md)] project can be configured to simulate having the same site of origin as the Web service it calls while debugging.</span></span> <span data-ttu-id="3700c-108">Cela permet la [!INCLUDE[TLA2#tla_xbap](../../../../includes/tla2sharptla-xbap-md.md)] à appeler en toute sécurité le service Web sans provoquer des exceptions de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3700c-108">This allows the [!INCLUDE[TLA2#tla_xbap](../../../../includes/tla2sharptla-xbap-md.md)] to safely call the Web service without causing security exceptions.</span></span>

## <a name="configuring-visual-studio"></a><span data-ttu-id="3700c-109">Configuration de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3700c-109">Configuring Visual Studio</span></span>
 <span data-ttu-id="3700c-110">Pour configurer Visual Studio 2005 pour déboguer un [!INCLUDE[TLA2#tla_xbap](../../../../includes/tla2sharptla-xbap-md.md)] qui appelle un service Web :</span><span class="sxs-lookup"><span data-stu-id="3700c-110">To configure Visual Studio 2005 to debug an [!INCLUDE[TLA2#tla_xbap](../../../../includes/tla2sharptla-xbap-md.md)] that calls a Web service:</span></span>

1. <span data-ttu-id="3700c-111">Après avoir sélectionné un projet dans l’ **Explorateur de solutions**, dans le menu **Projet** , cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="3700c-111">With a project selected in **Solution Explorer**, on the **Project** menu, click **Properties**.</span></span>

2. <span data-ttu-id="3700c-112">Dans le **Concepteur de projets**, cliquez sur le **déboguer** onglet.</span><span class="sxs-lookup"><span data-stu-id="3700c-112">In the **Project Designer**, click the **Debug** tab.</span></span>

3. <span data-ttu-id="3700c-113">Dans le **Action de démarrage** section, sélectionnez **démarrer le programme externe** et entrez les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="3700c-113">In the **Start Action** section, select **Start external program** and enter the following:</span></span>

     `C:\WINDOWS\System32\PresentationHost.exe`

4. <span data-ttu-id="3700c-114">Dans le **Options de démarrage** section, entrez le texte suivant dans le **arguments de ligne de commande** zone de texte :</span><span class="sxs-lookup"><span data-stu-id="3700c-114">In the **Start Options** section, enter the following into the **Command line arguments** text box:</span></span>

     `-debug`  *<span data-ttu-id="3700c-115">filename</span><span class="sxs-lookup"><span data-stu-id="3700c-115">filename</span></span>*

     <span data-ttu-id="3700c-116">Le *filename* valeur pour le **-déboguer** paramètre est le nom de fichier .xbap, par exemple :</span><span class="sxs-lookup"><span data-stu-id="3700c-116">The *filename* value for the **-debug** parameter is the .xbap filename; for example:</span></span>

     `-debug c:\example.xbap`

> [!NOTE]
>  <span data-ttu-id="3700c-117">C’est la configuration par défaut pour les solutions qui sont créés avec Visual Studio 2005 [!INCLUDE[TLA#tla_wpfbrowserappproj](../../../../includes/tlasharptla-wpfbrowserappproj-md.md)] modèle de projet.</span><span class="sxs-lookup"><span data-stu-id="3700c-117">This is the default configuration for solutions that are created with the Visual Studio 2005 [!INCLUDE[TLA#tla_wpfbrowserappproj](../../../../includes/tlasharptla-wpfbrowserappproj-md.md)] project template.</span></span>

1. <span data-ttu-id="3700c-118">Après avoir sélectionné un projet dans l’ **Explorateur de solutions**, dans le menu **Projet** , cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="3700c-118">With a project selected in **Solution Explorer**, on the **Project** menu, click **Properties**.</span></span>

2. <span data-ttu-id="3700c-119">Dans le **Concepteur de projets**, cliquez sur le **déboguer** onglet.</span><span class="sxs-lookup"><span data-stu-id="3700c-119">In the **Project Designer**, click the **Debug** tab.</span></span>

3. <span data-ttu-id="3700c-120">Dans le **Options de démarrage** , ajoutez le paramètre de ligne de commande suivant à la **arguments de ligne de commande** zone de texte :</span><span class="sxs-lookup"><span data-stu-id="3700c-120">In the **Start Options** section, add the following command-line parameter to the **Command line arguments** text box:</span></span>

     `-debugSecurityZoneURL`  *<span data-ttu-id="3700c-121">URL</span><span class="sxs-lookup"><span data-stu-id="3700c-121">URL</span></span>*

     <span data-ttu-id="3700c-122">Le *URL* valeur pour le **- debugSecurityZoneURL** paramètre est le [!INCLUDE[TLA#tla_url](../../../../includes/tlasharptla-url-md.md)] pour l’emplacement que vous souhaitez simuler comme étant le site d’origine de votre application.</span><span class="sxs-lookup"><span data-stu-id="3700c-122">The *URL* value for the **-debugSecurityZoneURL** parameter is the [!INCLUDE[TLA#tla_url](../../../../includes/tlasharptla-url-md.md)] for the location that you want to simulate as being the site of origin of your application.</span></span>

 <span data-ttu-id="3700c-123">Par exemple, imaginez un [!INCLUDE[TLA#tla_xbap](../../../../includes/tlasharptla-xbap-md.md)] qui utilise un service Web par le code suivant [!INCLUDE[TLA2#tla_url](../../../../includes/tla2sharptla-url-md.md)]:</span><span class="sxs-lookup"><span data-stu-id="3700c-123">As an example, consider a [!INCLUDE[TLA#tla_xbap](../../../../includes/tlasharptla-xbap-md.md)] that uses a Web service with the following [!INCLUDE[TLA2#tla_url](../../../../includes/tla2sharptla-url-md.md)]:</span></span>

 `http://services.msdn.microsoft.com/ContentServices/ContentService.asmx`

 <span data-ttu-id="3700c-124">Le site d’origine [!INCLUDE[TLA2#tla_url](../../../../includes/tla2sharptla-url-md.md)] pour ce site Web service est :</span><span class="sxs-lookup"><span data-stu-id="3700c-124">The site of origin [!INCLUDE[TLA2#tla_url](../../../../includes/tla2sharptla-url-md.md)] for this Web service is:</span></span>

 `http://services.msdn.microsoft.com`

 <span data-ttu-id="3700c-125">Par conséquent, la version complète **- debugSecurityZoneURL** paramètre de ligne de commande et la valeur est :</span><span class="sxs-lookup"><span data-stu-id="3700c-125">Consequently, the complete **-debugSecurityZoneURL** command-line parameter and value is:</span></span>

 `-debugSecurityZoneURL http://services.msdn.microsoft.com`

## <a name="see-also"></a><span data-ttu-id="3700c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3700c-126">See also</span></span>

- [<span data-ttu-id="3700c-127">Hôte WPF (PresentationHost.exe)</span><span class="sxs-lookup"><span data-stu-id="3700c-127">WPF Host (PresentationHost.exe)</span></span>](wpf-host-presentationhost-exe.md)
