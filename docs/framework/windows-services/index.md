---
title: Développement des applications de service Windows
ms.date: 03/30/2017
helpviewer_keywords:
- ServiceInstaller class, Windows Service applications
- Service class, Windows Service applications
- Windows Service applications
- Windows NT services
- ServiceProcessInstaller class, Windows Service applications
- services
- .NET applications, Windows applications
ms.assetid: ba72d648-9553-4849-b829-069ad5ea014b
author: ghogen
manager: douge
ms.openlocfilehash: 2c7fb148b96d5ff9804bcb0bb7c842c475c0f117
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "43886407"
---
# <a name="developing-windows-service-applications"></a><span data-ttu-id="c97bd-102">Développement des applications de service Windows</span><span class="sxs-lookup"><span data-stu-id="c97bd-102">Developing Windows Service Applications</span></span>
<span data-ttu-id="c97bd-103">Utilisez Microsoft Visual Studio ou le SDK Microsoft [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)] pour créer facilement des services. En fait, vous créez une application qui est installée comme service.</span><span class="sxs-lookup"><span data-stu-id="c97bd-103">Using Microsoft Visual Studio or the Microsoft [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)] SDK, you can easily create services by creating an application that is installed as a service.</span></span> <span data-ttu-id="c97bd-104">Ce type d’application est appelé un service Windows.</span><span class="sxs-lookup"><span data-stu-id="c97bd-104">This type of application is called a Windows service.</span></span> <span data-ttu-id="c97bd-105">Grâce aux fonctionnalités du framework, vous pouvez non seulement créer des services, les installer, les démarrer et les arrêter, mais aussi contrôler leur comportement.</span><span class="sxs-lookup"><span data-stu-id="c97bd-105">With framework features, you can create services, install them, and start, stop, and otherwise control their behavior.</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="c97bd-106">Le modèle de service Windows pour C++ n’était pas inclus dans Visual Studio 2010.</span><span class="sxs-lookup"><span data-stu-id="c97bd-106">The Windows service template for C++ was not included in Visual Studio 2010.</span></span> <span data-ttu-id="c97bd-107">Pour créer un service Windows, vous pouvez soit créer un service dans du code managé en Visual C# ou Visual Basic, celui-ci pouvant interagir avec le code C++ existant si nécessaire, soit créer un service Windows en C++ natif à l’aide de [l’Assistant Projet ATL](/cpp/atl/reference/atl-project-wizard).</span><span class="sxs-lookup"><span data-stu-id="c97bd-107">To create a Windows service, you can either create a service in managed code in Visual C# or Visual Basic, which could interoperate with existing C++ code if required, or you can create a Windows service in native C++ by using the [ATL Project Wizard](/cpp/atl/reference/atl-project-wizard).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="c97bd-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="c97bd-108">In This Section</span></span>  
 [<span data-ttu-id="c97bd-109">Introduction aux applications de service Windows</span><span class="sxs-lookup"><span data-stu-id="c97bd-109">Introduction to Windows Service Applications</span></span>](../../../docs/framework/windows-services/introduction-to-windows-service-applications.md)  
 <span data-ttu-id="c97bd-110">Fournit une vue d’ensemble des applications de service Windows, de la durée de vie d’un service, et des différences entre les applications de service et les autres types de projets courants.</span><span class="sxs-lookup"><span data-stu-id="c97bd-110">Provides an overview of Windows service applications, the lifetime of a service, and how service applications differ from other common project types.</span></span>  
  
 [<span data-ttu-id="c97bd-111">Procédure pas à pas : création d’une application de service Windows dans le Concepteur de composants</span><span class="sxs-lookup"><span data-stu-id="c97bd-111">Walkthrough: Creating a Windows Service Application in the Component Designer</span></span>](../../../docs/framework/windows-services/walkthrough-creating-a-windows-service-application-in-the-component-designer.md)  
 <span data-ttu-id="c97bd-112">Fournit un exemple de création d’un service en Visual Basic et Visual C#.</span><span class="sxs-lookup"><span data-stu-id="c97bd-112">Provides an example of creating a service in Visual Basic and Visual C#.</span></span>  
  
 [<span data-ttu-id="c97bd-113">Architecture de programmation d’une application de service</span><span class="sxs-lookup"><span data-stu-id="c97bd-113">Service Application Programming Architecture</span></span>](../../../docs/framework/windows-services/service-application-programming-architecture.md)  
 <span data-ttu-id="c97bd-114">Explique les éléments de langage utilisés dans la programmation d’un service.</span><span class="sxs-lookup"><span data-stu-id="c97bd-114">Explains the language elements used in service programming.</span></span>  
  
 [<span data-ttu-id="c97bd-115">Guide pratique pour créer des services Windows</span><span class="sxs-lookup"><span data-stu-id="c97bd-115">How to: Create Windows Services</span></span>](../../../docs/framework/windows-services/how-to-create-windows-services.md)  
 <span data-ttu-id="c97bd-116">Décrit le processus de création et de configuration de services Windows à l’aide du modèle de projet de service Windows.</span><span class="sxs-lookup"><span data-stu-id="c97bd-116">Describes the process of creating and configuring Windows services using the Windows service project template.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="c97bd-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c97bd-117">Related Sections</span></span>  
 <xref:System.ServiceProcess.ServiceBase>  
 <span data-ttu-id="c97bd-118">Décrit les principales fonctionnalités de la classe <xref:System.ServiceProcess.ServiceBase> qui est utilisée pour créer des services.</span><span class="sxs-lookup"><span data-stu-id="c97bd-118">Describes the major features of the <xref:System.ServiceProcess.ServiceBase> class, which is used to create services.</span></span>  
  
 <xref:System.ServiceProcess.ServiceProcessInstaller>  
 <span data-ttu-id="c97bd-119">Décrit les fonctionnalités de la classe <xref:System.ServiceProcess.ServiceProcessInstaller>. Celle-ci, utilisée avec la classe <xref:System.ServiceProcess.ServiceInstaller>, permet d’installer et de désinstaller vos services.</span><span class="sxs-lookup"><span data-stu-id="c97bd-119">Describes the features of the <xref:System.ServiceProcess.ServiceProcessInstaller> class, which is used along with the <xref:System.ServiceProcess.ServiceInstaller> class to install and uninstall your services.</span></span>  
  
 <xref:System.ServiceProcess.ServiceInstaller>  
 <span data-ttu-id="c97bd-120">Décrit les fonctionnalités de la classe <xref:System.ServiceProcess.ServiceInstaller>. Celle-ci, utilisée avec la classe <xref:System.ServiceProcess.ServiceProcessInstaller>, permet d’installer et de désinstaller votre service.</span><span class="sxs-lookup"><span data-stu-id="c97bd-120">Describes the features of the <xref:System.ServiceProcess.ServiceInstaller> class, which is used along with the <xref:System.ServiceProcess.ServiceProcessInstaller> class to install and uninstall your service.</span></span>  
  
 [<span data-ttu-id="c97bd-121">NIB Création de projets à partir de modèles</span><span class="sxs-lookup"><span data-stu-id="c97bd-121">NIB Creating Projects from Templates</span></span>](https://msdn.microsoft.com/library/7c36d86a-6b79-4480-8228-0f925f1204b2)  
 <span data-ttu-id="c97bd-122">Décrit les types de projets utilisés dans ce chapitre et comment faire votre choix.</span><span class="sxs-lookup"><span data-stu-id="c97bd-122">Describes the projects types used in this chapter and how to choose between them.</span></span>
