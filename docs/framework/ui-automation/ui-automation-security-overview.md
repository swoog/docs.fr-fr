---
title: Vue d'ensemble de la sécurité UI Automation
ms.date: 03/30/2017
helpviewer_keywords:
- UI Automation, security model
- security model, UI Automation
ms.assetid: 1d853695-973c-48ae-b382-4132ae702805
author: Xansky
ms.author: mhopkins
manager: markl
ms.openlocfilehash: f55112c5eead082eae10aa50590b915f5049d5a6
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43855163"
---
# <a name="ui-automation-security-overview"></a><span data-ttu-id="2ceb4-102">Vue d'ensemble de la sécurité UI Automation</span><span class="sxs-lookup"><span data-stu-id="2ceb4-102">UI Automation Security Overview</span></span>
> [!NOTE]
>  <span data-ttu-id="2ceb4-103">Cette documentation s'adresse aux développeurs .NET Framework qui souhaitent utiliser les classes [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] managées définies dans l'espace de noms <xref:System.Windows.Automation>.</span><span class="sxs-lookup"><span data-stu-id="2ceb4-103">This documentation is intended for .NET Framework developers who want to use the managed [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] classes defined in the <xref:System.Windows.Automation> namespace.</span></span> <span data-ttu-id="2ceb4-104">Pour plus d’informations sur [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], consultez [Windows Automation API : UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).</span><span class="sxs-lookup"><span data-stu-id="2ceb4-104">For the latest information about [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], see [Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).</span></span>  
  
 <span data-ttu-id="2ceb4-105">Cette vue d'ensemble décrit le modèle de sécurité pour [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] dans [!INCLUDE[TLA#tla_winvista](../../../includes/tlasharptla-winvista-md.md)].</span><span class="sxs-lookup"><span data-stu-id="2ceb4-105">This overview describes the security model for [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] in [!INCLUDE[TLA#tla_winvista](../../../includes/tlasharptla-winvista-md.md)].</span></span>  
  
<a name="User_Account_Control"></a>   
## <a name="user-account-control"></a><span data-ttu-id="2ceb4-106">Contrôle de compte d'utilisateur</span><span class="sxs-lookup"><span data-stu-id="2ceb4-106">User Account Control</span></span>  
 <span data-ttu-id="2ceb4-107">La sécurité est un objectif majeur de [!INCLUDE[TLA#tla_winvista](../../../includes/tlasharptla-winvista-md.md)] . Parmi les innovations apportées, citons pour les utilisateurs la possibilité d'exécuter le système d'exploitation sous un compte d'utilisateur standard (non-administrateur) sans être forcément bloqués par des applications et des services en cours d'exécution qui nécessitent des privilèges plus élevés.</span><span class="sxs-lookup"><span data-stu-id="2ceb4-107">Security is a major focus of [!INCLUDE[TLA#tla_winvista](../../../includes/tlasharptla-winvista-md.md)] and among the innovations is the ability for users to run as standard (non-administrator) users without necessarily being blocked from running applications and services that require higher privileges.</span></span>  
  
 <span data-ttu-id="2ceb4-108">Dans [!INCLUDE[TLA2#tla_winvista](../../../includes/tla2sharptla-winvista-md.md)], la plupart des applications sont fournies avec un jeton standard ou administratif.</span><span class="sxs-lookup"><span data-stu-id="2ceb4-108">In [!INCLUDE[TLA2#tla_winvista](../../../includes/tla2sharptla-winvista-md.md)], most applications are supplied with either a standard or an administrative token.</span></span> <span data-ttu-id="2ceb4-109">Si une application ne peut pas être identifiée en tant qu'application administrative, elle est lancée par défaut en tant qu'application standard.</span><span class="sxs-lookup"><span data-stu-id="2ceb4-109">If an application cannot be identified as an administrative application, it is launched as a standard application by default.</span></span> <span data-ttu-id="2ceb4-110">Avant le lancement d'une application identifiée en tant qu'application administrative, [!INCLUDE[TLA2#tla_winvista](../../../includes/tla2sharptla-winvista-md.md)] invite l'utilisateur à consentir l'exécution de l'application avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="2ceb4-110">Before an application identified as administrative can be launched, [!INCLUDE[TLA2#tla_winvista](../../../includes/tla2sharptla-winvista-md.md)] prompts the user for consent to run the application as elevated.</span></span> <span data-ttu-id="2ceb4-111">L'invite de consentement s'affiche par défaut, même si l'utilisateur est membre du groupe Administrateurs local. Cela est dû au fait que les administrateurs sont considérés comme des utilisateurs standard jusqu'à ce qu'une application ou un composant système nécessitant des informations d'identification d'administration demande l'autorisation de s'exécuter.</span><span class="sxs-lookup"><span data-stu-id="2ceb4-111">The consent prompt is displayed by default, even if the user is a member of the local Administrators group, because administrators run as standard users until an application or system component that requires administrative credentials requests permission to run.</span></span>  
  
<a name="Tasks_Requiring_Higher_Privileges"></a>   
## <a name="tasks-requiring-higher-privileges"></a><span data-ttu-id="2ceb4-112">Tâches nécessitant des privilèges plus élevés</span><span class="sxs-lookup"><span data-stu-id="2ceb4-112">Tasks Requiring Higher Privileges</span></span>  
 <span data-ttu-id="2ceb4-113">Quand un utilisateur tente d'effectuer une tâche qui nécessite des privilèges d'administrateur, [!INCLUDE[TLA2#tla_winvista](../../../includes/tla2sharptla-winvista-md.md)] affiche une boîte de dialogue qui invite l'utilisateur à donner son consentement pour continuer.</span><span class="sxs-lookup"><span data-stu-id="2ceb4-113">When a user attempts to perform a task that requires administrative privileges, [!INCLUDE[TLA2#tla_winvista](../../../includes/tla2sharptla-winvista-md.md)] presents a dialog box asking the user for consent to continue.</span></span> <span data-ttu-id="2ceb4-114">Cette boîte de dialogue bénéficie d'une protection contre les communications interprocessus, ce qui empêche les logiciels malveillants de simuler l'entrée de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2ceb4-114">This dialog box is protected from cross-process communication, so that malicious software cannot simulate user input.</span></span> <span data-ttu-id="2ceb4-115">De même, d'autres processus ne sont normalement pas autorisés à accéder à l'écran d'ouverture de session sur le Bureau.</span><span class="sxs-lookup"><span data-stu-id="2ceb4-115">Similarly, the desktop logon screen cannot normally be accessed by other processes.</span></span>  
  
 <span data-ttu-id="2ceb4-116">Les clients UI Automation doivent communiquer avec d’autres processus, certains d’entre eux pouvant être exécutés à un niveau de privilège supérieur.</span><span class="sxs-lookup"><span data-stu-id="2ceb4-116">UI Automation clients must communicate with other processes, some of them perhaps running at a higher privilege level.</span></span> <span data-ttu-id="2ceb4-117">Les clients peuvent aussi avoir besoin d'accéder à des boîtes de dialogue système qui ne sont normalement pas visibles à d'autres processus.</span><span class="sxs-lookup"><span data-stu-id="2ceb4-117">Clients also might need access to the system dialog boxes that are not normally visible to other processes.</span></span> <span data-ttu-id="2ceb4-118">Par conséquent, les clients [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] doivent être approuvés par le système et s'exécuter avec des privilèges spéciaux.</span><span class="sxs-lookup"><span data-stu-id="2ceb4-118">Therefore, [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] clients must be trusted by the system, and must run with special privileges.</span></span>  
  
 <span data-ttu-id="2ceb4-119">Pour avoir l'autorisation de communiquer avec des applications exécutées à un niveau de privilège plus élevé, les applications doivent être signées.</span><span class="sxs-lookup"><span data-stu-id="2ceb4-119">To be trusted to communicate with applications running at a higher privilege level, applications must be signed.</span></span>  
  
<a name="Manifest_Files"></a>   
## <a name="manifest-files"></a><span data-ttu-id="2ceb4-120">Fichiers manifeste</span><span class="sxs-lookup"><span data-stu-id="2ceb4-120">Manifest Files</span></span>  
 <span data-ttu-id="2ceb4-121">Pour accéder à l' [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)]du système protégé, les applications doivent être générées avec un fichier manifeste contenant un attribut spécial.</span><span class="sxs-lookup"><span data-stu-id="2ceb4-121">To gain access to the protected system [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)], applications must be built with a manifest file that includes a special attribute in the manifest file.</span></span> <span data-ttu-id="2ceb4-122">Cet attribut `uiAccess` est inclus dans la balise `requestedExecutionLevel` , comme suit :</span><span class="sxs-lookup"><span data-stu-id="2ceb4-122">This `uiAccess` attribute is included in the `requestedExecutionLevel` tag, as follows:</span></span>  
  
 `<trustInfo xmlns="urn:0073chemas-microsoft-com:asm.v3">`  
  
 `<security>`  
  
 `<requestedPrivileges>`  
  
 `<requestedExecutionLevel`  
  
 `level="highestAvailable"`  
  
 `UIAccess="true" />`  
  
 `</requestedPrivileges>`  
  
 `</security>`  
  
 `</trustInfo>`  
  
 <span data-ttu-id="2ceb4-123">Dans ce code, la valeur de l'attribut `level` n'est qu'un exemple.</span><span class="sxs-lookup"><span data-stu-id="2ceb4-123">The value of the `level` attribute in this code is an example only.</span></span>  
  
 <span data-ttu-id="2ceb4-124">`UIAccess` a la valeur « false » par défaut ; autrement dit, si l'attribut est omis ou qu'il n'existe aucun manifeste pour l'assembly, l'application ne pourra pas accéder à l' [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)]protégée.</span><span class="sxs-lookup"><span data-stu-id="2ceb4-124">`UIAccess` is "false" by default; that is, if the attribute is omitted, or if there is no manifest for the assembly, the application will not be able to gain access to protected [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)].</span></span>  
  
 <span data-ttu-id="2ceb4-125">Pour plus d’informations sur [!INCLUDE[TLA#tla_longhorn2](../../../includes/tlasharptla-longhorn2-md.md)] sécurité, la signature des applications et la création de manifestes d’assembly, consultez « Développeur meilleures pratiques et recommandations pour Applications dans un moins privilégié environnement » sur [MSDN](https://msdn.microsoft.com/library/default.asp?url=/library/dnlong/html/AccProtVista.asp).</span><span class="sxs-lookup"><span data-stu-id="2ceb4-125">For more information on [!INCLUDE[TLA#tla_longhorn2](../../../includes/tlasharptla-longhorn2-md.md)] security, on signing applications, and on creating assembly manifests, see "Developer Best Practices and Guidelines for Applications in a Least Privileged Environment" on  [MSDN](https://msdn.microsoft.com/library/default.asp?url=/library/dnlong/html/AccProtVista.asp).</span></span>
