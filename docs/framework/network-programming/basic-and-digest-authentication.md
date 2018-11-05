---
title: Authentification de base et authentification Digest
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- authentication [.NET Framework], classes
- Basic authentication
- authentication [.NET Framework], basic
- client authentication, basic
- user authentication, basic
- authentication [.NET Framework], digest
- receiving data, authentication
- client authentication, digest
- Internet, authentication
- digest authentication
- sending data, authentication
- network resources, authentication
- user authentication, digest
ms.assetid: 8cce2742-8d52-4643-9dd2-64ddf38aa878
ms.openlocfilehash: db39bdcaf2c3a4457028e30f9458a5626aa7e795
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/29/2018
ms.locfileid: "50190669"
---
# <a name="basic-and-digest-authentication"></a><span data-ttu-id="8b42f-102">Authentification de base et authentification Digest</span><span class="sxs-lookup"><span data-stu-id="8b42f-102">Basic and Digest Authentication</span></span>
<span data-ttu-id="8b42f-103">L’implémentation <xref:System.Net> de l’authentification de base et Digest est conforme à RFC2617 – Authentification HTTP : authentification de base et authentification Digest (disponible sur site web du [World Wide Web Consortium](https://www.w3.org)).</span><span class="sxs-lookup"><span data-stu-id="8b42f-103">The <xref:System.Net> implementation of basic and digest authentication complies with RFC2617 – HTTP Authentication: Basic and Digest Authentication (available on the [World Wide Web Consortium's](https://www.w3.org) website).</span></span>  
  
 <span data-ttu-id="8b42f-104">Pour utiliser l’authentification de base et l’authentification Digest, une application doit fournir un nom d’utilisateur et un mot de passe dans la propriété <xref:System.Net.WebRequest.Credentials%2A> de l’objet <xref:System.Net.WebRequest> qu’elle utilise pour demander des données à partir d’Internet, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="8b42f-104">To use basic and digest authentication, an application must provide a user name and password in the <xref:System.Net.WebRequest.Credentials%2A> property of the <xref:System.Net.WebRequest> object that it uses to request data from the Internet, as shown in the following example.</span></span>  
  
```vb  
Dim MyURI As String = "http://www.contoso.com/"  
Dim WReq As WebRequest = WebRequest.Create(MyURI)  
WReq.Credentials = New NetworkCredential(UserName, SecurelyStoredPassword)  
```  
  
```csharp  
String MyURI = "http://www.contoso.com/";  
WebRequest WReq = WebRequest.Create(MyURI);  
WReq.Credentials = new NetworkCredential(UserName, SecurelyStoredPassword);  
```  
  
> [!CAUTION]
>  <span data-ttu-id="8b42f-105">Les données transmises avec une authentification de base et Digest ne sont pas chiffrées, par conséquent les données sont visibles par tous.</span><span class="sxs-lookup"><span data-stu-id="8b42f-105">Data sent with Basic and Digest Authentication is not encrypted, so the data can be seen by an adversary.</span></span> <span data-ttu-id="8b42f-106">De plus, les informations d'authentification de base (nom d'utilisateur et mot de passe) sont envoyées en texte clair et peuvent être interceptées.</span><span class="sxs-lookup"><span data-stu-id="8b42f-106">Additionally, Basic Authentication credentials (user name and password) are sent in the clear and can be intercepted.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8b42f-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b42f-107">See Also</span></span>  
 [<span data-ttu-id="8b42f-108">Authentification NTLM et Kerberos</span><span class="sxs-lookup"><span data-stu-id="8b42f-108">NTLM and Kerberos Authentication</span></span>](../../../docs/framework/network-programming/ntlm-and-kerberos-authentication.md)  
 [<span data-ttu-id="8b42f-109">Authentification Internet</span><span class="sxs-lookup"><span data-stu-id="8b42f-109">Internet Authentication</span></span>](../../../docs/framework/network-programming/internet-authentication.md)
