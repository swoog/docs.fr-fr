---
title: HttpListener
ms.date: 03/30/2017
helpviewer_keywords:
- HTTP
ms.assetid: 5b89d3fb-3c9a-49e2-af1f-c34c020c68ac
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 0d5b7fccdac9dba3fd44d12241dd60cbaefa1b7a
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/29/2018
ms.locfileid: "47192938"
---
# <a name="httplistener"></a>HttpListener
La classe <xref:System.Net.HttpListener> fournit un écouteur de protocole HTTP contrôlé par programmation. L'écouteur est actif pendant toute la durée de vie de l'objet <xref:System.Net.HttpListener> et s'exécute au sein de votre application.  
  
## <a name="httpsys"></a>HTTP.SYS  
 La classe <xref:System.Net.HttpListener> repose sur HTTP.sys, qui est l'écouteur en mode noyau qui gère tout le trafic HTTP pour Windows. HTTP.sys assure la gestion des connexions, la limitation de la bande passante et la journalisation du serveur web. Utilisez l'outil `HttpCfg.exe` pour ajouter des certificats SSL. Pour plus d’informations, consultez les explications sur l’outil [HttpCfg.exe](https://go.microsoft.com/fwlink/?LinkID=178284) dans la documentation du [serveur](https://go.microsoft.com/fwlink/?LinkID=178285).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Net.HttpListener>  
 <xref:System.Net.HttpWebRequest>  
 <xref:System.Net.HttpWebResponse>  
 [Serveur HTTP](https://go.microsoft.com/fwlink/?LinkID=178285)  
 [Améliorations de la sécurité des informations Internet](https://go.microsoft.com/fwlink/?LinkID=178286)  
 [Exemple d’application hôte ASPX HttpListener](https://go.microsoft.com/fwlink/?LinkID=179560)  
 [Exemple de technologie HttpListener](https://go.microsoft.com/fwlink/?LinkID=179558)  
 [Exemples de programmation réseau](../../../docs/framework/network-programming/network-programming-samples.md)
