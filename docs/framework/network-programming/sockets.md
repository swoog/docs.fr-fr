---
title: sockets
ms.date: 03/30/2017
helpviewer_keywords:
- application protocols, sockets
- sending data, sockets
- data requests, sockets
- Windows Sockets
- sockets, about sockets
- Socket class, about Socket class
- sockets
- requesting data from Internet, sockets
- network, sockets
- receiving data, sockets
- protocols, sockets
- Internet, sockets
ms.assetid: 10d22735-bd37-42c1-a2be-c1932f979a7d
ms.openlocfilehash: 4a1b18f2c31bf8dad8cf32e2e5205cf3008e7b18
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59136043"
---
# <a name="sockets"></a><span data-ttu-id="b6769-102">sockets</span><span class="sxs-lookup"><span data-stu-id="b6769-102">Sockets</span></span>
<span data-ttu-id="b6769-103">L’espace de noms <xref:System.Net.Sockets> contient une implémentation managée de l’interface Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="b6769-103">The <xref:System.Net.Sockets> namespace contains a managed implementation of the Windows Sockets interface.</span></span> <span data-ttu-id="b6769-104">Toutes les autres classes d’accès réseau dans l’espace de noms <xref:System.Net> s’appuient sur cette implémentation de sockets.</span><span class="sxs-lookup"><span data-stu-id="b6769-104">All other network-access classes in the <xref:System.Net> namespace are built on top of this implementation of sockets.</span></span>  
  
 <span data-ttu-id="b6769-105">La classe <xref:System.Net.Sockets.Socket> du .NET Framework est une version de code managé des services de socket fournis par l’API Winsock32.</span><span class="sxs-lookup"><span data-stu-id="b6769-105">The .NET Framework <xref:System.Net.Sockets.Socket> class is a managed-code version of the socket services provided by the Winsock32 API.</span></span> <span data-ttu-id="b6769-106">Dans la plupart des cas, les méthodes de la classe **Socket** ne font que marshaler les données dans leurs équivalents Win32 natifs et gérer les vérifications de sécurité nécessaires.</span><span class="sxs-lookup"><span data-stu-id="b6769-106">In most cases, the **Socket** class methods simply marshal data into their native Win32 counterparts and handle any necessary security checks.</span></span>  
  
 <span data-ttu-id="b6769-107">La classe **Socket** prend en charge deux modes de base : le mode synchrone et le mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b6769-107">The **Socket** class supports two basic modes, synchronous and asynchronous.</span></span> <span data-ttu-id="b6769-108">En mode synchrone, les appels aux fonctions qui effectuent des opérations réseau (telles que <xref:System.Net.Sockets.Socket.Send%2A> et <xref:System.Net.Sockets.Socket.Receive%2A>) attendent que l’opération soit terminée avant de restituer le contrôle au programme appelant.</span><span class="sxs-lookup"><span data-stu-id="b6769-108">In synchronous mode, calls to functions that perform network operations (such as <xref:System.Net.Sockets.Socket.Send%2A> and <xref:System.Net.Sockets.Socket.Receive%2A>) wait until the operation completes before returning control to the calling program.</span></span> <span data-ttu-id="b6769-109">En mode asynchrone, ces appels retournent immédiatement.</span><span class="sxs-lookup"><span data-stu-id="b6769-109">In asynchronous mode, these calls return immediately.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b6769-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6769-110">See also</span></span>

- [<span data-ttu-id="b6769-111">Guide pratique pour créer un Socket</span><span class="sxs-lookup"><span data-stu-id="b6769-111">How to: Create a Socket</span></span>](../../../docs/framework/network-programming/how-to-create-a-socket.md)

- [<span data-ttu-id="b6769-112">Utilisation de protocoles d’application</span><span class="sxs-lookup"><span data-stu-id="b6769-112">Using Application Protocols</span></span>](../../../docs/framework/network-programming/using-application-protocols.md)
