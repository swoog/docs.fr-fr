---
title: Autorisation de sécurité pour la redirection de liaison d’assembly
ms.date: 03/30/2017
helpviewer_keywords:
- side-by-side execution, assembly binding redirection
- assemblies [.NET Framework], binding redirection
ms.assetid: 24a5cdff-7ed9-4195-93f3-edf6899019fc
ms.openlocfilehash: ba4e7e790860696f4489e9ef7b73bddcb8c4e399
ms.sourcegitcommit: b8ace47d839f943f785b89e2fff8092b0bf8f565
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2019
ms.locfileid: "55674436"
---
# <a name="assembly-binding-redirection-security-permission"></a>Autorisation de sécurité pour la redirection de liaison d’assembly
La redirection de liaison d’assembly explicite dans un fichier de configuration de l’application nécessite une autorisation de sécurité. Cela s'applique à la redirection des assemblys .NET Framework et des assemblys tiers. L’autorisation est accordée en définissant le <xref:System.Security.Permissions.SecurityPermissionFlag> indicateur sur le <xref:System.Security.Permissions.SecurityPermission>. Les assemblys managés n’ont aucune autorisation par défaut.  
  
 L’autorisation de sécurité est accordée aux applications exécutées dans la Zone de confiance (ordinateur local) et de la Zone Intranet. Applications qui s’exécutent dans la Zone Internet sont strictement autorisées à effectuer de redirection de liaison d’assembly.  
  
 L’autorisation n’est pas nécessaire si la redirection d’assembly est exécutée dans un fichier de stratégie d’éditeur qui est contrôlé par l’éditeur de composant, ou dans le fichier de configuration d’ordinateur qui est contrôlé par l’administrateur. Toutefois, l’autorisation est nécessaire pour une application ignore explicitement la stratégie de serveur de publication à l’aide du [ \<publisherPolicy appliquer = « no » / >](../../../docs/framework/configure-apps/file-schema/runtime/publisherpolicy-element.md) élément dans le fichier de configuration d’application.  
  
 Le tableau suivant présente la valeur par défaut des paramètres de sécurité pour le **BindingRedirects** indicateur.  
  
|Zone|Paramètre d’indicateur BindingRedirects|  
|----------|-----------------------------------|  
|Zone de confiance (ordinateur local)|**ON**|  
|Zone intranet|**ON**|  
|Zone Internet|**OFF**|  
|Zones non fiables|**OFF**|  
  
 Un administrateur peut modifier ces paramètres de sécurité pour prendre en charge ou restreindre des scénarios spécifiques sur un ordinateur donné. Aucun outil permettant de modifier le **BindingRedirects** le paramètre de la valeur par défaut ; indicateur un administrateur doit modifier manuellement le fichier Security.config sur l’ordinateur d’un utilisateur.  
  
## <a name="see-also"></a>Voir aussi

- [Fichiers de stratégie de serveur de publication et l’exécution côte à côte](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/06d2bae3(v=vs.100))
- [Guide pratique pour Activer et désactiver la redirection de liaison automatique](../../../docs/framework/configure-apps/how-to-enable-and-disable-automatic-binding-redirection.md)
- [Exécution côte à côte](../../../docs/framework/deployment/side-by-side-execution.md)
