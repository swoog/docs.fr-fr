---
title: 'Procédure : Lire des données d’objet à partir d’un fichier XML (C#)'
ms.date: 07/20/2015
ms.assetid: 6ad60d96-a4d9-48e6-a8b0-d7f6f803cafa
ms.openlocfilehash: 33e4395c2be421385948d256a989d06ac215c9c4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54583481"
---
# <a name="how-to-read-object-data-from-an-xml-file-c"></a>Procédure : Lire des données d’objet à partir d’un fichier XML (C#)
Cet exemple lit des données d’objet écrites précédemment dans un fichier XML en utilisant la classe <xref:System.Xml.Serialization.XmlSerializer>.  
  
## <a name="example"></a>Exemple  
  
```csharp  
public class Book  
{  
    public String title;  
}         
  
public void ReadXML()  
{  
    // First write something so that there is something to read ...  
    var b = new Book { title = "Serialization Overview" };  
    var writer = new System.Xml.Serialization.XmlSerializer(typeof(Book));  
    var wfile = new System.IO.StreamWriter(@"c:\temp\SerializationOverview.xml");  
    writer.Serialize(wfile, b);  
    wfile.Close();  
  
    // Now we can read the serialized book ...  
    System.Xml.Serialization.XmlSerializer reader =   
        new System.Xml.Serialization.XmlSerializer(typeof(Book));  
    System.IO.StreamReader file = new System.IO.StreamReader(  
        @"c:\temp\SerializationOverview.xml");  
    Book overview =  (Book)reader.Deserialize(file);  
    file.Close();  
  
    Console.WriteLine(overview.title);  
  
}  
```  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Remplacez le nom du fichier « c:\temp\SerializationOverview.xml » par le nom du fichier qui contient les données sérialisées. Pour plus d’informations sur la sérialisation des données, consultez [Guide pratique pour écrire des données d’objet dans un fichier XML (C#)](../../../../csharp/programming-guide/concepts/serialization/how-to-write-object-data-to-an-xml-file.md).  
  
 La classe doit disposer d’un constructeur public sans paramètres.  
  
 Seuls les propriétés et les champs publics sont désérialisés.  
  
## <a name="robust-programming"></a>Programmation fiable  
 Les conditions ci-dessous peuvent générer une exception.  
  
-   La classe qui est sérialisée n’a pas de constructeur public sans paramètres.  
  
-   Les données du fichier ne représentent pas les données de la classe à désérialiser.  
  
-   Le fichier n'existe pas (<xref:System.IO.IOException>).  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 Vérifiez toujours les entrées et ne désérialisez jamais les données provenant d’une source non fiable. L’objet recréé s’exécute sur un ordinateur local avec les autorisations du code qui l’a désérialisé. Vérifiez toutes les entrées avant d'utiliser les données dans votre application.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.IO.StreamWriter>
- [Guide pratique pour écrire des données d’objet dans un fichier XML (C#)](../../../../csharp/programming-guide/concepts/serialization/how-to-write-object-data-to-an-xml-file.md)
- [Sérialisation (C#)](../../../../csharp/programming-guide/concepts/serialization/index.md)
- [Guide de programmation C#](../../../../csharp/programming-guide/index.md)
