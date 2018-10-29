---
title: 'Comment : demander une page web et récupérer les résultats sous forme de flux'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d32b7f35-29d8-4fb7-ad71-d219edc5e359
ms.openlocfilehash: 6481e923c8daabfcfa94adc45d7d4172e47a779a
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2018
ms.locfileid: "50199069"
---
# <a name="how-to-request-a-web-page-and-retrieve-the-results-as-a-stream"></a>Comment : demander une page web et récupérer les résultats sous forme de flux
Cet exemple montre comment demander une page web et récupérer les résultats sous forme de flux.  
  
## <a name="example"></a>Exemple  
  
```csharp  
WebClient myClient = new WebClient();  
Stream response = myClient.OpenRead("http://www.contoso.com/index.htm");  
// The stream data is used here.  
response.Close();  
```  
  
```vb  
Dim myClient As WebClient = New WebClient()  
Dim response As Stream = myClient.OpenRead("http://www.contoso.com/index.htm")  
' The stream data is used here.  
response.Close()  
```  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   Références aux espaces de noms <xref:System.IO> et <xref:System.Net>.  
  
## <a name="see-also"></a>Voir aussi  
 [Demande de données](../../../docs/framework/network-programming/requesting-data.md)
