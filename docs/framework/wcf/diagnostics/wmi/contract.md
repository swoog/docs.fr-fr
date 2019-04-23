---
title: Contract1
ms.date: 03/30/2017
ms.assetid: aa00f6b3-7e1f-4213-841a-206463fca20b
ms.openlocfilehash: 10789f9a2940c239ae20c8fd1e9d48bca0e820ed
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59772997"
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
  
 Type d’accès : Propriétés en lecture seule  
  
 ID du domaine d'application qui héberge le contrat.  
  
### <a name="behaviors"></a>comportements  
 Type de données : Tableau de comportements  
  
 Type d’accès : Propriétés en lecture seule  
  
 Comportements associés à ce contrat.  
  
### <a name="name"></a>Nom  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Nom du contrat dans WSDL.  
  
### <a name="namespace"></a>Espace de noms  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Espace de noms de l'élément `portType` dans WSDL.  
  
### <a name="operations"></a>Opérations  
 Type de données : Tableau d’opérations  
  
 Type d’accès : Propriétés en lecture seule  
  
 Opérations de ce contrat.  
  
### <a name="processid"></a>ProcessId  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 ID du processus qui héberge le contrat.  
  
### <a name="ref"></a>ref  
 Type de données : Contrat  
  
 Type d’accès : Propriétés en lecture seule  
  
 Type de rappel lorsque le contrat est un contrat duplex.  
  
### <a name="sessionmode"></a>SessionMode  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Indique si le contrat nécessite que la liaison associée à ce contrat utilise les sessions de canal.  
  
### <a name="type"></a>Type  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Type du contrat.  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Description.ContractDescription>
