---
title: Configuration des services Internet (IIS) 7.0 pour Windows Communication Foundation
ms.date: 03/30/2017
ms.assetid: 1050d395-092e-44d3-b4ba-66be3b039ffb
ms.openlocfilehash: 13fd068f7a058a0fbf4e15fc99a8de91671fb2d5
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43563057"
---
# <a name="configuring-internet-information-services-70-for-windows-communication-foundation"></a><span data-ttu-id="ff0dd-102">Configuration des services Internet (IIS) 7.0 pour Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="ff0dd-102">Configuring Internet Information Services 7.0 for Windows Communication Foundation</span></span>

<span data-ttu-id="ff0dd-103">Les services Internet (IIS) 7.0 sont conçus de manière modulaire vous permettant ainsi d'installer uniquement les composants dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="ff0dd-103">Internet Information Services (IIS) 7.0 has a modular design that allows you to selectively install components that are required.</span></span> <span data-ttu-id="ff0dd-104">Leur conception s'appuie sur la nouvelle technologie multi-composant orientée manifeste, utilisée pour la première fois dans [!INCLUDE[wv](../../../../includes/wv-md.md)].</span><span class="sxs-lookup"><span data-stu-id="ff0dd-104">This design is based on the new manifest-driven componentization technology introduced in [!INCLUDE[wv](../../../../includes/wv-md.md)].</span></span> <span data-ttu-id="ff0dd-105">Il existe plus de 40 composants autonomes d’IIS 7.0 qui peut être installé indépendamment.</span><span class="sxs-lookup"><span data-stu-id="ff0dd-105">There are more than 40 standalone feature components of IIS 7.0 that can be installed independently.</span></span> <span data-ttu-id="ff0dd-106">Cela permet aux professionnels de l'informatique de personnaliser plus facilement leur installation en fonction de leurs besoins.</span><span class="sxs-lookup"><span data-stu-id="ff0dd-106">This allows IT professionals to easily customize the installation as required.</span></span> <span data-ttu-id="ff0dd-107">Cette rubrique explique comment configurer IIS 7.0 pour une utilisation avec Windows Communication Foundation (WCF) et déterminer quels composants sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="ff0dd-107">This topic discusses how to configure IIS 7.0 for use with Windows Communication Foundation (WCF) and determine which components are required.</span></span>

## <a name="minimal-installation-installing-was"></a><span data-ttu-id="ff0dd-108">Installation minimale : installation du service WAS</span><span class="sxs-lookup"><span data-stu-id="ff0dd-108">Minimal Installation: Installing WAS</span></span>
 <span data-ttu-id="ff0dd-109">L’installation minimale de l’ensemble du package IIS 7.0 est d’installer le Service de l’Activation des processus Windows (WAS).</span><span class="sxs-lookup"><span data-stu-id="ff0dd-109">The minimal installation of the whole IIS 7.0 package is to install the Windows Process Activation Service (WAS).</span></span> <span data-ttu-id="ff0dd-110">A été est une fonctionnalité autonome et il est la seule fonctionnalité à partir d’IIS 7.0 qui est disponible pour tous les [!INCLUDE[wv](../../../../includes/wv-md.md)] les systèmes d’exploitation (Édition Familiale Basique, Édition familiale Premium, Professionnel et Édition intégrale et entreprise).</span><span class="sxs-lookup"><span data-stu-id="ff0dd-110">WAS is a standalone feature and it is the only feature from the IIS 7.0 that is available for all [!INCLUDE[wv](../../../../includes/wv-md.md)] operating systems (Home Basic, Home Premium, Business, and Ultimate and Enterprise).</span></span>

 <span data-ttu-id="ff0dd-111">À partir du Panneau de configuration, cliquez sur **programmes** puis cliquez sur **ou désactiver des fonctionnalités Windows activer** sous **programmes et fonctionnalités**, le composant WAS s’affiche dans la liste, comme dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="ff0dd-111">From the Control Panel, click **Programs** and then click **Turn Windows features on or off** which is listed under **Programs and Features**, the WAS component is shown in the list as in the following illustration.</span></span>

 <span data-ttu-id="ff0dd-112">![Activer la boîte de dialogue désactiver ou de fonctionnalités sur](../../../../docs/framework/wcf/feature-details/media/wcfc-turnfeaturesonoroffs.gif "wcfc_TurnFeaturesOnOrOffs")</span><span class="sxs-lookup"><span data-stu-id="ff0dd-112">![Turn Features On or Off Dialog](../../../../docs/framework/wcf/feature-details/media/wcfc-turnfeaturesonoroffs.gif "wcfc_TurnFeaturesOnOrOffs")</span></span>

 <span data-ttu-id="ff0dd-113">Cette fonctionnalité intègre les sous-composants suivants :</span><span class="sxs-lookup"><span data-stu-id="ff0dd-113">This feature has the following sub-components:</span></span>

-   <span data-ttu-id="ff0dd-114">Environnement .NET</span><span class="sxs-lookup"><span data-stu-id="ff0dd-114">.NET Environment</span></span>

-   <span data-ttu-id="ff0dd-115">Interfaces API de configuration</span><span class="sxs-lookup"><span data-stu-id="ff0dd-115">Configuration APIs</span></span>

-   <span data-ttu-id="ff0dd-116">Modèle de processus</span><span class="sxs-lookup"><span data-stu-id="ff0dd-116">Process Model</span></span>

 <span data-ttu-id="ff0dd-117">Si vous sélectionnez le nœud racine WAS, le **modèle de processus** sous-nœud est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="ff0dd-117">If you select the root node of WAS, only the **Process Model** sub-node is checked by default.</span></span> <span data-ttu-id="ff0dd-118">Remarque : dans le cadre de la présente installation, seul le service WAS est installé car la prise en charge d’un serveur web n’est pas assurée.</span><span class="sxs-lookup"><span data-stu-id="ff0dd-118">Please note that with this installation you are only installing WAS, because there is no support for a Web server.</span></span>

 <span data-ttu-id="ff0dd-119">Pour WCF ou n’importe quel travail d’application ASP.NET, consultez le **environnement .NET** case à cocher.</span><span class="sxs-lookup"><span data-stu-id="ff0dd-119">To make WCF or any ASP.NET application work, check the **.NET Environment** checkbox.</span></span> <span data-ttu-id="ff0dd-120">Cela signifie que tous les composants du service WAS sont requises pour que WCF et ASP.NET pour un fonctionnement optimal.</span><span class="sxs-lookup"><span data-stu-id="ff0dd-120">This means that all of WAS components are required to make WCF and ASP.NET to work well.</span></span> <span data-ttu-id="ff0dd-121">Ces composants sont automatiquement activés dès lors que l'un d'entre eux est installé.</span><span class="sxs-lookup"><span data-stu-id="ff0dd-121">These are automatically checked once you install any of those components.</span></span>

## <a name="iis-70-default-installation"></a><span data-ttu-id="ff0dd-122">IIS 7.0 : installation par défaut</span><span class="sxs-lookup"><span data-stu-id="ff0dd-122">IIS 7.0: Default Installation</span></span>
 <span data-ttu-id="ff0dd-123">En vérifiant la **Internet Information Services** fonctionnalité, certains nœuds secondaires sont automatiquement vérifiés comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="ff0dd-123">By checking the **Internet Information Services** feature, some of the sub-nodes are automatically checked as shown in the following illustration.</span></span>

 <span data-ttu-id="ff0dd-124">![Paramètres par défaut pour les fonctionnalités d’IIS 7.0](../../../../docs/framework/wcf/feature-details/media/wcfc-turningfeaturesonoroff2.gif "wcfc_TurningFeaturesOnOrOff2")</span><span class="sxs-lookup"><span data-stu-id="ff0dd-124">![Default settings for IIS 7.0 features](../../../../docs/framework/wcf/feature-details/media/wcfc-turningfeaturesonoroff2.gif "wcfc_TurningFeaturesOnOrOff2")</span></span>

 <span data-ttu-id="ff0dd-125">Il s’agit de l’installation par défaut d’IIS 7.0.</span><span class="sxs-lookup"><span data-stu-id="ff0dd-125">This is the default installation of IIS 7.0.</span></span> <span data-ttu-id="ff0dd-126">Avec cette installation, vous pouvez utiliser IIS 7.0 pour fournir du contenu statique (par exemple, des pages HTML et d’autres contenus).</span><span class="sxs-lookup"><span data-stu-id="ff0dd-126">With this installation, you can use IIS 7.0 to service static content (such as HTML pages and other content).</span></span> <span data-ttu-id="ff0dd-127">Toutefois, vous ne pouvez pas exécuter les applications ASP.NET et CGI ou héberger des services WCF.</span><span class="sxs-lookup"><span data-stu-id="ff0dd-127">However, you cannot run ASP.NET or CGI applications or host WCF services.</span></span>

## <a name="iis-70-installation-with-aspnet-support"></a><span data-ttu-id="ff0dd-128">IIS 7.0 : installation avec prise en charge ASP.NET</span><span class="sxs-lookup"><span data-stu-id="ff0dd-128">IIS 7.0: Installation with ASP.NET Support</span></span>
 <span data-ttu-id="ff0dd-129">Vous devez installer ASP.NET pour utiliser ASP.NET sur IIS 7.0.</span><span class="sxs-lookup"><span data-stu-id="ff0dd-129">You must install ASP.NET to make ASP.NET work on IIS 7.0.</span></span> <span data-ttu-id="ff0dd-130">Après avoir vérifié **ASP.NET**, votre écran doit ressembler à l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="ff0dd-130">After checking **ASP.NET**, your screen should look like the following illustration.</span></span>

 <span data-ttu-id="ff0dd-131">![Asp.NET les paramètres requis](../../../../docs/framework/wcf/feature-details/media/wcfc-trunfeaturesonoroff3s.gif "wcfc_TrunFeaturesOnOrOFf3s")</span><span class="sxs-lookup"><span data-stu-id="ff0dd-131">![Asp.NET required settings](../../../../docs/framework/wcf/feature-details/media/wcfc-trunfeaturesonoroff3s.gif "wcfc_TrunFeaturesOnOrOFf3s")</span></span>

 <span data-ttu-id="ff0dd-132">Il s’agit de l’environnement minimal pour les applications WCF et ASP.NET fonctionne dans IIS 7.0.</span><span class="sxs-lookup"><span data-stu-id="ff0dd-132">This is the minimal environment for both WCF and ASP.NET applications to work in IIS 7.0.</span></span>

## <a name="iis-70-installation-with-iis-60-compatibility-components"></a><span data-ttu-id="ff0dd-133">IIS 7.0 : installation avec les composants de compatibilité IIS 6.0</span><span class="sxs-lookup"><span data-stu-id="ff0dd-133">IIS 7.0: Installation with IIS 6.0 Compatibility Components</span></span>
 <span data-ttu-id="ff0dd-134">Lors de l’installation d’IIS 7.0 sur un système avec Visual Studio 2005 ou certaines autres scripts d’automatisation ou certains outils (tels que Adsutil.vbs) qui configurent des applications virtuelles qui utilisent les API de métabase IIS 6.0, vérifiez que vous vérifiez l’IIS 6.0 **outils de script**.</span><span class="sxs-lookup"><span data-stu-id="ff0dd-134">When installing IIS 7.0 on a system with Visual Studio 2005 or some other automation scripts or tools (such as Adsutil.vbs) that configure virtual applications that use IIS 6.0 Metabase API, ensure that you check the IIS 6.0 **Scripting Tools**.</span></span> <span data-ttu-id="ff0dd-135">Cette procédure vérifie automatiquement les autres sous-nœuds d’IIS 6.0 **Management Compatibility**.</span><span class="sxs-lookup"><span data-stu-id="ff0dd-135">This automatically checks the other sub-nodes of IIS 6.0 **Management Compatibility**.</span></span> <span data-ttu-id="ff0dd-136">L’illustration suivante montre l’écran une fois cette opération est effectuée :</span><span class="sxs-lookup"><span data-stu-id="ff0dd-136">The following illustration shows the screen after this is done:</span></span>

 <span data-ttu-id="ff0dd-137">![Paramètres de compatibilité IIS 6.0 Management](../../../../docs/framework/wcf/feature-details/media/scfc-turnfeaturesonoroff5s.gif "scfc_TurnFeaturesOnOrOff5s")</span><span class="sxs-lookup"><span data-stu-id="ff0dd-137">![IIS 6.0 Management Compatibility Settings](../../../../docs/framework/wcf/feature-details/media/scfc-turnfeaturesonoroff5s.gif "scfc_TurnFeaturesOnOrOff5s")</span></span>

 <span data-ttu-id="ff0dd-138">Avec cette installation, vous disposez de tous les éléments requis pour utiliser les fonctionnalités IIS 7.0, ASP.NET et WCF et les exemples disponibles sur le Web.</span><span class="sxs-lookup"><span data-stu-id="ff0dd-138">With this installation, you have everything required to use IIS 7.0, ASP.NET and WCF features and samples available on the Web.</span></span>

## <a name="request-limits"></a><span data-ttu-id="ff0dd-139">Limites de la demande</span><span class="sxs-lookup"><span data-stu-id="ff0dd-139">Request Limits</span></span>
 <span data-ttu-id="ff0dd-140">Sur [!INCLUDE[wv](../../../../includes/wv-md.md)] avec IIS 7, la valeur par défaut des paramètres `maxUri` et `maxQueryStringSize` a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="ff0dd-140">On [!INCLUDE[wv](../../../../includes/wv-md.md)] with IIS 7 the default value of the `maxUri` and `maxQueryStringSize` settings have been changed.</span></span> <span data-ttu-id="ff0dd-141">Par défaut, le filtrage de demande dans IIS 7.0 autorise une URL d'une longueur de 4096 caractères et une longueur de chaîne de 2048 caractères.</span><span class="sxs-lookup"><span data-stu-id="ff0dd-141">By default, request filtering in IIS 7.0 allows a URL length of 4096 characters and a query string length of 2048 characters.</span></span> <span data-ttu-id="ff0dd-142">Pour modifier ces valeurs par défaut, ajoutez l'élément XML suivant au fichier App.config.</span><span class="sxs-lookup"><span data-stu-id="ff0dd-142">To change these defaults add the following XML to your App.config file.</span></span>

 `<system.webServer>`

 `<security>`

 `<requestFiltering>`

 `<requestLimits maxUrl="8192" maxQueryString="8192" />`

 `</requestFiltering>`

 `</security>`

 `</system.webServer>`

## <a name="see-also"></a><span data-ttu-id="ff0dd-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff0dd-143">See Also</span></span>

- [<span data-ttu-id="ff0dd-144">Architecture d’activation WAS</span><span class="sxs-lookup"><span data-stu-id="ff0dd-144">WAS Activation Architecture</span></span>](../../../../docs/framework/wcf/feature-details/was-activation-architecture.md)
- [<span data-ttu-id="ff0dd-145">Configuration du service WAS pour une utilisation avec WCF</span><span class="sxs-lookup"><span data-stu-id="ff0dd-145">Configuring WAS for Use with WCF</span></span>](../../../../docs/framework/wcf/feature-details/configuring-the-wpa--service-for-use-with-wcf.md)
- [<span data-ttu-id="ff0dd-146">Guide pratique pour installer et configurer des composants d’activation WCF</span><span class="sxs-lookup"><span data-stu-id="ff0dd-146">How to: Install and Configure WCF Activation Components</span></span>](../../../../docs/framework/wcf/feature-details/how-to-install-and-configure-wcf-activation-components.md)
- [<span data-ttu-id="ff0dd-147">Fonctionnalités d’hébergement de Windows Server App Fabric</span><span class="sxs-lookup"><span data-stu-id="ff0dd-147">Windows Server App Fabric Hosting Features</span></span>](https://go.microsoft.com/fwlink/?LinkId=201276)
