---
title: 'Comment : demander une page web et récupérer les résultats sous forme de flux'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d32b7f35-29d8-4fb7-ad71-d219edc5e359
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: 31856e7fc7136b3bdb8fab9fdf8185de32a3007a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33395211"
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
