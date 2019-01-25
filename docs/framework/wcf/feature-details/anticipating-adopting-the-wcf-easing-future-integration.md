---
title: 'Anticipation de l’adoption de Windows Communication Foundation : Faciliter l’intégration Future'
ms.date: 03/30/2017
ms.assetid: 3028bba8-6355-4ee0-9ecd-c56e614cb474
ms.openlocfilehash: c20011c6cf7a31d8c45769b6995bb6754088bba6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54731281"
---
# <a name="anticipating-adopting-the-windows-communication-foundation-easing-future-integration"></a>Anticipation de l’adoption de Windows Communication Foundation : Faciliter l’intégration Future
Si vous utilisez ASP.NET aujourd'hui et que vous prévoyez d’utiliser WCF à l’avenir, cette rubrique fournit des conseils pour vous assurer que les nouveaux services Web ASP.NET fonctionneront également avec les applications WCF.  
  
## <a name="general-recommendations"></a>Recommandations générales  
 Adoptez ASP.NET 2.0 pour les nouveaux services. Vous pourrez ainsi accéder aux améliorations et enrichissements de la nouvelle version. Toutefois, elle permettra également de la possibilité d’utiliser des composants ASP.NET 2.0 ainsi que des composants WCF dans la même application.  
  
## <a name="protocols"></a>Protocoles  
 Utilisez la nouvelle fonctionnalité d'ASP.NET 2.0 pour valider la conformité au profil WS-I Basic Profile 1.1 :  
  
```csharp  
[WebService(Namespace = "http://tempuri.org/")]  
[WebServiceBinding(  
     ConformsTo = WsiProfiles.BasicProfile1_1,  
     EmitConformanceClaims=true)]  
public interface IEcho  
```  
  
 Les services Web ASP.NET qui se conforment à WS-I Basic Profile 1.1 seront interopérable avec les clients WCF à l’aide de liaison, WCF prédéfinie <xref:System.ServiceModel.BasicHttpBinding>.  
  
## <a name="service-development"></a>Développement des services  
 Évitez d'utiliser l'attribut <xref:System.Web.Services.Protocols.SoapDocumentServiceAttribute> pour router des messages vers des méthodes basées sur le nom qualifié complet de l'élément de corps du message SOAP plutôt que l'en-tête HTTP SOAPAction. WCF utilise l’en-tête HTTP SOAPAction pour router des messages.  
  
## <a name="data-representation"></a>Représentation des données  
 Le XML dans lequel <xref:System.Xml.Serialization.XmlSerializer> sérialise un type par défaut est sémantiquement identique au XML dans lequel <xref:System.Runtime.Serialization.DataContractSerializer> sérialise un type, à condition que l'espace de noms du XML soit défini explicitement. Lorsque vous définissez un type de données pour une utilisation avec les services Web ASP.NET en prévision d’adoption WCF à l’avenir, procédez comme suit :  
  
1.  Définissez le type à l'aide des classes .NET Framework plutôt que XML Schema.  
  
2.  Ajoutez uniquement <xref:System.SerializableAttribute> et <xref:System.Xml.Serialization.XmlRootAttribute> à la classe, en utilisant ce dernier pour définir explicitement l'espace de noms du type. N'ajoutez pas d'attribut supplémentaire à partir de l'espace de noms <xref:System.Xml.Serialization> pour contrôler la manière dont la classe .NET Framework sera traduite dans XML.  
  
 En adoptant cette approche, vous devez être en mesure de créer ultérieurement les classes .NET dans des contrats de données avec l'ajout de <xref:System.Runtime.Serialization.DataContractAttribute> et <xref:System.Runtime.Serialization.DataMemberAttribute> sans modifier de manière significative le XML dans lequel les classes sont sérialisées pour la transmission. Les types utilisés dans les messages par les services Web ASP.NET sera en mesure d’être traités comme des contrats de données par les applications WCF, offrant, entre autres avantages, de meilleures performances dans les applications WCF.  
  
## <a name="security"></a>Sécurité  
 Évitez d'utiliser les options d'authentification fournies par des services IIS (Internet Information Services). Les clients WCF ne prennent pas en charge les. Si un service doit être sécurisé, utilisez les options fournies par WCF, car ces options sont plus riches et sont basées sur des protocoles standard.  
  
## <a name="see-also"></a>Voir aussi
- [Anticipation de l’adoption de Windows Communication Foundation : Faciliter la Migration Future](../../../../docs/framework/wcf/feature-details/anticipating-adopting-wcf-migration.md)
