---
title: 'Comment : activer un WebRequest pour utiliser un proxy pour communiquer avec Internet'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 63c0ef2c-44b5-4c54-9804-ba0b9b001ac7
ms.openlocfilehash: 09a50794995b9157504ceff8dd578d709bfee020
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50190437"
---
# <a name="how-to-enable-a-webrequest-to-use-a-proxy-to-communicate-with-the-internet"></a><span data-ttu-id="257cf-102">Comment : activer un WebRequest pour utiliser un proxy pour communiquer avec Internet</span><span class="sxs-lookup"><span data-stu-id="257cf-102">How to: Enable a WebRequest to Use a Proxy to Communicate With the Internet</span></span>
<span data-ttu-id="257cf-103">Cet exemple crée une instance proxy globale qui permet à tout <xref:System.Net.WebRequest> d’utiliser un proxy pour communiquer avec Internet.</span><span class="sxs-lookup"><span data-stu-id="257cf-103">This example creates a global proxy instance that will enable any <xref:System.Net.WebRequest> to use a proxy to communicate with the Internet.</span></span> <span data-ttu-id="257cf-104">L’exemple suppose que le serveur proxy est nommé `webproxy` et qu’il communique sur le port 80, le port HTTP standard.</span><span class="sxs-lookup"><span data-stu-id="257cf-104">The example assumes that the proxy server is named `webproxy` and that it communicates on port 80, the standard HTTP port.</span></span>  
  
## <a name="example"></a><span data-ttu-id="257cf-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="257cf-105">Example</span></span>  
  
```csharp  
WebProxy proxyObject = new WebProxy("http://webproxy:80/");  
GlobalProxySelection.Select = proxyObject;  
```  
  
```vb  
Dim proxyObject As WebProxy = New WebProxy("http://webproxy:80/")  
GlobalProxySelection.Select = proxyObject  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="257cf-106">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="257cf-106">Compiling the Code</span></span>  
 <span data-ttu-id="257cf-107">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="257cf-107">This example requires:</span></span>  
  
-   <span data-ttu-id="257cf-108">Références à l’espace de noms **System.Net**.</span><span class="sxs-lookup"><span data-stu-id="257cf-108">References to the **System.Net** namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="257cf-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="257cf-109">See Also</span></span>  
 [<span data-ttu-id="257cf-110">Utilisation de protocoles d’application</span><span class="sxs-lookup"><span data-stu-id="257cf-110">Using Application Protocols</span></span>](../../../docs/framework/network-programming/using-application-protocols.md)  
 [<span data-ttu-id="257cf-111">Accès à Internet via un proxy</span><span class="sxs-lookup"><span data-stu-id="257cf-111">Accessing the Internet Through a Proxy</span></span>](../../../docs/framework/network-programming/accessing-the-internet-through-a-proxy.md)
