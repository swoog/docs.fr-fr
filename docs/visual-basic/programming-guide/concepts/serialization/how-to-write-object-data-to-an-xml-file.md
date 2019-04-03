---
title: 'Procédure : Écrire des données de l’objet dans un fichier XML (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: f7966480-5ed2-43ac-9894-33427436de2a
ms.openlocfilehash: 52b896b0191f29f68cc31e02fc325638ca6341b4
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58843732"
---
# <a name="how-to-write-object-data-to-an-xml-file-visual-basic"></a>Procédure : Écrire des données de l’objet dans un fichier XML (Visual Basic)
Cet exemple écrit l’objet d’une classe dans un fichier XML en utilisant la classe <xref:System.Xml.Serialization.XmlSerializer>.  
  
## <a name="example"></a>Exemple  
  
```vb  
Public Module XMLWrite  
  
    Sub Main()  
        WriteXML()  
    End Sub  
  
    Public Class Book  
        Public Title As String  
    End Class  
  
    Public Sub WriteXML()  
        Dim overview As New Book  
        overview.Title = "Serialization Overview"  
        Dim writer As New System.Xml.Serialization.XmlSerializer(GetType(Book))  
        Dim file As New System.IO.StreamWriter(  
            "c:\temp\SerializationOverview.xml")  
        writer.Serialize(file, overview)  
        file.Close()  
    End Sub  
End Module  
```  
  
## <a name="compiling-the-code"></a>Compilation du code  
 La classe doit disposer d’un constructeur public sans paramètres.  
  
## <a name="robust-programming"></a>Programmation fiable  
 Les conditions ci-dessous peuvent générer une exception.  
  
-   La classe qui est sérialisée n’a pas de constructeur public sans paramètres.  
  
-   Le fichier existe et est en lecture seule (<xref:System.IO.IOException>).  
  
-   Le chemin est trop long (<xref:System.IO.PathTooLongException>).  
  
-   Le disque est plein (<xref:System.IO.IOException>).  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 Cet exemple crée un fichier s’il n’existe pas déjà. Si une application doit créer un fichier, elle doit disposer de l’autorisation `Create` pour accéder au dossier. Si le fichier existe déjà, l’application a uniquement besoin de l’autorisation `Write`, qui est une autorisation de niveau inférieur. Quand cela est possible, il est plus sûr de créer le fichier au cours du déploiement et de n’accorder l’autorisation `Read` que sur un seul fichier, plutôt que l’autorisation `Create` sur un dossier.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.IO.StreamWriter>
- [Guide pratique pour Lire les données d’objet à partir d’un fichier XML (Visual Basic)](../../../../visual-basic/programming-guide/concepts/serialization/how-to-read-object-data-from-an-xml-file.md)
- [Sérialisation (Visual Basic)](../../../../visual-basic/programming-guide/concepts/serialization/index.md)
