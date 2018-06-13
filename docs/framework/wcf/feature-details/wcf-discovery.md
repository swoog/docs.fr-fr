---
title: Discovery WCF
ms.date: 03/30/2017
helpviewer_keywords:
- WCF [WCF], discovery
- Windows Communication Foundation [WCF], discovery
- discovery [WCF]
ms.assetid: 462c4913-f388-45a9-9042-28ae96a4e735
ms.openlocfilehash: 175f79096d2bbda81a602d38e027d5a6d871fa12
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33497956"
---
# <a name="wcf-discovery"></a><span data-ttu-id="2a060-102">Discovery WCF</span><span class="sxs-lookup"><span data-stu-id="2a060-102">WCF Discovery</span></span>
<span data-ttu-id="2a060-103">Windows Communication Foundation (WCF) fournit la prise en charge pour activer les services d’être détectables pendant l’exécution d’une façon interopérable à l’aide du protocole WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="2a060-103">Windows Communication Foundation (WCF) provides support to enable services to be discoverable at runtime in an interoperable way using the WS-Discovery protocol.</span></span> <span data-ttu-id="2a060-104">Les services WCF peuvent annoncer leur disponibilité pour le réseau à l’aide d’un message de multidiffusion ou à un serveur proxy de découverte.</span><span class="sxs-lookup"><span data-stu-id="2a060-104">WCF services can announce their availability to the network using a multicast message or to a discovery proxy server.</span></span> <span data-ttu-id="2a060-105">Les applications clientes peuvent rechercher sur le réseau ou dans un serveur proxy de découverte des services qui répondent à un jeu de critères.</span><span class="sxs-lookup"><span data-stu-id="2a060-105">Client applications can search the network or a discovery proxy server to find services that meet a set of criteria.</span></span> <span data-ttu-id="2a060-106">Les rubriques de cette section donnent une vue d’ensemble et décrivent en détail le modèle de programmation pour cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="2a060-106">The topics in this section provide an overview and describe the programming model for this feature in detail.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="2a060-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="2a060-107">In This Section</span></span>  
 [<span data-ttu-id="2a060-108">Vue d’ensemble de la découverte WCF</span><span class="sxs-lookup"><span data-stu-id="2a060-108">WCF Discovery Overview</span></span>](../../../../docs/framework/wcf/feature-details/wcf-discovery-overview.md)  
 <span data-ttu-id="2a060-109">Fournit une vue d’ensemble de la prise en charge de WS-Discovery fournie par WCF.</span><span class="sxs-lookup"><span data-stu-id="2a060-109">Provides an overview of WS-Discovery support provided by WCF.</span></span>  
  
 [<span data-ttu-id="2a060-110">Modèle objet de découverte WCF</span><span class="sxs-lookup"><span data-stu-id="2a060-110">WCF Discovery Object Model</span></span>](../../../../docs/framework/wcf/feature-details/wcf-discovery-object-model.md)  
 <span data-ttu-id="2a060-111">Décrit les classes du modèle objet et l'extensibilité de la prise en charge de WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="2a060-111">Describes the classes in the object model and extensibility of WS-Discovery support.</span></span>  
  
 [<span data-ttu-id="2a060-112">Guide pratique pour ajouter la détectabilité par programmation à un service et un client WCF</span><span class="sxs-lookup"><span data-stu-id="2a060-112">How to: Programmatically Add Discoverability to a WCF Service and Client</span></span>](../../../../docs/framework/wcf/feature-details/how-to-programmatically-add-discoverability-to-a-wcf-service-and-client.md)  
 <span data-ttu-id="2a060-113">Montre comment rendre un service Windows Communication Foundation (WCF) détectable.</span><span class="sxs-lookup"><span data-stu-id="2a060-113">Shows how to make a Windows Communication Foundation (WCF) service discoverable.</span></span>  
  
 [<span data-ttu-id="2a060-114">Implémentation d’un proxy de découverte</span><span class="sxs-lookup"><span data-stu-id="2a060-114">Implementing a Discovery Proxy</span></span>](../../../../docs/framework/wcf/feature-details/implementing-a-discovery-proxy.md)  
 <span data-ttu-id="2a060-115">Décrit les étapes nécessaires pour implémenter un proxy de découverte, un service détectable qui s'enregistre avec le proxy de découverte et un client qui utilise le proxy de découverte pour rechercher le service détectable.</span><span class="sxs-lookup"><span data-stu-id="2a060-115">Describes the steps required to implement a discovery proxy, a discoverable service that registers with the discovery proxy, and a client that uses the discovery proxy to find the discoverable service.</span></span>  
  
 [<span data-ttu-id="2a060-116">Gestion de version de découverte</span><span class="sxs-lookup"><span data-stu-id="2a060-116">Discovery Versioning</span></span>](../../../../docs/framework/wcf/feature-details/discovery-versioning.md)  
 <span data-ttu-id="2a060-117">Donne une vue d’ensemble d’une implémentation prototype de nouvelles fonctionnalités de découverte.</span><span class="sxs-lookup"><span data-stu-id="2a060-117">Provides a brief overview of a prototype implementation of some new discovery features.</span></span> <span data-ttu-id="2a060-118">Elle donne également une vue d'ensemble de la manière de sélectionner la version de découverte à utiliser.</span><span class="sxs-lookup"><span data-stu-id="2a060-118">It also gives an overview on how to select the discovery version to use.</span></span>  
  
 [<span data-ttu-id="2a060-119">Configuration de la découverte dans un fichier de configuration</span><span class="sxs-lookup"><span data-stu-id="2a060-119">Configuring Discovery in a Configuration File</span></span>](../../../../docs/framework/wcf/feature-details/configuring-discovery-in-a-configuration-file.md)  
 <span data-ttu-id="2a060-120">Indique comment configurer la découverte dans la configuration.</span><span class="sxs-lookup"><span data-stu-id="2a060-120">Shows how to configure Discovery in configuration.</span></span>  
  
 [<span data-ttu-id="2a060-121">Utilisation du canal client de découverte</span><span class="sxs-lookup"><span data-stu-id="2a060-121">Using the Discovery Client Channel</span></span>](../../../../docs/framework/wcf/feature-details/using-the-discovery-client-channel.md)  
 <span data-ttu-id="2a060-122">Montre comment utiliser un canal Client de découverte lors de l’écriture d’une application cliente WCF.</span><span class="sxs-lookup"><span data-stu-id="2a060-122">Shows how to use a Discovery Client Channel when writing a WCF client application.</span></span>
