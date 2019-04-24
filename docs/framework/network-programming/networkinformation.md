---
title: NetworkInformation
ms.date: 03/30/2017
helpviewer_keywords:
- Network
ms.assetid: 31b44dd3-b903-4a48-8419-40419a3e4038
ms.openlocfilehash: 0820ad6a6d5000ef7ea575e856d883ba5325b1b0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59230978"
---
# <a name="networkinformation"></a>NetworkInformation
L’espace de noms <xref:System.Net.NetworkInformation> permet de recueillir des informations concernant les événements, les modifications, les statistiques et les propriétés liés au réseau. Vous pouvez également déterminer si un hôte distant est accessible à l’aide de la classe <xref:System.Net.NetworkInformation.Ping?displayProperty=nameWithType>.  
  
## <a name="network-availability-and-events"></a>Disponibilité du réseau et événements réseau  
 La classe <xref:System.Net.NetworkInformation.NetworkChange?displayProperty=nameWithType> permet de déterminer si l’adresse réseau ou la disponibilité du réseau ont changé. Pour utiliser cette classe, créez un gestionnaire d’événements en vue de traiter la modification, puis associez-la à un <xref:System.Net.NetworkInformation.NetworkAddressChangedEventHandler> ou un <xref:System.Net.NetworkInformation.NetworkAvailabilityChangedEventHandler>. Pour plus d'informations, voir [Procédure : détecter la disponibilité réseau et les changements d’adresse](../../../docs/framework/network-programming/how-to-detect-network-availability-and-address-changes.md).  
  
## <a name="network-statistics-and-properties"></a>Statistiques et propriétés du réseau  
 Vous pouvez collecter des informations relatives aux statistiques et aux propriétés du réseau au niveau d’une interface ou d’un protocole. Les classes <xref:System.Net.NetworkInformation.NetworkInterface>, <xref:System.Net.NetworkInformation.NetworkInterfaceType> et <xref:System.Net.NetworkInformation.PhysicalAddress> fournissent des informations sur les interfaces réseau, alors que les classes <xref:System.Net.NetworkInformation.IPInterfaceProperties>, <xref:System.Net.NetworkInformation.IPGlobalProperties>, <xref:System.Net.NetworkInformation.IPGlobalStatistics>, <xref:System.Net.NetworkInformation.TcpStatistics> et <xref:System.Net.NetworkInformation.UdpStatistics> fournissent des informations sur les paquets des couches 3 et 4. Pour plus d'informations, voir [Procédure : obtenir des informations d’interface et de protocole](../../../docs/framework/network-programming/how-to-get-interface-and-protocol-information.md).  
  
## <a name="determine-if-a-remote-host-is-reachable"></a>Déterminer si un hôte distant est accessible  
 Vous pouvez utiliser la classe <xref:System.Net.NetworkInformation.Ping> pour déterminer si un hôte distant est disponible, s’il se trouve dans le réseau et s’il est accessible. Pour plus d'informations, voir [Procédure : exécuter une requête ping](../../../docs/framework/network-programming/how-to-ping-a-host.md).  
  
## <a name="see-also"></a>Voir aussi

- [Exemples de programmation réseau](../../../docs/framework/network-programming/network-programming-samples.md)
- [Exemple de technologie d’informations réseau](https://go.microsoft.com/fwlink/?LinkID=179564)
- [Exemple de technologie NetStat](https://go.microsoft.com/fwlink/?LinkID=179562)
- [Exemple de technologie de test ping à partir d’une application cliente](https://go.microsoft.com/fwlink/?LinkID=179565)
