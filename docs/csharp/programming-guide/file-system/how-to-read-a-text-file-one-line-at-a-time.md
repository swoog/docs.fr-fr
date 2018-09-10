---
title: Guide pratique pour lire un fichier texte ligne par ligne (Visual C#)
ms.date: 07/20/2015
helpviewer_keywords:
- ReadLine method [C#]
- reading text files, line by line
- text files [C#]
ms.assetid: d62e22c5-a13c-48db-af9b-f10c801b0cb1
ms.openlocfilehash: 6ba479e341b71bebe60d9744f239b752d3d81167
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43738766"
---
# <a name="how-to-read-a-text-file-one-line-at-a-time-visual-c"></a><span data-ttu-id="99034-102">Guide pratique pour lire un fichier texte ligne par ligne (Visual C#)</span><span class="sxs-lookup"><span data-stu-id="99034-102">How to: Read a Text File One Line at a Time (Visual C#)</span></span>
<span data-ttu-id="99034-103">Cet exemple lit le contenu d’une chaîne d’un fichier texte, ligne par ligne, à l’aide de la méthode `ReadLine` de la classe `StreamReader`.</span><span class="sxs-lookup"><span data-stu-id="99034-103">This example reads the contents of a text file, one line at a time, into a string using the `ReadLine` method of the `StreamReader` class.</span></span> <span data-ttu-id="99034-104">Chaque ligne de texte est stockée dans la chaîne `line` et s’affiche à l’écran.</span><span class="sxs-lookup"><span data-stu-id="99034-104">Each text line is stored into the string `line` and displayed on the screen.</span></span>  
  
## <a name="example"></a><span data-ttu-id="99034-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="99034-105">Example</span></span>  
  
```csharp
int counter = 0;  
string line;  
  
// Read the file and display it line by line.  
System.IO.StreamReader file =   
    new System.IO.StreamReader(@"c:\test.txt");  
while((line = file.ReadLine()) != null)  
{  
    System.Console.WriteLine(line);  
    counter++;  
}  
  
file.Close();  
System.Console.WriteLine("There were {0} lines.", counter);  
// Suspend the screen.  
System.Console.ReadLine();  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="99034-106">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="99034-106">Compiling the Code</span></span>  
 <span data-ttu-id="99034-107">Copiez le code et collez-le dans la méthode `Main` d’une application console.</span><span class="sxs-lookup"><span data-stu-id="99034-107">Copy the code and paste it into the `Main` method of a console application.</span></span>  
  
 <span data-ttu-id="99034-108">Remplacez `"c:\test.txt"` par le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="99034-108">Replace `"c:\test.txt"` with the actual file name.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="99034-109">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="99034-109">Robust Programming</span></span>  
 <span data-ttu-id="99034-110">Les conditions ci-dessous peuvent générer une exception.</span><span class="sxs-lookup"><span data-stu-id="99034-110">The following conditions may cause an exception:</span></span>  
  
-   <span data-ttu-id="99034-111">Le fichier n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="99034-111">The file may not exist.</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="99034-112">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="99034-112">.NET Framework Security</span></span>  
 <span data-ttu-id="99034-113">Ne vous basez pas sur le nom d'un fichier pour en déterminer le contenu.</span><span class="sxs-lookup"><span data-stu-id="99034-113">Do not make decisions about the contents of the file based on the name of the file.</span></span> <span data-ttu-id="99034-114">Par exemple, le fichier `myFile.cs` peut ne pas être un fichier source C#.</span><span class="sxs-lookup"><span data-stu-id="99034-114">For example, the file `myFile.cs` may not be a C# source file.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="99034-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99034-115">See Also</span></span>

- <xref:System.IO?displayProperty=nameWithType>  
- [<span data-ttu-id="99034-116">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="99034-116">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="99034-117">Système de fichiers et Registre (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="99034-117">File System and the Registry (C# Programming Guide)</span></span>](../../../csharp/programming-guide/file-system/index.md)
