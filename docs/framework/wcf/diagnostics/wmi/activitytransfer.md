---
title: ActivityTransfer
ms.date: 03/30/2017
ms.assetid: fc40ef17-2a92-4ce2-853c-6ba8e5d571f3
ms.openlocfilehash: 936e870c1ec991e2e33acf8a08ccc93975989679
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50034420"
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
  
## <a name="properties"></a>Propriétés  
 La classe ActivityTransfer a les propriétés suivantes :  
  
### <a name="activityid"></a>ActivityID  
  
-   Type de données : objet  
    Type d'accès : lecture seule  
  
-   ID d'activité  
  
### <a name="relatedactivityid"></a>RelatedActivityID  
  
-   Type de données : objet  
    Type d'accès : lecture seule  
  
-   ID d'activité connexe  
  
## <a name="requirements"></a>Spécifications  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel.|
