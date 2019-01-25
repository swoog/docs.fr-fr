---
title: ServiceAuthorizationBehavior
ms.date: 03/30/2017
ms.assetid: 77dad8e8-fea4-4d1c-b366-2f01a2a87f78
ms.openlocfilehash: 58eb2a9fd9017aaf9966644180936f5871e086d1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54613894"
---
# <a name="serviceauthorizationbehavior"></a>ServiceAuthorizationBehavior
ServiceAuthorizationBehavior  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class ServiceAuthorizationBehavior : Behavior  
{  
  boolean ImpersonateCallerForAllOperations;  
  string PrincipalPermissionMode;  
  string RoleProvider;  
  string ServiceAuthorizationManager;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe ServiceAuthorizationBehavior ne définit pas de méthode.  
  
## <a name="properties"></a>Properties  
 La classe ServiceAuthorizationBehavior a les propriétés suivantes :  
  
### <a name="impersonatecallerforalloperations"></a>ImpersonateCallerForAllOperations  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 Valeur qui contrôle si le service essaie d'emprunter l'identité à l'aide des informations d'identification fournies par le message entrant.  
  
### <a name="principalpermissionmode"></a>PrincipalPermissionMode  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Principal de sécurité utilisée pour effectuer les opérations sur le serveur.  
  
### <a name="roleprovider"></a>RoleProvider  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Nom du fournisseur de rôles ASP.NET.  
  
### <a name="serviceauthorizationmanager"></a>ServiceAuthorizationManager  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Gestionnaire d'autorisations utilisé pour l'autorisation personnalisée.  
  
## <a name="requirements"></a>Spécifications  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.Description.ServiceAuthorizationBehavior>
