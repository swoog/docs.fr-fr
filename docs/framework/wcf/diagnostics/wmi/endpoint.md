---
title: Point de terminaison
ms.date: 03/30/2017
ms.assetid: fe63370d-81a1-40f3-97c2-59cb357c78d2
ms.openlocfilehash: 4562481e8b0b18c0ea0d9df0af3427ffe6419821
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61963603"
---
# <a name="endpoint"></a>Point de terminaison
Point de terminaison  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class Endpoint  
{  
  string Address;  
  string AddressHeaders[];  
  string AddressIdentity;  
  sint32 AppDomainId;  
  Behavior Behaviors[];  
  Binding Binding;  
  string ContractName;  
  string CounterInstanceName;  
  string ListenUri;  
  string Name;  
  sint32 ProcessId;  
  Contract ref;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe Endpoint définit la méthode suivante.  
  
|Méthode|Description|  
|------------|-----------------|  
|[GetOperationCounterInstanceName](../../../../../docs/framework/wcf/diagnostics/wmi/getoperationcounterinstancename.md)|Récupère le nom d'instance du compteur de performance d'opération|  
  
## <a name="properties"></a>Properties  
 La classe Endpoint a les propriétés suivantes :  
  
### <a name="address"></a>Adresse  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 URI qui contient l'adresse du point de terminaison.  
  
### <a name="addressheaders"></a>AddressHeaders  
 Type de données : tableau de chaînes  
  
 Type d’accès : Propriétés en lecture seule  
  
 Collection d’en-têtes d’adresse jointe à ce point de terminaison.  
  
### <a name="addressidentity"></a>AddressIdentity  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Identité du point de terminaison.  
  
### <a name="appdomainid"></a>AppDomainId  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 ID du domaine d'application qui héberge le point de terminaison.  
  
### <a name="behaviors"></a>comportements  
 Type de données : Tableau de comportements  
  
 Type d’accès : Propriétés en lecture seule  
  
 Collection de comportements implémentée par ce point de terminaison.  
  
### <a name="binding"></a>Liaison  
 Type de données : Liaison  
  
 Type d’accès : Propriétés en lecture seule  
  
 Liaison utilisée par ce point de terminaison.  
  
### <a name="contractname"></a>ContractName  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Chaîne qui spécifie quel contrat est exposé par ce point de terminaison.  
  
### <a name="counterinstancename"></a>CounterInstanceName  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Nom de l'instance des compteurs de performance du point de terminaison.  
  
### <a name="listenuri"></a>ListenUri  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 URI sur lequel le point de terminaison écoute.  
  
### <a name="name"></a>Nom  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Nom unique de ce point de terminaison.  
  
### <a name="processid"></a>ProcessId  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 ID du processus qui héberge le point de terminaison.  
  
### <a name="ref"></a>ref  
 Type de données : Contrat  
  
 Type d’accès : Propriétés en lecture seule  
  
 Le contrat exposé par ce point de terminaison.  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|
