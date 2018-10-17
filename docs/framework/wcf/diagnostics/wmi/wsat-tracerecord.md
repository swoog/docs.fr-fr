---
title: WSAT_TraceRecord
ms.date: 03/30/2017
ms.assetid: 99bc7f66-1335-40d8-aa68-e754d569dc0d
ms.openlocfilehash: 907e764cf032e595c7aba455fd4808a640f68016
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "49373994"
---
# <a name="wsattracerecord"></a>WSAT_TraceRecord
WSAT_TraceRecord  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class WSAT_TraceRecord : WSAT_TraceEvent  
{  
  object ActivityID;  
  sint32 EventID;  
  string TraceRecord;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe WSAT_TraceRecord ne définit aucune méthode.  
  
## <a name="properties"></a>Properties  
 La classe WSAT_TraceRecord a les propriétés suivantes :  
  
### <a name="activityid"></a>ActivityID  
 Type de données : objet  
Type d'accès : lecture seule  
  
 ID d'activité de l'enregistrement de suivi.  
  
### <a name="eventid"></a>ID de l’événement  
 Type de données : sint32  
Type d'accès : lecture seule  
  
 ID d'événement de l'enregistrement de suivi.  
  
### <a name="tracerecord"></a>TraceRecord  
 Type de données : chaîne  
Type d'accès : lecture seule  
  
 Enregistrement de suivi  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|
