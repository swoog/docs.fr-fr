---
title: 'Procédure : accéder aux propriétés spécifiques à HTTP'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: f8848c7e-f5c5-4d42-b86d-9951ff8f4146
ms.openlocfilehash: 107e57ca947012f5e2f65835d684f5e6068b3681
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59176590"
---
# <a name="how-to-access-http-specific-properties"></a><span data-ttu-id="663ff-102">Procédure : accéder aux propriétés spécifiques à HTTP</span><span class="sxs-lookup"><span data-stu-id="663ff-102">How to: Access HTTP-Specific Properties</span></span>
<span data-ttu-id="663ff-103">Cet exemple montre comment désactiver le comportement HTTP **Keep-alive** et obtenir le numéro de version du protocole du serveur web.</span><span class="sxs-lookup"><span data-stu-id="663ff-103">This sample shows how to turn off the HTTP **Keep-alive** behavior and get the protocol version number from the Web server.</span></span>  
  
## <a name="example"></a><span data-ttu-id="663ff-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="663ff-104">Example</span></span>  
  
```vb  
Dim HttpWReq As HttpWebRequest= _  
    CType(WebRequest.Create("http://www.contoso.com"), HttpWebRequest)  
' Turn off connection keep-alives.  
HttpWReq.KeepAlive = False  
  
Dim HttpWResp As HttpWebResponse = _  
    CType(HttpWReq.GetResponse(), HttpWebResponse)  
  
' Get the HTTP protocol version number returned by the server.  
Dim ver As String = HttpWResp.ProtocolVersion.ToString()  
HttpWResp.Close()  
```  
  
```csharp  
HttpWebRequest HttpWReq =   
    (HttpWebRequest)WebRequest.Create("http://www.contoso.com");  
// Turn off connection keep-alives.  
HttpWReq.KeepAlive = false;  
  
HttpWebResponse HttpWResp = (HttpWebResponse)HttpWReq.GetResponse();  
  
// Get the HTTP protocol version number returned by the server.  
String ver = HttpWResp.ProtocolVersion.ToString();  
HttpWResp.Close();  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="663ff-105">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="663ff-105">Compiling the Code</span></span>  
 <span data-ttu-id="663ff-106">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="663ff-106">This example requires:</span></span>  
  
-   <span data-ttu-id="663ff-107">Références à l’espace de noms **System.Net**.</span><span class="sxs-lookup"><span data-stu-id="663ff-107">References to the **System.Net** namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="663ff-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="663ff-108">See also</span></span>

- [<span data-ttu-id="663ff-109">Accès à Internet via un proxy</span><span class="sxs-lookup"><span data-stu-id="663ff-109">Accessing the Internet Through a Proxy</span></span>](../../../docs/framework/network-programming/accessing-the-internet-through-a-proxy.md)
- [<span data-ttu-id="663ff-110">Utilisation de protocoles d’application</span><span class="sxs-lookup"><span data-stu-id="663ff-110">Using Application Protocols</span></span>](../../../docs/framework/network-programming/using-application-protocols.md)
- [<span data-ttu-id="663ff-111">HTTP</span><span class="sxs-lookup"><span data-stu-id="663ff-111">HTTP</span></span>](../../../docs/framework/network-programming/http.md)
