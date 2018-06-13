---
title: 'Procédure : créer un participant de persistance personnalisé'
ms.date: 03/30/2017
ms.assetid: 1d9cc47a-8966-4286-94d5-4221403d9c06
ms.openlocfilehash: fcd96e41d8fc7b36f9dff5f10e9bc2d9034d79b2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33517239"
---
# <a name="how-to-create-a-custom-persistence-participant"></a>Procédure : créer un participant de persistance personnalisé
La procédure suivante permet de créer un participant de persistance. Consultez le [participant de persistance](http://go.microsoft.com/fwlink/?LinkID=177735) exemple et [extensibilité de magasin](../../../docs/framework/windows-workflow-foundation/store-extensibility.md) rubrique pour des exemples d’implémentation de participants de persistance.  
  
1.  Créez une classe dérivant des classes <xref:System.Activities.Persistence.PersistenceParticipant> ou <xref:System.Activities.Persistence.PersistenceIOParticipant>. La classe PersistenceIOParticipant offre les mêmes points d’extensibilité que la classe PersistenceParticipant en plus de pouvoir participer aux opérations d’e/s. Effectuez l'une ou l'ensemble des étapes suivantes :  
  
2.  Implémentez la méthode <xref:System.Activities.Persistence.PersistenceParticipant.CollectValues%2A>. Le **CollectValues** méthode possède deux paramètres de dictionnaire, pour le stockage des valeurs en lecture/écriture et l’autre pour stocker des valeurs en écriture seule (utilisés ultérieurement dans les requêtes). Dans cette méthode, vous devez remplir ces dictionnaires avec les données propres à un participant de persistance. Chaque dictionnaire contient le nom de la valeur comme clé et la valeur elle-même comme un objet <xref:System.Runtime.DurableInstancing.InstanceValue>.  
  
     Les valeurs du dictionnaire readWriteValues sont fournies en tant que **InstanceValue** objets. Les valeurs dans le dictionnaire en écriture seule sont empaquetés en tant que **InstanceValue** objets avec les valeurs InstanceValueOptions.Optional et InstanceValueOption.WriteOnly définies. Chaque **InstanceValue** fournie par le **CollectValues** implémentations dans tous les participants de persistance doivent avoir un nom unique.  
  
    ```  
    protected virtual void CollectValues (out IDictionary<XName,Object> readWriteValues, out IDictionary<XName,Object> writeOnlyValues)  
    ```  
  
3.  Implémentez la méthode <xref:System.Activities.Persistence.PersistenceParticipant.MapValues%2A>. Le **MapValues** méthode accepte deux paramètres qui sont similaires aux paramètres qui le **CollectValues** méthode reçoit. Toutes les valeurs collectées dans le **CollectValues** étape sont transmises à ces paramètres de dictionnaire. Les nouvelles valeurs ajoutées par le **MapValues** étape sont ajoutées aux valeurs en écriture seule.  Le dictionnaire en écriture seule est utilisé pour fournir des données à une source externe qui n'est pas directement associée aux valeurs d'instance. Chaque valeur fournie par les implémentations de la **MapValues** méthode tous les participants de persistance doit avoir un nom unique.  
  
    ```  
    protected virtual IDictionary<XName,Object> MapValues (IDictionary<XName,Object> readWriteValues,IDictionary<XName,Object> writeOnlyValues)  
    ```  
  
     La méthode <xref:System.Activities.Persistence.PersistenceParticipant.MapValues%2A> fournit des fonctionnalités non fournies par la méthode <xref:System.Activities.Persistence.PersistenceParticipant.CollectValues%2A>, car elle permet une dépendance sur une autre valeur fournie par un autre participant de persistance qui n'a pas encore été traité par <xref:System.Activities.Persistence.PersistenceParticipant.CollectValues%2A>.  
  
4.  Implémentez la **PublishValues** (méthode). Le **PublishValues** méthode reçoit un dictionnaire contenant toutes les valeurs chargées à partir du magasin de persistance.  
  
    ```  
    protected virtual void PublishValues (IDictionary<XName,Object> readWriteValues)  
    ```  
  
5.  Implémentez la **BeginOnSave** méthode si le participant est un participant de persistance d’e/s. Cette méthode est appelée lors d'une opération d'enregistrement. Dans cette méthode, vous devez effectuer l’adjonction d’e/s pour la persistance (des instances de flux de travail Enregistrer).  Si l’hôte utilise une transaction pour la commande de persistance correspondante, la même transaction est fournie dans Transaction.Current.  En outre, les PersistenceIOParticipants peuvent rendre publique une spécification de cohérence transactionnelle. Dans ce cas, l’hôte crée une transaction pour l’épisode de persistance si aucune transaction ne serait utilisée sinon.  
  
    ```  
    protected virtual IAsyncResult BeginOnSave (IDictionary<XName,Object> readWriteValues, IDictionary<XName,Object> writeOnlyValues, TimeSpan timeout, AsyncCallback callback, Object state)  
    ```  
  
6.  Implémentez la **BeginOnLoad** méthode si le participant est un participant de persistance d’e/s. Cette méthode est appelée lors d'une opération de chargement. Dans cette méthode, vous devez effectuer l’adjonction d’e/s pour le chargement des instances de workflow. Si l’hôte utilise une transaction pour la commande de persistance correspondante, la même transaction est fournie dans Transaction.Current. En outre, les participants d’e/s de persistance peuvent rendre publique une spécification de cohérence transactionnelle, dans ce cas, l’hôte crée une transaction pour l’épisode de persistance si une ne serait sinon utilisée.  
  
    ```  
    protected virtual IAsyncResult BeginOnLoad (IDictionary<XName,Object> readWriteValues, TimeSpan timeout, AsyncCallback callback, Object state)  
    ```
