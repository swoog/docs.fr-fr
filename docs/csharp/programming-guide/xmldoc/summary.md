---
title: '&lt;summary&gt; - Guide de programmation C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- <summary>
- summary
helpviewer_keywords:
- <summary> C# XML tag
- summary C# XML tag
ms.assetid: b4c43d92-2067-4eac-a59a-d32f5248c08b
ms.openlocfilehash: 5aaa9b08b422c06cc6b009e5e9d781e8be46af7e
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53237296"
---
# <a name="ltsummarygt-c-programming-guide"></a><span data-ttu-id="a8150-102">&lt;summary&gt; (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="a8150-102">&lt;summary&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="a8150-103">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8150-103">Syntax</span></span>  
  
```xml  
<summary>description</summary>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a8150-104">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8150-104">Parameters</span></span>  
 `description`  
 <span data-ttu-id="a8150-105">Résumé de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a8150-105">A summary of the object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a8150-106">Notes</span><span class="sxs-lookup"><span data-stu-id="a8150-106">Remarks</span></span>  
 <span data-ttu-id="a8150-107">La balise \<summary> doit être utilisée pour décrire un type ou un membre de type.</span><span class="sxs-lookup"><span data-stu-id="a8150-107">The \<summary> tag should be used to describe a type or a type member.</span></span> <span data-ttu-id="a8150-108">Utilisez [\<remarks>](../../../csharp/programming-guide/xmldoc/remarks.md) pour ajouter des informations supplémentaires à une description de type.</span><span class="sxs-lookup"><span data-stu-id="a8150-108">Use [\<remarks>](../../../csharp/programming-guide/xmldoc/remarks.md) to add supplemental information to a type description.</span></span> <span data-ttu-id="a8150-109">Utilisez l’[attribut cref](../../../csharp/programming-guide/xmldoc/cref-attribute.md) pour activer des outils de documentation tels que [Sandcastle](https://github.com/EWSoftware/SHFB) afin de créer des liens hypertexte internes aux pages de documentation pour les éléments de code.</span><span class="sxs-lookup"><span data-stu-id="a8150-109">Use the [cref Attribute](../../../csharp/programming-guide/xmldoc/cref-attribute.md) to enable documentation tools such as [Sandcastle](https://github.com/EWSoftware/SHFB) to create internal hyperlinks to documentation pages for code elements.</span></span>  
  
 <span data-ttu-id="a8150-110">Le texte de la balise \<summary> est la seule source d’informations sur le type dans IntelliSense et il est également affiché dans la fenêtre Explorateur d’objets.</span><span class="sxs-lookup"><span data-stu-id="a8150-110">The text for the \<summary> tag is the only source of information about the type in IntelliSense, and is also displayed in the Object Browser Window.</span></span>  
  
 <span data-ttu-id="a8150-111">Compilez avec [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="a8150-111">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span> <span data-ttu-id="a8150-112">Pour créer la documentation finale basée sur le fichier généré par le compilateur, vous pouvez créer un outil personnalisé ou utiliser un outil tel que [Sandcastle](https://github.com/EWSoftware/SHFB).</span><span class="sxs-lookup"><span data-stu-id="a8150-112">To create the final documentation based on the compiler-generated file, you can create a custom tool, or use a tool such as [Sandcastle](https://github.com/EWSoftware/SHFB).</span></span>  
  
## <a name="example"></a><span data-ttu-id="a8150-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="a8150-113">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#12](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/summary_1.cs)]  
  
 <span data-ttu-id="a8150-114">L’exemple précédent génère le fichier XML suivant.</span><span class="sxs-lookup"><span data-stu-id="a8150-114">The previous example produces the following XML file.</span></span>  
  
```xml  
<?xml version="1.0"?>  
<doc>  
    <assembly>  
        <name>YourNamespace</name>  
    </assembly>  
    <members>  
        <member name="T:DotNetEvents.TestClass">  
            text for class TestClass  
        </member>  
        <member name="M:DotNetEvents.TestClass.DoWork(System.Int32)">  
            <summary>DoWork is a method in the TestClass class.  
            <para>Here's how you could make a second paragraph in a description. <see cref="M:System.Console.WriteLine(System.String)"/> for information about output statements.</para>  
            <seealso cref="M:DotNetEvents.TestClass.Main"/>  
            </summary>  
        </member>  
        <member name="M:DotNetEvents.TestClass.Main">  
            text for Main  
        </member>  
    </members>  
</doc>  
```  
  
## <a name="example"></a><span data-ttu-id="a8150-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="a8150-115">Example</span></span>  
 <span data-ttu-id="a8150-116">L’exemple suivant montre comment effectuer une référence `cref` à un type générique.</span><span class="sxs-lookup"><span data-stu-id="a8150-116">The following example shows how to make a `cref` reference to a generic type.</span></span>  
  
 [!code-csharp[csProgGuideDocComments#11](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/summary_2.cs)]  
  
 <span data-ttu-id="a8150-117">L’exemple précédent génère le fichier XML suivant.</span><span class="sxs-lookup"><span data-stu-id="a8150-117">The previous example produces the following XML file.</span></span>  
  
```xml  
<?xml version="1.0"?>  
<doc>  
    <assembly>  
        <name>YourNamespace</name>  
    </assembly>  
    <members>  
        <member name="T:ExtensionMethodsDemo1.A">  
            <summary cref="T:ExtensionMethodsDemo1.C`1">  
            </summary>  
        </member>  
        <member name="T:ExtensionMethodsDemo1.B">  
            <summary cref="T:C`1">  
            </summary>  
        </member>  
        <member name="T:ExtensionMethodsDemo1.C`1">  
            <summary cref="T:ExtensionMethodsDemo1.A">  
            </summary>  
            <typeparam name="T"></typeparam>  
        </member>  
    </members>  
</doc>  
```  
  
## <a name="see-also"></a><span data-ttu-id="a8150-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8150-118">See Also</span></span>

- [<span data-ttu-id="a8150-119">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="a8150-119">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="a8150-120">Balises recommandées pour les commentaires de documentation</span><span class="sxs-lookup"><span data-stu-id="a8150-120">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
