---
title: Publication du service WCF
ms.date: 03/30/2017
ms.assetid: c806b253-cd47-4b96-b831-e73cbf08808f
ms.openlocfilehash: b62b2616233eb81e64945e997a2efe17973dedd2
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2018
ms.locfileid: "46585307"
---
# <a name="wcf-service-publishing"></a>Publication du service WCF

Publication de Service Windows Communication Foundation (WCF) vous aide à la progression de l’environnement de développement anticipée fourni par l’hôte de Service WCF et le Client Test WCF à déployer réellement l’application dans un environnement de production à des fins de test. Avant de vous engager à un plan de déploiement final, vous pouvez utiliser publication de Service Windows Communication Foundation (WCF) pour vérifier que votre service WCF s’exécute correctement et est prêt à être publié. Vous pouvez également choisir de déployer vos bibliothèques de service WCF à différents emplacements cibles pour le test.

## <a name="supported-services-and-target-locations"></a>Services pris en charge et emplacements cibles

Publication de Service WCF prend en charge la publication des services WCF créés à partir de l’ensemble des modèles de bibliothèque de service WCF et leurs modèles d’élément correspondants, qui incluent les éléments suivants :

-   Modèle de bibliothèque du Service WCF avec le modèle d’élément.

-   Bibliothèque du service de syndication.

Vous trouverez ces modèles de service en choisissant **fichier** > **nouveau projet** > [**Visual Basic** ou **Visual C#**] > **WCF**. Pour les autres modèles WCF à cet emplacement (y compris l’Application de Service de Workflow WCF et Application de Service WCF), vous pouvez publier à l’aide de [de publication pour les applications web à un clic](https://msdn.microsoft.com/library/dd465337\(v=vs.110\).aspx).

Le service peut être publié aux emplacements cibles suivants.

-   IIS local

-   Système de fichiers

-   Site FTP

## <a name="using-wcf-service-publishing"></a>Utilisation de la publication de service WCF

Pour déployer une implémentation de service, procédez comme suit :

1.  Ouvrez Visual Studio avec des privilèges élevés (cliquez sur le fichier exécutable et choisissez **exécuter en tant qu’administrateur** pour l’ouvrir).  Si vous utilisez IIS 7.0 ou version ultérieure, assurez-vous que vous avez installé le composant « La métabase et IIS6 Configuration compatibilité IIS » à l’aide de « Windows d’activer ou désactiver des fonctionnalités » dans le panneau de configuration.

2.  Ouvrez un projet de service, sélectionnez **Build** > **publier \<nom_projet >** dans le menu principal, ou cliquez sur le projet dans **l’Explorateur de solutions**et cliquez sur **publier**.

3.  Le **publier** fenêtre s’affiche. Cliquez sur le **...** . pour spécifier l'emplacement cible où doit être déployé le service. Vous pouvez sélectionner pour déployer l’application à local IIS, un système de fichiers ou un FTP Site. Si vous déployez l’application sur l’IIS local, vous pouvez sélectionner votre site Web et créez votre application web en cours, en cliquant sur le **créer une Application Web** icône dans l’angle supérieur droit.

4.  Après avoir cliqué sur **publier** dans la fenêtre principale, Visual Studio déploie l’application à l’emplacement cible indiqué et copie les fichiers Web.config, .svc et l’assembly dans le répertoire cible. . Le nom du fichier .svc sera « ProjectName.ServiceName.svc ». Une fois que le service est publié avec succès, vous trouverez un lien est disponible dans la fenêtre Sortie de Visual Studio, qui est similaire à « Connexion à un lien hypertexte » http://localhost/WebApplicationFolderName« http://localhost/WebApplicationFolderName ... ». Vous pouvez appuyer sur Ctrl et cliquer sur le lien pour ouvrir une page du navigateur dans Visual Studio afin d'afficher la structure des répertoires du service.

     S'il est impossible de visiter le site, l'explorateur de répertoires n'est peut-être pas activé dans IIS. Suivez les conseils fournis dans la section « Choses à essayer » pour l’activer. Ou bien, vous pouvez aussi taper directement » lien hypertexte « http://localhost/WebApplicationFolderName« http://localhost/WebApplicationFolderName/ProjectName.ServiceName.svc« pour afficher la page de votre service.

Vous pouvez utiliser **publier** pour spécifier si vous souhaitez copier l’assembly, la configuration et le fichier .svc pour tous les services définis dans le projet à l’emplacement cible et remplacer les fichiers existants dans la destination.

Si vous choisissez de déployer votre application sur le serveur IIS local, vous pouvez rencontrer des erreurs liées à l'installation d'IIS. Vérifiez que IIS est installé correctement. Vous pouvez entrer `http://localhost` dans la barre d’adresse et la vérification de votre navigateur si la page IIS par défaut affiche. Dans certains cas, les problèmes peuvent également provenir d’un enregistrement incorrect d’ASP.NET ou WCF dans IIS. Vous pouvez ouvrir l’invite de commandes développeur pour Visual Studio et exécutez la commande `aspnet_regiis.exe -ir` à résoudre les problèmes de l’inscription d’ASP.NET, ou exécutez la commande `ServiceModelReg.exe –ia` pour résoudre les problèmes d’inscription WCF.

## <a name="files-generated-for-publishing"></a>Fichiers générés en vue de leur publication
 Avant d’une bibliothèque de service WCF peut être hébergé sur le Web, les fichiers suivants sont générés par l’outil : fichiers d’assembly, fichier Web.config et fichier .svc. Tous les fichiers sont copiés à l'emplacement cible. Le service est ensuite publié.

### <a name="assembly-files"></a>Fichiers d'assembly
 Lorsque vous publiez un service WCF à l’aide de cet outil, le service est automatiquement créé en premier et les fichiers d’assembly sont générés dans le projet de service après la génération.

### <a name="svc-file"></a>Fichier .SVC
 L’opération de publication génère un fichier *.svc pour chaque service WCF, si le fichier existe ou non, pour garantir la validité de la version. Il existe deux types de fichiers svc différents : un pour la bibliothèque du Service WCF et de la bibliothèque de Service de Syndication et une autre pour séquentiel et de la bibliothèque de Service de flux de travail de Machine état. Le texte généré \*fichier .svc est copié dans le dossier racine dans l’emplacement cible.

### <a name="webconfig-file"></a>Fichier Web.config
 Chaque fois qu'un projet de service est publié à un emplacement cible spécifique, un fichier Web.config est créé.

 Le fichier Web.config généré contient des sections Web qui sont utiles pour l’hébergement Web et le contenu du fichier App.config pour la bibliothèque de service WCF avec les modifications suivantes :

-   L'adresse de base est exclue.

-   Les paramètres dans l'élément `<diagnostics>` sont exclus pour préserver les paramètres de suivi de la plateforme cible.

## <a name="publishing-wcf-services-with-non-http-bindings-to-iis"></a>Publication sur IIS de services WCF avec des liaisons non-HTTP
 Si vous utilisez IIS 7.0 ou une version ultérieure, vous pouvez publier des services WCF avec des liaisons non-HTTP à IIS. Vous devez effectuer plusieurs tâches de préconfiguration. Pour plus d’informations, consultez les rubriques à [hébergement dans Windows Process Activation Service](../../../docs/framework/wcf/feature-details/hosting-in-windows-process-activation-service.md).

## <a name="security"></a>Sécurité
 La publication sur le serveur IIS local requiert des privilèges d'administrateur car IIS doit être exécuté sous un compte Administrateur. Si un utilisateur sans privilège d’administrateur ouvre la publication de Service WCF, IIS n’est pas disponible en tant qu’un emplacement cible. Publication sur le système de fichiers, ou le FTP Site fonctionne sans privilège d’administrateur.

## <a name="see-also"></a>Voir aussi

- [Modèles Visual Studio WCF](../../../docs/framework/wcf/wcf-vs-templates.md)
- [WCF Service Host (WcfSvcHost.exe)](../../../docs/framework/wcf/wcf-service-host-wcfsvchost-exe.md)
- [Client test WCF (WcfTestClient.exe)](../../../docs/framework/wcf/wcf-test-client-wcftestclient-exe.md)