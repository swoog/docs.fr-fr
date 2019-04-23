---
title: <exception> - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- exception
- <exception>
helpviewer_keywords:
- <exception> C# XML tag
- exception C# XML tag
ms.assetid: dd73aac5-3c74-4fcf-9498-f11bff3a2f3c
ms.openlocfilehash: 639e3a345fc8ed3d348461718f73ead6167158db
ms.sourcegitcommit: 438919211260bb415fc8f96ca3eabc33cf2d681d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2019
ms.locfileid: "59610910"
---
# <a name="exception-c-programming-guide"></a>\<exception> (Guide de programmation C#)
## <a name="syntax"></a>Syntaxe  
  
```xml  
<exception cref="member">description</exception>  
```  
  
## <a name="parameters"></a>Paramètres  
 cref = " `member`"  
 Référence à une exception qui est disponible à partir de l’environnement de compilation actuel. Le compilateur vérifie que l’exception donnée existe, et il traduit `member` en nom d’élément canonique dans le fichier XML de sortie. `member` doit apparaître entre guillemets doubles (" ").  
  
 Pour plus d’informations sur la façon de mettre en forme `member` pour référencer un type générique, consultez [Traitement du fichier XML](processing-the-xml-file.md).
  
 `description`  
 Description de l'exception.  
  
## <a name="remarks"></a>Remarques  
 La balise \<exception> vous permet de spécifier quelles exceptions peuvent être levées. Cette balise peut être appliquée à des définitions de méthodes, de propriétés, d’événements et d’indexeurs.  
  
 Compilez avec [/doc](../../language-reference/compiler-options/doc-compiler-option.md) pour traiter les commentaires de documentation dans un fichier.  
  
 Pour plus d’informations sur la gestion des exceptions, consultez [Exceptions et gestion des exceptions](../exceptions/index.md).  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csProgGuideDocComments#4](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideDocComments/CS/DocComments.cs#4)]  
  
## <a name="see-also"></a>Voir aussi

- [Guide de programmation C#](../index.md)
- [Balises recommandées pour les commentaires de documentation](recommended-tags-for-documentation-comments.md)
