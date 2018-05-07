---
title: 'Anticipation de l‘adoption de Windows Communication Foundation : faciliter la future migration'
ms.date: 03/30/2017
ms.assetid: f49664d9-e9e0-425c-a259-93f0a569d01b
ms.openlocfilehash: aeafc164d16d9dc60ad0b3012da292e9b0bb38b3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="anticipating-adopting-the-windows-communication-foundation-easing-future-migration"></a>Anticipation de l‘adoption de Windows Communication Foundation : faciliter la future migration
Afin de faciliter une future migration de nouvelles applications ASP.NET vers WCF, suivez les recommandations précédentes ainsi que les recommandations suivantes.  
  
## <a name="protocols"></a>Protocoles  
 Désactivez la prise en charge d'ASP.NET 2.0 pour SOAP 1.2 :  
  
```xml  
<configuration>  
     <system.web>  
      <webServices >  
          <protocols>  
           <remove name="HttpSoap12"/>  
          </protocols>    
      </webServices>  
     </system.web>   
</configuration>  
```  
  
 Cela est recommandé, car celui-ci requiert des messages qui se conforment à différents protocoles, tels que SOAP 1.1 et SOAP 1.2, pour accéder à l’aide de points de terminaison différents. Si Web ASP.NET 2.0 service est configuré pour prendre en charge SOAP 1.1 et SOAP 1.2, ce qui est la configuration par défaut, il ne peut pas être migré avant un point de terminaison WCF unique à l’adresse originale qui serait certainement être compatible avec l’ensemble du site Web ASP.NET clients existants du service. De plus, le choix de SOAP 1.2 au lieu de 1.1 restreint davantage la clientèle du service.  
  
## <a name="service-development"></a>Développement des services  
 WCF vous permet de définir des contrats de service en appliquant la <xref:System.ServiceModel.ServiceContractAttribute> aux interfaces ou aux classes. Il est recommandé d'appliquer l'attribut à une interface plutôt qu'à une classe, afin de créer une définition d'un contrat qui peut être implémenté de différentes façons par un nombre illimité de classes. ASP.NET 2.0 prend en charge la possibilité d'appliquer l'attribut <xref:System.Web.Services.WebService> aux interfaces aussi bien qu'aux classes. Toutefois, comme indiqué précédemment, ASP.NET 2.0 présente un défaut qui fait que le paramètre Namespace de l'attribut <xref:System.Web.Services.WebService> n'a aucun effet lorsque cet attribut est appliqué à une interface plutôt qu'à une classe. Dans la mesure où il est généralement recommandé de modifier l’espace de noms d’un service à partir de la valeur par défaut, http://tempuri.org, en utilisant le paramètre Namespace de le <xref:System.Web.Services.WebService> attribut, il faut continuer la définition des Services Web ASP.NET en appliquant la <xref:System.ServiceModel.ServiceContractAttribute> attribut aux interfaces ou aux classes.  
  
-   Les méthodes chargées de définir ces interfaces doivent contenir un minimum de code. Faites-les déléguer leur tâche à d'autres classes. Nouveaux types de service WCF peuvent aussi déléguer les tâches importantes à ces classes.  
  
-   Fournissez des noms explicites pour les opérations d'un service à l'aide du paramètre `MessageName` de <xref:System.Web.Services.WebMethodAttribute>.  
  
    ```  
    [WebMethod(MessageName="ExplicitName")]  
    string Echo(string input);  
    ```  
  
     Cela est important, car les noms par défaut pour les opérations dans ASP.NET sont différents des noms par défaut fournies par WCF. En fournissant des noms explicites, vous n'avez pas à vous reposer sur les noms par défaut.  
  
-   N’implémentez pas les opérations de service Web ASP.NET avec des méthodes polymorphes, étant donné que WCF ne prend pas en charge l’implémentation des opérations avec des méthodes polymorphes.  
  
-   Utilisez le <xref:System.Web.Services.Protocols.SoapDocumentMethodAttribute> afin de fournir des valeurs explicites pour les en-têtes HTTP SOAPAction chargés d'acheminer les demandes HTTP aux méthodes.  
  
    ```  
    [WebMethod]  
    [SoapDocumentMethod(RequestElementName="ExplicitAction")]  
    string Echo(string input);  
    ```  
  
     Cette approche résoudra devoir compter sur la valeur par défaut des valeurs SOAPAction utilisés par ASP.NET et WCF qui sont identiques.  
  
-   Évitez l’utilisation des extensions SOAP. Si les extensions SOAP sont requises, déterminez si le but pour lequel elles sont envisagées est une fonctionnalité déjà fournie par WCF. Si tel est le cas, reconsidérez le choix de ne pas adopter WCF immédiatement.  
  
## <a name="state-management"></a>Gestion des états  
 Évitez de devoir maintenir l'état dans les services. Non seulement conserver l’état sont susceptibles de compromettre l’évolutivité d’une application, mais les mécanismes de gestion de l’état d’ASP.NET et WCF sont très différents, bien que WCF ne prend pas en charge les mécanismes ASP.NET en mode de compatibilité ASP.NET.  
  
## <a name="exception-handling"></a>Gestion des exceptions  
 Lors de la conception des structures des types de données à envoyer et à recevoir par un service, concevez aussi des structures pour représenter les divers types d'exceptions qui peuvent se produire dans un service et qu'il faut décrire éventuellement à un client.  
  
```  
[Serializable]  
[XmlRoot(  
     Namespace="ExplicitNamespace", IsNullable=true)]  
    public partial class AnticipatedException {  
  
     private string anticipatedExceptionInformationField;  
  
     public string AnticipatedExceptionInformation {  
      get {  
          return this.anticipatedExceptionInformationField;  
          }  
      set {  
          this.anticipatedExceptionInformationField = value;  
          }  
     }  
}  
```  
  
 Donnez à ces classes la possibilité de se sérialiser en code XML :  
  
```  
public XmlNode ToXML()  
{  
     XmlSerializer serializer = new XmlSerializer(  
      typeof(AnticipatedException));  
     MemoryStream memoryStream = new MemoryStream();  
     XmlTextWriter writer = new XmlTextWriter(  
     memoryStream, UnicodeEncoding.UTF8);  
     serializer.Serialize(writer, this);  
     XmlDocument document = new XmlDocument();  
     document.LoadXml(new string(  
     UnicodeEncoding.UTF8.GetChars(  
     memoryStream.GetBuffer())).Trim());  
    return document.DocumentElement;  
}  
```  
  
 Ces classes peuvent ensuite servir à fournir les détails pour les instances <xref:System.Web.Services.Protocols.SoapException> levées explicitement :  
  
```  
AnctipatedException exception = new AnticipatedException();  
exception.AnticipatedExceptionInformation = "…";  
throw new SoapException(  
     "Fault occurred",  
     SoapException.ClientFaultCode,  
     Context.Request.Url.AbsoluteUri,  
     exception.ToXML());  
```  
  
 Ces classes d’exceptions sera réutilisables avec WCF<xref:System.ServiceModel.FaultException%601> pour lever une nouvelle classe `FaultException<AnticipatedException>(anticipatedException);`  
  
## <a name="security"></a>Sécurité  
 Les éléments suivants sont des recommandations de sécurité.  
  
-   Éviter à l’aide de profils ASP.NET 2.0, car leur utilisation peut restreindre l’utilisation du Mode intégration ASP.NET si le service a été migré vers WCF.  
  
-   Évitez d’utiliser des ACL pour contrôler l’accès aux services, en tant que services Web ASP.NET prend en charge les ACL à l’aide d’Internet Information Services (IIS), n’est pas le cas de WCF, étant donné que les services Web ASP.NET dépendent d’IIS pour l’hébergement et WCF ne doit pas nécessaire être hébergés dans IIS.  
  
-   Vous pouvez faire appel à des fournisseurs de rôles ASP.NET 2.0 pour autoriser l'accès aux ressources d'un service.  
  
## <a name="see-also"></a>Voir aussi  
 [Anticipation de l’adoption de Windows Communication Foundation : faciliter l’intégration future](../../../../docs/framework/wcf/feature-details/anticipating-adopting-the-wcf-easing-future-integration.md)
