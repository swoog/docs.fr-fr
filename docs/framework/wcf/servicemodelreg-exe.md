---
title: Outil d'inscription ServiceModel (ServiceModelReg.exe)
ms.date: 03/30/2017
ms.assetid: 396ec5ae-e34f-4c64-a164-fcf50e86b6ac
ms.openlocfilehash: 5fab1a356cd035ed006bfe90d713e179907e0137
ms.sourcegitcommit: 15109844229ade1c6449f48f3834db1b26907824
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2018
---
# <a name="servicemodel-registration-tool-servicemodelregexe"></a><span data-ttu-id="c8d2d-102">Outil d'inscription ServiceModel (ServiceModelReg.exe)</span><span class="sxs-lookup"><span data-stu-id="c8d2d-102">ServiceModel Registration Tool (ServiceModelReg.exe)</span></span>
<span data-ttu-id="c8d2d-103">Cet outil en ligne de commande permet de gérer l'inscription des composants WCF et WF sur un ordinateur unique.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-103">This command-line tool provides the ability to manage the registration of WCF and WF components on a single machine.</span></span> <span data-ttu-id="c8d2d-104">Dans des circonstances normales vous n'avez pas à utiliser cet outil, car les composants WCF et WF sont configurés lors de l'installation.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-104">Under normal circumstances you should not need to use this tool as WCF and WF components are configured when installed.</span></span> <span data-ttu-id="c8d2d-105">Mais si vous rencontrez des problèmes avec l'activation de service, vous pouvez essayer d'inscrire les composants à l'aide de cet outil.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-105">But if you are experiencing problems with service activation, you can try to register the components using this tool.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c8d2d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8d2d-106">Syntax</span></span>  
  
```  
ServiceModelReg.exe[(-ia|-ua|-r)|((-i|-u) -c:<command>)] [-v|-q] [-nologo] [-?]  
```  
  
## <a name="remarks"></a><span data-ttu-id="c8d2d-107">Notes</span><span class="sxs-lookup"><span data-stu-id="c8d2d-107">Remarks</span></span>  
 <span data-ttu-id="c8d2d-108">Cet outil se trouve à l'emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="c8d2d-108">The tool can be found in the following location:</span></span>  
  
 <span data-ttu-id="c8d2d-109">%SystemRoot%\Microsoft.Net\Framework\v3.0\Windows Communication Foundation\\</span><span class="sxs-lookup"><span data-stu-id="c8d2d-109">%SystemRoot%\Microsoft.Net\Framework\v3.0\Windows Communication Foundation\\</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c8d2d-110">Lorsque l’outil d’inscription ServiceModel est exécuté [!INCLUDE[wv](../../../includes/wv-md.md)], le **des fonctionnalités Windows** boîte de dialogue peut ne pas refléter à qui le **Activation HTTP de Windows Communication Foundation** option sous **Microsoft .NET Framework 3.0** est activée.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-110">When the ServiceModel Registration Tool is run on [!INCLUDE[wv](../../../includes/wv-md.md)], the **Windows Features** dialog may not reflect that the **Windows Communication Foundation HTTP Activation** option under **Microsoft .NET Framework 3.0** is turned on.</span></span> <span data-ttu-id="c8d2d-111">Le **des fonctionnalités Windows** boîte de dialogue est accessible en cliquant sur **Démarrer**, puis cliquez sur **exécuter** , puis en tapant **OptionalFeatures**.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-111">The **Windows Features** dialog can be accessed by clicking **Start**, then click **Run** and then typing **OptionalFeatures**.</span></span>  
  
 <span data-ttu-id="c8d2d-112">Les tableaux suivants décrivent les options qui peuvent être utilisées avec ServiceModelReg.exe.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-112">The following tables describe the options that can be used with ServiceModelReg.exe.</span></span>  
  
|<span data-ttu-id="c8d2d-113">Option</span><span class="sxs-lookup"><span data-stu-id="c8d2d-113">Option</span></span>|<span data-ttu-id="c8d2d-114">Description</span><span class="sxs-lookup"><span data-stu-id="c8d2d-114">Description</span></span>|  
|------------|-----------------|  
|`-ia`|<span data-ttu-id="c8d2d-115">Installe les composants WCF et WF.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-115">Installs all WCF and WF components.</span></span>|  
|`-ua`|<span data-ttu-id="c8d2d-116">Désinstalle les composants WCF et WF.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-116">Uninstalls all WCF and WF components.</span></span>|  
|`-r`|<span data-ttu-id="c8d2d-117">Répare les composants WCF et WF.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-117">Repairs all WCF and WF components.</span></span>|  
|`-i`|<span data-ttu-id="c8d2d-118">Installe les composants WCF et WF spécifiés avec –c.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-118">Installs WCF and WF components specified with –c.</span></span>|  
|`-u`|<span data-ttu-id="c8d2d-119">Désinstalle les composants WCF et WF spécifiés avec –c.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-119">Uninstalls WCF and WF components specified with –c.</span></span>|  
|`-c`|<span data-ttu-id="c8d2d-120">Installe ou désinstalle un composant :</span><span class="sxs-lookup"><span data-stu-id="c8d2d-120">Installs or uninstalls a component:</span></span><br /><br /> <span data-ttu-id="c8d2d-121">-httpnamespace – réservation de Namespace HTTP</span><span class="sxs-lookup"><span data-stu-id="c8d2d-121">-   httpnamespace – HTTP Namespace Reservation</span></span><br /><span data-ttu-id="c8d2d-122">port - tcpportsharing – TCP service de partage</span><span class="sxs-lookup"><span data-stu-id="c8d2d-122">-   tcpportsharing – TCP port sharing service</span></span><br /><span data-ttu-id="c8d2d-123">service d’activation - tcpactivation – TCP (non pris en charge sur .NET 4 Client Profile)</span><span class="sxs-lookup"><span data-stu-id="c8d2d-123">-   tcpactivation – TCP activation service (unsupported on .NET 4 Client Profile)</span></span><br /><span data-ttu-id="c8d2d-124">service - namedpipeactivation – l’activation de canal nommé (non pris en charge sur .NET 4 Client Profile</span><span class="sxs-lookup"><span data-stu-id="c8d2d-124">-   namedpipeactivation – Named pipe activation service (unsupported on .NET 4 Client Profile</span></span><br /><span data-ttu-id="c8d2d-125">service d’activation - msmqactivation – MSMQ (non pris en charge sur .NET 4 Client Profile</span><span class="sxs-lookup"><span data-stu-id="c8d2d-125">-   msmqactivation – MSMQ activation service (unsupported on .NET 4 Client Profile</span></span><br /><span data-ttu-id="c8d2d-126">manifestes de suivi des événements - etw – ETW (Windows Vista ou version ultérieure)</span><span class="sxs-lookup"><span data-stu-id="c8d2d-126">-   etw – ETW event tracing manifests (Windows Vista or later)</span></span>|  
|`-q`|<span data-ttu-id="c8d2d-127">Mode silencieux (enregistrement des erreurs d'affichage uniquement)</span><span class="sxs-lookup"><span data-stu-id="c8d2d-127">Quiet mode (only display error logging)</span></span>|  
|`-v`|<span data-ttu-id="c8d2d-128">Mode documenté.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-128">Verbose mode.</span></span>|  
|`-nologo`|<span data-ttu-id="c8d2d-129">Supprime le message de copyright et de bannière.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-129">Suppresses the copyright and banner message.</span></span>|  
|`-?`|<span data-ttu-id="c8d2d-130">Affiche le texte de l'aide.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-130">Displays help text</span></span>|  
  
## <a name="fixing-the-fileloadexception-error"></a><span data-ttu-id="c8d2d-131">Résolution de l'erreur FileLoadException</span><span class="sxs-lookup"><span data-stu-id="c8d2d-131">Fixing the FileLoadException Error</span></span>  
 <span data-ttu-id="c8d2d-132">Si vous avez installé des versions antérieures de WCF sur votre ordinateur, vous risquez d’obtenir un `FileLoadFoundException` erreur lorsque vous exécutez l’outil ServiceModelReg pour enregistrer une nouvelle installation.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-132">If you installed previous versions of WCF on your machine, you may get a `FileLoadFoundException` error when you run the ServiceModelReg tool to register a new installation.</span></span> <span data-ttu-id="c8d2d-133">Cela peut se produire même si vous avez supprimé manuellement les fichiers de la précédente installation, mais que vous avez conservé les paramètres machine.config.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-133">This can happen even if you have manually removed files from the previous install, but left the machine.config settings intact.</span></span>  
  
 <span data-ttu-id="c8d2d-134">Le message d'erreur est semblable au message suivant.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-134">The error message is similar to the following.</span></span>  
  
```  
Error: System.IO.FileLoadException: Could not load file or assembly 'System.ServiceModel, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089' or one of its dependencies. The located assembly's manifest definition does not match the assembly reference. (Exception from HRESULT: 0x80131040)  
File name: 'System.ServiceModel, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089'  
```  
  
 <span data-ttu-id="c8d2d-135">Ce message d'erreur indique que l'assembly de la version 2.0.0.0 de System.ServiceModel a été installé par une version antérieure de CTP (Customer Technology Preview).</span><span class="sxs-lookup"><span data-stu-id="c8d2d-135">You should note from the error message that the System.ServiceModel Version 2.0.0.0 assembly was installed by an early Customer Technology Preview (CTP) release.</span></span> <span data-ttu-id="c8d2d-136">La version actuelle de l’assembly System.ServiceModel est la version 3.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-136">The current version of the System.ServiceModel assembly released is 3.0.0.0 instead.</span></span> <span data-ttu-id="c8d2d-137">Par conséquent, vous rencontrerez ce problème lorsque vous souhaitez installer la version officielle de WCF sur un ordinateur sur lequel une version CTP anticipée de WCF a été installée, mais pas complètement désinstallée.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-137">Therefore, this issue is encountered when you want to install the official WCF release on a machine where an early CTP release of WCF was installed, but not completely uninstalled.</span></span>  
  
 <span data-ttu-id="c8d2d-138">ServiceModelReg.exe ne peut pas nettoyer les entrées de versions antérieures ; il ne peut pas non plus enregistrer les entrées de la nouvelle version.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-138">ServiceModelReg.exe cannot clean up prior version entries, nor can it register the new version's entries.</span></span> <span data-ttu-id="c8d2d-139">La seule solution consiste à modifier manuellement le fichier machine.config. Vous trouverez ce fichier à l'emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="c8d2d-139">The only workaround is to manually edit machine.config. You can locate this file at the following location.</span></span>  
  
```  
%windir%\Microsoft.NET\Framework\v2.0.50727\config\machine.config   
```  
  
 <span data-ttu-id="c8d2d-140">Si vous exécutez WCF sur un ordinateur 64 bits, vous devez également modifier le même fichier à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-140">If you are running WCF on a 64-bit machine, you should also edit the same file at this location.</span></span>  
  
```  
%windir%\Microsoft.NET\Framework64\v2.0.50727\config\machine.config   
```  
  
 <span data-ttu-id="c8d2d-141">Localiser des nœuds XML dans ce fichier qui font référence à « System.ServiceModel, Version = 2.0.0.0 », supprimez les et les nœuds enfants.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-141">Locate any XML nodes in this file that refer to "System.ServiceModel, Version=2.0.0.0", delete them and any child nodes.</span></span> <span data-ttu-id="c8d2d-142">Enregistrez le fichier et réexécutez ServiceModelReg.exe afin de résoudre ce problème.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-142">Save the file and re-run ServiceModelReg.exe resolves this problem.</span></span>  
  
## <a name="examples"></a><span data-ttu-id="c8d2d-143">Exemples</span><span class="sxs-lookup"><span data-stu-id="c8d2d-143">Examples</span></span>  
 <span data-ttu-id="c8d2d-144">Les exemples suivants indiquent comment utiliser les options les plus courantes de l'outil ServiceModelReg.exe.</span><span class="sxs-lookup"><span data-stu-id="c8d2d-144">The following examples show how to use the most common options of the ServiceModelReg.exe tool.</span></span>  
  
```  
ServiceModelReg.exe -ia  
  Installs all components  
ServiceModelReg.exe -i -c:httpnamespace -c:etw  
  Installs HTTP namespace reservation and ETW manifests  
ServiceModelReg.exe -u -c:etw  
  Uninstalls ETW manifests  
ServiceModelReg.exe -r  
  Repairs an extended install  
```
