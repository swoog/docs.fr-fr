---
title: <remarks> - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- remarks
- <remarks>
helpviewer_keywords:
- remarks C# XML tag
- <remarks> C# XML tag
ms.assetid: f8641391-31f3-4735-af7a-c502a5b6a251
ms.openlocfilehash: b2e91b868c35773033418c796b7c43b08e87a28b
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57480375"
---
# <a name="remarks-c-programming-guide"></a>\<remarks> (Guide de programmation C#)
## <a name="syntax"></a>Syntaxe  
  
```xml  
<remarks>description</remarks>  
```  
  
## <a name="parameters"></a>Paramètres  
 `Description`  
 Description du membre.  
  
## <a name="remarks"></a>Remarques  
 La balise \<remarks> permet d’ajouter des informations sur un type en complétant les informations spécifiées par [\<summary>](../../../csharp/programming-guide/xmldoc/summary.md). Ces informations sont affichées dans la fenêtre Explorateur d’objets.  
  
 Compilez avec [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csProgGuideDocComments#9](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideDocComments/CS/DocComments.cs#9)]  
  
## <a name="see-also"></a>Voir aussi

- [Guide de programmation C#](../../../csharp/programming-guide/index.md)
- [Balises recommandées pour les commentaires de documentation](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
