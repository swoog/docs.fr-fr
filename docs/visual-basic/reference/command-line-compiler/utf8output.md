---
title: -utf8output (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- -utf8output compiler option [Visual Basic]
- utf8output compiler option [Visual Basic]
- /utf8output compiler option [Visual Basic]
ms.assetid: 8ab36b1e-027a-49ac-85b4-f48997d9e4d6
ms.openlocfilehash: e6bb04364c2f92129993e19c746fd7cb9c18dc8a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54648532"
---
# <a name="-utf8output-visual-basic"></a>-utf8output (Visual Basic)
Affiche les résultats de la compilation au format d'encodage UTF-8.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-utf8output[+ | -]  
```  
  
## <a name="arguments"></a>Arguments  
 `+` &#124; `-`  
 Facultatif. La valeur par défaut pour cette option est `-utf8output-`, ce qui signifie que la sortie du compilateur n’utilise pas l’encodage UTF-8. Les options `-utf8output` et `-utf8output+` sont équivalentes.  
  
## <a name="remarks"></a>Notes  
 Dans certaines configurations internationales, sortie du compilateur ne peut pas être affiché correctement dans la console. Dans ce cas, utilisez `-utf8output` et redirigez la sortie du compilateur vers un fichier.  
  
> [!NOTE]
>  Le `-utf8output` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.  
  
## <a name="example"></a>Exemple  
 Le code suivant compile `In.vb` et indique au compilateur d’afficher de sortie à l’aide du codage UTF-8.  
  
```console  
vbc -utf8output in.vb  
```  
  
## <a name="see-also"></a>Voir aussi
- [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)
- [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
