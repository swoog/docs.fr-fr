---
title: Formats de métadonnées
ms.date: 03/30/2017
ms.assetid: baad1e68-28fc-4a6a-8a43-75e47e7fa871
ms.openlocfilehash: 55f68f4b56e50b19da19ecc941e9ec537b846006
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59173821"
---
# <a name="metadata-formats"></a>Formats de métadonnées
Windows Communication Foundation (WCF) prend en charge les formats de métadonnées dans le tableau suivant.  
  
## <a name="metadata-specifications-and-usage"></a>Spécification et utilisation des métadonnées  
  
|Protocole|Spécification et utilisation|  
|--------------|-----------------------------|  
|WSDL 1.1|[WSDL (Web Services Description Language) 1.1 (page pouvant être en anglais)](https://go.microsoft.com/fwlink/?LinkId=94859)<br /><br /> WCF utilise les Web Services Description Language (WSDL) pour décrire des services.|  
|Schéma XML|[XML Schema Part 2 : Types de données deuxième édition](https://go.microsoft.com/fwlink/?LinkId=94861) et [XML Schema Part 1 : Structures deuxième édition](https://go.microsoft.com/fwlink/?LinkId=94862)<br /><br /> WCF utilise le schéma XML pour décrire les types de données utilisés dans les messages.|  
|WS-Policy|[Services Web-Policy 1.2 - Infrastructure (WS-Policy)  (page pouvant être en anglais)](https://go.microsoft.com/fwlink/?LinkId=94864)<br /><br /> [Services Web-Policy 1.5 - Infrastructure  (page pouvant être en anglais)](https://go.microsoft.com/fwlink/?LinkId=94865)<br /><br /> WCF utilise le WS-Policy 1.2 ou 1.5 spécifications avec des assertions spécifiques au domaine pour décrire les fonctionnalités et exigences de service.|  
|Pièces jointes WS-Policy|[Services Web-Policy 1.2 – Pièces jointes (WS-PolicyAttachment)  (page pouvant être en anglais)](https://go.microsoft.com/fwlink/?LinkId=94866)<br /><br /> WCF implémente les pièces jointes WS-Policy pour joindre des expressions de stratégie à différentes portées dans WSDL.|  
|Échange de métadonnées WS|[WS-MetadataExchange (Web Services Metadata Exchange) version 1.1  (page pouvant être en anglais)](https://go.microsoft.com/fwlink/?LinkId=94868)<br /><br /> WCF implémente WS-MetadataExchange pour récupérer le schéma XML, WSDL et WS-Policy.|  
|WS-Addressing Binding pour WSDL|[Web Services Addressing 1.0 – Liaison WSDL (page pouvant être en anglais)](https://go.microsoft.com/fwlink/?LinkId=94869)<br /><br /> WCF implémente WS-Addressing Binding pour WSDL pour joindre des informations d’adressage dans WSDL.|  
  
## <a name="see-also"></a>Voir aussi

- [Protocoles de services Web pris en charge par des liaisons d’interopérabilité fournies par le système](../../../../docs/framework/wcf/feature-details/web-services-protocols-supported-by-system-provided-interoperability-bindings.md)
- [WSDL et stratégie](../../../../docs/framework/wcf/feature-details/wsdl-and-policy.md)
