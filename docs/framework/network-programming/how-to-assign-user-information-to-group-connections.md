---
title: 'Comment : assigner des informations utilisateur aux connexions de groupe'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 7ce550d6-8f7c-4ea7-add8-5bc27a7b51be
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 009c23d0015f366ab5f1ee92609f0131465d827b
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2018
ms.locfileid: "47193096"
---
# <a name="how-to-assign-user-information-to-group-connections"></a><span data-ttu-id="6472c-102">Comment : assigner des informations utilisateur aux connexions de groupe</span><span class="sxs-lookup"><span data-stu-id="6472c-102">How to: Assign User Information to Group Connections</span></span>

  
 <span data-ttu-id="6472c-103">L’exemple suivant montre comment assigner des informations utilisateur aux connexions de groupe, en supposant que l’application définit les variables *UserName*, *SecurelyStoredPassword* et *Domain* avant que cette section de code ne soit appelée et que la variable *UserName* est unique.</span><span class="sxs-lookup"><span data-stu-id="6472c-103">The following example demonstrates how to assign user information to group connections, assuming that the application sets the variables *UserName*, *SecurelyStoredPassword*, and *Domain* before this section of code is called and that *UserName* is unique.</span></span>  
  
### <a name="to-assign-user-information-to-a-group-connection"></a><span data-ttu-id="6472c-104">Pour assigner des informations utilisateur à une connexion de groupe</span><span class="sxs-lookup"><span data-stu-id="6472c-104">To assign user information to a group connection</span></span>  
  
1.  <span data-ttu-id="6472c-105">Créez un nom de groupe de connexions.</span><span class="sxs-lookup"><span data-stu-id="6472c-105">Create a connection group name.</span></span>  
  
    ```csharp  
    SHA1Managed Sha1 = new SHA1Managed();  
    Byte[] updHash = Sha1.ComputeHash(Encoding.UTF8.GetBytes(UserName + SecurelyStoredPassword + Domain));  
    String secureGroupName = Encoding.Default.GetString(updHash);  
    ```  
  
    ```vb  
    Dim Sha1 As New SHA1Managed()  
    Dim updHash As [Byte]() = Sha1.ComputeHash(Encoding.UTF8.GetBytes((UserName + SecurelyStoredPassword + Domain)))  
    Dim secureGroupName As [String] = Encoding.Default.GetString(updHash)  
    ```  
  
2.  <span data-ttu-id="6472c-106">Créez une demande pour une URL spécifique.</span><span class="sxs-lookup"><span data-stu-id="6472c-106">Create a request for a specific URL.</span></span> <span data-ttu-id="6472c-107">Par exemple, le code suivant crée une demande pour l’URL `http://www.contoso.com.`</span><span class="sxs-lookup"><span data-stu-id="6472c-107">For example, the following code creates a request for the URL `http://www.contoso.com.`</span></span>  
  
    ```csharp  
    WebRequest myWebRequest=WebRequest.Create("http://www.contoso.com");  
    ```  
  
    ```vb  
    Dim myWebRequest As WebRequest = WebRequest.Create("http://www.contoso.com")  
    ```  
  
3.  <span data-ttu-id="6472c-108">Définissez les informations d’identification et la valeur GroupName de la connexion pour la demande web, puis appelez **GetResponse** pour récupérer un objet **WebResponse**.</span><span class="sxs-lookup"><span data-stu-id="6472c-108">Set the credentials and Connection GroupName for the Web request, and call **GetResponse** to retrieve a **WebResponse** object.</span></span>  
  
    ```csharp  
    myWebRequest.Credentials = new NetworkCredential(UserName, SecurelyStoredPassword, Domain);   
    myWebRequest.ConnectionGroupName = secureGroupName;  
  
    WebResponse myWebResponse=myWebRequest.GetResponse();  
    ```  
  
    ```vb  
    myWebRequest.Credentials = New NetworkCredential(UserName, SecurelyStoredPassword, Domain)  
    myWebRequest.ConnectionGroupName = secureGroupName  
  
    Dim myWebResponse As WebResponse = myWebRequest.GetResponse()  
    ```  
  
4.  <span data-ttu-id="6472c-109">Fermez le flux de réponse après avoir utilisé l’objet WebResponse.</span><span class="sxs-lookup"><span data-stu-id="6472c-109">Close the response stream after using the WebRespose object.</span></span>  
  
    ```csharp  
    MyWebResponse.Close();  
    ```  
  
    ```vb  
    MyWebResponse.Close()  
    ```  
  
 <span data-ttu-id="6472c-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="6472c-110">Example</span></span>  
  
```csharp  
// Create a connection group name.  
SHA1Managed Sha1 = new SHA1Managed();  
Byte[] updHash = Sha1.ComputeHash(Encoding.UTF8.GetBytes(UserName + SecurelyStoredPassword + Domain));  
String secureGroupName = Encoding.Default.GetString(updHash);  
  
// Create a request for a specific URL.  
WebRequest myWebRequest=WebRequest.Create("http://www.contoso.com");  
  
myWebRequest.Credentials = new NetworkCredential(UserName, SecurelyStoredPassword, Domain);   
myWebRequest.ConnectionGroupName = secureGroupName;  
  
WebResponse myWebResponse=myWebRequest.GetResponse();  
  
// Insert the code that uses myWebResponse.  
  
MyWebResponse.Close();  
```  
  
```vb  
' Create a secure group name.  
Dim Sha1 As New SHA1Managed()  
Dim updHash As [Byte]() = Sha1.ComputeHash(Encoding.UTF8.GetBytes((UserName + SecurelyStoredPassword + Domain)))  
Dim secureGroupName As [String] = Encoding.Default.GetString(updHash)  
  
' Create a request for a specific URL.  
Dim myWebRequest As WebRequest = WebRequest.Create("http://www.contoso.com")  
  
myWebRequest.Credentials = New NetworkCredential(UserName, SecurelyStoredPassword, Domain)  
myWebRequest.ConnectionGroupName = secureGroupName  
  
Dim myWebResponse As WebResponse = myWebRequest.GetResponse()  
  
' Insert the code that uses myWebResponse.  
MyWebResponse.Close()  
```  
  
## <a name="see-also"></a><span data-ttu-id="6472c-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6472c-111">See Also</span></span>  
 [<span data-ttu-id="6472c-112">Gestion des connexions</span><span class="sxs-lookup"><span data-stu-id="6472c-112">Managing Connections</span></span>](../../../docs/framework/network-programming/managing-connections.md)  
 [<span data-ttu-id="6472c-113">Regroupement de connexions</span><span class="sxs-lookup"><span data-stu-id="6472c-113">Connection Grouping</span></span>](../../../docs/framework/network-programming/connection-grouping.md)
