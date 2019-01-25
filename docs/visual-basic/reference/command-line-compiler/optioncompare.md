---
title: -optioncompare
ms.date: 07/20/2015
f1_keywords:
- /optioncompare
- -optioncompare
helpviewer_keywords:
- optioncompare compiler option [Visual Basic]
- -optioncompare compiler option [Visual Basic]
- /optioncompare compiler option [Visual Basic]
ms.assetid: 7237b766-b44d-4cc5-9a3c-885348a7d9e4
ms.openlocfilehash: 86564b7ce419ef6c6e56a6b677b71009830b5fc4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54662307"
---
# <a name="-optioncompare"></a>-optioncompare
Spécifie la façon dont sont effectuées les comparaisons de chaînes.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-optioncompare:{binary | text}  
```  
  
## <a name="remarks"></a>Notes  
 Vous pouvez spécifier `-optioncompare` dans un des deux formes : `-optioncompare:binary` à utiliser des comparaisons de chaînes binaires et `-optioncompare:text` à utiliser des comparaisons de chaînes de texte. Par défaut, le compilateur utilise `-optioncompare:binary`.  
  
 Dans Microsoft Windows, la page de codes actuelle détermine l’ordre de tri binaire. Un ordre de tri binaire standard est la suivante :  
  
 `A < B < E < Z < a < b < e < z < À < Ê < Ø < à < ê < ø`  
  
 Les comparaisons de chaînes textuelles sont basées sur un ordre de tri de texte respectant la casse déterminé par les paramètres régionaux de votre système. Un ordre de tri de texte classique est comme suit :  
  
 `(A = a) < (À = à) < (B=b) < (E=e) < (Ê = ê) < (Z=z) < (Ø = ø)`  
  
### <a name="to-set--optioncompare-in-the-visual-studio-ide"></a>Pour définir - optioncompare dans l’IDE Visual Studio  
  
1.  Sélectionnez un projet dans l' **Explorateur de solutions**. Dans le menu **Projet**, cliquez sur **Propriétés**.   
  
2.  Cliquez sur l’onglet **Compiler**.  
  
3.  Modifiez la valeur dans le **Option Compare** boîte.  
  
### <a name="to-set--optioncompare-programmatically"></a>Pour définir - optioncompare par programmation  
  
-   Consultez [Option Compare (instruction)](../../../visual-basic/language-reference/statements/option-compare-statement.md).  
  
## <a name="example"></a>Exemple  
 Le code suivant compile `ProjFile.vb` et utilise des comparaisons de chaînes binaires.  
  
```console
vbc -optioncompare:binary projFile.vb  
```  
  
## <a name="see-also"></a>Voir aussi
- [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)
- [-optionexplicit](../../../visual-basic/reference/command-line-compiler/optionexplicit.md)
- [-optionstrict](../../../visual-basic/reference/command-line-compiler/optionstrict.md)
- [-optioninfer](../../../visual-basic/reference/command-line-compiler/optioninfer.md)
- [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
- [Option Compare (instruction)](../../../visual-basic/language-reference/statements/option-compare-statement.md)
- [Valeurs par défaut Visual Basic, Projets, boîte de dialogue Options](/visualstudio/ide/reference/visual-basic-defaults-projects-options-dialog-box)
