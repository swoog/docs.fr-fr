---
title: Documentation XML (F#)
description: En savoir plus sur la prise en charge dans F# pour générer la documentation à partir de commentaires.
ms.date: 05/16/2016
ms.openlocfilehash: a1fb5eb682ff1188136b31b64e2d7c537d2c9a0e
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53153642"
---
# <a name="xml-documentation"></a>Documentation XML

Vous pouvez générer la documentation à partir de trois barres obliques (/ / /) commentaires dans du code F#. Commentaires XML peuvent précéder les déclarations dans les fichiers de code (.fs) ou des fichiers de signature (.fsi).

## <a name="generating-documentation-from-comments"></a>Générer la Documentation à partir de commentaires

La prise en charge dans F# pour générer la documentation à partir de commentaires est identique à celui dans d’autres langages .NET Framework. Comme dans d’autres langages .NET Framework, le [-doc option du compilateur](https://msdn.microsoft.com/library/434394ae-0d4a-459c-a684-bffede519a04) vous permet de produire un fichier XML qui contient des informations que vous pouvez convertir dans la documentation à l’aide d’un outil tel que Sandcastle. La documentation générée à l’aide des outils conçus pour une utilisation avec les assemblys qui sont écrits dans d’autres langages .NET Framework généralement produire une vue de l’API sont basées sur la forme compilée de F# construit. À moins que les outils prennent en charge F#, documentation générée par ces outils ne correspond pas à la F# vue d’une API.

Pour plus d’informations sur la façon de générer la documentation à partir de XML, consultez [commentaires de Documentation XML &#40;C&#35; Guide de programmation&#41;](https://msdn.microsoft.com/library/b2s063f7).

## <a name="recommended-tags"></a>Balises recommandées

Il existe deux façons d’écrire des commentaires de documentation XML. Une consiste à écrire la documentation directement dans un commentaire de trois barres obliques, sans l’aide de balises XML. Si vous procédez ainsi, le texte de commentaire entier est pris comme documentation de résumé pour la construction de code qui suit immédiatement. Utilisez cette méthode lorsque vous souhaitez écrire uniquement un bref résumé pour chaque construction. L’autre méthode consiste à utiliser des balises XML pour fournir une documentation plus structurée. La deuxième méthode vous permet de spécifier des remarques séparées pour un bref résumé, remarques supplémentaires, la documentation pour chaque paramètre et le paramètre de type et la levée des exceptions et une description de la valeur de retour. Le tableau suivant décrit les balises XML qui sont reconnues dans F# commentaires de code XML.

|Syntaxe de balise|Description|
|----------|-----------|
|**\<c\>**_texte_**\</c\>**|Spécifie que *texte* est le code. Cette balise peut être utilisée par les générateurs de documentation pour afficher du texte dans une police appropriée pour le code.|
|**\<Résumé\>**_texte_ **\< /summary\>**|Spécifie que *texte* est une brève description de l’élément de programme. La description est généralement une ou deux phrases.|
|**\<Remarques\>**_texte_ **\< /Remarques\>**|Spécifie que *texte* contient des informations supplémentaires sur l’élément de programme.|
|**\<Param nom = «**_nom_**»\>**_description_**\</param\>**|Spécifie le nom et la description pour un paramètre de fonction ou une méthode.|
|**\<typeparam nom = «**_nom_**»\>**_description_**\</typeparam\>**|Spécifie le nom et la description pour un paramètre de type.|
|**\<Retourne\>**_texte_ **\< /retourne\>**|Spécifie que *texte* décrit la valeur de retour d’une fonction ou une méthode.|
|**\<exception cref = »**_type_**»\>**_description_**\</exception\>**|Spécifie le type d’exception qui peut être générée et les circonstances dans lesquelles elle est levée.|
|**\<Voir cref = »**_référence_**»\>**_texte_ **\< /consultez\>**|Spécifie un lien inline vers un autre élément de programme. Le *référence* est le nom tel qu’il apparaît dans le fichier de documentation XML. Le *texte* est le texte affiché dans le lien.|
|**\<seealso cref = »**_référence_**» /\>**|Spécifie un lien Voir aussi la documentation pour un autre type. Le *référence* est le nom tel qu’il apparaît dans le fichier de documentation XML. Voir aussi des liens apparaissent généralement en bas d’une page de documentation.|
|**\<Para\>**_texte_**\</para\>**|Spécifie un paragraphe de texte. Cela permet de séparer le texte à l’intérieur de la **notes** balise.|

## <a name="example"></a>Exemple

### <a name="description"></a>Description

Voici un commentaire de documentation XML standard dans un fichier de signature.

### <a name="code"></a>Code

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet7101.fs)]

## <a name="example"></a>Exemple

### <a name="description"></a>Description

L’exemple suivant montre la méthode alternative, sans les balises XML. Dans cet exemple, l’intégralité du texte dans le commentaire est considéré comme un résumé. Notez que si vous ne spécifiez pas explicitement de balise de résumé, vous ne devez pas spécifier d’autres balises, tel que **param** ou **retourne** balises.

### <a name="code"></a>Code

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet7102.fs)]

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)
- [Options du compilateur](compiler-options.md)
