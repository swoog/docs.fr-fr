---
title: Vue d'ensemble de la sécurité UI Automation
ms.date: 03/30/2017
helpviewer_keywords:
- UI Automation, security model
- security model, UI Automation
ms.assetid: 1d853695-973c-48ae-b382-4132ae702805
author: Xansky
ms.author: mhopkins
ms.openlocfilehash: d86293e2d8fedab1d9ed8a5dc0ad59bd1f386d93
ms.sourcegitcommit: bef803e2025642df39f2f1e046767d89031e0304
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56303866"
---
# <a name="ui-automation-security-overview"></a>Vue d'ensemble de la sécurité UI Automation
> [!NOTE]
>  Cette documentation s'adresse aux développeurs .NET Framework qui souhaitent utiliser les classes [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] managées définies dans l'espace de noms <xref:System.Windows.Automation>. Pour plus d’informations sur [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], consultez [Windows Automation API : UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).  
  
 Cette vue d'ensemble décrit le modèle de sécurité pour [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] dans [!INCLUDE[TLA#tla_winvista](../../../includes/tlasharptla-winvista-md.md)].  
  
<a name="User_Account_Control"></a>   
## <a name="user-account-control"></a>Contrôle de compte d'utilisateur  
 La sécurité est un objectif majeur de [!INCLUDE[TLA#tla_winvista](../../../includes/tlasharptla-winvista-md.md)] . Parmi les innovations apportées, citons pour les utilisateurs la possibilité d'exécuter le système d'exploitation sous un compte d'utilisateur standard (non-administrateur) sans être forcément bloqués par des applications et des services en cours d'exécution qui nécessitent des privilèges plus élevés.  
  
 Dans [!INCLUDE[TLA2#tla_winvista](../../../includes/tla2sharptla-winvista-md.md)], la plupart des applications sont fournies avec un jeton standard ou administratif. Si une application ne peut pas être identifiée en tant qu'application administrative, elle est lancée par défaut en tant qu'application standard. Avant le lancement d'une application identifiée en tant qu'application administrative, [!INCLUDE[TLA2#tla_winvista](../../../includes/tla2sharptla-winvista-md.md)] invite l'utilisateur à consentir l'exécution de l'application avec des privilèges élevés. L'invite de consentement s'affiche par défaut, même si l'utilisateur est membre du groupe Administrateurs local. Cela est dû au fait que les administrateurs sont considérés comme des utilisateurs standard jusqu'à ce qu'une application ou un composant système nécessitant des informations d'identification d'administration demande l'autorisation de s'exécuter.  
  
<a name="Tasks_Requiring_Higher_Privileges"></a>   
## <a name="tasks-requiring-higher-privileges"></a>Tâches nécessitant des privilèges plus élevés  
 Quand un utilisateur tente d'effectuer une tâche qui nécessite des privilèges d'administrateur, [!INCLUDE[TLA2#tla_winvista](../../../includes/tla2sharptla-winvista-md.md)] affiche une boîte de dialogue qui invite l'utilisateur à donner son consentement pour continuer. Cette boîte de dialogue bénéficie d'une protection contre les communications interprocessus, ce qui empêche les logiciels malveillants de simuler l'entrée de l'utilisateur. De même, d'autres processus ne sont normalement pas autorisés à accéder à l'écran d'ouverture de session sur le Bureau.  
  
 Les clients UI Automation doivent communiquer avec d’autres processus, certains d’entre eux pouvant être exécutés à un niveau de privilège supérieur. Les clients peuvent aussi avoir besoin d'accéder à des boîtes de dialogue système qui ne sont normalement pas visibles à d'autres processus. Par conséquent, les clients [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] doivent être approuvés par le système et s'exécuter avec des privilèges spéciaux.  
  
 Pour avoir l'autorisation de communiquer avec des applications exécutées à un niveau de privilège plus élevé, les applications doivent être signées.  
  
<a name="Manifest_Files"></a>   
## <a name="manifest-files"></a>Fichiers manifeste  
 Pour accéder à l' [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)]du système protégé, les applications doivent être générées avec un fichier manifeste contenant un attribut spécial. Cet attribut `uiAccess` est inclus dans la balise `requestedExecutionLevel` , comme suit :  
  
 `<trustInfo xmlns="urn:0073chemas-microsoft-com:asm.v3">`  
  
 `<security>`  
  
 `<requestedPrivileges>`  
  
 `<requestedExecutionLevel`  
  
 `level="highestAvailable"`  
  
 `UIAccess="true" />`  
  
 `</requestedPrivileges>`  
  
 `</security>`  
  
 `</trustInfo>`  
  
 Dans ce code, la valeur de l'attribut `level` n'est qu'un exemple.  
  
 `UIAccess` a la valeur « false » par défaut ; autrement dit, si l'attribut est omis ou qu'il n'existe aucun manifeste pour l'assembly, l'application ne pourra pas accéder à l' [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)]protégée.  
  
 Pour plus d’informations sur [!INCLUDE[TLA#tla_longhorn2](../../../includes/tlasharptla-longhorn2-md.md)] de sécurité, la signature des applications et la création de manifestes d’assembly, consultez [pratiques recommandées et directives pour des Applications dans un environnement de privilège minimum](https://docs.microsoft.com/previous-versions/dotnet/articles/aa480150(v=msdn.10)).
