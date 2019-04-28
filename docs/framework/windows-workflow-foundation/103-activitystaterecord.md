---
title: 103 - ActivityStateRecord
ms.date: 03/30/2017
ms.assetid: 57636a9a-561e-44aa-aef9-1f1894aaa6dd
ms.openlocfilehash: 38cec570cffebf6af6d35df481cbec8c7dca8cd1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61924382"
---
# <a name="103---activitystaterecord"></a>103 - ActivityStateRecord
## <a name="properties"></a>Properties  
  
|||  
|-|-|  
|Id|103|  
|Mots clés|EndToEndMonitoring, Dépannage, HealthMonitoring, WFTracking|  
|Niveau|Information|  
|Canal|Microsoft-Windows-Application Server-Applications/Analyse|  
  
## <a name="description"></a>Description  
 Cet événement est émis par le participant de suivi ETW lorsqu'une activité dans une instance de workflow émet un événement ActivityStateRecord.  
  
## <a name="message"></a>Message  
 TrackRecord = ActivityStateRecord, InstanceID =% 1, RecordNumber=%2, EventTime=%3, état =% 4, Name=%5, ActivityId=%6, ActivityInstanceId=%7, ActivityTypeName=%8, Arguments=%9, Variables=%10, Annotations=%11, ProfileName =% 12  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|InstanceId|xs:GUID|ID d'instance pour le workflow|  
|RecordNumber|xs:long|Numéro de séquence de l'enregistrement émis.|  
|EventTime|xs:dateTime|Heure au format UTC à laquelle l'événement a été émis|  
|État|xs:string|État de l'activité.|  
|Nom|xs:string|Nom de l'activité qui a émis l'événement|  
|ActivityId|xs:string|ID d'activité de l'activité émettrice|  
|ActivityInstanceId|xs:string|ID d'instance de l'activité de l'activité émettrice|  
|ActivityTypeName|xs:string|Nom de type de l'activité émettrice|  
|Arguments|xs:string|Arguments suivis avec cet événement.  Les valeurs sont stockées dans un élément xml au format \<éléments >\< nom de l’élément = « argumentName » type = "> argumentValue\</élément > \< /éléments >.  Si aucun argument n’a été suivie, la chaîne contient \<éléments / >. La taille d'événement ETW est limitée par la taille de la mémoire tampon ETW ou par la charge utile maximale pour un événement ETW. Si la taille de l’événement dépasse les limites ETW, l’événement est tronqué en supprimant les annotations et en remplaçant la valeur de l’annotation avec \<éléments >... \</Items >.  Les types suivants sont stockés en tant que valeur telle que retournée par ToString(); string,char,bool,int,short,long,uint,ushort,ulong,System.Single,float,double,System.Guid,System.DateTimeOffset,System.DateTime.  Tous les autres types sont sérialisés à l'aide de System.Runtime.Serialization.NetDataContractSerializer.|  
|Variables|xs:string|Les variables suivies avec cet événement.  Les valeurs sont stockées dans un élément xml au format \<éléments >\< nom de l’élément = « variableName » type = "> variableValue\</élément > \< /éléments >.  Si aucune variable a été suivie, la chaîne contient \<éléments / >. La taille d'événement ETW est limitée par la taille de la mémoire tampon ETW ou par la charge utile maximale pour un événement ETW. Si la taille de l’événement dépasse les limites ETW, l’événement est tronqué en supprimant les annotations et en remplaçant la valeur des variables avec \<éléments >... \</Items >.  Les types suivants sont stockés en tant que valeur telle que retournée par ToString(); string,char,bool,int,short,long,uint,ushort,ulong,System.Single,float,double,System.Guid,System.DateTimeOffset,System.DateTime.  Tous les autres types sont sérialisés à l'aide de System.Runtime.Serialization.NetDataContractSerializer.|  
|Annotations|xs:string|Annotations ayant été ajoutées à cet événement.  Les valeurs sont stockées dans un élément xml au format \<éléments >\< nom de l’élément = « annotationName » type = "> annotationValue\</élément > \< /éléments >.  Si aucune annotation n’est spécifiée, la chaîne contient \<éléments / >. La taille d'événement ETW est limitée par la taille de la mémoire tampon ETW ou par la charge utile maximale pour un événement ETW. Si la taille de l’événement dépasse les limites ETW, l’événement est tronqué en supprimant les annotations et en remplaçant la valeur de l’annotation avec \<éléments >... \</Items >.|  
|ProfileName|xs:string|Nom ou modèle de suivi qui a provoqué l'émission de cet événement|  
|HostReference|xs:string|Pour les services hébergés sur le Web, ce champ identifie de manière unique le service dans la hiérarchie Web.  Son format est défini en tant que « chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName' exemple : « Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService »|  
|AppDomain|xs:string|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
