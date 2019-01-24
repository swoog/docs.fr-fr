---
title: Transfert de données et sérialisation
ms.date: 03/30/2017
helpviewer_keywords:
- data serialization [WCF]
- data transfer [WCF]
ms.assetid: 0f03c635-f3e7-4c5c-9463-3cb0135e221e
ms.openlocfilehash: 5192030fa2eda45431dd8a3765603d3081b93fa3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54595316"
---
# <a name="data-transfer-and-serialization"></a>Transfert de données et sérialisation
Dans un système connecté, les services et les clients se reposent sur l’échange de données pour accomplir une tâche. En tant que développeur d’un service ou d’un client, vous devez également comprendre comment Windows Communication Foundation (WCF) gère les données et la sérialisation de données afin de créer des applications qui sont efficaces et faciles à gérer.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Spécification du transfert de données dans des contrats de service](../../../../docs/framework/wcf/feature-details/specifying-data-transfer-in-service-contracts.md)  
 Décrit les concepts de base du transfert de données dans les services.  
  
 [Utilisation de contrats de données](../../../../docs/framework/wcf/feature-details/using-data-contracts.md)  
 Définit les contrats de données et la méthode utilisée pour les créer et les utiliser.  
  
 [Sérialiseur de contrat de données](../../../../docs/framework/wcf/feature-details/data-contract-serializer.md)  
 Décrit comment accomplir la sérialisation des données avec la classe <xref:System.Runtime.Serialization.DataContractSerializer> ou une extension de la classe <xref:System.Runtime.Serialization.XmlObjectSerializer>.  
  
 [Utilisation de la classe XmlSerializer](../../../../docs/framework/wcf/feature-details/using-the-xmlserializer-class.md)  
 Décrit comment et pourquoi utiliser la classe <xref:System.Xml.Serialization.XmlSerializer>, une alternative à la classe <xref:System.Runtime.Serialization.DataContractSerializer>.  
  
 [Utilisation de contrats de message](../../../../docs/framework/wcf/feature-details/using-message-contracts.md)  
 Décrit comment les contrats de message autorisent un contrôle pointu sur les messages SOAP.  
  
 [Utilisation de la classe de message](../../../../docs/framework/wcf/feature-details/using-the-message-class.md)  
 Décrit comment utiliser les fonctionnalités de la classe Message.  
  
 [Filtrage](../../../../docs/framework/wcf/feature-details/filtering.md)  
 Décrit le filtrage qui permet le pré-traitement d'un message selon différents critères.  
  
 [Données volumineuses et streaming](../../../../docs/framework/wcf/feature-details/large-data-and-streaming.md)  
 Décrit comment envoyer un grand bloc de données, tel qu'un fichier binaire.  
  
 [Considérations sur la sécurité des données](../../../../docs/framework/wcf/feature-details/security-considerations-for-data.md)  
 Décrit des éléments à connaître lors de la programmation du transfert de données et de la sérialisation.  
  
 [Vue d’ensemble de l’architecture de transfert de données](../../../../docs/framework/wcf/feature-details/data-transfer-architectural-overview.md)  
 Décrit une vue de la conception globale de transfert de données dans WCF.  
  
## <a name="reference"></a>Référence  
 <xref:System.ServiceModel>  
  
 <xref:System.Runtime.Serialization.DataContractSerializer>  
  
 <xref:System.Xml.Serialization.XmlSerializer>  
  
 <xref:System.Runtime.Serialization>  
  
 <xref:System.Xml.Serialization>  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Extension des encodeurs et des sérialiseurs](../../../../docs/framework/wcf/extending/extending-encoders-and-serializers.md)  
  
## <a name="see-also"></a>Voir aussi
- [Meilleures pratiques : Concernant les contrats de données](../../../../docs/framework/wcf/best-practices-data-contract-versioning.md)
- [Gestion des versions des services](../../../../docs/framework/wcf/service-versioning.md)
