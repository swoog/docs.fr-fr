---
title: CallbackBehavior
ms.date: 03/30/2017
ms.assetid: 42acd302-2b62-4849-a2d1-a03084343ecd
ms.openlocfilehash: 38a38a71db2927d187ccdd93e5e364b0d4955373
ms.sourcegitcommit: b22705f1540b237c566721018f974822d5cd8758
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/19/2018
ms.locfileid: "49452610"
---
# <a name="callbackbehavior"></a>CallbackBehavior
CallbackBehavior  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class CallbackBehavior : Behavior  
{  
  boolean AutomaticSessionShutdown;  
  string ConcurrencyMode;  
  boolean IgnoreExtensionDataObject;  
  boolean IncludeExceptionDetailInFaults;  
  boolean MaxItemsInObjectGraph;  
  boolean UseSynchronizationContext;  
  boolean ValidateMustUnderstand;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe CallbackBehavior ne définit pas de méthode.  
  
## <a name="properties"></a>Properties  
 La classe CallbackBehavior a les propriétés suivantes :  
  
### <a name="automaticsessionshutdown"></a>AutomaticSessionShutdown  
 Type de données : booléen  
  
 Type d'accès : lecture seule  
  
 Lorsque sa valeur est « true », la session est fermée automatiquement lorsqu'un service ferme une session duplex.  
  
### <a name="concurrencymode"></a>ConcurrencyMode  
 Type de données : chaîne  
Type d'accès : lecture seule  
  
 Spécifie si le service prend en charge un thread, plusieurs threads ou les appels réentrants.  
  
### <a name="ignoreextensiondataobject"></a>IgnoreExtensionDataObject  
 Type de données : booléen  
  
 Type d'accès : lecture seule  
  
 Valeur qui spécifie s'il faut envoyer des données de sérialisation inconnues sur le câble.  
  
### <a name="includeexceptiondetailinfaults"></a>IncludeExceptionDetailInFaults  
 Type de données : booléen  
  
 Type d'accès : lecture seule  
  
 En cas d'activation, des détails au sujet des exceptions levées sur le rappel sont joints aux erreurs retournées au service.  
  
### <a name="maxitemsinobjectgraph"></a>MaxItemsInObjectGraph  
 Type de données : booléen  
  
 Type d'accès : lecture seule  
  
 Nombre maximal d'éléments autorisés dans un objet sérialisé.  
  
### <a name="usesynchronizationcontext"></a>UseSynchronizationContext  
 Type de données : booléen  
  
 Type d'accès : lecture seule  
  
 Spécifie s’il faut utiliser le contexte de synchronisation actuel pour choisir le thread d’exécution.  
  
### <a name="validatemustunderstand"></a>ValidateMustUnderstand  
 Type de données : booléen  
  
 Type d'accès : lecture seule  
  
 Spécifie si le système ou l'application applique le traitement d'en-tête SOAP MustUnderstand.  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.CallbackBehaviorAttribute>
