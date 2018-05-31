---
title: Guide pratique pour utiliser les fonctionnalités de la documentation XML (Guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- XML documentation [C#]
- C# language, XML documentation features
ms.assetid: 8f33917b-9577-4c9a-818a-640dbbb0b399
ms.openlocfilehash: d7f1f51040033cf25f7f1aefb04d249e6e028ca3
ms.sourcegitcommit: 77d9a94dac4c05827ed0663d95e0f9ad35d6682e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2018
ms.locfileid: "34472774"
---
# <a name="how-to-use-the-xml-documentation-features-c-programming-guide"></a><span data-ttu-id="63431-102">Guide pratique pour utiliser les fonctionnalités de la documentation XML (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="63431-102">How to: Use the XML Documentation Features (C# Programming Guide)</span></span>
<span data-ttu-id="63431-103">L’exemple suivant montre un type qui a été documenté.</span><span class="sxs-lookup"><span data-stu-id="63431-103">The following sample provides a basic overview of a type that has been documented.</span></span>  
  
## <a name="example"></a><span data-ttu-id="63431-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="63431-104">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#15](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/how-to-use-the-xml-documentation-features_1.cs)]  

<span data-ttu-id="63431-105">L’exemple génère un fichier .xml avec le contenu suivant :</span><span class="sxs-lookup"><span data-stu-id="63431-105">The example generates an .xml file with the following contents:</span></span>

```xml  
<?xml version="1.0"?>  
<doc>  
 <assembly>  
 <name>xmlsample</name>  
 </assembly>  
 <members>  
 <member name="T:SomeClass">  
 <summary>  
 Class level summary documentation goes here.</summary>  
 <remarks>  
 Longer comments can be associated with a type or member  
 through the remarks tag</remarks>  
 </member>  
 <member name="F:SomeClass.m_Name">  
 <summary>  
 Store for the name property</summary>  
 </member>  
 <member name="M:SomeClass.#ctor">  
 <summary>The class constructor.</summary>  
 </member>  
 <member name="M:SomeClass.SomeMethod(System.String)">  
 <summary>  
 Description for SomeMethod.</summary>  
 <param name="s"> Parameter description for s goes here</param>  
 <seealso cref="T:System.String">  
 You can use the cref attribute on any tag to reference a type or member  
 and the compiler will check that the reference exists. </seealso>  
 </member>  
 <member name="M:SomeClass.SomeOtherMethod">  
 <summary>  
 Some other method. </summary>  
 <returns>  
 Return results are described through the returns tag.</returns>  
 <seealso cref="M:SomeClass.SomeMethod(System.String)">  
 Notice the use of the cref attribute to reference a specific method </seealso>  
 </member>  
 <member name="M:SomeClass.Main(System.String[])">  
 <summary>  
 The entry point for the application.  
 </summary>  
 <param name="args"> A list of command line arguments</param>  
 </member>  
 <member name="P:SomeClass.Name">  
 <summary>  
 Name property </summary>  
 <value>A value tag is used to describe the property value</value>  
 </member>  
 </members>  
</doc>   
```

## <a name="compiling-the-code"></a><span data-ttu-id="63431-106">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="63431-106">Compiling the Code</span></span>  
 <span data-ttu-id="63431-107">Pour compiler l’exemple, tapez ce qui suit sur la ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="63431-107">To compile the example, type the following command line:</span></span>  
  
 `csc XMLsample.cs /doc:XMLsample.xml`  
  
 <span data-ttu-id="63431-108">Cela créera le fichier XML XMLsample.xml, que vous pouvez afficher dans votre navigateur ou à l’aide de la commande TYPE.</span><span class="sxs-lookup"><span data-stu-id="63431-108">This will create the XML file XMLsample.xml, which you can view in your browser or by using the TYPE command.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="63431-109">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="63431-109">Robust Programming</span></span>  
 <span data-ttu-id="63431-110">Le début de la documentation XML est symbolisé par trois barres obliques (///).</span><span class="sxs-lookup"><span data-stu-id="63431-110">XML documentation starts with ///.</span></span> <span data-ttu-id="63431-111">Lorsque vous créez un projet, les Assistants insèrent quelques lignes de début (///) pour vous.</span><span class="sxs-lookup"><span data-stu-id="63431-111">When you create a new project, the wizards put some starter /// lines in for you.</span></span> <span data-ttu-id="63431-112">Le traitement de ces commentaires présente certaines restrictions :</span><span class="sxs-lookup"><span data-stu-id="63431-112">The processing of these comments has some restrictions:</span></span>  
  
-   <span data-ttu-id="63431-113">La documentation doit être dans un format XML correct.</span><span class="sxs-lookup"><span data-stu-id="63431-113">The documentation must be well-formed XML.</span></span> <span data-ttu-id="63431-114">Si le XML n’est pas correct, un avertissement est généré. En outre, un commentaire indiquant qu’une erreur s’est produite est ajouté au fichier de documentation.</span><span class="sxs-lookup"><span data-stu-id="63431-114">If the XML is not well-formed, a warning is generated and the documentation file will contain a comment that says that an error was encountered.</span></span>  
  
-   <span data-ttu-id="63431-115">Les développeurs sont libres de créer leur propre jeu de balises.</span><span class="sxs-lookup"><span data-stu-id="63431-115">Developers are free to create their own set of tags.</span></span> <span data-ttu-id="63431-116">Il existe un jeu de balises recommandées (consultez [Balises recommandées pour les commentaires de documentation](recommended-tags-for-documentation-comments.md)).</span><span class="sxs-lookup"><span data-stu-id="63431-116">There is a recommended set of tags (see [Recommended tags for documentation comments](recommended-tags-for-documentation-comments.md)).</span></span> <span data-ttu-id="63431-117">Certaines des balises recommandées ont des significations spéciales :</span><span class="sxs-lookup"><span data-stu-id="63431-117">Some of the recommended tags have special meanings:</span></span>  
  
    -   <span data-ttu-id="63431-118">La balise \<param> est utilisée pour décrire les paramètres.</span><span class="sxs-lookup"><span data-stu-id="63431-118">The \<param> tag is used to describe parameters.</span></span> <span data-ttu-id="63431-119">Quand elle est utilisée, le compilateur vérifie que le paramètre existe et que tous les paramètres sont décrits dans la documentation.</span><span class="sxs-lookup"><span data-stu-id="63431-119">If used, the compiler will verify that the parameter exists and that all parameters are described in the documentation.</span></span> <span data-ttu-id="63431-120">Si ce n’est pas le cas, le compilateur émet un avertissement.</span><span class="sxs-lookup"><span data-stu-id="63431-120">If the verification failed, the compiler issues a warning.</span></span>  
  
    -   <span data-ttu-id="63431-121">L’attribut `cref` peut être joint à n’importe quelle balise pour fournir une référence à un élément de code.</span><span class="sxs-lookup"><span data-stu-id="63431-121">The `cref` attribute can be attached to any tag to provide a reference to a code element.</span></span> <span data-ttu-id="63431-122">Le compilateur vérifie l’existence de cet élément de code.</span><span class="sxs-lookup"><span data-stu-id="63431-122">The compiler will verify that this code element exists.</span></span> <span data-ttu-id="63431-123">Si ce n’est pas le cas, le compilateur émet un avertissement.</span><span class="sxs-lookup"><span data-stu-id="63431-123">If the verification failed, the compiler issues a warning.</span></span> <span data-ttu-id="63431-124">Le compilateur respecte toutes les instructions `using` lorsqu’il recherche un type décrit dans l’attribut `cref`.</span><span class="sxs-lookup"><span data-stu-id="63431-124">The compiler respects any `using` statements when it looks for a type described in the `cref` attribute.</span></span>  
  
    -   <span data-ttu-id="63431-125">La balise \<summary> est utilisée par IntelliSense dans Visual Studio pour afficher des informations supplémentaires sur un type ou un membre.</span><span class="sxs-lookup"><span data-stu-id="63431-125">The \<summary> tag is used by IntelliSense inside Visual Studio to display additional information about a type or member.</span></span>  
  
        > [!NOTE]
        >  <span data-ttu-id="63431-126">Le fichier XML ne fournit pas des informations complètes sur le type et les membres (par exemple, il ne contient pas d’informations sur le type).</span><span class="sxs-lookup"><span data-stu-id="63431-126">The XML file does not provide full information about the type and members (for example, it does not contain any type information).</span></span> <span data-ttu-id="63431-127">Pour obtenir des informations complètes sur un type ou sur un membre, le fichier de documentation doit être utilisé avec la réflexion sur le type ou sur le membre.</span><span class="sxs-lookup"><span data-stu-id="63431-127">To get full information about a type or member, the documentation file must be used together with reflection on the actual type or member.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="63431-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63431-128">See Also</span></span>  
 [<span data-ttu-id="63431-129">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="63431-129">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="63431-130">/doc (Options du compilateur C#)</span><span class="sxs-lookup"><span data-stu-id="63431-130">/doc (C# Compiler Options)</span></span>](../../../csharp/language-reference/compiler-options/doc-compiler-option.md)  
 [<span data-ttu-id="63431-131">Commentaires sur la documentation XML</span><span class="sxs-lookup"><span data-stu-id="63431-131">XML Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/xml-documentation-comments.md)
