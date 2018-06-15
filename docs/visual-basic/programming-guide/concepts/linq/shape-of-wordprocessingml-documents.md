---
title: Forme des Documents de WordprocessingML (Visual Basic)
ms.date: 07/20/2015
ms.assetid: 2dfb446b-5a07-4c00-9ab3-a74ba734ff3a
ms.openlocfilehash: 1ff5f0e42336e894f0ee808edb61661c1f850284
ms.sourcegitcommit: 2ad7d06f4f469b5d8a5280ac0e0289a81867fc8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2018
ms.locfileid: "35231406"
---
# <a name="shape-of-wordprocessingml-documents-visual-basic"></a><span data-ttu-id="0d4dc-102">Forme des Documents de WordprocessingML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="0d4dc-102">Shape of WordprocessingML Documents (Visual Basic)</span></span>
<span data-ttu-id="0d4dc-103">Cette rubrique présente la forme XML d'un document WordprocessingML.</span><span class="sxs-lookup"><span data-stu-id="0d4dc-103">This topic introduces the XML shape of a WordprocessingML document.</span></span>  
  
## <a name="microsoft-office-formats"></a><span data-ttu-id="0d4dc-104">Formats Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="0d4dc-104">Microsoft Office Formats</span></span>  
 <span data-ttu-id="0d4dc-105">Le format de fichier natif pour la version 2007 de Microsoft Office System est le format XML ouvert Microsoft Office (communément appelé Open XML).</span><span class="sxs-lookup"><span data-stu-id="0d4dc-105">The native file format for the 2007 Microsoft Office system is Office Open XML (commonly called Open XML).</span></span> <span data-ttu-id="0d4dc-106">Open XML est un format XML compatible avec la norme ECMA et actuellement soumis à un processus de normalisation ISO-IEC.</span><span class="sxs-lookup"><span data-stu-id="0d4dc-106">Open XML is an XML-based format that an Ecma standard and is currently going through the ISO-IEC standards process.</span></span> <span data-ttu-id="0d4dc-107">Le langage de balisage pour les fichiers de traitement de texte dans Open XML se nomme WordprocessingML.</span><span class="sxs-lookup"><span data-stu-id="0d4dc-107">The markup language for word processing files within Open XML is called WordprocessingML.</span></span> <span data-ttu-id="0d4dc-108">Ce didacticiel utilise des fichiers sources WordprocessingML comme entrée pour les exemples.</span><span class="sxs-lookup"><span data-stu-id="0d4dc-108">This tutorial uses WordprocessingML source files as input for the examples.</span></span>  
  
 <span data-ttu-id="0d4dc-109">Si vous utilisez Microsoft Office 2003, vous pouvez enregistrer des documents au format Office Open XML si vous avez installé le Module de compatibilité Microsoft Office pour formats de fichiers Word, Excel et PowerPoint 2007.</span><span class="sxs-lookup"><span data-stu-id="0d4dc-109">If you are using Microsoft Office 2003, you can save documents in the Office Open XML format if you have installed the Microsoft Office Compatibility Pack for Word, Excel, and PowerPoint 2007 File Formats.</span></span>  
  
## <a name="the-shape-of-wordprocessingml-documents"></a><span data-ttu-id="0d4dc-110">Forme des documents WordprocessingML</span><span class="sxs-lookup"><span data-stu-id="0d4dc-110">The Shape of WordprocessingML Documents</span></span>  
 <span data-ttu-id="0d4dc-111">La première chose à comprendre est la forme des documents WordprocessingML.</span><span class="sxs-lookup"><span data-stu-id="0d4dc-111">The first thing to understand is the shape of WordprocessingML documents.</span></span> <span data-ttu-id="0d4dc-112">Un document WordprocessingML contient un élément de corps (nommé `w:body`) qui contient les paragraphes du document.</span><span class="sxs-lookup"><span data-stu-id="0d4dc-112">A WordprocessingML document contains a body element (named `w:body`) that contains the paragraphs of the document.</span></span> <span data-ttu-id="0d4dc-113">Chaque paragraphe contient une ou plusieurs exécutions de texte (nommées `w:r`).</span><span class="sxs-lookup"><span data-stu-id="0d4dc-113">Each paragraph contains one or more text runs (named `w:r`).</span></span> <span data-ttu-id="0d4dc-114">Chaque exécution de texte contient un ou plusieurs segments de texte (nommés `w:t`).</span><span class="sxs-lookup"><span data-stu-id="0d4dc-114">Each text run contains one or more text pieces (named `w:t`).</span></span>  
  
 <span data-ttu-id="0d4dc-115">Voici un document WordprocessingML très simple :</span><span class="sxs-lookup"><span data-stu-id="0d4dc-115">The following is a very simple WordprocessingML document:</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8" standalone="yes"?>  
<w:document  
xmlns:ve="http://schemas.openxmlformats.org/markup-compatibility/2006"  
xmlns:o="urn:schemas-microsoft-com:office:office"  
xmlns:r="http://schemas.openxmlformats.org/officeDocument/2006/relationships"  
xmlns:m="http://schemas.openxmlformats.org/officeDocument/2006/math"  
xmlns:v="urn:schemas-microsoft-com:vml"  
xmlns:wp="http://schemas.openxmlformats.org/drawingml/2006/wordprocessingDrawing"  
xmlns:w10="urn:schemas-microsoft-com:office:word"  
xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main"  
xmlns:wne="http://schemas.microsoft.com/office/word/2006/wordml">  
  <w:body>  
    <w:p w:rsidR="00E22EB6"  
         w:rsidRDefault="00E22EB6">  
      <w:r>  
        <w:t>This is a paragraph.</w:t>  
      </w:r>  
    </w:p>  
    <w:p w:rsidR="00E22EB6"  
         w:rsidRDefault="00E22EB6">  
      <w:r>  
        <w:t>This is another paragraph.</w:t>  
      </w:r>  
    </w:p>  
  </w:body>  
</w:document>  
```  
  
 <span data-ttu-id="0d4dc-116">Ce document contient deux paragraphes.</span><span class="sxs-lookup"><span data-stu-id="0d4dc-116">This document contains two paragraphs.</span></span> <span data-ttu-id="0d4dc-117">Tous deux contiennent une seule exécution de texte et chaque exécution de texte contient un seul segment de texte.</span><span class="sxs-lookup"><span data-stu-id="0d4dc-117">They both contain a single text run, and each text run contains a single text piece.</span></span>  
  
 <span data-ttu-id="0d4dc-118">Le moyen le plus simple d'afficher le contenu d'un fichier WordprocessingML au format XML consiste à en créer un à l'aide de Microsoft Word, de l'enregistrer, puis d'exécuter le programme suivant qui imprime le code XML sur la console.</span><span class="sxs-lookup"><span data-stu-id="0d4dc-118">The easiest way to see the contents of a WordprocessingML document in XML form is to create one using Microsoft Word, save it, and then run the following program that prints the XML to the console.</span></span>  
  
 <span data-ttu-id="0d4dc-119">Cet exemple utilise des classes de l'assembly WindowsBase.</span><span class="sxs-lookup"><span data-stu-id="0d4dc-119">This example uses classes found in the WindowsBase assembly.</span></span> <span data-ttu-id="0d4dc-120">Il utilise des types dans l'espace de noms <xref:System.IO.Packaging?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="0d4dc-120">It uses types in the <xref:System.IO.Packaging?displayProperty=nameWithType> namespace.</span></span>  
  
```vb  
Imports <xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main">  
  
Module Module1  
    Sub Main()  
        Dim documentRelationshipType = _  
          "http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument"  
  
        Using wdPackage As Package = _  
          Package.Open("SampleDoc.docx", _  
                       FileMode.Open, FileAccess.Read)  
            Dim docPackageRelationship As PackageRelationship = wdPackage _  
                .GetRelationshipsByType(documentRelationshipType).FirstOrDefault()  
            If (docPackageRelationship IsNot Nothing) Then  
                Dim documentUri As Uri = PackUriHelper.ResolvePartUri( _  
                            New Uri("/", UriKind.Relative), _  
                            docPackageRelationship.TargetUri)  
                Dim documentPart As PackagePart = wdPackage.GetPart(documentUri)  
  
                ' Get the officeDocument part from the package.  
                ' Load the XML in the part into an XDocument instance.  
                Dim xDoc As XDocument = _  
                    XDocument.Load(XmlReader.Create(documentPart.GetStream()))  
                Console.WriteLine(xDoc.Root)  
            End If  
        End Using  
    End Sub  
End Module  
```  
  
## <a name="external-resources"></a><span data-ttu-id="0d4dc-121">Ressources externes</span><span class="sxs-lookup"><span data-stu-id="0d4dc-121">External Resources</span></span>  
 <span data-ttu-id="0d4dc-122">[Présentation des formats de fichier Open XML Microsoft Office (2007)](https://docs.microsoft.com/previous-versions/office/developer/office-2007/aa338205(v=office.12))</span><span class="sxs-lookup"><span data-stu-id="0d4dc-122">[Introducing the Office (2007) Open XML File Formats](https://docs.microsoft.com/previous-versions/office/developer/office-2007/aa338205(v=office.12))</span></span>  
  
 <span data-ttu-id="0d4dc-123">[Vue d’ensemble de WordprocessingML](https://msdn.microsoft.com/en-us/library/aa212812(office.11).aspx)</span><span class="sxs-lookup"><span data-stu-id="0d4dc-123">[Overview of WordprocessingML](https://msdn.microsoft.com/en-us/library/aa212812(office.11).aspx)</span></span>  
  
 [<span data-ttu-id="0d4dc-124">Office 2003: Page de téléchargement des schémas de référence XML</span><span class="sxs-lookup"><span data-stu-id="0d4dc-124">Office 2003: XML Reference Schemas Download page</span></span>](http://go.microsoft.com/fwlink/?LinkId=98095)  
  
## <a name="see-also"></a><span data-ttu-id="0d4dc-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d4dc-125">See Also</span></span>  
 [<span data-ttu-id="0d4dc-126">Didacticiel : Manipulation de contenu dans un Document WordprocessingML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="0d4dc-126">Tutorial: Manipulating Content in a WordprocessingML Document (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/tutorial-manipulating-content-in-a-wordprocessingml-document.md)
