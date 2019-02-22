---
title: 'Procédure : Créer des objets GenericPrincipal et GenericIdentity'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Creating Generic Identity Objects
- GenericPrincipal Objects
- Creating GenericPrincipal Objects
- GenericIdentity Objects
ms.assetid: 465694cf-258b-4747-9dae-35b01a5bcdbb
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d8dd255aafe16cf0cb893ff4157b3590b3fc8d03
ms.sourcegitcommit: 07c4368273b446555cb2c85397ea266b39d5fe50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56583678"
---
# <a name="how-to-create-genericprincipal-and-genericidentity-objects"></a><span data-ttu-id="d8715-102">Procédure : Créer des objets GenericPrincipal et GenericIdentity</span><span class="sxs-lookup"><span data-stu-id="d8715-102">How to: Create GenericPrincipal and GenericIdentity Objects</span></span>
<span data-ttu-id="d8715-103">Vous pouvez utiliser la <xref:System.Security.Principal.GenericIdentity> classe conjointement avec la <xref:System.Security.Principal.GenericPrincipal> classe pour créer un schéma d’autorisation qui existe indépendamment d’un domaine Windows.</span><span class="sxs-lookup"><span data-stu-id="d8715-103">You can use the <xref:System.Security.Principal.GenericIdentity> class in conjunction with the <xref:System.Security.Principal.GenericPrincipal> class to create an authorization scheme that exists independent of a Windows domain.</span></span>  
  
### <a name="to-create-a-genericprincipal-object"></a><span data-ttu-id="d8715-104">Pour créer un objet GenericPrincipal</span><span class="sxs-lookup"><span data-stu-id="d8715-104">To create a GenericPrincipal object</span></span>  
  
1.  <span data-ttu-id="d8715-105">Créez une instance de la classe identity et initialisez-la avec le nom que vous souhaitez conserver.</span><span class="sxs-lookup"><span data-stu-id="d8715-105">Create a new instance of the identity class and initialize it with the name you want it to hold.</span></span> <span data-ttu-id="d8715-106">Le code suivant crée un objet **GenericIdentity** et l’initialise avec le nom `MyUser`.</span><span class="sxs-lookup"><span data-stu-id="d8715-106">The following code creates a new **GenericIdentity** object and initializes it with the name `MyUser`.</span></span>  
  
    ```vb  
    Dim myIdentity As New GenericIdentity("MyUser")  
    ```  
  
    ```csharp  
    GenericIdentity myIdentity = new GenericIdentity("MyUser");  
    ```  
  
2.  <span data-ttu-id="d8715-107">Créez une instance de la classe **GenericPrincipal** et initialisez-la avec l’objet **GenericIdentity** créé précédemment et un tableau de chaînes qui représentent les rôles que vous souhaitez associer à ce principal.</span><span class="sxs-lookup"><span data-stu-id="d8715-107">Create a new instance of the **GenericPrincipal** class and initialize it with the previously created **GenericIdentity** object and an array of strings that represent the roles that you want associated with this principal.</span></span> <span data-ttu-id="d8715-108">L’exemple de code suivant spécifie un tableau de chaînes qui représentent un rôle d’administrateur et un rôle d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d8715-108">The following code example specifies an array of strings that represent an administrator role and a user role.</span></span> <span data-ttu-id="d8715-109">Le **GenericPrincipal** est ensuite initialisé avec le **GenericIdentity** précédent et le tableau de chaînes.</span><span class="sxs-lookup"><span data-stu-id="d8715-109">The **GenericPrincipal** is then initialized with the previous **GenericIdentity** and the string array.</span></span>  
  
    ```vb  
    Dim myStringArray As String() = {"Manager", "Teller"}  
    DIm myPrincipal As New GenericPrincipal(myIdentity, myStringArray)  
    ```  
  
    ```csharp  
    String[] myStringArray = {"Manager", "Teller"};  
    GenericPrincipal myPrincipal = new GenericPrincipal(myIdentity, myStringArray);  
    ```  
  
3.  <span data-ttu-id="d8715-110">Utilisez le code suivant pour joindre le principal au thread actuel.</span><span class="sxs-lookup"><span data-stu-id="d8715-110">Use the following code to attach the principal to the current thread.</span></span> <span data-ttu-id="d8715-111">Ceci est utile dans les situations où le principal doit être validé à plusieurs reprises, il doit être validé par un autre code exécuté dans votre application, ou il doit être validé par un <xref:System.Security.Permissions.PrincipalPermission> objet.</span><span class="sxs-lookup"><span data-stu-id="d8715-111">This is valuable in situations where the principal must be validated several times, it must be validated by other code running in your application, or it must be validated by a <xref:System.Security.Permissions.PrincipalPermission> object.</span></span> <span data-ttu-id="d8715-112">Vous pouvez toujours exécuter une validation basée sur les rôles sur l’objet principal sans le joindre au thread.</span><span class="sxs-lookup"><span data-stu-id="d8715-112">You can still perform role-based validation on the principal object without attaching it to the thread.</span></span> <span data-ttu-id="d8715-113">Pour plus d’informations, consultez [Remplacement d’un objet Principal](../../../docs/standard/security/replacing-a-principal-object.md).</span><span class="sxs-lookup"><span data-stu-id="d8715-113">For more information, see [Replacing a Principal Object](../../../docs/standard/security/replacing-a-principal-object.md).</span></span>  
  
    ```vb  
    Thread.CurrentPrincipal = myPrincipal  
    ```  
  
    ```csharp  
    Thread.CurrentPrincipal = myPrincipal;  
    ```  
  
## <a name="example"></a><span data-ttu-id="d8715-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="d8715-114">Example</span></span>  
 <span data-ttu-id="d8715-115">L’exemple de code suivant montre comment créer une instance d’un **GenericPrincipal** et d’un **GenericIdentity**.</span><span class="sxs-lookup"><span data-stu-id="d8715-115">The following code example demonstrates how to create an instance of a **GenericPrincipal** and a **GenericIdentity**.</span></span> <span data-ttu-id="d8715-116">Ce code affiche les valeurs de ces objets dans la console.</span><span class="sxs-lookup"><span data-stu-id="d8715-116">This code displays the values of these objects to the console.</span></span>  
  
```vb  
Imports System  
Imports System.Security.Principal  
Imports System.Threading  
  
Public Class Class1  
  
    Public Shared Sub Main()  
        ' Create generic identity.  
        Dim myIdentity As New GenericIdentity("MyIdentity")  
  
        ' Create generic principal.  
        Dim myStringArray As String() =  {"Manager", "Teller"}  
        Dim myPrincipal As New GenericPrincipal(myIdentity, myStringArray)  
  
        ' Attach the principal to the current thread.  
        ' This is not required unless repeated validation must occur,  
        ' other code in your application must validate, or the   
        ' PrincipalPermisson object is used.   
        Thread.CurrentPrincipal = myPrincipal  
  
        ' Print values to the console.  
        Dim name As String = myPrincipal.Identity.Name  
        Dim auth As Boolean = myPrincipal.Identity.IsAuthenticated  
        Dim isInRole As Boolean = myPrincipal.IsInRole("Manager")  
  
        Console.WriteLine("The name is: {0}", name)  
        Console.WriteLine("The isAuthenticated is: {0}", auth)  
        Console.WriteLine("Is this a Manager? {0}", isInRole)  
  
    End Sub  
  
End Class  
```  
  
```csharp  
using System;  
using System.Security.Principal;  
using System.Threading;  
  
public class Class1  
{  
    public static int Main(string[] args)  
    {  
    // Create generic identity.  
    GenericIdentity myIdentity = new GenericIdentity("MyIdentity");  
  
    // Create generic principal.  
    String[] myStringArray = {"Manager", "Teller"};  
    GenericPrincipal myPrincipal =   
        new GenericPrincipal(myIdentity, myStringArray);  
  
    // Attach the principal to the current thread.  
    // This is not required unless repeated validation must occur,  
    // other code in your application must validate, or the   
    // PrincipalPermisson object is used.   
    Thread.CurrentPrincipal = myPrincipal;  
  
    // Print values to the console.  
    String name =  myPrincipal.Identity.Name;  
    bool auth =  myPrincipal.Identity.IsAuthenticated;   
    bool isInRole =  myPrincipal.IsInRole("Manager");  
  
    Console.WriteLine("The name is: {0}", name);  
    Console.WriteLine("The isAuthenticated is: {0}", auth);  
    Console.WriteLine("Is this a Manager? {0}", isInRole);  
  
    return 0;  
    }  
}  
```  
  
 <span data-ttu-id="d8715-117">Lorsqu’elle est exécutée, l’application affiche une sortie similaire à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="d8715-117">When executed, the application displays output similar to the following.</span></span>  
  
```  
The Name is: MyIdentity  
The IsAuthenticated is: True  
Is this a Manager? True  
```  
  
## <a name="see-also"></a><span data-ttu-id="d8715-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8715-118">See also</span></span>

- <xref:System.Security.Principal.GenericIdentity>
- <xref:System.Security.Principal.GenericPrincipal>
- <xref:System.Security.Permissions.PrincipalPermission>
- [<span data-ttu-id="d8715-119">Remplacement d’un objet Principal</span><span class="sxs-lookup"><span data-stu-id="d8715-119">Replacing a Principal Object</span></span>](../../../docs/standard/security/replacing-a-principal-object.md)
- [<span data-ttu-id="d8715-120">Objets Principal et Identity</span><span class="sxs-lookup"><span data-stu-id="d8715-120">Principal and Identity Objects</span></span>](../../../docs/standard/security/principal-and-identity-objects.md)
