---
title: Extension du système de métadonnées
ms.date: 03/30/2017
helpviewer_keywords:
- extending metadata [WCF]
ms.assetid: 8c6b3b00-61b8-4589-8fa5-546cc33719bf
ms.openlocfilehash: 7ccef0c2b908a8f78249742decd6c46a862e541e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="extending-the-metadata-system"></a>Extension du système de métadonnées
Le système de métadonnées Windows Communication Foundation (WCF) est un groupe de classes et interfaces qui représentent les métadonnées requises pour implémenter des applications basées sur le service. Modifiez ou étendez les classes ou implémentez et configurez les interfaces pour exporter et importer des métadonnées personnalisées telles que les extensions WSDL (Web Services Description Language) ou des assertions WS-PolicyAttachments personnalisées.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Exportation de métadonnées personnalisées pour une extension WCF](../../../../docs/framework/wcf/extending/exporting-custom-metadata-for-a-wcf-extension.md)  
 Décrit comment implémenter et utiliser l'interface <xref:System.ServiceModel.Description.IPolicyExportExtension?displayProperty=nameWithType> pour incorporer des assertions de stratégie personnalisées dans des documents WSDL.  
  
 [Importation de métadonnées personnalisées pour une extension WCF](../../../../docs/framework/wcf/extending/importing-custom-metadata-for-a-wcf-extension.md)  
 Décrit comment implémenter et utiliser l'interface <xref:System.ServiceModel.Description.IPolicyImportExtension?displayProperty=nameWithType> pour lire et répondre à des assertions de stratégie personnalisées dans des documents WSDL.  
  
 [Publication et récupération de métadonnées sur une liaison personnalisée](../../../../docs/framework/wcf/extending/publishing-and-retrieving-metadata-over-a-custom-binding.md)  
 Décrit comment échanger des métadonnées sur des liaisons personnalisées.
