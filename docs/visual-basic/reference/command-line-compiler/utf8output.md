---
title: -utf8output (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- -utf8output compiler option [Visual Basic]
- utf8output compiler option [Visual Basic]
- /utf8output compiler option [Visual Basic]
ms.assetid: 8ab36b1e-027a-49ac-85b4-f48997d9e4d6
ms.openlocfilehash: 753c92cdf2124ee7fb1b471c7bc543b6db6f3daa
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33653583"
---
# <a name="-utf8output-visual-basic"></a>-utf8output (Visual Basic)
Affiche les résultats de la compilation au format d'encodage UTF-8.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-utf8output[+ | -]  
```  
  
## <a name="arguments"></a>Arguments  
 `+` &#124; `-`  
 Facultatif. La valeur par défaut de cette option est `-utf8output-`, ce qui signifie que la sortie du compilateur n’utilise pas le codage UTF-8. Spécification de `-utf8output` est identique à la spécification `-utf8output+`.  
  
## <a name="remarks"></a>Notes  
 Dans certaines configurations internationales, sortie du compilateur ne peut pas être affiché correctement dans la console. Dans ce cas, utilisez `-utf8output` et rediriger la sortie du compilateur vers un fichier.  
  
> [!NOTE]
>  Le `-utf8output` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.  
  
## <a name="example"></a>Exemple  
 Le code suivant compile `In.vb` et indique au compilateur d’afficher de sortie à l’aide du codage UTF-8.  
  
```console  
vbc -utf8output in.vb  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)  
 [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
