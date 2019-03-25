---
title: 'Tutoriel : Prise en main les applications Windows Communication Foundation'
description: Ces didacticiels fournit une introduction à la création d’applications WCF.
ms.date: 01/25/2019
helpviewer_keywords:
- WCF [WCF], get started
- Windows Communication Foundation [WCF], get started
- get started [WCF]
ms.assetid: df939177-73cb-4440-bd95-092a421516a1
ms.openlocfilehash: 66211cfcf2b742e43eccbefb2bc7c4bd1147b05b
ms.sourcegitcommit: 3630c2515809e6f4b7dbb697a3354efec105a5cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2019
ms.locfileid: "58408858"
---
# <a name="tutorial-get-started-with-windows-communication-foundation-applications"></a><span data-ttu-id="5542d-103">Tutoriel : Prise en main les applications Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="5542d-103">Tutorial: Get started with Windows Communication Foundation applications</span></span>
<span data-ttu-id="5542d-104">Les séries suivantes de didacticiels présentent pour le Windows Communication Foundation (WCF) expérience de programmation.</span><span class="sxs-lookup"><span data-stu-id="5542d-104">The following series of tutorials introduce you to the Windows Communication Foundation (WCF) programming experience.</span></span> <span data-ttu-id="5542d-105">Utilisation de ces didacticiels dans l’ordre vous donnera une compréhension de base des étapes requises pour créer des applications WCF.</span><span class="sxs-lookup"><span data-stu-id="5542d-105">Working through these tutorials in order will give you an introductory understanding of the steps required to create WCF applications.</span></span> <span data-ttu-id="5542d-106">Une fois que vous avez terminé, vous disposerez d’un service WCF en cours d’exécution et un client WCF qui appelle le service.</span><span class="sxs-lookup"><span data-stu-id="5542d-106">After you finish, you'll have a running WCF service and a WCF client that calls the service.</span></span> 

<span data-ttu-id="5542d-107">Ce didacticiel suppose que vous utilisez Visual Studio comme environnement de développement.</span><span class="sxs-lookup"><span data-stu-id="5542d-107">The tutorial assumes you're using Visual Studio as the development environment.</span></span> <span data-ttu-id="5542d-108">Si vous utilisez un autre environnement de développement, ignorer les instructions spécifiques à Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5542d-108">If you're using another development environment, ignore the Visual Studio-specific instructions.</span></span> 

<span data-ttu-id="5542d-109">Pour plus d’exemples d’applications WCF que vous pouvez télécharger et exécuter, consultez [exemples Windows Communication Foundation](samples/index.md).</span><span class="sxs-lookup"><span data-stu-id="5542d-109">For sample WCF applications that you can download and run, see [Windows Communication Foundation samples](samples/index.md).</span></span> <span data-ttu-id="5542d-110">Pour une introduction aux exemples, consultez [exemple de mise en route](samples/getting-started-sample.md).</span><span class="sxs-lookup"><span data-stu-id="5542d-110">For an introduction to the samples, see [Getting started sample](samples/getting-started-sample.md).</span></span>

<span data-ttu-id="5542d-111">Pour plus d’informations sur la création de services et les clients, consultez [programmation WCF de base](basic-wcf-programming.md).</span><span class="sxs-lookup"><span data-stu-id="5542d-111">For more in-depth information about creating services and clients, see [Basic WCF programming](basic-wcf-programming.md).</span></span>

## <a name="wcf-tutorials"></a><span data-ttu-id="5542d-112">Didacticiels WCF</span><span class="sxs-lookup"><span data-stu-id="5542d-112">WCF tutorials</span></span>

<span data-ttu-id="5542d-113">Les trois premiers didacticiels décrivent comment définir un contrat de service WCF, comment l’implémenter et comment héberger.</span><span class="sxs-lookup"><span data-stu-id="5542d-113">The first three tutorials describe how to define a WCF service contract, how to implement it, and how to host it.</span></span> <span data-ttu-id="5542d-114">Le service que vous créez est auto-hébergé dans une application console.</span><span class="sxs-lookup"><span data-stu-id="5542d-114">The service that you create is self-hosted within a console application.</span></span> <span data-ttu-id="5542d-115">Vous pouvez également héberger des services sous Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="5542d-115">You can also host services under Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="5542d-116">Pour plus d'informations, voir [Procédure : Héberger un Service WCF dans IIS](feature-details/how-to-host-a-wcf-service-in-iis.md).</span><span class="sxs-lookup"><span data-stu-id="5542d-116">For more information, see [How to: Host a WCF Service in IIS](feature-details/how-to-host-a-wcf-service-in-iis.md).</span></span> <span data-ttu-id="5542d-117">Bien que vous utilisez le code pour configurer le service dans le didacticiel, vous pouvez également [configurer des services au sein d’un fichier de configuration](configuring-services-using-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="5542d-117">Although you use code to configure the service in the tutorial, you can also [configure services within a configuration file](configuring-services-using-configuration-files.md).</span></span> 

- [<span data-ttu-id="5542d-118">Tutoriel : Définir un contrat de service</span><span class="sxs-lookup"><span data-stu-id="5542d-118">Tutorial: Define a service contract</span></span>](how-to-define-a-wcf-service-contract.md)

    <span data-ttu-id="5542d-119">Vous créez un contrat WCF avec une interface définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5542d-119">You create a WCF contract with a user-defined interface.</span></span> <span data-ttu-id="5542d-120">Ce contrat définit les fonctionnalités exposées par le service.</span><span class="sxs-lookup"><span data-stu-id="5542d-120">This contract defines the functionality that the service exposes.</span></span>

- [<span data-ttu-id="5542d-121">Tutoriel : Implémenter un contrat de service</span><span class="sxs-lookup"><span data-stu-id="5542d-121">Tutorial: Implement a service contract</span></span>](how-to-implement-a-wcf-contract.md)

    <span data-ttu-id="5542d-122">Une fois que vous définissez un contrat, vous devez l’implémenter avec une classe de service.</span><span class="sxs-lookup"><span data-stu-id="5542d-122">After you define a contract, you must implement it with a service class.</span></span>

- [<span data-ttu-id="5542d-123">Tutoriel : Héberger et exécuter un service de base</span><span class="sxs-lookup"><span data-stu-id="5542d-123">Tutorial: Host and run a basic service</span></span>](how-to-host-and-run-a-basic-wcf-service.md)

    <span data-ttu-id="5542d-124">Configurer un point de terminaison pour le service et héberger le service dans une application console.</span><span class="sxs-lookup"><span data-stu-id="5542d-124">Configure an endpoint for the service and host the service in a console application.</span></span> <span data-ttu-id="5542d-125">Pour un service devienne actif, vous devez le configurer et héberger dans un environnement d’exécution.</span><span class="sxs-lookup"><span data-stu-id="5542d-125">For a service to become active, you must configure it and host it within a run-time environment.</span></span> <span data-ttu-id="5542d-126">Cet environnement d’exécution crée le service et contrôle son contexte et la durée de vie.</span><span class="sxs-lookup"><span data-stu-id="5542d-126">This run-time environment creates the service and controls its context and lifetime.</span></span>

<span data-ttu-id="5542d-127">Les deux didacticiels expliquent comment créer, configurer et utiliser une application cliente pour appeler les opérations du service expose.</span><span class="sxs-lookup"><span data-stu-id="5542d-127">The next two tutorials describe how to create, configure, and use a client application to call the operations the service exposes.</span></span> <span data-ttu-id="5542d-128">Les services publient les métadonnées qui définissent les informations dont une application cliente a besoin pour communiquer avec le service.</span><span class="sxs-lookup"><span data-stu-id="5542d-128">Services publish metadata that define the information a client application needs to communicate with the service.</span></span> <span data-ttu-id="5542d-129">Visual Studio automatise le processus d’accès à ces métadonnées et l’utilise pour construire l’application cliente pour le service.</span><span class="sxs-lookup"><span data-stu-id="5542d-129">Visual Studio automates the process of accessing this metadata and uses it to construct the client application for the service.</span></span> <span data-ttu-id="5542d-130">Si vous décidez de ne pas utiliser Visual Studio, vous pouvez utiliser la [outil ServiceModel Metadata Utility (*Svcutil.exe*)](servicemodel-metadata-utility-tool-svcutil-exe.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="5542d-130">If you decide not to use Visual Studio, you can use the [ServiceModel Metadata Utility tool (*Svcutil.exe*)](servicemodel-metadata-utility-tool-svcutil-exe.md) instead.</span></span>

- [<span data-ttu-id="5542d-131">Tutoriel : Créer un client</span><span class="sxs-lookup"><span data-stu-id="5542d-131">Tutorial: Create a client</span></span>](how-to-create-a-wcf-client.md)

    <span data-ttu-id="5542d-132">Récupérer les métadonnées pour la création d’un proxy de client WCF à partir d’un service WCF.</span><span class="sxs-lookup"><span data-stu-id="5542d-132">Retrieve metadata for creating a WCF client proxy from a WCF service.</span></span> <span data-ttu-id="5542d-133">Récupérer des métadonnées à l’aide de Visual Studio pour ajouter une référence de service, ou vous pouvez utiliser l’outil ServiceModel Metadata Utility.</span><span class="sxs-lookup"><span data-stu-id="5542d-133">You retrieve metadata by using Visual Studio to add a service reference or you can use the ServiceModel Metadata Utility tool.</span></span> <span data-ttu-id="5542d-134">Vous spécifiez le point de terminaison que le client utilise pour accéder au service.</span><span class="sxs-lookup"><span data-stu-id="5542d-134">You specify the endpoint that the client uses to access the service.</span></span>

- [<span data-ttu-id="5542d-135">Tutoriel : Utiliser un client</span><span class="sxs-lookup"><span data-stu-id="5542d-135">Tutorial: Use a client</span></span>](how-to-use-a-wcf-client.md)

    <span data-ttu-id="5542d-136">Utiliser le proxy client WCF pour appeler les opérations de service.</span><span class="sxs-lookup"><span data-stu-id="5542d-136">Use the WCF client proxy to call the service operations.</span></span>

## <a name="reference"></a><span data-ttu-id="5542d-137">Référence</span><span class="sxs-lookup"><span data-stu-id="5542d-137">Reference</span></span>

- <xref:System.ServiceModel.ServiceContractAttribute>
- <xref:System.ServiceModel.OperationContractAttribute>

## <a name="see-also"></a><span data-ttu-id="5542d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5542d-138">See also</span></span>

- [<span data-ttu-id="5542d-139">Vue d’ensemble conceptuelle</span><span class="sxs-lookup"><span data-stu-id="5542d-139">Conceptual overview</span></span>](conceptual-overview.md)
- [<span data-ttu-id="5542d-140">Guide de la documentation</span><span class="sxs-lookup"><span data-stu-id="5542d-140">Guide to the documentation</span></span>](guide-to-the-documentation.md)
- [<span data-ttu-id="5542d-141">Nouveautés de Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="5542d-141">What is Windows Communication Foundation</span></span>](whats-wcf.md)
- [<span data-ttu-id="5542d-142">Informations sur les fonctionnalités WCF</span><span class="sxs-lookup"><span data-stu-id="5542d-142">WCF feature details</span></span>](feature-details/index.md)
- [<span data-ttu-id="5542d-143">Cycle de vie de programmation base</span><span class="sxs-lookup"><span data-stu-id="5542d-143">Basic programming lifecycle</span></span>](basic-programming-lifecycle.md)
- [<span data-ttu-id="5542d-144">Génération de clients</span><span class="sxs-lookup"><span data-stu-id="5542d-144">Building clients</span></span>](building-clients.md)
- [<span data-ttu-id="5542d-145">Programmation de WCF de base</span><span class="sxs-lookup"><span data-stu-id="5542d-145">Basic WCF programming</span></span>](basic-wcf-programming.md)
- [<span data-ttu-id="5542d-146">Guide pratique pour Créer un contrat duplex</span><span class="sxs-lookup"><span data-stu-id="5542d-146">How to: Create a duplex contract</span></span>](feature-details/how-to-create-a-duplex-contract.md)
- [<span data-ttu-id="5542d-147">Guide pratique pour Access services avec un contrat duplex</span><span class="sxs-lookup"><span data-stu-id="5542d-147">How to: Access services with a duplex contract</span></span>](feature-details/how-to-access-services-with-a-duplex-contract.md)
- [<span data-ttu-id="5542d-148">ServiceModel Metadata Utility tool (Svcutil.exe)</span><span class="sxs-lookup"><span data-stu-id="5542d-148">ServiceModel Metadata Utility tool (Svcutil.exe)</span></span>](servicemodel-metadata-utility-tool-svcutil-exe.md)
- [<span data-ttu-id="5542d-149">Guide pratique pour Utiliser Svcutil.exe pour télécharger des documents de métadonnées</span><span class="sxs-lookup"><span data-stu-id="5542d-149">How to: Use Svcutil.exe to download metadata documents</span></span>](feature-details/how-to-use-svcutil-exe-to-download-metadata-documents.md)
- [<span data-ttu-id="5542d-150">Guide pratique pour Publier les métadonnées pour un service à l’aide d’un fichier de configuration</span><span class="sxs-lookup"><span data-stu-id="5542d-150">How to: Publish metadata for a service using a configuration file</span></span>](feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)
- [<span data-ttu-id="5542d-151">À l’aide de liaisons pour configurer les clients et services</span><span class="sxs-lookup"><span data-stu-id="5542d-151">Using bindings to configure services and clients</span></span>](using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="5542d-152">Getting started, exemple</span><span class="sxs-lookup"><span data-stu-id="5542d-152">Getting started sample</span></span>](samples/getting-started-sample.md)
- [<span data-ttu-id="5542d-153">Exemples Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="5542d-153">Windows Communication Foundation samples</span></span>](samples/index.md)
- [<span data-ttu-id="5542d-154">Auto-hébergement</span><span class="sxs-lookup"><span data-stu-id="5542d-154">Self-Host</span></span>](samples/self-host.md)


