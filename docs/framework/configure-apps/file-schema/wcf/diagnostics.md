---
title: <diagnostics>
ms.date: 03/30/2017
ms.assetid: 0c2f95c4-cc12-4fb5-a70c-7fc6fa95db58
ms.openlocfilehash: 3fc7828d399555f7c459f6dd067ce9a24b8998b6
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61704053"
---
# <a name="diagnostics"></a>\<diagnostics>
L'élément `diagnostics` définit des paramètres qui peuvent être utilisés par un administrateur à des fins d'inspection et de contrôle au moment de l'exécution.  
  
 \<system.ServiceModel>  
\<diagnostics>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<system.serviceModel>
  <diagnostics etwProviderId="String"
               performanceCounters="Off/ServiceOnly/All/Default"
               wmiProviderEnabled="Boolean">
    <endToEndTracing activityTracing="Boolean"
                     messageFlowTracing="Boolean"
                     propagateActivity="Boolean" />
    <messageLogging logEntireMessage="Boolean"
                    logMalformedMessages="Boolean"
                    logMessagesAtServiceLevel="Boolean"
                    logMessagesAtTransportLevel="Boolean"
                    maxMessagesToLog="Integer"
                    maxSizeOfMessageToLog="Integer">
      <filters>
        <clear />
      </filters>
    </messageLogging>
  </diagnostics>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|etwProviderId|Chaîne qui spécifie l'identificateur du fournisseur de suivi d'événements, qui écrit des événements dans les sessions ETW.|  
|performanceCounters|Spécifie si les compteurs de performance de l'assembly sont activés. Les valeurs valides sont les suivantes :<br /><br /> -Désactivé : Les compteurs de performance sont désactivés.<br />-   ServiceOnly: Seuls les compteurs de performance pertinents pour ce service sont activés.<br />-Toutes les : Les compteurs de performance peuvent être affichés pendant l'exécution.<br />-Valeur par défaut : Un compteur de performance unique de l'instance _WCF_Admin est créé. Cette instance est employée pour activer la collection de données SQM utilisée par l’infrastructure. Aucune des valeurs du compteur de cette instance n'est mise à jour et par conséquent toutes resteront à zéro. Il s'agit de la valeur par défaut si aucune configuration n'est présente pour WCF.|  
|wmiProviderEnabled|Valeur booléenne qui spécifie si le fournisseur WMI de l'assembly est activé. Le fournisseur WMI est requis pour que l’utilisateur puisse obtenir l’accès au moment de l’exécution aux fonctionnalités d’inspection et de contrôle de Windows Communication Foundation (WCF). La valeur par défaut est `false`.|  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<endToEndTracing>](../../../../../docs/framework/configure-apps/file-schema/wcf/endtoendtracing.md)|Élément de configuration qui vous permet d'activer et désactiver différents aspects du suivi de bout en bout pendant l'exécution d'une application de service.|  
|[\<messageLogging>](../../../../../docs/framework/configure-apps/file-schema/wcf/messagelogging.md)|Décrit les paramètres d'enregistrement des messages WCF.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|serviceModel|Élément racine de tous les éléments de configuration WCF.|  
  
## <a name="remarks"></a>Notes  
 La section `diagnostics` définit les paramètres de diagnostic pour tous les services situés dans un assembly. Il est impossible de définir des paramètres de diagnostic distincts au niveau du service à moins qu'il n'y ait qu'un seul service dans l'assembly. Les attributs sont définis d’après les exigences de la section.  
  
## <a name="example"></a>Exemple  
  
```xml  
<diagnostics wmiProviderEnabled="false"
             performanceCounters="all">
  <messageLogging logEntireMessage="true"
                  logMalformedMessages="true"
                  logMessagesAtServiceLevel="true"
                  logMessagesAtTransportLevel="true"
                  maxMessagesToLog="42"
                  maxSizeOfMessageToLog="42">
    <filters>
      <clear />
    </filters>
  </messageLogging>
</diagnostics>
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Configuration.DiagnosticSection>
- <xref:System.ServiceModel.Diagnostics>
