---
title: 'Procédure : remplacer une sélection de proxy global'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 0da481a9-b414-4230-beb0-e3ceba882fe5
ms.openlocfilehash: 6973503f12e0e60ee139c5cd7da09ab319d70218
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54592122"
---
# <a name="how-to-override-a-global-proxy-selection"></a>Procédure : remplacer une sélection de proxy global
Cet exemple envoie une **WebRequest** à `www.contoso.com` qui substitue la sélection de proxy global avec un serveur proxy nommé `alternateproxy` sur le port 80.  
  
## <a name="example"></a>Exemple  
  
```csharp  
WebRequest req = WebRequest.Create("http://www.contoso.com/");  
req.Proxy = new WebProxy("http://alternateproxy:80/");  
```  
  
```vb  
Dim req As WebRequest = WebRequest.Create("http://www.contoso.com/")  
req.Proxy = New WebProxy("http://alternateproxy:80/")  
```  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   Une [directive `using`](~/docs/csharp/language-reference/keywords/using-directive.md) pour l’espace de noms **System.Net**.  
  
## <a name="see-also"></a>Voir aussi
- [Utilisation de protocoles d’application](../../../docs/framework/network-programming/using-application-protocols.md)
- [Accès à Internet via un proxy](../../../docs/framework/network-programming/accessing-the-internet-through-a-proxy.md)
