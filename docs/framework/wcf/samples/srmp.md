---
title: SRMP
ms.date: 03/30/2017
ms.assetid: cf37078c-dcb4-45e0-acaf-2f196521b226
ms.openlocfilehash: 736633733ab9c882c1d1520a5acf20c49324eeb3
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58828020"
---
# <a name="srmp"></a>SRMP
Cet exemple illustre comment établir une communication en file d'attente avec transaction à l'aide de MSMQ (Message Queuing) sur HTTP.  
  
 Dans le cadre d'une communication en file d'attente, le client communique avec le service à l'aide d'une file d'attente. Cela signifie que le client envoie ses messages à cette file d'attente. Le service reçoit des messages de la file d'attente. Par conséquent, dans le cadre d'une communication en file d'attente, il n'est pas nécessaire que le service et le client s'exécutent simultanément.  
  
 Le protocole MSMQ permet d'utiliser HTTP (notamment HTTPS) pour l'envoi des messages à la file d'attente. Dans cet exemple, nous expliquons à l’aide de Windows Communication Foundation (WCF) en la file d’attente de communication et comment envoyer des messages via HTTP. Le protocole MSMQ utilise le protocole SRMP basé sur le protocole SOAP pour communiquer sur HTTP.  
  
### <a name="to-set-up-build-and-run-the-sample"></a>Pour configurer, générer et exécuter l'exemple  
  
1.  Vérifiez que vous avez effectué la [procédure d’installation unique pour les exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).  
  
2.  Pour générer l’édition C# ou Visual Basic .NET de la solution, conformez-vous aux instructions figurant dans [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).  
  
3.  Pour exécuter l’exemple dans une configuration unique ou plusieurs ordinateurs, suivez les instructions de [en cours d’exécution les exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/running-the-samples.md).  
  
4.  Avant d’exécuter l’exemple **ajouter/supprimer des composants Windows**, assurez-vous que MSMQ est installé avec prise en charge HTTP. L'installation de la prise en charge HTTP installe automatiquement les services IIS et ajoute la prise en charge de ce protocole dans IIS pour MSMQ.  
  
5.  Si vous souhaitez vous assurer que le transport HTTP est bien utilisé pour la communication, configurez MSMQ de sorte à ce qu'il s'exécute en mode renforcé. Cela garantit qu'aucun message ne peut être transmis à une file d'attente hébergée sur l'ordinateur, quelle qu'elle soit, à l'aide d'un transport autre que HTTP.  
  
6.  Après avoir choisi d'exécuter MSMQ en mode renforcé, vous devez redémarrer l'ordinateur sur [!INCLUDE[ws2003](../../../../includes/ws2003-md.md)].  
  
7.  Exécutez le service.  
  
8.  Exécutez le client. Assurez-vous de remplacer les occurrences de localhost de l'adresse de point de terminaison par le nom de l'ordinateur ou l'adresse IP appropriée. Le client envoie un message, puis s'arrête.  
  
## <a name="requirements"></a>Configuration requise  
 Pour exécuter cet exemple, le protocole MSMQ ainsi que les services IIS doivent être installés sur l'ordinateur du client et celui du service.  
  
## <a name="demonstrates"></a>Démonstrations  
 L’exemple illustre l’envoi de WCF en file d’attente de messages à l’aide de MSMQ sur HTTP. Ce type de transmission est également appelé messagerie SRMP. Lorsqu'un message en file d'attente est envoyé, le protocole MSMQ sur l'ordinateur expéditeur transfère les messages vers le gestionnaire de files d'attente de réception via le transport TCP ou HTTP. Lorsque l'utilisateur sélectionne SRMP, cela signifie que le transport HTTP sera utilisé pour le transfert des messages vers la file d'attente. Le protocole SRMP Secure permet d'utiliser HTTPS.  
  
## <a name="example"></a>Exemple  
 L'exemple de code est basé sur l'exemple avec transaction. Les modalités d'envoi et de réception des messages à et depuis la file d'attente à l'aide du protocole SRMP sont identiques à celles utilisées pour l'envoi et la réception des messages à l'aide d'un protocole natif.  
  
 La configuration du client est modifiée en fonction du protocole de transfert vers la file d'attente souhaitée. Il peut s'agir de l'un des protocoles suivants : natif, SRMP ou SrmpSecure. Par défaut, le protocole de transfert correspond au protocole natif. Dans cet exemple, les configurations du client et du service spécifient l'utilisation du protocole SRMP.  
  
 Le protocole SRMP présente des restrictions en matière de sécurité de niveau transport. La sécurité de niveau transport MSMQ par défaut requiert Active Directory, lequel nécessite que les gestionnaires respectifs des files d'attente d'envoi et de réception figurent dans le même domaine Windows. Cette spécification n'est pas compatible avec l'envoi des messages sur la limite HTTP. Dans un tel cas, la sécurité de niveau transport par défaut ne peut pas fonctionner. La sécurité de niveau transport doit avoir pour valeur Certificat lorsqu'une telle sécurité est souhaitée. La sécurité de niveau message peut également être utilisée pour sécuriser les messages. Dans cet exemple, ces deux modes de sécurité sont tous deux désactivés afin d'illustrer le fonctionnement de la messagerie SRMP.  
  
```xml  
<?xml version="1.0" encoding="utf-8" ?>  
<configuration>  
  
  <system.serviceModel>  
  
    <client>  
      <!-- Define NetMsmqEndpoint -->  
      <endpoint name="OrderProcessorEndpoint"  
           address=  
          "net.msmq://localhost/private/ServiceModelSamplesSrmp"   
           bindingConfiguration="srmpBinding"   
           binding="netMsmqBinding"   
           contract="IOrderProcessor" />  
    </client>  
    <bindings>  
      <netMsmqBinding>  
        <binding name="srmpBinding"  
                 queueTransferProtocol="Srmp">  
          <security mode="None" />  
        </binding>  
      </netMsmqBinding>  
    </bindings>  
  </system.serviceModel>  
  
</configuration>  
```  
  
 L'exécution de l'exemple retourne le résultat suivant.  
  
```  
Processing Purchase Order: 556b70be-31ee-4a3b-8df4-ed5e538015a4   
Customer: somecustomer.com   
OrderDetails   
    Order LineItem: 54 of Blue Widget @unit price: $29.99   
    Order LineItem: 890 of Red Widget @unit price: $45.89   
    Total cost of this order: $42461.56   
    Order status: Pending  
```  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Binding\Net\MSMQ\SRMP`  
  
