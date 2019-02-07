---
title: <include> - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- include
- <include>
helpviewer_keywords:
- <include> C# XML tag
- include C# XML tag
ms.assetid: a8a70302-6196-4643-bd09-ef33f411f18f
ms.openlocfilehash: 1e933647487f966e9f8448cf60a2bdecdd29cdff
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55286259"
---
# <a name="include-c-programming-guide"></a><span data-ttu-id="34a7d-102">\<include> (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="34a7d-102">\<include> (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="34a7d-103">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34a7d-103">Syntax</span></span>  
  
```xml  
<include file='filename' path='tagpath[@name="id"]' />  
```  
  
#### <a name="parameters"></a><span data-ttu-id="34a7d-104">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34a7d-104">Parameters</span></span>  
 `filename`  
 <span data-ttu-id="34a7d-105">Nom du fichier XML contenant la documentation.</span><span class="sxs-lookup"><span data-stu-id="34a7d-105">The name of the XML file containing the documentation.</span></span> <span data-ttu-id="34a7d-106">Le nom de fichier peut être qualifié avec un chemin relatif au fichier de code source.</span><span class="sxs-lookup"><span data-stu-id="34a7d-106">The file name can be qualified with a path relative to the source code file.</span></span> <span data-ttu-id="34a7d-107">Mettez `filename` entre guillemets simples (' ').</span><span class="sxs-lookup"><span data-stu-id="34a7d-107">Enclose `filename` in single quotation marks (' ').</span></span>  
  
 `tagpath`  
 <span data-ttu-id="34a7d-108">Chemin des balises contenues dans `filename` qui mène à la balise `name`.</span><span class="sxs-lookup"><span data-stu-id="34a7d-108">The path of the tags in `filename` that leads to the tag `name`.</span></span> <span data-ttu-id="34a7d-109">Mettez le chemin entre guillemets simples (' ').</span><span class="sxs-lookup"><span data-stu-id="34a7d-109">Enclose the path in single quotation marks (' ').</span></span>  
  
 `name`  
 <span data-ttu-id="34a7d-110">Spécificateur de nom contenu dans la balise qui précède les commentaires ; `name` possède un `id`.</span><span class="sxs-lookup"><span data-stu-id="34a7d-110">The name specifier in the tag that precedes the comments; `name` will have an `id`.</span></span>  
  
 `id`  
 <span data-ttu-id="34a7d-111">ID de la balise qui précède les commentaires.</span><span class="sxs-lookup"><span data-stu-id="34a7d-111">The ID for the tag that precedes the comments.</span></span> <span data-ttu-id="34a7d-112">Mettez l’ID entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="34a7d-112">Enclose the ID in double quotation marks (" ").</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="34a7d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="34a7d-113">Remarks</span></span>  
 <span data-ttu-id="34a7d-114">La balise \<include> vous permet de faire référence à des commentaires dans un autre fichier qui décrivent les types et les membres dans votre code source.</span><span class="sxs-lookup"><span data-stu-id="34a7d-114">The \<include> tag lets you refer to comments in another file that describe the types and members in your source code.</span></span> <span data-ttu-id="34a7d-115">Il s’agit d’une solution alternative au placement direct des commentaires de la documentation dans votre fichier de code source.</span><span class="sxs-lookup"><span data-stu-id="34a7d-115">This is an alternative to placing documentation comments directly in your source code file.</span></span> <span data-ttu-id="34a7d-116">En plaçant la documentation dans un fichier distinct, vous pouvez appliquer un contrôle de code source à la documentation indépendamment du code source.</span><span class="sxs-lookup"><span data-stu-id="34a7d-116">By putting the documentation in a separate file, you can apply source control to the documentation separately from the source code.</span></span> <span data-ttu-id="34a7d-117">Ainsi, une personne peut extraire le fichier de code source et une autre personne peut extraire le fichier de documentation.</span><span class="sxs-lookup"><span data-stu-id="34a7d-117">One person can have the source code file checked out and someone else can have the documentation file checked out.</span></span>  
  
 <span data-ttu-id="34a7d-118">La balise \<include> utilise la syntaxe XML XPath.</span><span class="sxs-lookup"><span data-stu-id="34a7d-118">The \<include> tag uses the XML XPath syntax.</span></span> <span data-ttu-id="34a7d-119">Reportez-vous à la documentation de XPath pour savoir comment personnaliser votre utilisation de \<include>.</span><span class="sxs-lookup"><span data-stu-id="34a7d-119">Refer to XPath documentation for ways to customize your \<include> use.</span></span>  
  
## <a name="example"></a><span data-ttu-id="34a7d-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="34a7d-120">Example</span></span>  
 <span data-ttu-id="34a7d-121">Cet exemple comprend plusieurs fichiers.</span><span class="sxs-lookup"><span data-stu-id="34a7d-121">This is a multifile example.</span></span> <span data-ttu-id="34a7d-122">Le premier, qui utilise \<include>, est présenté ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="34a7d-122">The first file, which uses \<include>, is listed below:</span></span>  
  
 [!code-csharp[csProgGuideDocComments#5](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/include_1.cs)]  
  
 <span data-ttu-id="34a7d-123">Le deuxième, xml_include_tag.doc, contient les commentaires de la documentation suivants :</span><span class="sxs-lookup"><span data-stu-id="34a7d-123">The second file, xml_include_tag.doc, contains the following documentation comments:</span></span>  
  
```xml  
<MyDocs>  
  
<MyMembers name="test">  
<summary>  
The summary for this type.  
</summary>  
</MyMembers>  
  
<MyMembers name="test2">  
<summary>  
The summary for this other type.  
</summary>  
</MyMembers>  
  
</MyDocs>  
```  
  
## <a name="program-output"></a><span data-ttu-id="34a7d-124">Sortie du programme</span><span class="sxs-lookup"><span data-stu-id="34a7d-124">Program Output</span></span>  
 <span data-ttu-id="34a7d-125">La sortie suivante est générée lorsque vous compilez les classes Test et Test2 avec la ligne de commande suivante : `/doc:DocFileName.xml.` Dans Visual Studio, vous spécifiez l’option de commentaires de document XML dans le volet Générer du Concepteur de projets.</span><span class="sxs-lookup"><span data-stu-id="34a7d-125">The following output is generated when you compile the Test and Test2 classes with the following command line: `/doc:DocFileName.xml.` In Visual Studio, you specify the XML doc comments option in the Build pane of the Project Designer.</span></span> <span data-ttu-id="34a7d-126">Dès que le compilateur C# trouve la balise \<include>, il recherche des commentaires de la documentation dans xml_include_tag.doc et non dans le fichier source actuel.</span><span class="sxs-lookup"><span data-stu-id="34a7d-126">When the C# compiler sees the \<include> tag, it will search for documentation comments in xml_include_tag.doc instead of the current source file.</span></span> <span data-ttu-id="34a7d-127">Le compilateur génère ensuite DocFileName.xml, c’est-à-dire le fichier dont se servent les outils de documentation tels que [DocFX](https://dotnet.github.io/docfx/) et [Sandcastle](https://github.com/EWSoftware/SHFB) pour produire la documentation finale.</span><span class="sxs-lookup"><span data-stu-id="34a7d-127">The compiler then generates DocFileName.xml, and this is the file that is consumed by documentation tools such as [DocFX](https://dotnet.github.io/docfx/) and [Sandcastle](https://github.com/EWSoftware/SHFB) to produce the final documentation.</span></span>  
  
```xml  
<?xml version="1.0"?>   
<doc>   
    <assembly>   
        <name>xml_include_tag</name>   
    </assembly>   
    <members>   
        <member name="T:Test">   
            <summary>   
The summary for this type.   
</summary>   
        </member>   
        <member name="T:Test2">   
            <summary>   
The summary for this other type.   
</summary>   
        </member>   
    </members>   
</doc>   
```  
  
## <a name="see-also"></a><span data-ttu-id="34a7d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34a7d-128">See also</span></span>

- [<span data-ttu-id="34a7d-129">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="34a7d-129">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="34a7d-130">Balises recommandées pour les commentaires de documentation</span><span class="sxs-lookup"><span data-stu-id="34a7d-130">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
