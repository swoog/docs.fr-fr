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
# <a name="how-to-create-genericprincipal-and-genericidentity-objects"></a>Procédure : Créer des objets GenericPrincipal et GenericIdentity
Vous pouvez utiliser la <xref:System.Security.Principal.GenericIdentity> classe conjointement avec la <xref:System.Security.Principal.GenericPrincipal> classe pour créer un schéma d’autorisation qui existe indépendamment d’un domaine Windows.  
  
### <a name="to-create-a-genericprincipal-object"></a>Pour créer un objet GenericPrincipal  
  
1.  Créez une instance de la classe identity et initialisez-la avec le nom que vous souhaitez conserver. Le code suivant crée un objet **GenericIdentity** et l’initialise avec le nom `MyUser`.  
  
    ```vb  
    Dim myIdentity As New GenericIdentity("MyUser")  
    ```  
  
    ```csharp  
    GenericIdentity myIdentity = new GenericIdentity("MyUser");  
    ```  
  
2.  Créez une instance de la classe **GenericPrincipal** et initialisez-la avec l’objet **GenericIdentity** créé précédemment et un tableau de chaînes qui représentent les rôles que vous souhaitez associer à ce principal. L’exemple de code suivant spécifie un tableau de chaînes qui représentent un rôle d’administrateur et un rôle d’utilisateur. Le **GenericPrincipal** est ensuite initialisé avec le **GenericIdentity** précédent et le tableau de chaînes.  
  
    ```vb  
    Dim myStringArray As String() = {"Manager", "Teller"}  
    DIm myPrincipal As New GenericPrincipal(myIdentity, myStringArray)  
    ```  
  
    ```csharp  
    String[] myStringArray = {"Manager", "Teller"};  
    GenericPrincipal myPrincipal = new GenericPrincipal(myIdentity, myStringArray);  
    ```  
  
3.  Utilisez le code suivant pour joindre le principal au thread actuel. Ceci est utile dans les situations où le principal doit être validé à plusieurs reprises, il doit être validé par un autre code exécuté dans votre application, ou il doit être validé par un <xref:System.Security.Permissions.PrincipalPermission> objet. Vous pouvez toujours exécuter une validation basée sur les rôles sur l’objet principal sans le joindre au thread. Pour plus d’informations, consultez [Remplacement d’un objet Principal](../../../docs/standard/security/replacing-a-principal-object.md).  
  
    ```vb  
    Thread.CurrentPrincipal = myPrincipal  
    ```  
  
    ```csharp  
    Thread.CurrentPrincipal = myPrincipal;  
    ```  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant montre comment créer une instance d’un **GenericPrincipal** et d’un **GenericIdentity**. Ce code affiche les valeurs de ces objets dans la console.  
  
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
  
 Lorsqu’elle est exécutée, l’application affiche une sortie similaire à ce qui suit.  
  
```  
The Name is: MyIdentity  
The IsAuthenticated is: True  
Is this a Manager? True  
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Security.Principal.GenericIdentity>
- <xref:System.Security.Principal.GenericPrincipal>
- <xref:System.Security.Permissions.PrincipalPermission>
- [Remplacement d’un objet Principal](../../../docs/standard/security/replacing-a-principal-object.md)
- [Objets Principal et Identity](../../../docs/standard/security/principal-and-identity-objects.md)
