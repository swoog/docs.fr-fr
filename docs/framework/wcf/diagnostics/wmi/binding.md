---
title: Binding2
ms.date: 03/30/2017
ms.assetid: 09511c6c-5749-4bb0-874e-0f0be36bfe04
ms.openlocfilehash: a040cc6e12833d2c737eb14c591300e5873ddce7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59979158"
---
# <a name="binding"></a>Liaison
WMI Binding  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class Binding  
{  
  BindingElement BindingElements[];  
  datetime CloseTimeout;  
  string Name;  
  string Namespace;  
  datetime OpenTimeout;  
  datetime ReceiveTimeout;  
  string Scheme;  
  datetime SendTimeout;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe Binding ne définit pas de méthodes.  
  
## <a name="properties"></a>Properties  
 La classe Binding a les propriétés suivantes :  
  
### <a name="bindingelements"></a>BindingElement  
 Type de données : Tableau BindingElement  
  
 Type d’accès : Propriétés en lecture seule  
  
 Collection d'éléments de liaison implémentés par la liaison.  
  
### <a name="closetimeout"></a>CloseTimeout  
 Type de données : datetime  
  
 Type d’accès : Propriétés en lecture seule  
  
 Intervalle de temps spécifié pour l'exécution d'une opération de fermeture.  
  
### <a name="name"></a>Nom  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Le nom de la liaison.  
  
### <a name="namespace"></a>Espace de noms  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Espace de noms XML de la liaison.  
  
### <a name="opentimeout"></a>OpenTimeout  
 Type de données : datetime  
  
 Type d’accès : Propriétés en lecture seule  
  
 Intervalle de temps spécifié pour l'exécution d'une opération d'ouverture.  
  
### <a name="receivetimeout"></a>ReceiveTimeout  
 Type de données : datetime  
  
 Type d’accès : Propriétés en lecture seule  
  
 Intervalle de temps spécifié pour l'exécution d'une opération de réception.  
  
### <a name="scheme"></a>Scheme  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Modèle de transport URI utilisé par les fabrications et écouteurs de canal construits par la liaison.  
  
### <a name="sendtimeout"></a>SendTimeout  
 Type de données : datetime  
  
 Type d’accès : Propriétés en lecture seule  
  
 Intervalle de temps spécifié pour l'exécution d'une opération d'envoi.  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Channels.Binding>
