---
title: Nuages PNRP
ms.date: 03/30/2017
ms.assetid: a82e2bf1-62ab-4c2d-83f3-3217a6aead2e
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: ef3f4fd2f7333c5a78024edf7eb536e9254c0293
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="pnrp-clouds"></a>Nuages PNRP
Un « cloud » PNRP représente un ensemble de nœuds qui peuvent communiquer entre eux via le réseau. Le terme « cloud » est un synonyme de « maille d’homologue ».  
  
 La communication entre les nœuds ne doit jamais se faire entre différents clouds. Une instance <xref:System.Net.PeerToPeer.Cloud> est identifiée par son nom, qui respecte la casse. Il est possible de connecter un même pair ou nœud à plusieurs clouds.  
  
 Les clouds sont très liés aux interfaces réseau.  Sur un ordinateur multirésident comprenant deux cartes réseau connectées à différents sous-réseaux, trois clouds sont retournés : un pour chacune des adresses link-local par interface, et un cloud global.  
  
 PNRP utilise trois « étendues » cloud, où chaque étendue représente un regroupement d’ordinateurs capables de se trouver les uns les autres :  
  
-   Le cloud global correspond à l’étendue d’adresse IPv6 globale et aux adresses globales, et représente tous les ordinateurs du réseau Internet IPv6. Il n’existe qu’un seul cloud global.  
  
-   Le cloud link-local correspond à l’étendue d’adresse IPv6 link-local et aux adresses link-local. Un cloud link-local correspond à une liaison spécifique, qui est généralement identique à celle du sous-réseau connecté localement. Il peut y avoir plusieurs clouds link-local.  
  
 Un troisième cloud, le cloud spécifique au site, correspond à l’étendue d’adresses IPv6 de site et aux adresses locales de site. Ce cloud est désormais déprécié, même s’il est toujours pris en charge dans PNRP.  
  
## <a name="clouds"></a>Clouds  
 Les clouds PNRP sont représentés par des instances de la classe <xref:System.Net.PeerToPeer.Cloud>. Les groupes de cloud utilisant un pair sont représentés par des instances de la classe énumérable <xref:System.Net.PeerToPeer.CloudCollection>. Les collections de clouds PNRP connues du pair actuel peuvent être obtenues en appelant la méthode statique <xref:System.Net.PeerToPeer.Cloud.GetAvailableClouds%2A>.  
  
 Chaque cloud porte un nom unique, constitué d’une chaîne Unicode de 256 caractères. Le nom des clouds, ainsi que l’étendue mentionnée plus haut, sont utilisés pour construire des instances uniques de la classe Cloud. Ces instances peuvent être sérialisées et reconstruites en vue d’une utilisation régulière.  
  
 Une fois qu’une instance Cloud est créée ou obtenue, les noms de pairs peuvent y être inscrits pour créer une maille d’homologues connus.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Net.PeerToPeer.Cloud>  
 [Peer Name Resolution Protocol](../../../docs/framework/network-programming/peer-name-resolution-protocol.md)
