---
title: Traitement ordonné des messages en mode de concurrence simple
ms.date: 03/30/2017
ms.assetid: a90f5662-a796-46cd-ae33-30a4072838af
ms.openlocfilehash: 785c2953e57eaf967209b0d9e52ab85a3a99c450
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59229717"
---
# <a name="ordered-processing-of-messages-in-single-concurrency-mode"></a>Traitement ordonné des messages en mode de concurrence simple
WCF n’offre aucune garantie concernant l’ordre dans lequel les messages sont traités, à moins que le canal sous-jacent soit session.  Par exemple, un service WCF qui utilise MsmqInputChannel, qui n’est pas un canal de session, ne traite pas les messages dans l’ordre. Il existe certains cas où un développeur peut le comportement de traitement dans l’ordre, mais pas souhaitent utiliser des sessions. Cette rubrique décrit comment configurer ce comportement lorsqu'un service s'exécute en mode de concurrence simple.  
  
## <a name="in-order-message-processing"></a>Traitement des messages dans l'ordre  
 Un nouvel attribut nommé <xref:System.ServiceModel.ServiceBehaviorAttribute.EnsureOrderedDispatch%2A> a été ajouté à la classe <xref:System.ServiceModel.ServiceBehaviorAttribute>. Lorsque <xref:System.ServiceModel.ServiceBehaviorAttribute.EnsureOrderedDispatch%2A> a la valeur true et <xref:System.ServiceModel.ServiceBehaviorAttribute.ConcurrencyMode%2A> a la valeur <xref:System.ServiceModel.ConcurrencyMode.Single> les messages envoyés au service sont traités dans l'ordre. L'extrait de code suivant illustre comment définir ces attributs.  
  
```  
[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Single, EnsureOrderedDispatch = true )]  
    class Service : IService  
    {  
         // ...  
    }  
```  
  
 Si une autre valeur est affectée à la propriété <xref:System.ServiceModel.ServiceBehaviorAttribute.ConcurrencyMode%2A>, une exception <xref:System.InvalidOperationException> est levée.  
  
## <a name="see-also"></a>Voir aussi

- [Sessions, instanciation et accès concurrentiel](../../../../docs/framework/wcf/feature-details/sessions-instancing-and-concurrency.md)
- [Concurrence](../../../../docs/framework/wcf/samples/concurrency.md)
