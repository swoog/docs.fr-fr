---
title: Formats de métadonnées
ms.date: 03/30/2017
ms.assetid: baad1e68-28fc-4a6a-8a43-75e47e7fa871
ms.openlocfilehash: a3c6b1f551d1bff8c68a91f33e62df289d2078cc
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="metadata-formats"></a>Formats de métadonnées
Windows Communication Foundation (WCF) prend en charge les formats de métadonnées dans le tableau suivant.  
  
## <a name="metadata-specifications-and-usage"></a>Spécification et utilisation des métadonnées  
  
|Protocole|Spécification et utilisation|  
|--------------|-----------------------------|  
|WSDL 1.1|[Web Services Description Language (WSDL) 1.1](http://go.microsoft.com/fwlink/?LinkId=94859)<br /><br /> WCF utilise Web Services Description Language (WSDL) pour décrire des services.|  
|Schéma XML|[XML Schema Part 2 : Datatypes Second Edition](http://go.microsoft.com/fwlink/?LinkId=94861) et [XML Schema Part 1 : Structures, deuxième édition](http://go.microsoft.com/fwlink/?LinkId=94862)<br /><br /> WCF utilise le schéma XML pour décrire les types de données utilisés dans les messages.|  
|WS-Policy|[Stratégie de Services Web 1.2 - infrastructure (WS-Policy)](http://go.microsoft.com/fwlink/?LinkId=94864)<br /><br /> [Web Services Policy 1.5 - infrastructure](http://go.microsoft.com/fwlink/?LinkId=94865)<br /><br /> WCF utilise la WS-Policy 1.2 ou 1.5 avec des assertions spécifiques au domaine pour décrire les fonctions et les exigences de service.|  
|Pièces jointes WS-Policy|[Stratégie de Services Web 1.2 - pièce jointe (WS-PolicyAttachment)](http://go.microsoft.com/fwlink/?LinkId=94866)<br /><br /> WCF implémente les pièces jointes WS-Policy pour joindre des expressions de stratégie à différentes portées dans WSDL.|  
|Échange de métadonnées WS|[Échange de métadonnées de Services Web (WS-MetadataExchange) version 1.1](http://go.microsoft.com/fwlink/?LinkId=94868)<br /><br /> WCF implémente WS-MetadataExchange pour récupérer XML Schema, WSDL et WS-Policy.|  
|WS-Addressing Binding pour WSDL|[Web Services Addressing 1.0 - liaison WSDL](http://go.microsoft.com/fwlink/?LinkId=94869)<br /><br /> WCF implémente WS-Addressing Binding pour WSDL pour joindre des informations d’adressage dans WSDL.|  
  
## <a name="see-also"></a>Voir aussi  
 [Protocoles de services web pris en charge par des liaisons d’interopérabilité fournies par le système](../../../../docs/framework/wcf/feature-details/web-services-protocols-supported-by-system-provided-interoperability-bindings.md)  
 [WSDL et stratégie](../../../../docs/framework/wcf/feature-details/wsdl-and-policy.md)
