---
title: 'Procédure : Créer des assemblys friend non signés (C#)'
ms.date: 07/20/2015
ms.assetid: 78cbc4f0-b021-4141-a4ff-eb4edbd814ca
ms.openlocfilehash: 6bc2d807b3d1cf6c82a9ba6303139b9758581f35
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59318232"
---
# <a name="how-to-create-unsigned-friend-assemblies-c"></a>Procédure : Créer des assemblys friend non signés (C#)
Cet exemple montre comment utiliser des assemblys friend avec des assemblys qui ne sont pas signés.  
  
### <a name="to-create-an-assembly-and-a-friend-assembly"></a>Pour créer un assembly et un assembly friend  
  
1. Ouvrez une invite de commandes.  
  
2. Créez un fichier C# nommé `friend_unsigned_A.` qui contient le code suivant. Le code utilise l’attribut <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> pour déclarer friend_unsigned_B comme assembly friend.  
  
    ```csharp  
    // friend_unsigned_A.cs  
    // Compile with:   
    // csc /target:library friend_unsigned_A.cs  
    using System.Runtime.CompilerServices;  
    using System;  
  
    [assembly: InternalsVisibleTo("friend_unsigned_B")]  
  
    // Type is internal by default.  
    class Class1  
    {  
        public void Test()  
        {  
            Console.WriteLine("Class1.Test");  
        }  
    }  
  
    // Public type with internal member.  
    public class Class2  
    {  
        internal void Test()  
        {  
            Console.WriteLine("Class2.Test");  
        }  
    }  
    ```  
  
3. Compilez et signez friend_unsigned_A à l’aide de la commande suivante.  
  
    ```csharp  
    csc /target:library friend_unsigned_A.cs  
    ```  
  
4. Créez un fichier C# nommé `friend_unsigned_B` qui contient le code suivant. Étant donné que friend_unsigned_A spécifie friend_unsigned_B comme assembly friend, le code de friend_unsigned_B peut accéder aux membres et aux types `internal` de friend_unsigned_A.  
  
    ```csharp  
    // friend_unsigned_B.cs  
    // Compile with:   
    // csc /r:friend_unsigned_A.dll /out:friend_unsigned_B.exe friend_unsigned_B.cs  
    public class Program  
    {  
        static void Main()  
        {  
            // Access an internal type.  
            Class1 inst1 = new Class1();  
            inst1.Test();  
  
            Class2 inst2 = new Class2();  
            // Access an internal member of a public type.  
            inst2.Test();  
  
            System.Console.ReadLine();  
        }  
    }  
    ```  
  
5. Compilez friend_unsigned_B à l’aide de la commande suivante.  
  
    ```csharp  
    csc /r:friend_unsigned_A.dll /out:friend_unsigned_B.exe friend_unsigned_B.cs  
    ```  
  
     Le nom de l’assembly qui est généré par le compilateur doit correspondre au nom de l’assembly friend qui est passé à l’attribut <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute>. Vous devez spécifier explicitement le nom de l’assembly de sortie (.exe ou .dll) à l’aide de l’option du compilateur `/out`. Pour plus d’informations, consultez l’article [/out (C# Compiler Options) (/out [Options du compilateur C#])](../../../../csharp/language-reference/compiler-options/out-compiler-option.md).  
  
6. Exécutez le fichier friend_unsigned_B.exe.  
  
     Le programme imprime deux chaînes : « Class1.Test » et « Class2.Test ».  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 Il existe des similitudes entre l’attribut <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> et la classe <xref:System.Security.Permissions.StrongNameIdentityPermission>. La principale différence est que <xref:System.Security.Permissions.StrongNameIdentityPermission> peut demander des autorisations de sécurité pour exécuter une section de code particulière, tandis que l’attribut <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> contrôle la visibilité des membres et types `internal`.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute>
- [Assemblys dans .NET](../../../../standard/assembly/index.md)
- [Assemblys friend](../../../../standard/assembly/friend-assemblies.md)
- [Procédure : Créer des assemblys friend signés (C#)](../../../../csharp/programming-guide/concepts/assemblies-gac/how-to-create-signed-friend-assemblies.md)
- [Guide de programmation C#](../../../../csharp/programming-guide/index.md)
