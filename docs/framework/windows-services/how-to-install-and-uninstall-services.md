---
title: Guide pratique pour installer et désinstaller des services Windows
ms.date: 02/05/2019
helpviewer_keywords:
- Windows Service applications, deploying
- services, uninstalling
- services, installing
- installing Windows Services
- uninstalling applications, apps, Windows services
- installation, Windows services
- uninstalling Windows services
- installutil.exe tool
ms.assetid: c89c5169-f567-4305-9d62-db31a1de5481
author: ghogen
ms.openlocfilehash: 43b5ad2f346406897e8bcbcce5660a6c9524f9af
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55826256"
---
# <a name="how-to-install-and-uninstall-windows-services"></a><span data-ttu-id="2bcc2-102">Guide pratique pour installer et désinstaller des services Windows</span><span class="sxs-lookup"><span data-stu-id="2bcc2-102">How to: Install and uninstall Windows services</span></span>
<span data-ttu-id="2bcc2-103">Si vous développez un service Windows à l’aide du .NET Framework, vous pouvez installer rapidement votre application de service à l’aide de l’utilitaire en ligne de commande [*InstallUtil.exe*](../tools/installutil-exe-installer-tool.md).</span><span class="sxs-lookup"><span data-stu-id="2bcc2-103">If you’re developing a Windows service with the .NET Framework, you can quickly install your service app by using the [*InstallUtil.exe*](../tools/installutil-exe-installer-tool.md) command-line utility.</span></span> <span data-ttu-id="2bcc2-104">Les développeurs désireux de mettre à la disposition de certains utilisateurs un service Windows qu’ils peuvent installer et désinstaller doivent utiliser InstallShield.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-104">Developers who want to release a Windows service that users can install and uninstall should use InstallShield.</span></span> <span data-ttu-id="2bcc2-105">Pour plus d’informations, consultez [Créer un package d’installation (client Windows)](https://docs.microsoft.com/visualstudio/deployment/deploying-applications-services-and-components#create-an-installer-package-windows-client).</span><span class="sxs-lookup"><span data-stu-id="2bcc2-105">For more information, see [Create an installer package (Windows client)](https://docs.microsoft.com/visualstudio/deployment/deploying-applications-services-and-components#create-an-installer-package-windows-client).</span></span>
  
> [!WARNING]
>  <span data-ttu-id="2bcc2-106">Si vous voulez désinstaller un service de votre ordinateur, ne suivez pas les étapes décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-106">If you want to uninstall a service from your computer, don’t follow the steps in this article.</span></span> <span data-ttu-id="2bcc2-107">Au lieu de cela, déterminez quel programme ou package logiciel a installé le service, puis choisissez **Applications** dans les paramètres pour désinstaller ce programme.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-107">Instead, find out which program or software package installed the service, and then choose **Apps** in Settings to uninstall that program.</span></span> <span data-ttu-id="2bcc2-108">Notez que de nombreux services font partie intégrante de Windows. Si vous les supprimez, vous pouvez rendre le système instable.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-108">Note that many services are integral parts of Windows; if you remove them, you might cause system instability.</span></span>  
  
 <span data-ttu-id="2bcc2-109">Pour utiliser les étapes décrites dans cet article, vous devez d’abord ajouter un programme d’installation de service à votre service Windows.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-109">To use the steps in this article, you first need to add a service installer to your Windows service.</span></span> <span data-ttu-id="2bcc2-110">Pour plus d’informations, consultez [Procédure pas à pas : Création d’une application de service Windows](../windows-services/walkthrough-creating-a-windows-service-application-in-the-component-designer.md).</span><span class="sxs-lookup"><span data-stu-id="2bcc2-110">For more information, see [Walkthrough: Creating a Windows service app](../windows-services/walkthrough-creating-a-windows-service-application-in-the-component-designer.md).</span></span>  
  
 <span data-ttu-id="2bcc2-111">Vous ne pouvez pas exécuter les projets de service Windows directement à partir de l’environnement de développement Visual Studio en appuyant sur F5.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-111">You can't run Windows service projects directly from the Visual Studio development environment by pressing F5.</span></span> <span data-ttu-id="2bcc2-112">Avant de pouvoir exécuter le projet, vous devez installer le service dans le projet.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-112">Before you can run the project, you must install the service in the project.</span></span>  
  
> [!TIP]
>  <span data-ttu-id="2bcc2-113">Vous pouvez utiliser l’**Explorateur de serveurs** pour vérifier que vous avez bien installé ou désinstallé le service.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-113">You can use **Server Explorer** to verify that you've installed or uninstalled your service.</span></span> <span data-ttu-id="2bcc2-114">Pour plus d’informations, consultez [Guide pratique pour utiliser l’Explorateur de serveurs dans Visual Studio](https://support.microsoft.com/help/316649/how-to-use-the-server-explorer-in-visual-studio-net-and-visual-studio).</span><span class="sxs-lookup"><span data-stu-id="2bcc2-114">For more information, see [How to use Server Explorer in Visual Studio](https://support.microsoft.com/help/316649/how-to-use-the-server-explorer-in-visual-studio-net-and-visual-studio).</span></span>
  
### <a name="install-your-service-manually"></a><span data-ttu-id="2bcc2-115">Installer votre service manuellement</span><span class="sxs-lookup"><span data-stu-id="2bcc2-115">Install your service manually</span></span>  
  
1.  <span data-ttu-id="2bcc2-116">Dans le menu **Démarrer**, sélectionnez le répertoire **Visual Studio \<*version*>**, puis **Invite de commandes développeur pour VS \<*version*>**.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-116">From the **Start** menu, select the **Visual Studio \<*version*>** directory, then select **Developer Command Prompt for VS \<*version*>**.</span></span>
  
     <span data-ttu-id="2bcc2-117">L’invite de commandes développeur pour Visual Studio s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-117">The Developer Command Prompt for Visual Studio appears.</span></span> 
  
2.  <span data-ttu-id="2bcc2-118">Accédez au répertoire dans lequel se trouve le fichier exécutable compilé de votre projet.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-118">Access the directory where your project's compiled executable file is located.</span></span>  
  
3.  <span data-ttu-id="2bcc2-119">Exécutez *InstallUtil.exe* à partir de l’invite de commandes avec le fichier exécutable de votre projet en guise de paramètre :</span><span class="sxs-lookup"><span data-stu-id="2bcc2-119">Run *InstallUtil.exe* from the command prompt with your project's executable as a parameter:</span></span>  
  
    ```console
    installutil <yourproject>.exe  
    ```  

     <span data-ttu-id="2bcc2-120">Si vous utilisez l’invite de commandes développeur pour Visual Studio, *InstallUtil.exe* doit se trouver dans le chemin système.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-120">If you’re using the Developer Command Prompt for Visual Studio, *InstallUtil.exe* should be on the system path.</span></span> <span data-ttu-id="2bcc2-121">Si ce n’est pas le cas, vous pouvez l’ajouter au chemin ou utiliser le chemin complet pour l’appeler.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-121">Otherwise, you can add it to the path, or use the fully qualified path to invoke it.</span></span> <span data-ttu-id="2bcc2-122">Cet outil est installé avec le .NET Framework dans *%WINDIR%\Microsoft.NET\Framework[64]\\<version_framework>*.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-122">This tool is installed with the .NET Framework in *%WINDIR%\Microsoft.NET\Framework[64]\\<framework_version>*.</span></span>
     
     <span data-ttu-id="2bcc2-123">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="2bcc2-123">For example:</span></span>
     - <span data-ttu-id="2bcc2-124">Pour la version 32 bits de .NET Framework 4 ou 4.5 et ultérieur, si votre répertoire d’installation Windows est *C:\Windows*, le chemin par défaut est *C:\Windows\Microsoft.NET\Framework\v4.0.30319\InstallUtil.exe*.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-124">For the 32-bit version of the .NET Framework 4 or 4.5 and later, if your Windows installation directory is *C:\Windows*, the default path is *C:\Windows\Microsoft.NET\Framework\v4.0.30319\InstallUtil.exe*.</span></span>
     - <span data-ttu-id="2bcc2-125">Pour la version 64 bits de .NET Framework 4 ou 4.5 et ultérieur, le chemin par défaut est *C:\Windows\Microsoft.NET\Framework64\v4.0.30319\InstallUtil.exe*.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-125">For the 64-bit version of the .NET Framework 4 or 4.5 and later, the default path is *C:\Windows\Microsoft.NET\Framework64\v4.0.30319\InstallUtil.exe*.</span></span>
  
### <a name="uninstall-your-service-manually"></a><span data-ttu-id="2bcc2-126">Désinstaller votre service manuellement</span><span class="sxs-lookup"><span data-stu-id="2bcc2-126">Uninstall your service manually</span></span>  
  
1. <span data-ttu-id="2bcc2-127">Dans le menu **Démarrer**, sélectionnez le répertoire **Visual Studio \<*version*>**, puis **Invite de commandes développeur pour VS \<*version*>**.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-127">From the **Start** menu, select the **Visual Studio \<*version*>** directory, then select **Developer Command Prompt for VS \<*version*>**.</span></span>
  
     <span data-ttu-id="2bcc2-128">L’invite de commandes développeur pour Visual Studio s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-128">The Developer Command Prompt for Visual Studio appears.</span></span>  
  
2.  <span data-ttu-id="2bcc2-129">Exécutez *InstallUtil.exe* à partir de l’invite de commandes avec la sortie de votre projet en guise de paramètre :</span><span class="sxs-lookup"><span data-stu-id="2bcc2-129">Run *InstallUtil.exe* from the command prompt with your project's output as a parameter:</span></span>  
  
    ```console  
    installutil /u <yourproject>.exe  
    ```  
  
3. <span data-ttu-id="2bcc2-130">Après avoir supprimé l’exécutable d’un service, il est possible que ce service soit toujours présent dans le Registre.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-130">After the executable for a service is deleted, the service might still be present in the registry.</span></span> <span data-ttu-id="2bcc2-131">Si c’est le cas, utilisez la commande [sc delete](/windows-server/administration/windows-commands/sc-delete) pour supprimer l’entrée du service dans le Registre.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-131">If that's the case, use the command [sc delete](/windows-server/administration/windows-commands/sc-delete) to remove the entry for the service from the registry.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2bcc2-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2bcc2-132">See also</span></span>
- [<span data-ttu-id="2bcc2-133">Introduction aux applications de service Windows</span><span class="sxs-lookup"><span data-stu-id="2bcc2-133">Introduction to Windows service applications</span></span>](../windows-services/introduction-to-windows-service-applications.md)
- [<span data-ttu-id="2bcc2-134">Guide pratique pour créer des services Windows</span><span class="sxs-lookup"><span data-stu-id="2bcc2-134">How to: Create Windows services</span></span>](../windows-services/how-to-create-windows-services.md)
- [<span data-ttu-id="2bcc2-135">Guide pratique pour ajouter des programmes d’installation à votre application de service</span><span class="sxs-lookup"><span data-stu-id="2bcc2-135">How to: Add installers to your service application</span></span>](../windows-services/how-to-add-installers-to-your-service-application.md)
- [<span data-ttu-id="2bcc2-136">Installutil.exe (outil Installer)</span><span class="sxs-lookup"><span data-stu-id="2bcc2-136">Installutil.exe (Installer tool)</span></span>](../tools/installutil-exe-installer-tool.md)
