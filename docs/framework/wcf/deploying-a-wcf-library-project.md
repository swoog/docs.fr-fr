---
title: Déploiement d'un projet de bibliothèque WCF
ms.date: 03/30/2017
ms.assetid: 9f9222fe-d358-443c-9a49-12c5498e35e7
ms.openlocfilehash: 0400fc9ec5a5629139348709bbd3a5554ce251c7
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65593344"
---
# <a name="deploying-a-wcf-library-project"></a>Déploiement d'un projet de bibliothèque WCF
Cette rubrique décrit comment vous pouvez déployer un projet de bibliothèque de Service Windows Communication Foundation (WCF).  
  
## <a name="deploying-a-wcf-service-library"></a>Déploiement d'une bibliothèque du service WCF  
 Une bibliothèque de service WCF est une bibliothèque de liens dynamiques (DLL). À ce titre, elle ne peut pas être exécutée seule. Elle doit être déployée dans un environnement d'hébergement. Pour plus d’informations sur ce processus, consultez [Hosting and Consuming WCF Services](https://go.microsoft.com/fwlink/?LinkId=99932).  
  
 Une bibliothèque de service WCF peut être déployée comme tout autre service WCF. Toutefois, n’oubliez pas que .NET Framework ne prend pas en charge configuration pour les DLL. <xref:System.Configuration> prend en charge un fichier de configuration par domaine d'application. Le projet de bibliothèque de service WCF contourne cette limitation en fournissant un fichier App.config pour la bibliothèque pendant le développement. Toutefois, le fichier App.config n'est pas reconnu après le déploiement.  
  
 Vous devez placer votre code de configuration dans le fichier de configuration reconnu par votre environnement d'hébergement. Pour l'auto-hébergement, vous devez copier le contenu du fichier App.config dans le fichier App.config de l'exécutable d'hébergement. Si vous utilisez IIS pour héberger votre service, vous devez copier le contenu du fichier App.config dans le fichier Web.config du répertoire virtuel.
