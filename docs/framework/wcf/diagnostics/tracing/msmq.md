---
title: MSMQ
ms.date: 03/30/2017
ms.assetid: d9fca29f-fa44-4ec4-bb48-b10800694500
ms.openlocfilehash: 5e157da25829a0741de988d1d6dde0318a93b109
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61663724"
---
# <a name="msmq"></a>MSMQ
Dans une application MSMQ, aucune activité supplémentaire n'est transférée du canal mis en file d'attente vers MSMQ et de MSMQ vers le canal mis en file d'attente.  
  
 De plus, l'ID de message MSMQ et l'ID de message SOAP (ainsi que l'ID d'activité, s'il existe) sont suivis dans le cadre des suivis de canaux mis en file d'attente lors d'une opération d'envoi.  
  
 L'ID de message MSMQ et l'ID de message SOAP (ainsi que l'ID d'activité, s'il existe) sont suivis dans le cadre des suivis de canaux mis en file d'attente lors d'une opération de réception.  
  
 Les transferts requis sur l’opération de réception sont exécutés de la même façon que tout autre transport (réception octets -> à traiter le message -> opération).
