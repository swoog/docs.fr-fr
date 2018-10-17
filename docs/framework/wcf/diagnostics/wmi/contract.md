---
title: Contract1
ms.date: 03/30/2017
ms.assetid: aa00f6b3-7e1f-4213-841a-206463fca20b
ms.openlocfilehash: 12e9cbf5232ebbad33ccc4fdca33233997d27357
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "49371561"
---
# <a name="contract"></a>Contrat
Contrat  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class Contract  
{  
  sint32 AppDomainId;  
  Behavior Behaviors[];  
  string Name;  
  string Namespace;  
  Operation Operations[];  
  sint32 ProcessId;  
  Contract ref;  
  string SessionMode;  
  string Type;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe Contract ne définit pas de méthodes.  
  
## <a name="properties"></a>Properties  
 La classe Contract a les propriétés suivantes :  
  
### <a name="appdomainid"></a>AppDomainId  
 Type de données : sint32  
  
 Type d'accès : lecture seule  
  
 ID du domaine d'application qui héberge le contrat.  
  
### <a name="behaviors"></a>Comportements  
 Type de données : tableau de comportements  
  
 Type d'accès : lecture seule  
  
 Comportements associés à ce contrat.  
  
### <a name="name"></a>Name  
 Type de données : chaîne  
  
 Type d'accès : lecture seule  
  
 Nom du contrat dans WSDL.  
  
### <a name="namespace"></a>Espace de noms  
 Type de données : chaîne  
  
 Type d'accès : lecture seule  
  
 Espace de noms de l'élément `portType` dans WSDL.  
  
### <a name="operations"></a>Opérations  
 Type de données : tableau d'opérations  
  
 Type d'accès : lecture seule  
  
 Opérations de ce contrat.  
  
### <a name="processid"></a>ProcessId  
 Type de données : sint32  
  
 Type d'accès : lecture seule  
  
 ID du processus qui héberge le contrat.  
  
### <a name="ref"></a>ref  
 Type de données: contrat  
  
 Type d'accès : lecture seule  
  
 Type de rappel lorsque le contrat est un contrat duplex.  
  
### <a name="sessionmode"></a>SessionMode  
 Type de données : chaîne  
  
 Type d'accès : lecture seule  
  
 Indique si le contrat nécessite que la liaison associée à ce contrat utilise les sessions de canal.  
  
### <a name="type"></a>Type  
 Type de données : chaîne  
  
 Type d'accès : lecture seule  
  
 Type du contrat.  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Description.ContractDescription>
