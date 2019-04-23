---
title: 'Procédure : activer un WebRequest pour utiliser un proxy pour communiquer avec Internet'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 63c0ef2c-44b5-4c54-9804-ba0b9b001ac7
ms.openlocfilehash: a2179e767a0556f5223f2f4c1cc91708133120a5
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59103699"
---
# <a name="how-to-enable-a-webrequest-to-use-a-proxy-to-communicate-with-the-internet"></a><span data-ttu-id="58a4e-102">Procédure : activer un WebRequest pour utiliser un proxy pour communiquer avec Internet</span><span class="sxs-lookup"><span data-stu-id="58a4e-102">How to: Enable a WebRequest to Use a Proxy to Communicate With the Internet</span></span>
<span data-ttu-id="58a4e-103">Cet exemple crée une instance proxy globale qui permet à tout <xref:System.Net.WebRequest> d’utiliser un proxy pour communiquer avec Internet.</span><span class="sxs-lookup"><span data-stu-id="58a4e-103">This example creates a global proxy instance that will enable any <xref:System.Net.WebRequest> to use a proxy to communicate with the Internet.</span></span> <span data-ttu-id="58a4e-104">L’exemple suppose que le serveur proxy est nommé `webproxy` et qu’il communique sur le port 80, le port HTTP standard.</span><span class="sxs-lookup"><span data-stu-id="58a4e-104">The example assumes that the proxy server is named `webproxy` and that it communicates on port 80, the standard HTTP port.</span></span>  
  
## <a name="example"></a><span data-ttu-id="58a4e-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="58a4e-105">Example</span></span>  
  
```csharp  
WebProxy proxyObject = new WebProxy("http://webproxy:80/");  
GlobalProxySelection.Select = proxyObject;  
```  
  
```vb  
Dim proxyObject As WebProxy = New WebProxy("http://webproxy:80/")  
GlobalProxySelection.Select = proxyObject  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="58a4e-106">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="58a4e-106">Compiling the Code</span></span>  
 <span data-ttu-id="58a4e-107">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="58a4e-107">This example requires:</span></span>  
  
-   <span data-ttu-id="58a4e-108">Une [directive `using`](../../csharp/language-reference/keywords/using-directive.md) pour l’espace de noms **System.Net**.</span><span class="sxs-lookup"><span data-stu-id="58a4e-108">A [`using` directive](../../csharp/language-reference/keywords/using-directive.md) for the **System.Net** namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="58a4e-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58a4e-109">See also</span></span>

- [<span data-ttu-id="58a4e-110">Utilisation de protocoles d’application</span><span class="sxs-lookup"><span data-stu-id="58a4e-110">Using Application Protocols</span></span>](../../../docs/framework/network-programming/using-application-protocols.md)
- [<span data-ttu-id="58a4e-111">Accès à Internet via un proxy</span><span class="sxs-lookup"><span data-stu-id="58a4e-111">Accessing the Internet Through a Proxy</span></span>](../../../docs/framework/network-programming/accessing-the-internet-through-a-proxy.md)
