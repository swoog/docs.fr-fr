---
title: Contrats
ms.date: 03/30/2017
helpviewer_keywords:
- WCF [WCF], contracts
- contracts [WCF]
- Windows Communication Foundation [WCF], contracts
ms.assetid: c8364183-4ac1-480b-804a-c5e6c59a5d7d
ms.openlocfilehash: 839f7790a5dd300313931672c60e7826af39aeea
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64651101"
---
# <a name="contracts"></a>Contrats
Cette section vous montre comment définir et implémenter des contrats de Windows Communication Foundation (WCF). Un contrat de service spécifie ce qu'un point de terminaison communique au monde extérieur. À un niveau plus concret, il s'agit d'une instruction à propos d'un ensemble de messages spécifiques organisé en modèles d'échange de messages de base, tels que les messages demande/réponse, unidirectionnels et duplex. Si un contrat de service est un ensemble d'échanges de messages liés de manière logique, une opération de service est un échange de messages unique. Par exemple, une opération `Hello` doit évidemment accepter un message (de sorte que l'appelant puisse annoncer la salutation) et peut ou non retourner un message (en fonction du niveau de courtoisie de l'opération).  
  
 Pour plus d’informations sur les contrats et autres concepts WCF, consultez [Concepts fondamentaux Windows Communication Foundation](../../../../docs/framework/wcf/fundamental-concepts.md). Cette rubrique est consacrée au fonctionnement des contrats de service. Pour plus d’informations sur la création de clients qui utilisent des contrats de service pour se connecter aux services, consultez [WCF Client Overview](../../../../docs/framework/wcf/wcf-client-overview.md). Pour plus d’informations sur les canaux clients, l’architecture du client et d’autres problèmes de client, consultez [Clients](../../../../docs/framework/wcf/feature-details/clients.md).  
  
## <a name="overview"></a>Vue d'ensemble  
 Cette rubrique fournit une orientation conceptuelle de haut niveau à la conception et implémentation des services WCF. Les sous-rubriques fournissent des informations plus détaillées sur les aspects spécifiques à la conception et à l'implémentation. Avant de concevoir et implémenter votre application WCF, il est recommandé que vous avez :  
  
- comprendre ce qu'est un contrat de service, comment il fonctionne et comment en créer un ;  
  
- comprendre que les contrats définissent des exigences minimales que la configuration à l’exécution ou l’environnement d’hébergement peuvent ne pas prendre en charge.  
  
## <a name="service-contracts"></a>Contrats de service  
 Un contrat de service est une instruction qui fournit des informations sur :  
  
- le groupement d'opérations dans un service ;  
  
- la signature des opérations en termes de messages échangés ;  
  
- les types de données de ces messages ;  
  
- l'emplacement des opérations ;  
  
- les protocoles et formats de sérialisation spécifiques utilisés pour prendre en charge la communication avec le service.  
  
 Par exemple, un contrat de commande fournisseur peut avoir une opération `CreateOrder` qui accepte une entrée de types d'informations de commande et retourne des information de succès ou d'échec, y compris un identificateur de commande. Il peut également avoir une opération `GetOrderStatus` qui accepte un identificateur de commande et retourne des informations d'état de commande. Un tel contrat de service spécifie alors :  
  
- que le contrat de commande fournisseur serait composé d'opérations `CreateOrder` et `GetOrderStatus` ;  
  
- que les opérations auraient des messages d'entrée et des messages de sortie spécifiés ;  
  
- les données que ces messages pourraient transporter ;  
  
- des instructions catégoriques à propos de l'infrastructure de communication nécessaire pour traiter les messages avec succès. Par exemple, ces détails incluent les éventuelles formes de sécurité requises pour établir la communication.  
  
 Pour communiquer ce type d’informations à des applications sur d’autres plateformes (y compris les plateformes non-Microsoft), les contrats de service XML sont exprimés publiquement dans des formats XML standards, tels que [Web Services Description Language (WSDL)](https://go.microsoft.com/fwlink/?LinkId=87004) et [XSD (XML Schema)](https://go.microsoft.com/fwlink/?LinkId=87005), entre autres. Les développeurs qui travaillent avec un grand nombre de plateformes différentes peuvent utiliser ces informations de contrat publiques pour créer des applications capables de communiquer avec le service, ces applications comprenant le langage des spécifications, d'une part, et ce langage assurant l'interopérabilité grâce à sa description de formes, formats et protocoles publics pris en charge par ce service, d'autre part. Pour plus d’informations sur la façon dont WCF gère ce type d’informations, consultez [métadonnées](../../../../docs/framework/wcf/feature-details/metadata.md).  
  
 Les contrats peuvent toutefois être exprimés de nombreuses manières, et bien que WSDL et XSD constituent d'excellents langages pour décrire des services d'une manière accessible, ce sont des langages difficiles à utiliser directement ; en tous les cas, ils constituent simplement des descriptions d'un service, et non des implémentations de contrat de service. Par conséquent, les applications WCF utilisent attributs managés, des interfaces et des classes pour définir la structure d’et d’implémenter un service.  
  
 Le contrat résultant défini dans les types managés peut être converti (également appelé *exporté*) en tant que métadonnées : WSDL et XSD, si nécessaire, en les clients ou d’autres implémenteurs de service, en particulier sur d’autres plateformes. Le résultat est un modèle de programmation simple qui peut être décrit à l'aide de métadonnées publiques à toute application cliente. Les détails des messages SOAP sous-jacents, tels que le transport et les informations relatives à la sécurité, peuvent être conservés à WCF, qui effectue automatiquement les conversions nécessaires vers et depuis le système de type de contrat de service pour le système de type XML.  
  
 Pour plus d’informations sur la conception de contrats, consultez [Designing Service Contracts](../../../../docs/framework/wcf/designing-service-contracts.md). Pour plus d’informations sur l’implémentation de contrats, consultez [Implementing Service Contracts](../../../../docs/framework/wcf/implementing-service-contracts.md).  
  
 En outre, WCF fournit également la possibilité de développer des contrats de service entièrement au niveau du message. Pour plus d’informations sur le développement des contrats de service au niveau du message, consultez [Using Message Contracts](../../../../docs/framework/wcf/feature-details/using-message-contracts.md). Pour plus d’informations sur le développement de services dans XML SOAP, consultez [l’interopérabilité avec les Applications POX](../../../../docs/framework/wcf/feature-details/interoperability-with-pox-applications.md).  
  
### <a name="understanding-the-hierarchy-of-requirements"></a>Présentation de la hiérarchie des exigences  
 Un contrat de service groupe les opérations, spécifie les modèles d'échange de messages, les types de messages et les types de données que ces messages transportent, et indique les catégories de comportement à l'exécution qu'une implémentation doit avoir pour prendre en charge le contrat (par exemple, il peut exiger que les messages soient chiffrés et signés). Toutefois, le contrat de service lui-même ne spécifie pas précisément comment ces exigences sont satisfaites, mais uniquement qu’elles doivent l’être. Le type de chiffrement utilisé ou la façon dont un message est signé incombe à l'implémentation et à la configuration d'un service conforme.  
  
 Remarquez la façon dont le contrat requiert certaines choses de l'implémentation de contrat de service et de la configuration à l'exécution pour ajouter un comportement. L’ensemble d’exigences qui doivent être satisfaites pour exposer un service pour une utilisation repose sur l’ensemble d’exigences précédent. Si un contrat spécifie des exigences concernant l'implémentation, une implémentation peut requérir une plus grande partie de la configuration et des liaisons qui autorisent l'exécution du service. Pour finir, l’application hôte doit également prendre en charge les exigences ajoutées par la configuration du service et les liaisons.  
  
 Ce processus d’exigence additif est important à prendre en compte lors de la conception, l’implémentation, configuration et hébergement de votre application de service Windows Communication Foundation (WCF). Par exemple, le contrat peut spécifier qu'il doit prendre en charge une session. Dans ce cas, vous devez configurer la liaison de façon à prendre en charge cette spécification contractuelle, sinon l’implémentation de service ne fonctionnera pas. Si votre service requiert l'authentification intégrée de Windows et qu'il est hébergé par les services IIS, l'option Authentification intégrée de Windows de l'application Web dans laquelle se trouve le service doit être activée et l'option de prise en charge anonyme doit être désactivée. Pour plus d’informations sur les fonctionnalités et l’impact des types d’application hôte service différent, consultez [hébergement](../../../../docs/framework/wcf/feature-details/hosting.md).  
  
## <a name="see-also"></a>Voir aussi

- [Points de terminaison : Adresses, liaisons et contrats](../../../../docs/framework/wcf/feature-details/endpoints-addresses-bindings-and-contracts.md)
- [Conception de contrats de service](../../../../docs/framework/wcf/designing-service-contracts.md)
- [Implémentation de contrats de service](../../../../docs/framework/wcf/implementing-service-contracts.md)
