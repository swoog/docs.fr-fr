---
title: 'Procédure : récupérer une classe WebResponse spécifique au protocole qui correspond à une classe WebRequest'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d8c90785-f16b-42a5-8439-ed2f731b2ba8
ms.openlocfilehash: 3b3b523d6248b3c61a0994728b035bc6f02d5cf1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54745345"
---
# <a name="how-to-retrieve-a-protocol-specific-webresponse-that-matches-a-webrequest"></a>Procédure : récupérer une classe WebResponse spécifique au protocole qui correspond à une classe WebRequest
Cet exemple montre comment récupérer une classe WebResponse spécifique au protocole qui correspond à une classe WebRequest.  
  
## <a name="example"></a>Exemple  
  
```csharp  
WebRequest req = WebRequest.Create("http://www.contoso.com/");  
WebResponse resp = req.GetResponse();  
```  
  
```vb  
Dim req As WebRequest = WebRequest.Create("http://www.contoso.com")  
Dim resp As WebResponse = req.GetResponse()  
```  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   Références à l’espace de noms **System.Net**.  
  
## <a name="see-also"></a>Voir aussi
- [Demande de données](../../../docs/framework/network-programming/requesting-data.md)
