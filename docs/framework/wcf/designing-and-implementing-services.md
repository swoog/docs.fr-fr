---
title: Conception et implémentation de services
ms.date: 03/30/2017
helpviewer_keywords:
- defining service contracts [WCF]
ms.assetid: 036fae20-7c55-4002-b71d-ac4466e167a3
ms.openlocfilehash: ad7e713ac4cbbe5bf227f4ab93e8f88684dcb0d3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61785019"
---
# <a name="designing-and-implementing-services"></a>Conception et implémentation de services
Cette section vous montre comment définir et implémenter des contrats WCF. Un contrat de service spécifie ce qu'un point de terminaison communique au monde extérieur. À un niveau plus concret, il s'agit d'une instruction à propos d'un ensemble de messages spécifiques organisé en modèles d'échange de messages de base, tels que les messages demande/réponse, unidirectionnels et duplex. Si un contrat de service est un ensemble d'échanges de messages liés de manière logique, une opération de service est un échange de messages unique. Par exemple, une opération `Hello` doit évidemment accepter un message (de sorte que l'appelant puisse annoncer la salutation) et peut ou non retourner un message (en fonction du niveau de courtoisie de l'opération).  
  
 Pour plus d’informations sur les contrats et autres concepts de Windows Communication Foundation (WCF), consultez [Concepts fondamentaux Windows Communication Foundation](../../../docs/framework/wcf/fundamental-concepts.md). Cette rubrique est consacrée au fonctionnement des contrats de service. Pour plus d’informations sur la création de clients qui utilisent des contrats de service pour se connecter aux services, consultez [WCF Client Overview](../../../docs/framework/wcf/wcf-client-overview.md).  
  
## <a name="overview"></a>Vue d'ensemble  
 Cette rubrique fournit une orientation conceptuelle de haut niveau à la conception et implémentation des services WCF. Les sous-rubriques contiennent des informations détaillées sur les particularités de ce type de conception et d'implémentation. Avant de concevoir et implémenter votre application WCF, il est recommandé que vous avez :  
  
- comprendre ce qu'est un contrat de service, comment il fonctionne et comment en créer un ;  
  
- comprendre que les contrats définissent des exigences minimales susceptibles de ne pas être prises en charge par la configuration d’exécution et l’environnement d’hébergement.  
  
## <a name="service-contracts"></a>Contrats de service  
 Un contrat de service spécifie les éléments suivants :  
  
- les opérations qu'un contrat expose ;  
  
- la signature des opérations en termes de messages échangés ;  
  
- les types de données de ces messages ;  
  
- l'emplacement des opérations ;  
  
- les protocoles et formats de sérialisation spécifiques utilisés pour prendre en charge la communication avec le service.  
  
 Par exemple, un contrat de commande fournisseur peut avoir une opération `CreateOrder` qui accepte une entrée de types d'informations de commande et retourne des information de succès ou d'échec, y compris un identificateur de commande. Il peut également avoir une opération `GetOrderStatus` qui accepte un identificateur de commande et retourne des informations d'état de commande. Un tel contrat de service spécifie alors :  
  
1. que le contrat de commande fournisseur serait composé d'opérations `CreateOrder` et `GetOrderStatus` ;  
  
2. que les opérations auraient des messages d'entrée et des messages de sortie spécifiés ;  
  
3. les données que ces messages pourraient transporter ;  
  
4. des instructions catégoriques à propos de l'infrastructure de communication nécessaire pour traiter les messages avec succès. Par exemple, ces détails incluent les éventuelles formes de sécurité requises pour établir la communication.  
  
 Pour communiquer ce type d’informations à d’autres applications sur de nombreuses plateformes (y compris les plateformes non-Microsoft), les contrats de service XML sont exprimés publiquement dans des formats XML standards, tels que [Web Services Description Language](https://go.microsoft.com/fwlink/?LinkId=94952) () WSDL) et [schéma XML](https://go.microsoft.com/fwlink/?LinkId=94953) (XSD), entre autres. Les développeurs qui travaillent avec un grand nombre de plateformes différentes peuvent utiliser ces informations de contrat publiques pour créer des applications capables de communiquer avec le service, ces applications comprenant le langage des spécifications, d'une part, et ce langage assurant l'interopérabilité grâce à sa description de formes, formats et protocoles publics pris en charge par ce service, d'autre part. Pour plus d’informations sur la façon dont WCF gère ce type d’informations, consultez [métadonnées](../../../docs/framework/wcf/feature-details/metadata.md).  
  
 Les contrats peuvent être exprimés dans un grand nombre de langages différents et bien que WSDL et XSD constituent d'excellents langages pour décrire des services de manière accessible, ce sont des langages difficiles à utiliser directement. En outre, ils contiennent uniquement des descriptions de service et ne correspondent pas à des implémentations de contrat de service. Par conséquent, les applications WCF utilisent les attributs managés, des interfaces et des classes pour définir la structure d’un service et mettre en œuvre.  
  
 Le contrat résultant défini dans les types managés peut être *exporté* en tant que métadonnées : WSDL et XSD, si nécessaire, en les clients ou d’autres implémenteurs de service. Le résultat est un modèle de programmation simple qui peut être décrit (à l'aide de métadonnées publiques) à toute application cliente. Les détails des messages SOAP sous-jacents, le transport et informations relatives à la sécurité et ainsi de suite, peuvent être conservés à WCF, qui effectue automatiquement les conversions nécessaires vers et depuis le système de type de contrat de service pour le système de type XML.  
  
 Pour plus d’informations sur la conception de contrats, consultez [Designing Service Contracts](../../../docs/framework/wcf/designing-service-contracts.md). Pour plus d’informations sur l’implémentation de contrats, consultez [Implementing Service Contracts](../../../docs/framework/wcf/implementing-service-contracts.md).  
  
### <a name="messages-up-front-and-center"></a>Messages avant et centre  
 L'utilisation d'interfaces, de classes et de méthodes managées pour modeler des opérations de service ne pose aucune difficulté dès lors que vous êtes familiarisé avec les signatures de méthode de style « appels de procédure distante » (remote call procedure, RPC), pour lesquelles le passage des paramètres dans les méthodes et la réception des valeurs retournées constituent le procédé standard de demande de fonctionnalités auprès d'un objet ou d'un autre type de code. Par exemple, les programmeurs qui utilisent des langages managés tels que Visual Basic et C++ COM peuvent appliquer leur connaissance de l’approche de style RPC (qu’il soit à l’aide des objets ou des interfaces) pour la création de contrats de service WCF sans rencontre des problèmes inhérents à RPC-style distribué des systèmes de l’objet. La programmation orientée service présente les mêmes avantages que la programmation orientée message faiblement couplée tout en permettant aux développeurs de continuer à bénéficier de la convivialité de la programmation RPC.  
  
 De nombreux programmeurs préfèrent les interfaces de programmation d'application orientées message, telles que les files d'attente de messages comme Microsoft MSMQ, les espaces de noms <xref:System.Messaging> dans le .NET Framework ou l'envoi sous forme de langage XML non structuré dans les requêtes HTTP, pour n'en nommer que quelques-unes. Pour plus d’informations sur la programmation au niveau du message, consultez [Using Message Contracts](../../../docs/framework/wcf/feature-details/using-message-contracts.md), [de programmation au niveau du canal de Service](../../../docs/framework/wcf/extending/service-channel-level-programming.md), et [l’interopérabilité avec les Applications POX](../../../docs/framework/wcf/feature-details/interoperability-with-pox-applications.md).  
  
### <a name="understanding-the-hierarchy-of-requirements"></a>Présentation de la hiérarchie des exigences  
 Un contrat de service regroupe les opérations, spécifie le modèle d'échange de messages, les types de messages et les types de données transportés par ces messages et indique les catégories de comportements que l'implémentation doit pouvoir adopter en cours d'exécution pour assurer la prise en charge du contrat (il peut, par exemple, s'agir des comportements en matière de chiffrement et de signature des messages). Le contrat de service proprement dit ne spécifie pas précisément comment ces spécifications sont satisfaites, mais uniquement qu'elles doivent l'être. Le type de chiffrement ou la manière dont un message doit être signé incombent à l'implémentation et à la configuration des services concernés.  
  
 Remarquez la façon dont le contrat requiert certaines choses de l'implémentation de contrat de service et de la configuration à l'exécution pour ajouter un comportement. L’ensemble d’exigences qui doivent être satisfaites pour exposer un service pour une utilisation repose sur l’ensemble d’exigences précédent. Si un contrat spécifie des exigences concernant l'implémentation, une implémentation peut requérir une plus grande partie de la configuration et des liaisons qui autorisent l'exécution du service. Pour finir, l’application hôte doit également prendre en charge les exigences ajoutées par la configuration du service et les liaisons.  
  
 Ce processus d’exigence additif est important à prendre en compte lors de la conception, l’implémentation, configuration et hébergement d’une application de service Windows Communication Foundation (WCF). Par exemple, le contrat peut spécifier qu'il doit prendre en charge une session. Dans ce cas, vous devez configurer la liaison de façon à prendre en charge cette spécification contractuelle, sinon l’implémentation de service ne fonctionnera pas. Si votre service requiert l'authentification intégrée Windows (Windows Integrated Authentification, WIA) et qu'il est hébergé par les services IIS, l'option WIA de l'application Web dans laquelle se trouve le service doit être activée et l'option de prise en charge anonyme doit être désactivée. Pour plus d’informations sur les fonctionnalités et l’impact des types d’application hôte service différent, consultez [Services d’hébergement](../../../docs/framework/wcf/hosting-services.md).  
  
## <a name="see-also"></a>Voir aussi

- [Conception de contrats de service](../../../docs/framework/wcf/designing-service-contracts.md)
- [Implémentation de contrats de service](../../../docs/framework/wcf/implementing-service-contracts.md)
