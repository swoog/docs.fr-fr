---
title: 'Comment : activer un WebRequest pour utiliser un proxy pour communiquer avec Internet'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 63c0ef2c-44b5-4c54-9804-ba0b9b001ac7
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: 0f57869dfecce3e59d0a255a6201dd966bc407e6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33396904"
---
# <a name="how-to-enable-a-webrequest-to-use-a-proxy-to-communicate-with-the-internet"></a><span data-ttu-id="da935-102">Comment : activer un WebRequest pour utiliser un proxy pour communiquer avec Internet</span><span class="sxs-lookup"><span data-stu-id="da935-102">How to: Enable a WebRequest to Use a Proxy to Communicate With the Internet</span></span>
<span data-ttu-id="da935-103">Cet exemple crée une instance proxy globale qui permet à tout <xref:System.Net.WebRequest> d’utiliser un proxy pour communiquer avec Internet.</span><span class="sxs-lookup"><span data-stu-id="da935-103">This example creates a global proxy instance that will enable any <xref:System.Net.WebRequest> to use a proxy to communicate with the Internet.</span></span> <span data-ttu-id="da935-104">L’exemple suppose que le serveur proxy est nommé `webproxy` et qu’il communique sur le port 80, le port HTTP standard.</span><span class="sxs-lookup"><span data-stu-id="da935-104">The example assumes that the proxy server is named `webproxy` and that it communicates on port 80, the standard HTTP port.</span></span>  
  
## <a name="example"></a><span data-ttu-id="da935-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="da935-105">Example</span></span>  
  
```csharp  
WebProxy proxyObject = new WebProxy("http://webproxy:80/");  
GlobalProxySelection.Select = proxyObject;  
```  
  
```vb  
Dim proxyObject As WebProxy = New WebProxy("http://webproxy:80/")  
GlobalProxySelection.Select = proxyObject  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="da935-106">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="da935-106">Compiling the Code</span></span>  
 <span data-ttu-id="da935-107">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="da935-107">This example requires:</span></span>  
  
-   <span data-ttu-id="da935-108">Références à l’espace de noms **System.Net**.</span><span class="sxs-lookup"><span data-stu-id="da935-108">References to the **System.Net** namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="da935-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da935-109">See Also</span></span>  
 [<span data-ttu-id="da935-110">Utilisation de protocoles d’application</span><span class="sxs-lookup"><span data-stu-id="da935-110">Using Application Protocols</span></span>](../../../docs/framework/network-programming/using-application-protocols.md)  
 [<span data-ttu-id="da935-111">Accès à Internet via un proxy</span><span class="sxs-lookup"><span data-stu-id="da935-111">Accessing the Internet Through a Proxy</span></span>](../../../docs/framework/network-programming/accessing-the-internet-through-a-proxy.md)
