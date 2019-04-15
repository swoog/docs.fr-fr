---
title: 'Procédure : inscrire un protocole personnalisé à l’aide de WebRequest'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 98ddbdb9-66b1-4080-92ad-51f5c447fcf8
ms.openlocfilehash: 5c9a81fc61a2272056ba34fa387fdafee6203824
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59079498"
---
# <a name="how-to-register-a-custom-protocol-using-webrequest"></a><span data-ttu-id="4649c-102">Procédure : inscrire un protocole personnalisé à l’aide de WebRequest</span><span class="sxs-lookup"><span data-stu-id="4649c-102">How to: Register a Custom Protocol Using WebRequest</span></span>
<span data-ttu-id="4649c-103">Cet exemple montre comment inscrire une classe spécifique à un protocole qui est définie ailleurs dans du code.</span><span class="sxs-lookup"><span data-stu-id="4649c-103">This example shows how to register a protocol specific class that is defined elsewhere.</span></span> <span data-ttu-id="4649c-104">Dans cet exemple, `CustomWebRequestCreator` est l’objet implémenté par l’utilisateur qui implémente la méthode **Create** utilisée pour retourner l’objet `CustomWebRequest`.</span><span class="sxs-lookup"><span data-stu-id="4649c-104">In this example, `CustomWebRequestCreator` is the user-implemented object that implements the **Create** method that returns the `CustomWebRequest` object.</span></span> <span data-ttu-id="4649c-105">L’exemple de code suppose que vous avez écrit le code `CustomWebRequest` qui implémente le protocole personnalisé.</span><span class="sxs-lookup"><span data-stu-id="4649c-105">The code example assumes that you have written the `CustomWebRequest` code that implements the custom protocol.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4649c-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="4649c-106">Example</span></span>  
  
```csharp  
WebRequest.RegisterPrefix("custom", new CustomWebRequestCreator());  
WebRequest req = WebRequest.Create("custom://customHost.contoso.com/");  
```  
  
```vb  
WebRequest.RegisterPrefix("custom", New CustomWebRequestCreator())  
Dim req As WebRequest = WebRequest.Create("custom://customHost.contoso.com/")  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="4649c-107">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="4649c-107">Compiling the Code</span></span>  
 <span data-ttu-id="4649c-108">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="4649c-108">This example requires:</span></span>  
  
 <span data-ttu-id="4649c-109">Références à l’espace de noms <xref:System.Net>.</span><span class="sxs-lookup"><span data-stu-id="4649c-109">References to the <xref:System.Net> namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4649c-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4649c-110">See also</span></span>

- [<span data-ttu-id="4649c-111">programmation de protocoles enfichables</span><span class="sxs-lookup"><span data-stu-id="4649c-111">Programming Pluggable Protocols</span></span>](../../../docs/framework/network-programming/programming-pluggable-protocols.md)
