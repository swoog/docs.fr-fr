---
title: 'Procédure : Écrire des données d’objet dans un fichier XML (C#)'
ms.date: 07/20/2015
ms.assetid: 7681eb98-703d-4005-a369-26a7bca0f894
ms.openlocfilehash: 064d7ed61921f3f700311a1b09ee77e0c9818d71
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54554281"
---
# <a name="how-to-write-object-data-to-an-xml-file-c"></a><span data-ttu-id="19d18-102">Procédure : Écrire des données d’objet dans un fichier XML (C#)</span><span class="sxs-lookup"><span data-stu-id="19d18-102">How to: Write Object Data to an XML File (C#)</span></span>
<span data-ttu-id="19d18-103">Cet exemple écrit l’objet d’une classe dans un fichier XML en utilisant la classe <xref:System.Xml.Serialization.XmlSerializer>.</span><span class="sxs-lookup"><span data-stu-id="19d18-103">This example writes the object from a class to an XML file using the <xref:System.Xml.Serialization.XmlSerializer> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="19d18-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="19d18-104">Example</span></span>  
  
```csharp  
public class XMLWrite  
{  
  
   static void Main(string[] args)  
    {  
        WriteXML();  
    }  
  
    public class Book  
    {  
        public String title;   
    }  
  
    public static void WriteXML()  
    {  
        Book overview = new Book();  
        overview.title = "Serialization Overview";  
        System.Xml.Serialization.XmlSerializer writer =   
            new System.Xml.Serialization.XmlSerializer(typeof(Book));  
  
        var path = Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments) + "//SerializationOverview.xml";  
        System.IO.FileStream file = System.IO.File.Create(path);  
  
        writer.Serialize(file, overview);  
        file.Close();  
    }  
}  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="19d18-105">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="19d18-105">Compiling the Code</span></span>  
 <span data-ttu-id="19d18-106">La classe doit disposer d’un constructeur public sans paramètres.</span><span class="sxs-lookup"><span data-stu-id="19d18-106">The class must have a public constructor without parameters.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="19d18-107">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="19d18-107">Robust Programming</span></span>  
 <span data-ttu-id="19d18-108">Les conditions ci-dessous peuvent générer une exception.</span><span class="sxs-lookup"><span data-stu-id="19d18-108">The following conditions may cause an exception:</span></span>  
  
-   <span data-ttu-id="19d18-109">La classe qui est sérialisée n’a pas de constructeur public sans paramètres.</span><span class="sxs-lookup"><span data-stu-id="19d18-109">The class being serialized does not have a public, parameterless constructor.</span></span>  
  
-   <span data-ttu-id="19d18-110">Le fichier existe et est en lecture seule (<xref:System.IO.IOException>).</span><span class="sxs-lookup"><span data-stu-id="19d18-110">The file exists and is read-only (<xref:System.IO.IOException>).</span></span>  
  
-   <span data-ttu-id="19d18-111">Le chemin est trop long (<xref:System.IO.PathTooLongException>).</span><span class="sxs-lookup"><span data-stu-id="19d18-111">The path is too long (<xref:System.IO.PathTooLongException>).</span></span>  
  
-   <span data-ttu-id="19d18-112">Le disque est plein (<xref:System.IO.IOException>).</span><span class="sxs-lookup"><span data-stu-id="19d18-112">The disk is full (<xref:System.IO.IOException>).</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="19d18-113">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="19d18-113">.NET Framework Security</span></span>  
 <span data-ttu-id="19d18-114">Cet exemple crée un fichier s’il n’existe pas déjà.</span><span class="sxs-lookup"><span data-stu-id="19d18-114">This example creates a new file, if the file does not already exist.</span></span> <span data-ttu-id="19d18-115">Si une application doit créer un fichier, elle doit disposer de l’autorisation `Create` pour accéder au dossier.</span><span class="sxs-lookup"><span data-stu-id="19d18-115">If an application needs to create a file, that application needs `Create` access for the folder.</span></span> <span data-ttu-id="19d18-116">Si le fichier existe déjà, l’application a uniquement besoin de l’autorisation `Write`, qui est une autorisation de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="19d18-116">If the file already exists, the application needs only `Write` access, a lesser privilege.</span></span> <span data-ttu-id="19d18-117">Quand cela est possible, il est plus sûr de créer le fichier au cours du déploiement et de n’accorder l’autorisation `Read` que sur un seul fichier, plutôt que l’autorisation `Create` sur un dossier.</span><span class="sxs-lookup"><span data-stu-id="19d18-117">Where possible, it is more secure to create the file during deployment, and only grant `Read` access to a single file, rather than `Create` access for a folder.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="19d18-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19d18-118">See also</span></span>

- <xref:System.IO.StreamWriter>
- [<span data-ttu-id="19d18-119">Guide pratique pour lire des données d’objet à partir d’un fichier XML (C#)</span><span class="sxs-lookup"><span data-stu-id="19d18-119">How to: Read Object Data from an XML File (C#)</span></span>](../../../../csharp/programming-guide/concepts/serialization/how-to-read-object-data-from-an-xml-file.md)
- [<span data-ttu-id="19d18-120">Sérialisation (C#)</span><span class="sxs-lookup"><span data-stu-id="19d18-120">Serialization (C#)</span></span>](../../../../csharp/programming-guide/concepts/serialization/index.md)
