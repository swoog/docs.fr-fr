---
title: Déploiement d'un projet de bibliothèque WCF
ms.date: 03/30/2017
ms.assetid: 9f9222fe-d358-443c-9a49-12c5498e35e7
ms.openlocfilehash: 08a1d794aeeea1a41cd1eb3abf298f3f4a0f6d15
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="deploying-a-wcf-library-project"></a>Déploiement d'un projet de bibliothèque WCF
Cette rubrique décrit comment vous pouvez déployer un projet de bibliothèque de Service Windows Communication Foundation (WCF).  
  
## <a name="deploying-a-wcf-service-library"></a>Déploiement d'une bibliothèque du service WCF  
 Une bibliothèque du service [!INCLUDE[indigo2](../../../includes/indigo2-md.md)] est une bibliothèque de liens dynamiques (DLL). À ce titre, elle ne peut pas être exécutée seule. Elle doit être déployée dans un environnement d'hébergement. Pour plus d’informations sur ce processus, consultez [hébergement et utilisation des Services WCF](http://go.microsoft.com/fwlink/?LinkId=99932).  
  
 Une bibliothèque du service [!INCLUDE[indigo2](../../../includes/indigo2-md.md)] peut être déployée comme tout autre service [!INCLUDE[indigo2](../../../includes/indigo2-md.md)]. Sachez toutefois que [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)] ne prend pas en charge de configuration pour les DLL. <xref:System.Configuration> prend en charge un fichier de configuration par domaine d'application. Le projet de bibliothèque du service [!INCLUDE[indigo2](../../../includes/indigo2-md.md)] contourne cette limitation en fournissant un fichier App.config pour la bibliothèque pendant la phase de développement. Toutefois, le fichier App.config n'est pas reconnu après le déploiement.  
  
 Vous devez placer votre code de configuration dans le fichier de configuration reconnu par votre environnement d'hébergement. Pour l'auto-hébergement, vous devez copier le contenu du fichier App.config dans le fichier App.config de l'exécutable d'hébergement. Si vous utilisez IIS pour héberger votre service, vous devez copier le contenu du fichier App.config dans le fichier Web.config du répertoire virtuel.
