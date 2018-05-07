---
title: Déploiement d'applications WCF à l'aide de ClickOnce
ms.date: 03/30/2017
ms.assetid: 1a11feee-2a47-4d3e-a28a-ad69d5ff93e0
ms.openlocfilehash: ceb652eed1a7cc377538f5d693dcb85ed99da4b3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="deploying-wcf-applications-with-clickonce"></a>Déploiement d'applications WCF à l'aide de ClickOnce
Les applications clientes à l’aide de Windows Communication Foundation (WCF) peuvent être déployées à l’aide de la technologie ClickOnce. Cette technologie leur permet de tirer parti des protections de sécurité d'exécution fournies par la sécurité d'accès du code, sous réserve qu'elles soient signées numériquement avec un certificat approuvé. Le certificat utilisé pour signer l'application ClickOnce doit résider dans le magasin d'éditeurs approuvés, et la stratégie de sécurité locale sur l'ordinateur client doit être configurée pour accorder des autorisations Confiance totale aux applications signées avec le certificat de l'éditeur.  
  
 Pour plus d’informations sur la configuration des applications ClickOnce et éditeurs approuvés, consultez [configuration d’éditeurs approuvés ClickOnce](http://go.microsoft.com/fwlink/?LinkId=94774).  
  
## <a name="see-also"></a>Voir aussi  
 [Vue d’ensemble du déploiement d’applications approuvées](http://go.microsoft.com/fwlink/?LinkId=94775)  
 [Applications de déploiement de ClickOnce pour les Windows Forms](http://go.microsoft.com/fwlink/?LinkId=94776)
