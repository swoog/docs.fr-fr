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
# <a name="how-to-use-the-xml-documentation-features-c-programming-guide"></a>Guide pratique pour utiliser les fonctionnalités de la documentation XML (Guide de programmation C#)
L’exemple suivant montre un type qui a été documenté.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csProgGuideDocComments#15](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/how-to-use-the-xml-documentation-features_1.cs)]  

L’exemple génère un fichier .xml avec le contenu suivant :

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

## <a name="compiling-the-code"></a>Compilation du code  
 Pour compiler l’exemple, tapez ce qui suit sur la ligne de commande :  
  
 `csc XMLsample.cs /doc:XMLsample.xml`  
  
 Cela créera le fichier XML XMLsample.xml, que vous pouvez afficher dans votre navigateur ou à l’aide de la commande TYPE.  
  
## <a name="robust-programming"></a>Programmation fiable  
 Le début de la documentation XML est symbolisé par trois barres obliques (///). Lorsque vous créez un projet, les Assistants insèrent quelques lignes de début (///) pour vous. Le traitement de ces commentaires présente certaines restrictions :  
  
-   La documentation doit être dans un format XML correct. Si le XML n’est pas correct, un avertissement est généré. En outre, un commentaire indiquant qu’une erreur s’est produite est ajouté au fichier de documentation.  
  
-   Les développeurs sont libres de créer leur propre jeu de balises. Il existe un jeu de balises recommandées (consultez [Balises recommandées pour les commentaires de documentation](recommended-tags-for-documentation-comments.md)). Certaines des balises recommandées ont des significations spéciales :  
  
    -   La balise \<param> est utilisée pour décrire les paramètres. Quand elle est utilisée, le compilateur vérifie que le paramètre existe et que tous les paramètres sont décrits dans la documentation. Si ce n’est pas le cas, le compilateur émet un avertissement.  
  
    -   L’attribut `cref` peut être joint à n’importe quelle balise pour fournir une référence à un élément de code. Le compilateur vérifie l’existence de cet élément de code. Si ce n’est pas le cas, le compilateur émet un avertissement. Le compilateur respecte toutes les instructions `using` lorsqu’il recherche un type décrit dans l’attribut `cref`.  
  
    -   La balise \<summary> est utilisée par IntelliSense dans Visual Studio pour afficher des informations supplémentaires sur un type ou un membre.  
  
        > [!NOTE]
        >  Le fichier XML ne fournit pas des informations complètes sur le type et les membres (par exemple, il ne contient pas d’informations sur le type). Pour obtenir des informations complètes sur un type ou sur un membre, le fichier de documentation doit être utilisé avec la réflexion sur le type ou sur le membre.  
  
## <a name="see-also"></a>Voir aussi  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [/doc (Options du compilateur C#)](../../../csharp/language-reference/compiler-options/doc-compiler-option.md)  
 [Commentaires sur la documentation XML](../../../csharp/programming-guide/xmldoc/xml-documentation-comments.md)
