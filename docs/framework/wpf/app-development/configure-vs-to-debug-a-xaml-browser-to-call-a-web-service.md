---
title: 'Comment : configurer Visual Studio pour déboguer une application de navigateur XAML et appeler un service Web'
ms.date: 03/30/2017
helpviewer_keywords:
- debugging XBAPs that call a Web service [WPF]
- debugging security exceptions for XBAPs [WPF]
- security exception for XBAPs [WPF], debugging
- configuring Visual Studio to debug XAML browser applications [WPF]
- configuring Visual Studio to debug XBAPs [WPF]
ms.assetid: fd1db082-a7bb-4c4b-9331-6ad74a0682d0
ms.openlocfilehash: 182ceb96385bdca74d1d5c20079f78fe589982cf
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48779190"
---
# <a name="how-to-configure-visual-studio-to-debug-a-xaml-browser-application-to-call-a-web-service"></a>Comment : configurer Visual Studio pour déboguer une application de navigateur XAML et appeler un service Web
[!INCLUDE[TLA#tla_xbap#plural](../../../../includes/tlasharptla-xbapsharpplural-md.md)] s’exécutent dans un bac à sable de sécurité de confiance partielle qui est limité au jeu de la zone Internet d’autorisations. Ce jeu d’autorisations restreint les appels de service Web seulement services Web qui sont trouvent dans le [!INCLUDE[TLA2#tla_xbap](../../../../includes/tla2sharptla-xbap-md.md)] site de l’application d’origine. Quand un [!INCLUDE[TLA2#tla_xbap](../../../../includes/tla2sharptla-xbap-md.md)] du débogage à partir de Visual Studio 2005, cependant, il n'est pas considérée comme ayant le même site d’origine que le service Web il références. Cette causes des exceptions de sécurité à déclencher lorsque la [!INCLUDE[TLA2#tla_xbap](../../../../includes/tla2sharptla-xbap-md.md)] tente d’appeler le service Web. Toutefois, un Visual Studio 2005 [!INCLUDE[TLA#tla_wpfbrowserappproj](../../../../includes/tlasharptla-wpfbrowserappproj-md.md)] projet peut être configuré pour simuler le même site d’origine que le service Web qu’elle appelle pendant le débogage. Cela permet la [!INCLUDE[TLA2#tla_xbap](../../../../includes/tla2sharptla-xbap-md.md)] à appeler en toute sécurité le service Web sans provoquer des exceptions de sécurité.

## <a name="configuring-visual-studio"></a>Configuration de Visual Studio
 Pour configurer Visual Studio 2005 pour déboguer un [!INCLUDE[TLA2#tla_xbap](../../../../includes/tla2sharptla-xbap-md.md)] qui appelle un service Web :

1.  Après avoir sélectionné un projet dans l’ **Explorateur de solutions**, dans le menu **Projet** , cliquez sur **Propriétés**.

2.  Dans le **Concepteur de projets**, cliquez sur le **déboguer** onglet.

3.  Dans le **Action de démarrage** section, sélectionnez **démarrer le programme externe** et entrez les informations suivantes :

     `C:\WINDOWS\System32\PresentationHost.exe`

4.  Dans le **Options de démarrage** section, entrez le texte suivant dans le **arguments de ligne de commande** zone de texte :

     `-debug`  *Nom de fichier*

     Le *filename* valeur pour le **-déboguer** paramètre est le nom de fichier .xbap, par exemple :

     `-debug c:\example.xbap`

> [!NOTE]
>  C’est la configuration par défaut pour les solutions qui sont créés avec Visual Studio 2005 [!INCLUDE[TLA#tla_wpfbrowserappproj](../../../../includes/tlasharptla-wpfbrowserappproj-md.md)] modèle de projet.

1.  Après avoir sélectionné un projet dans l’ **Explorateur de solutions**, dans le menu **Projet** , cliquez sur **Propriétés**.

2.  Dans le **Concepteur de projets**, cliquez sur le **déboguer** onglet.

3.  Dans le **Options de démarrage** , ajoutez le paramètre de ligne de commande suivant à la **arguments de ligne de commande** zone de texte :

     `-debugSecurityZoneURL`  *URL*

     Le *URL* valeur pour le **- debugSecurityZoneURL** paramètre est le [!INCLUDE[TLA#tla_url](../../../../includes/tlasharptla-url-md.md)] pour l’emplacement que vous souhaitez simuler comme étant le site d’origine de votre application.

 Par exemple, imaginez un [!INCLUDE[TLA#tla_xbap](../../../../includes/tlasharptla-xbap-md.md)] qui utilise un service Web par le code suivant [!INCLUDE[TLA2#tla_url](../../../../includes/tla2sharptla-url-md.md)]:

 `http://services.msdn.microsoft.com/ContentServices/ContentService.asmx`

 Le site d’origine [!INCLUDE[TLA2#tla_url](../../../../includes/tla2sharptla-url-md.md)] pour ce site Web service est :

 `http://services.msdn.microsoft.com`

 Par conséquent, la version complète **- debugSecurityZoneURL** paramètre de ligne de commande et la valeur est :

 `-debugSecurityZoneURL http://services.msdn.microsoft.com`

## <a name="see-also"></a>Voir aussi
 [Hôte WPF (PresentationHost.exe)](../../../../docs/framework/wpf/app-development/wpf-host-presentationhost-exe.md)
