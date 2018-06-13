---
title: Interopérabilité avec les services Web ASP.NET
ms.date: 03/30/2017
ms.assetid: 622422f8-6651-442f-b8be-e654a4aabcac
ms.openlocfilehash: 8a0737a36989dd8bc6f5d5670555c7b2218798bb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33494294"
---
# <a name="interoperability-with-aspnet-web-services"></a>Interopérabilité avec les services Web ASP.NET
L’interopérabilité entre [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] services Web et les services Web de Windows Communication Foundation (WCF) peuvent être obtenus en garantissant que les services implémentés à l’aide de ces deux technologies conforment à WS-I Basic Profile 1.1 spécification. [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] Les services Web qui se conforment à WS-I Basic Profile 1.1 sont interopérables avec les clients WCF à l’aide d’une liaison WCF fournie par le système, <xref:System.ServiceModel.BasicHttpBinding>.  
  
 Utilisez l'option [!INCLUDE[vstecasplong](../../../../includes/vstecasplong-md.md)] d'ajout des attributs <xref:System.Web.Services.WebService> et <xref:System.Web.Services.WebMethodAttribute> à une interface plutôt qu'à une classe et d'écriture d'une classe pour implémenter l'interface, comme le montre l'exemple de code suivant.  
  
```  
[WebService]  
public interface IEcho  
{  
    [WebMethod]  
    string Echo(string input);  
}  
  
public class Service : IEcho  
{  
  
   public string Echo(string input)  
   {  
        return input;  
    }  
}  
```  
  
 L'utilisation de cette option est recommandée, car l'interface avec l'attribut <xref:System.Web.Services.WebService> constitue un contrat pour les opérations exécutées par le service qui peut être réutilisé avec différentes classes, qui peuvent implémenter ce même contrat de différentes façons.  
  
 Évitez d'utiliser l'attribut <xref:System.Web.Services.Protocols.SoapDocumentServiceAttribute> pour router des messages vers des méthodes basées sur le nom qualifié complet de l'élément de corps du message SOAP plutôt que l'en-tête HTTP `SOAPAction`. WCF utilise le `SOAPAction` en-tête HTTP pour acheminer les messages.  
  
 Le XML dans lequel <xref:System.Xml.Serialization.XmlSerializer> sérialise un type par défaut est sémantiquement identique au XML dans lequel <xref:System.Runtime.Serialization.DataContractSerializer> sérialise un type, à condition que l'espace de noms du XML soit défini explicitement. Lors de la définition d’un type de données pour une utilisation avec [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)]Web des services en prévision de l’adoption de WCF, procédez comme suit :  
  
-   Définissez le type à l'aide des classes .NET Framework plutôt que XML Schema.  
  
-   Ajoutez uniquement <xref:System.SerializableAttribute> et <xref:System.Xml.Serialization.XmlRootAttribute> à la classe, en utilisant ce dernier pour définir explicitement l'espace de noms du type. N'ajoutez pas d'attribut supplémentaire à partir de l'espace de noms <xref:System.Xml.Serialization> pour contrôler la manière dont la classe .NET Framework sera traduite dans XML.  
  
-   En adoptant cette approche, vous devez être en mesure de créer ultérieurement les classes .NET dans des contrats de données avec l'ajout de <xref:System.Runtime.Serialization.DataContractAttribute> et <xref:System.Runtime.Serialization.DataMemberAttribute> sans modifier de manière significative le XML dans lequel les classes sont sérialisées pour la transmission. Les types utilisés dans les messages par [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] services Web peuvent être traitées comme des contrats de données par les applications WCF, en offrant, entre autres avantages, de meilleures performances dans les applications WCF.  
  
 Évitez d'utiliser les options d'authentification fournies par des services IIS (Internet Information Services). Clients WCF ne prennent pas en charge les. Si un service doit être sécurisé, utilisez les options fournies par WCF, car ces options sont fiables et sont basées sur des protocoles standard.  
  
## <a name="performance-impact-caused-by-loading-the-servicemodel-httpmodule"></a>Impact sur les performances causé par le chargement de ServiceModel HttpModule  
 Dans le .NET Framework 3.0, `HttpModule` WCF a été installé dans le fichier Web.config racine pour que chaque application ASP.NET soit compatible WCF. Cela peut affecter les performances, vous pouvez donc supprimer  `ServiceModel` pour le fichier Web.config comme illustré dans l'exemple suivant.  
  
```xml  
<httpModules>  
    <remove name="ServiceModel" />  
<httpModules/>  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Guide pratique pour configurer le service WCF pour interagir avec des clients du service web ASP.NET](../../../../docs/framework/wcf/feature-details/config-wcf-service-with-aspnet-web-service.md)
