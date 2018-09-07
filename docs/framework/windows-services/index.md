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
# <a name="developing-windows-service-applications"></a>Développement des applications de service Windows
Utilisez Microsoft Visual Studio ou le SDK Microsoft [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)] pour créer facilement des services. En fait, vous créez une application qui est installée comme service. Ce type d’application est appelé un service Windows. Grâce aux fonctionnalités du framework, vous pouvez non seulement créer des services, les installer, les démarrer et les arrêter, mais aussi contrôler leur comportement.  
  
> [!WARNING]
>  Le modèle de service Windows pour C++ n’était pas inclus dans Visual Studio 2010. Pour créer un service Windows, vous pouvez soit créer un service dans du code managé en Visual C# ou Visual Basic, celui-ci pouvant interagir avec le code C++ existant si nécessaire, soit créer un service Windows en C++ natif à l’aide de [l’Assistant Projet ATL](/cpp/atl/reference/atl-project-wizard).  
  
## <a name="in-this-section"></a>Dans cette section  
 [Introduction aux applications de service Windows](../../../docs/framework/windows-services/introduction-to-windows-service-applications.md)  
 Fournit une vue d’ensemble des applications de service Windows, de la durée de vie d’un service, et des différences entre les applications de service et les autres types de projets courants.  
  
 [Procédure pas à pas : création d’une application de service Windows dans le Concepteur de composants](../../../docs/framework/windows-services/walkthrough-creating-a-windows-service-application-in-the-component-designer.md)  
 Fournit un exemple de création d’un service en Visual Basic et Visual C#.  
  
 [Architecture de programmation d’une application de service](../../../docs/framework/windows-services/service-application-programming-architecture.md)  
 Explique les éléments de langage utilisés dans la programmation d’un service.  
  
 [Guide pratique pour créer des services Windows](../../../docs/framework/windows-services/how-to-create-windows-services.md)  
 Décrit le processus de création et de configuration de services Windows à l’aide du modèle de projet de service Windows.  
  
## <a name="related-sections"></a>Rubriques connexes  
 <xref:System.ServiceProcess.ServiceBase>  
 Décrit les principales fonctionnalités de la classe <xref:System.ServiceProcess.ServiceBase> qui est utilisée pour créer des services.  
  
 <xref:System.ServiceProcess.ServiceProcessInstaller>  
 Décrit les fonctionnalités de la classe <xref:System.ServiceProcess.ServiceProcessInstaller>. Celle-ci, utilisée avec la classe <xref:System.ServiceProcess.ServiceInstaller>, permet d’installer et de désinstaller vos services.  
  
 <xref:System.ServiceProcess.ServiceInstaller>  
 Décrit les fonctionnalités de la classe <xref:System.ServiceProcess.ServiceInstaller>. Celle-ci, utilisée avec la classe <xref:System.ServiceProcess.ServiceProcessInstaller>, permet d’installer et de désinstaller votre service.  
  
 [NIB Création de projets à partir de modèles](https://msdn.microsoft.com/library/7c36d86a-6b79-4480-8228-0f925f1204b2)  
 Décrit les types de projets utilisés dans ce chapitre et comment faire votre choix.
