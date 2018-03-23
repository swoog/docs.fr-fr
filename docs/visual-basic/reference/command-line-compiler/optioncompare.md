---
title: -optioncompare
ms.date: 07/20/2015
ms.prod: .net
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
f1_keywords:
- /optioncompare
- -optioncompare
helpviewer_keywords:
- optioncompare compiler option [Visual Basic]
- -optioncompare compiler option [Visual Basic]
- /optioncompare compiler option [Visual Basic]
ms.assetid: 7237b766-b44d-4cc5-9a3c-885348a7d9e4
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 033be2ce3845ed470d56c2097b89b81d10275046
ms.sourcegitcommit: 498799639937c89de777361aab74261efe7b79ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2018
---
# <a name="-optioncompare"></a><span data-ttu-id="fc526-102">-optioncompare</span><span class="sxs-lookup"><span data-stu-id="fc526-102">-optioncompare</span></span>
<span data-ttu-id="fc526-103">Spécifie la façon dont sont effectuées les comparaisons de chaînes.</span><span class="sxs-lookup"><span data-stu-id="fc526-103">Specifies how string comparisons are made.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fc526-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc526-104">Syntax</span></span>  
  
```  
-optioncompare:{binary | text}  
```  
  
## <a name="remarks"></a><span data-ttu-id="fc526-105">Notes</span><span class="sxs-lookup"><span data-stu-id="fc526-105">Remarks</span></span>  
 <span data-ttu-id="fc526-106">Vous pouvez spécifier `-optioncompare` dans un des deux formes : `-optioncompare:binary` pour utiliser des comparaisons de chaînes binaires et `-optioncompare:text` pour utiliser des comparaisons de chaînes de texte.</span><span class="sxs-lookup"><span data-stu-id="fc526-106">You can specify `-optioncompare` in one of two forms: `-optioncompare:binary` to use binary string comparisons, and `-optioncompare:text` to use text string comparisons.</span></span> <span data-ttu-id="fc526-107">Par défaut, le compilateur utilise `-optioncompare:binary`.</span><span class="sxs-lookup"><span data-stu-id="fc526-107">By default, the compiler uses `-optioncompare:binary`.</span></span>  
  
 <span data-ttu-id="fc526-108">Dans Microsoft Windows, la page de codes actuelle détermine l’ordre de tri binaire.</span><span class="sxs-lookup"><span data-stu-id="fc526-108">In Microsoft Windows, the current code page determines the binary sort order.</span></span> <span data-ttu-id="fc526-109">Un ordre de tri binaire standard est la suivante :</span><span class="sxs-lookup"><span data-stu-id="fc526-109">A typical binary sort order is as follows:</span></span>  
  
 `A < B < E < Z < a < b < e < z < À < Ê < Ø < à < ê < ø`  
  
 <span data-ttu-id="fc526-110">Les comparaisons de chaînes de texte sont basées sur un ordre de tri de texte respectant la casse déterminé par les paramètres régionaux de votre système.</span><span class="sxs-lookup"><span data-stu-id="fc526-110">Text-based string comparisons are based on a case-insensitive text sort order determined by your system's locale.</span></span> <span data-ttu-id="fc526-111">Un ordre de tri de texte par défaut est la suivante :</span><span class="sxs-lookup"><span data-stu-id="fc526-111">A typical text sort order is as follows:</span></span>  
  
 `(A = a) < (À = à) < (B=b) < (E=e) < (Ê = ê) < (Z=z) < (Ø = ø)`  
  
### <a name="to-set--optioncompare-in-the-visual-studio-ide"></a><span data-ttu-id="fc526-112">Pour définir des - optioncompare dans l’IDE de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fc526-112">To set -optioncompare in the Visual Studio IDE</span></span>  
  
1.  <span data-ttu-id="fc526-113">Sélectionnez un projet dans l' **Explorateur de solutions**.</span><span class="sxs-lookup"><span data-stu-id="fc526-113">Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="fc526-114">Dans le menu **Projet**, cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="fc526-114">On the **Project** menu, click **Properties**.</span></span>   
  
2.  <span data-ttu-id="fc526-115">Cliquez sur l’onglet **Compiler**.</span><span class="sxs-lookup"><span data-stu-id="fc526-115">Click the **Compile** tab.</span></span>  
  
3.  <span data-ttu-id="fc526-116">Modifiez la valeur dans la **Option Compare** boîte.</span><span class="sxs-lookup"><span data-stu-id="fc526-116">Modify the value in the **Option Compare** box.</span></span>  
  
### <a name="to-set--optioncompare-programmatically"></a><span data-ttu-id="fc526-117">Pour définir - optioncompare par programmation</span><span class="sxs-lookup"><span data-stu-id="fc526-117">To set -optioncompare programmatically</span></span>  
  
-   <span data-ttu-id="fc526-118">Consultez [Option Compare, instruction](../../../visual-basic/language-reference/statements/option-compare-statement.md).</span><span class="sxs-lookup"><span data-stu-id="fc526-118">See [Option Compare Statement](../../../visual-basic/language-reference/statements/option-compare-statement.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="fc526-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="fc526-119">Example</span></span>  
 <span data-ttu-id="fc526-120">Le code suivant compile `ProjFile.vb` et utilise des comparaisons de chaînes binaires.</span><span class="sxs-lookup"><span data-stu-id="fc526-120">The following code compiles `ProjFile.vb` and uses binary string comparisons.</span></span>  
  
```console
vbc -optioncompare:binary projFile.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="fc526-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc526-121">See Also</span></span>  
 [<span data-ttu-id="fc526-122">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="fc526-122">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="fc526-123">-optionexplicit</span><span class="sxs-lookup"><span data-stu-id="fc526-123">-optionexplicit</span></span>](../../../visual-basic/reference/command-line-compiler/optionexplicit.md)  
 [<span data-ttu-id="fc526-124">-optionstrict</span><span class="sxs-lookup"><span data-stu-id="fc526-124">-optionstrict</span></span>](../../../visual-basic/reference/command-line-compiler/optionstrict.md)  
 [<span data-ttu-id="fc526-125">-optioninfer</span><span class="sxs-lookup"><span data-stu-id="fc526-125">-optioninfer</span></span>](../../../visual-basic/reference/command-line-compiler/optioninfer.md)  
 [<span data-ttu-id="fc526-126">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="fc526-126">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [<span data-ttu-id="fc526-127">Option Compare (instruction)</span><span class="sxs-lookup"><span data-stu-id="fc526-127">Option Compare Statement</span></span>](../../../visual-basic/language-reference/statements/option-compare-statement.md)  
 [<span data-ttu-id="fc526-128">Valeurs par défaut Visual Basic, Projets, boîte de dialogue Options</span><span class="sxs-lookup"><span data-stu-id="fc526-128">Visual Basic Defaults, Projects, Options Dialog Box</span></span>](/visualstudio/ide/reference/visual-basic-defaults-projects-options-dialog-box)
