---
title: Outil Identité et accès pour Visual Studio 2012
ms.date: 03/30/2017
ms.assetid: 87b8f8f2-4074-44fd-9fd6-08278e877390
author: BrucePerlerMS
ms.openlocfilehash: 65d771b87cd3198848ffac387446abb17df18250
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61940411"
---
# <a name="identity-and-access-tool-for-visual-studio-2012"></a><span data-ttu-id="e1311-102">Outil Identité et accès pour Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="e1311-102">Identity and Access Tool for Visual Studio 2012</span></span>
<span data-ttu-id="e1311-103">Cette rubrique décrit le nouvel outil Identité et accès pour Visual Studio 11.</span><span class="sxs-lookup"><span data-stu-id="e1311-103">This topic describes the new Identity and Access Tool for Visual Studio 11.</span></span> <span data-ttu-id="e1311-104">Vous pouvez télécharger cet outil à partir de l’URL suivante : <https://go.microsoft.com/fwlink/?LinkID=245849> ou directement à partir de Visual Studio 11 en recherchant « identity » dans le Gestionnaire d’Extensions.</span><span class="sxs-lookup"><span data-stu-id="e1311-104">You can download this tool from the following URL: <https://go.microsoft.com/fwlink/?LinkID=245849> or directly from within Visual Studio 11 by searching for "identity" directly in the Extensions Manager.</span></span>  
  
 <span data-ttu-id="e1311-105">L'outil Identité et accès pour Visual Studio 11 offre une expérience très simplifiée du développement et met en avant les points suivants :</span><span class="sxs-lookup"><span data-stu-id="e1311-105">The Identity and Access Tool for Visual Studio 11 delivers a dramatically simplified development-time experience with the following highlights:</span></span>  
  
- <span data-ttu-id="e1311-106">À l'aide de ce nouvel outil, vous pouvez développer l'utilisation de types de projet d'application Web et IIS Express cibles.</span><span class="sxs-lookup"><span data-stu-id="e1311-106">Using the new tool, you can develop using web applications project types and target IIS express.</span></span>  
  
- <span data-ttu-id="e1311-107">Contrairement à l'authentification de protection générale uniquement, avec ce nouvel outil, vous pouvez spécifier la page de découverte/le contrôleur d'accueil de domaine local (ou tout autre point de terminaison qui gère l'expérience d'authentification dans votre application) et WIF configure toutes les demandes non authentifiées pour y accéder, au lieu de les rediriger vers STS.</span><span class="sxs-lookup"><span data-stu-id="e1311-107">Unlike with the blanket protection-only authentication, with the new tool, you can specify your local home realm discovery page/controller (or any other endpoint handling the authentication experience within your application) and WIF will configure all unauthenticated requests to go there, instead of redirecting them to the STS.</span></span>  
  
- <span data-ttu-id="e1311-108">L'outil inclut un service d'émission de jetons de sécurité (STS) de test qui s'exécute sur l'ordinateur local lorsque vous lancez une session de débogage.</span><span class="sxs-lookup"><span data-stu-id="e1311-108">The tool includes a test Security Token Service (STS) which runs on your local machine when you launch a debug session.</span></span> <span data-ttu-id="e1311-109">Par conséquent, vous n'avez plus à créer de projets STS personnalisés et à les manipuler pour obtenir les revendications dont vous avez besoin pour tester vos applications.</span><span class="sxs-lookup"><span data-stu-id="e1311-109">Therefore, you no longer need to create custom STS projects and tweak them in order to get the claims you need to test your applications.</span></span> <span data-ttu-id="e1311-110">Les types et les valeurs de revendication sont entièrement personnalisables.</span><span class="sxs-lookup"><span data-stu-id="e1311-110">The claim types and values are fully customizable.</span></span>  
  
- <span data-ttu-id="e1311-111">Vous pouvez modifier les paramètres courants directement via l'interface utilisateur de l'outil, sans avoir à modifier le fichier web.config.</span><span class="sxs-lookup"><span data-stu-id="e1311-111">You can modify common settings directly via the tool’s UI, without the need to edit web.config.</span></span>  
  
- <span data-ttu-id="e1311-112">Vous pouvez générer la fédération avec les services ADFS (Active Directory Federation Services) (AD FS) 2.0 (ou d'autres fournisseurs de WS-Federation) dans un même écran.</span><span class="sxs-lookup"><span data-stu-id="e1311-112">You can establish federation with Active Directory Federation Services (AD FS) 2.0 (or other WS-Federation providers) in a single screen.</span></span>  
  
- <span data-ttu-id="e1311-113">L’outil tire parti des fonctionnalités de Windows Azure Access Control Service (ACS) avec une simple liste de cases à cocher pour tous les fournisseurs d’identité que vous souhaitez utiliser : Facebook, Google, Live ID, Yahoo!, tout fournisseur OpenID et n’importe quel fournisseur de WS-Federation.</span><span class="sxs-lookup"><span data-stu-id="e1311-113">The tool leverages Windows Azure Access Control Service (ACS) capabilities with a simple list of checkboxes for all the identity providers that you want to use: Facebook, Google, Live ID, Yahoo!, any OpenID provider, and any WS-Federation provider.</span></span> <span data-ttu-id="e1311-114">Sélectionnez les fournisseurs d'identité, cliquez sur OK, puis sur F5, et votre application et ACS sont automatiquement configurés et votre application de test prend en charge ACS.</span><span class="sxs-lookup"><span data-stu-id="e1311-114">Select your identity providers, click OK, then F5, and both your application and ACS will be automatically configured and your test application will be ACS-aware.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e1311-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1311-115">See also</span></span>

- [<span data-ttu-id="e1311-116">Fonctionnalités WIF</span><span class="sxs-lookup"><span data-stu-id="e1311-116">WIF Features</span></span>](../../../docs/framework/security/wif-features.md)
