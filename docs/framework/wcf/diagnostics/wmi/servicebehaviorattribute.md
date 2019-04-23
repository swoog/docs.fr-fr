---
title: ServiceBehaviorAttribute
ms.date: 03/30/2017
ms.assetid: 5faa266f-587f-4e03-828d-1c7dd5acfe65
ms.openlocfilehash: b6221e93f10b87a368bd594932a8c36ae14df8f3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59772821"
---
# <a name="servicebehaviorattribute"></a>ServiceBehaviorAttribute
ServiceBehaviorAttribute  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class ServiceBehaviorAttribute : Behavior  
{  
  boolean AutomaticSessionShutdown;  
  string ConcurrencyMode;  
  string ConfigurationName;  
  boolean IgnoreExtensionDataObject;  
  boolean IncludeExceptionDetailInFaults;  
  string InstanceContextMode;  
  sint32 MaxItemsInObjectGraph;  
  string Name;  
  string Namespace;  
  boolean ReleaseServiceInstanceOnTransactionComplete;  
  boolean TransactionAutoCompleteOnSessionClose;  
  string TransactionIsolationLevel;  
  datetime TransactionTimeout;  
  boolean UseSynchronizationContext;  
  boolean ValidateMustUnderstand;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe ServiceBehaviorAttribute ne définit pas de méthode.  
  
## <a name="properties"></a>Properties  
 La classe ServiceBehaviorAttribute a les propriétés suivantes :  
  
### <a name="automaticsessionshutdown"></a>AutomaticSessionShutdown  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 Indique s'il faut fermer automatiquement une session lorsqu'un client ferme une session de sortie.  
  
### <a name="concurrencymode"></a>ConcurrencyMode  
 Type de données : chaîne  
Type d’accès : Propriétés en lecture seule  
  
 Indique si un service prend en charge un thread, plusieurs threads ou des appels réentrants.  
  
### <a name="configurationname"></a>ConfigurationName  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Nom de la configuration du service.  
  
### <a name="ignoreextensiondataobject"></a>IgnoreExtensionDataObject  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 Spécifie s'il faut envoyer des données de sérialisation inconnues sur le câble.  
  
### <a name="includeexceptiondetailinfaults"></a>IncludeExceptionDetailInFaults  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 Spécifie s'il convient d'inclure des informations d'exception gérées dans les détails des fautes SOAP renvoyées aux clients à des fins de débogage.  
  
### <a name="instancecontextmode"></a>InstanceContextMode  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Spécifie quand un nouvel objet de service est créé.  
  
### <a name="maxitemsinobjectgraph"></a>MaxItemsInObjectGraph  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 Nombre maximal d'éléments autorisés dans un objet sérialisé.  
  
### <a name="name"></a>Nom  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Attribut de nom du service dans WSDL.  
  
### <a name="namespace"></a>Espace de noms  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Espace de noms cible du service dans WSDL.  
  
### <a name="releaseserviceinstanceontransactioncomplete"></a>ReleaseServiceInstanceOnTransactionComplete  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 Spécifie si l’objet de service est recyclé lorsque la transaction actuelle se termine.  
  
### <a name="transactionautocompleteonsessionclose"></a>TransactionAutoCompleteOnSessionClose  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 Spécifie si les transactions en attente sont complétées lorsque la session actuelle se ferme.  
  
### <a name="transactionisolationlevel"></a>TransactionIsolationLevel  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Spécifie le niveau d'isolation de la transaction.  
  
### <a name="transactiontimeout"></a>TransactionTimeout  
 Type de données : datetime  
  
 Type d’accès : Propriétés en lecture seule  
  
 Période pendant laquelle une transaction doit s’effectuer.  
  
### <a name="usesynchronizationcontext"></a>UseSynchronizationContext  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 Spécifie s’il faut utiliser le contexte de synchronisation actuel pour choisir l’exécution d’un thread.  
  
### <a name="validatemustunderstand"></a>ValidateMustUnderstand  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 Spécifie si le système ou l'application applique le traitement d'en-tête SOAP MustUnderstand.  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.ServiceBehaviorAttribute>
