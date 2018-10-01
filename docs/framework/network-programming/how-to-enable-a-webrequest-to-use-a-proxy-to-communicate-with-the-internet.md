---
title: 'Comment : activer un WebRequest pour utiliser un proxy pour communiquer avec Internet'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 63c0ef2c-44b5-4c54-9804-ba0b9b001ac7
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 86bf21580db9bc6d9890f0935e283b653ba2e0b5
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47397788"
---
# <a name="how-to-enable-a-webrequest-to-use-a-proxy-to-communicate-with-the-internet"></a>Comment : activer un WebRequest pour utiliser un proxy pour communiquer avec Internet
Cet exemple crée une instance proxy globale qui permet à tout <xref:System.Net.WebRequest> d’utiliser un proxy pour communiquer avec Internet. L’exemple suppose que le serveur proxy est nommé `webproxy` et qu’il communique sur le port 80, le port HTTP standard.  
  
## <a name="example"></a>Exemple  
  
```csharp  
WebProxy proxyObject = new WebProxy("http://webproxy:80/");  
GlobalProxySelection.Select = proxyObject;  
```  
  
```vb  
Dim proxyObject As WebProxy = New WebProxy("http://webproxy:80/")  
GlobalProxySelection.Select = proxyObject  
```  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   Références à l’espace de noms **System.Net**.  
  
## <a name="see-also"></a>Voir aussi  
 [Utilisation de protocoles d’application](../../../docs/framework/network-programming/using-application-protocols.md)  
 [Accès à Internet via un proxy](../../../docs/framework/network-programming/accessing-the-internet-through-a-proxy.md)
