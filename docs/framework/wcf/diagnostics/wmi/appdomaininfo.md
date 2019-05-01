---
title: AppDomainInfo
ms.date: 03/30/2017
ms.assetid: 6610b7d8-81eb-4bec-a543-9b72ad7b6f73
ms.openlocfilehash: 0b7f8aadbd9a9dfcdd33fc65be3a5a41ea95f5be
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61964253"
---
# <a name="appdomaininfo"></a>AppDomainInfo
Informations du domaine d'application  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class AppDomainInfo  
{  
  sint32 AppDomainId;  
  boolean IsDefault;  
  boolean LogMalformedMessages;  
  boolean LogMessagesAtServiceLevel;  
  boolean LogMessagesAtTransportLevel;  
  TraceListener MessageLoggingTraceListeners[];  
  string Name;  
  string PerformanceCounters;  
  sint32 ProcessId;  
  string ServiceConfigPath;  
  string TraceLevel;  
  TraceListener wmiTraceListeners[];  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe AppDomainInfo ne définit pas de méthode.  
  
## <a name="properties"></a>Properties  
 La classe AppDomainInfo a les propriétés suivantes :  
  
### <a name="appdomainid"></a>AppDomainId  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 ID de l'appdomain.  
  
### <a name="isdefault"></a>IsDefault  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 Indique si l'appdomain est l'appdomain par défaut.  
  
### <a name="logmalformedmessages"></a>LogMalformedMessages  
 Type de données : booléen  
  
 Type d’accès : En lecture/écriture  
  
 Valeur qui spécifie si les messages incorrects sont enregistrés.  
  
### <a name="logmessagesatservicelevel"></a>LogMessagesAtServiceLevel  
 Type de données : booléen  
  
 Type d’accès : En lecture/écriture  
  
 Valeur qui spécifie si les messages sont suivis au niveau du service (avant les transformations associées au chiffrement et au transport).  
  
### <a name="logmessagesattransportlevel"></a>LogMessagesAtTransportLevel  
 Type de données : booléen  
  
 Type d’accès : En lecture/écriture  
  
 Valeur qui spécifie si les messages sont suivis au niveau du transport.  
  
### <a name="messageloggingtracelisteners"></a>MessageLoggingTraceListeners  
 Type de données : Tableau TraceListener  
  
 Type d’accès : Propriétés en lecture seule  
  
 Écouteurs de suivi de la collection qui écoutent la source de suivi System.Wmi.MessageLogging.  
  
### <a name="name"></a>Nom  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Nom de l'appdomain.  
  
### <a name="performancecounters"></a>PerformanceCounters  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Portée de compteurs de performance actifs dans l'appdomain.  
  
### <a name="processid"></a>ProcessId  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 ID de processus.  
  
### <a name="serviceconfigpath"></a>ServiceConfigPath  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Chemin d’accès à la configuration du service.  
  
### <a name="tracelevel"></a>TraceLevel  
 Type de données : chaîne  
  
 Type d’accès : En lecture/écriture  
  
 Niveau de suivi de la source de suivi System.Wmi.  
  
### <a name="servicemodeltracelisteners"></a>ServiceModelTraceListeners  
 Type de données : Tableau TraceListener  
  
 Type d’accès : Propriétés en lecture seule  
  
 Collection d’écouteurs de la source de suivi System.ServiceModel.  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|
