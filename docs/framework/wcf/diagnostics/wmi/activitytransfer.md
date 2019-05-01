---
title: ActivityTransfer
ms.date: 03/30/2017
ms.assetid: fc40ef17-2a92-4ce2-853c-6ba8e5d571f3
ms.openlocfilehash: 936e870c1ec991e2e33acf8a08ccc93975989679
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61964292"
---
# <a name="activitytransfer"></a>ActivityTransfer
Événement du transfert de l'activité  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class ActivityTransfer : WSAT_TraceEvent  
{  
  object ActivityID;  
  object RelatedActivityID;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe ActivityTransfer ne définit pas de méthode.  
  
## <a name="properties"></a>Properties  
 La classe ActivityTransfer a les propriétés suivantes :  
  
### <a name="activityid"></a>ActivityID  
  
- Type de données : objet  
    Type d’accès : Propriétés en lecture seule  
  
- ID d'activité  
  
### <a name="relatedactivityid"></a>RelatedActivityID  
  
- Type de données : objet  
    Type d’accès : Propriétés en lecture seule  
  
- ID d'activité connexe  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel.|
