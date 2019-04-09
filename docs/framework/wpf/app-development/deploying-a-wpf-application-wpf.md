---
title: Déploiement d'une application WPF (WPF)
ms.date: 03/30/2017
helpviewer_keywords:
- WPF applications [WPF], deployment
- deployment [WPF], applications
ms.assetid: 12cadca0-b32c-4064-9a56-e6a306dcc76d
ms.openlocfilehash: 35515d37756c46d7d38ca272d76da3126fde385f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59132354"
---
# <a name="deploying-a-wpf-application-wpf"></a>Déploiement d'une application WPF (WPF)
Une fois que les applications de Windows Presentation Foundation (WPF) sont créées, elles doivent être déployées. [!INCLUDE[TLA#tla_mswin](../../../../includes/tlasharptla-mswin-md.md)] et le .NET Framework inclut plusieurs technologies de déploiement. La technologie de déploiement utilisée pour déployer une application [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] dépend du type d’application. Cette rubrique fournit une vue d’ensemble des différentes technologies de déploiement et explique leur utilisation avec les spécifications de déploiement de chaque type d’application [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)].  

<a name="Deployment_Technologies"></a>   
## <a name="deployment-technologies"></a>Technologies de déploiement  
 [!INCLUDE[TLA#tla_mswin](../../../../includes/tlasharptla-mswin-md.md)] et le .NET Framework inclut plusieurs technologies de déploiement, notamment :  
  
-   Déploiement XCopy.  
  
-   [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)] déploiement.  
  
-   [!INCLUDE[TLA#tla_clickonce](../../../../includes/tlasharptla-clickonce-md.md)] déploiement.  
  
<a name="XCopy_Deployment"></a>   
### <a name="xcopy-deployment"></a>Déploiement XCopy  
 Le déploiement XCopy fait référence à l’utilisation du programme en ligne de commande XCopy pour copier les fichiers d’un emplacement vers un autre. Le déploiement XCopy convient dans les cas suivants :  
  
-   L’application est autonome. Elle n’a pas besoin de mettre à jour le client pour fonctionner.  
  
-   Les fichiers d’application doivent être déplacés d’un emplacement vers un autre, par exemple d’un emplacement de génération (disque local, partage de fichiers [!INCLUDE[TLA2#tla_unc](../../../../includes/tla2sharptla-unc-md.md)], etc.) vers un emplacement de publication (site web, partage de fichiers [!INCLUDE[TLA2#tla_unc](../../../../includes/tla2sharptla-unc-md.md)], etc.).  
  
-   L’application ne nécessite pas d’interface intégrée (raccourci du menu Démarrer, icône sur le Bureau, et ainsi de suite).  
  
 XCopy convient pour les scénarios de déploiement simples. Toutefois, il est limité quand des fonctions de déploiement plus complexes sont requises. En particulier, l’utilisation de XCopy entraîne souvent une surcharge de temps afin de créer, d’exécuter et de gérer des scripts permettant de gérer le déploiement de manière fiable. En outre, XCopy ne prend pas en charge la gestion de version, la désinstallation ni la restauration.  
  
<a name="Windows_Installer"></a>   
### <a name="windows-installer"></a>Windows Installer  
 [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)] Permet d’empaqueter en tant qu’exécutables autonomes qui peuvent être facilement distribués aux clients et exécuter des applications. Par ailleurs, [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)] est installé avec [!INCLUDE[TLA#tla_mswin](../../../../includes/tlasharptla-mswin-md.md)] et permet l’intégration au Bureau, au menu Démarrer et au Panneau de configuration des programmes.  
  
 [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)] simplifie l’installation et la désinstallation d’applications, mais il ne fournit pas de fonctions permettant de garantir que les applications installées sont mises à jour à partir d’un point de vue de contrôle de version.  
  
 Pour plus d’informations sur le programme d’installation de Windows, consultez [déploiement de Windows Installer](/visualstudio/deployment/deploying-applications-services-and-components#create-an-installer-package-windows-desktop).
  
<a name="ClickOnce_Deployment"></a>   
### <a name="clickonce-deployment"></a>déploiement ClickOnce  
 [!INCLUDE[TLA2#tla_clickonce](../../../../includes/tla2sharptla-clickonce-md.md)] permet le déploiement d’applications de style Web pour les applications non-Web. Les applications sont publiées vers et déployées depuis des serveurs de fichiers ou web. [!INCLUDE[TLA2#tla_clickonce](../../../../includes/tla2sharptla-clickonce-md.md)] ne prend pas en charge l’ensemble des fonctionnalités clientes proposées par les applications installées par [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)], mais prend en charge un sous-ensemble qui intègre les éléments suivants :  
  
-   Intégration au menu Démarrer et au Panneau de configuration des programmes.  
  
-   Gestion de version, restauration et désinstallation.  
  
-   Mode d’installation en ligne, qui lance toujours une application à partir de l’emplacement de déploiement.  
  
-   Mise à jour automatique quand de nouvelles versions sont disponibles.  
  
-   Inscription d’extensions de fichiers.  
  
 Pour plus d’informations sur [!INCLUDE[TLA2#tla_clickonce](../../../../includes/tla2sharptla-clickonce-md.md)], consultez [Sécurité et déploiement ClickOnce](/visualstudio/deployment/clickonce-security-and-deployment).  
  
<a name="Deploying_WPF_Applications"></a>   
## <a name="deploying-wpf-applications"></a>Déploiement d’applications WPF  
 Les options de déploiement d’une application [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] dépendent du type d’application. Du point de vue du déploiement, [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] a trois types d’applications significatifs :  
  
-   Applications autonomes.  
  
-   Applications [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] à balisage.  
  
-   [!INCLUDE[TLA#tla_xbap#plural](../../../../includes/tlasharptla-xbapsharpplural-md.md)].  
  
<a name="Deploying_Standalone_Applications"></a>   
### <a name="deploying-standalone-applications"></a>Déploiement d’applications autonomes  
 Les applications autonomes sont déployées à l’aide de [!INCLUDE[TLA#tla_clickonce](../../../../includes/tlasharptla-clickonce-md.md)] ou de [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)]. Dans tous les cas, pour pouvoir être exécutées, les applications autonomes nécessitent un niveau de confiance totale. La confiance totale est accordée automatiquement aux applications autonomes déployées à l’aide de [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)], mais pas aux applications autonomes déployées à l’aide de [!INCLUDE[TLA2#tla_clickonce](../../../../includes/tla2sharptla-clickonce-md.md)]. Au lieu de cela, [!INCLUDE[TLA2#tla_clickonce](../../../../includes/tla2sharptla-clickonce-md.md)] affiche une boîte de dialogue d’avertissement de sécurité que l’utilisateur doit accepter avant de pouvoir installer une application autonome. Si l’avertissement est accepté, l’application autonome est installée et bénéficie de la confiance totale. Dans le cas contraire, l’application autonome n’est pas installée.  
  
<a name="Deploying_Markup_Only_XAML_Applications"></a>   
### <a name="deploying-markup-only-xaml-applications"></a>Déploiement d’applications XAML à balisage  
 Les pages [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] à balisage sont généralement publiées sur des serveurs web, comme des pages [!INCLUDE[TLA2#tla_html](../../../../includes/tla2sharptla-html-md.md)], et peuvent être affichées avec [!INCLUDE[TLA2#tla_iegeneric](../../../../includes/tla2sharptla-iegeneric-md.md)]. Les pages [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] à balisage sont exécutées dans un bac à sable (sandbox) de sécurité de confiance partielle en fonction de restrictions définies par le jeu d’autorisations de la zone Internet. Ainsi, les applications web [!INCLUDE[TLA2#tla_html](../../../../includes/tla2sharptla-html-md.md)] disposent d’un bac à sable (sandbox) de sécurité équivalent.  
  
 Pour plus d’informations sur la sécurité pour les applications [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)], consultez [Sécurité](../security-wpf.md).  
  
 Les pages [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] à balisage peuvent être installées sur le système de fichiers local à l’aide de XCopy ou de [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)]. Ces pages peuvent être visualisés [!INCLUDE[TLA2#tla_iegeneric](../../../../includes/tla2sharptla-iegeneric-md.md)] ou de l’Explorateur Windows.  
  
 Pour plus d’informations sur XAML, consultez [Vue d’ensemble du langage XAML (WPF)](../advanced/xaml-overview-wpf.md).  
  
<a name="Deploying_XAML_Browser_Applications"></a>   
### <a name="deploying-xaml-browser-applications"></a>Déploiement d’applications du navigateur XAML  
 [!INCLUDE[TLA2#tla_xbap#plural](../../../../includes/tla2sharptla-xbapsharpplural-md.md)] sont des applications compilées qui nécessitent les trois fichiers suivants à déployer :  
  
-   *ApplicationName*.exe : Fichier application de l’assembly exécutable.  
  
-   *ApplicationName*.xbap : Le manifeste de déploiement.  
  
-   *ApplicationName*. exe.manifest : Manifeste d’application.  
  
> [!NOTE]
>  Pour plus d’informations sur les manifestes de déploiement et d’application, consultez [Génération d’une application WPF](building-a-wpf-application-wpf.md).  
  
 Ces fichiers sont produits quand une [!INCLUDE[TLA2#tla_xbap](../../../../includes/tla2sharptla-xbap-md.md)] est générée. Pour plus d'informations, voir [Procédure : Créer un nouveau projet d’Application de navigateur WPF](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/bb628663(v=vs.100)). Comme les pages [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] à balisage, les [!INCLUDE[TLA2#tla_xbap#plural](../../../../includes/tla2sharptla-xbapsharpplural-md.md)] sont généralement publiées sur un serveur web et affichées avec [!INCLUDE[TLA2#tla_iegeneric](../../../../includes/tla2sharptla-iegeneric-md.md)].  
  
 [!INCLUDE[TLA2#tla_xbap#plural](../../../../includes/tla2sharptla-xbapsharpplural-md.md)] peut être déployé à l’aide d’une des techniques de déploiement. Toutefois, [!INCLUDE[TLA#tla_clickonce](../../../../includes/tlasharptla-clickonce-md.md)] est recommandé puisqu’il fournit les fonctions suivantes :  
  
1.  Mises à jour automatiques quand une nouvelle version est publiée.  
  
2.  Privilèges d’élévation pour l’[!INCLUDE[TLA2#tla_xbap](../../../../includes/tla2sharptla-xbap-md.md)] en cours d’exécution avec une confiance totale.  
  
 Par défaut, ClickOnce publie les fichiers d’application avec l’extension .deploy. Cela peut s’avérer problématique, mais peut être désactivé. Pour plus d’informations, consultez [Problèmes de configuration de serveur et de client lors de déploiements ClickOnce](/visualstudio/deployment/server-and-client-configuration-issues-in-clickonce-deployments).  
  
 Pour plus d’informations sur le déploiement des [!INCLUDE[TLA#tla_xbap#plural](../../../../includes/tlasharptla-xbapsharpplural-md.md)], consultez [Vue d’ensemble des applications de navigateur XAML](wpf-xaml-browser-applications-overview.md).  
  
<a name="Installing__NET_Framework_3_0"></a>   
## <a name="installing-the-net-framework"></a>Installation du .NET Framework  
 Pour exécuter un [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] application, Microsoft .NET Framework doit être installé sur le client. [!INCLUDE[TLA2#tla_ie](../../../../includes/tla2sharptla-ie-md.md)] détecte automatiquement si les clients sont installés avec le .NET Framework lorsque [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] applications hébergées par un navigateur sont affichées. Si le .NET Framework n’est pas installé, [!INCLUDE[TLA2#tla_ie](../../../../includes/tla2sharptla-ie-md.md)] invitant les utilisateurs à installer.  
  
 Pour détecter si .NET Framework est installé, [!INCLUDE[TLA2#tla_ie](../../../../includes/tla2sharptla-ie-md.md)] inclut une application de programme d’amorçage qui est inscrit en tant que la procédure de secours [!INCLUDE[TLA#tla_mime](../../../../includes/tlasharptla-mime-md.md)] gestionnaire pour les fichiers de contenu avec les extensions suivantes : .xaml, .xps, .xbap et .application. Si vous accédez à ces types de fichiers et le .NET Framework n’est pas installé sur le client, le programme d’amorçage demande l’autorisation pour l’installer. Si l’autorisation n’est pas fournie, l’application ni .NET Framework est installée.  
  
 Si l’autorisation est accordée, [!INCLUDE[TLA2#tla_ie](../../../../includes/tla2sharptla-ie-md.md)] télécharge et installe le .NET Framework à l’aide de la [!INCLUDE[TLA#tla_bits](../../../../includes/tlasharptla-bits-md.md)]. Après l’installation du .NET Framework, le fichier demandé à l’origine est ouvert dans une nouvelle fenêtre de navigateur.  
  
 La détection automatique de .NET framework est disponible sur [!INCLUDE[TLA#tla_longhorn](../../../../includes/tlasharptla-longhorn-md.md)], [!INCLUDE[TLA#tla_winxpsp2](../../../../includes/tlasharptla-winxpsp2-md.md)], et [!INCLUDE[TLA#tla_winnetsvrfamsp1](../../../../includes/tlasharptla-winnetsvrfamsp1-md.md)] les clients qui ont [!INCLUDE[TLA2#tla_ie7](../../../../includes/tla2sharptla-ie7-md.md)] ou version ultérieure.  
  
 Pour plus d’informations, consultez [Déploiement d’applications et du .NET Framework](../../deployment/index.md).  
  
## <a name="see-also"></a>Voir aussi

- [Génération d'une application WPF](building-a-wpf-application-wpf.md)
- [Sécurité](../security-wpf.md)
