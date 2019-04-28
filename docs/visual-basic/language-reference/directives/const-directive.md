---
title: '##Const (directive) (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- vb.#Const
- '#vb.Const'
- '#Const'
helpviewer_keywords:
- '#Const directive'
- conditional compilation [Visual Basic], directives
- Const directive (#Const)
- Visual Basic compiler, compiler directives
- constants [Visual Basic], Const directive
- constants [Visual Basic], declaring
- Const statement [Visual Basic], directive (#Const)
- 'declaring constants [Visual Basic], #const directive'
ms.assetid: 707669e5-23f9-4f17-8622-a0d534429386
ms.openlocfilehash: 5458bbebc6064eb6273b8deb5447b8941e1d233f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61746679"
---
# <a name="const-directive"></a><span data-ttu-id="bdcbc-102">#Const, directive</span><span class="sxs-lookup"><span data-stu-id="bdcbc-102">#Const Directive</span></span>
<span data-ttu-id="bdcbc-103">Définit des constantes conditionnelles du compilateur pour Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bdcbc-103">Defines conditional compiler constants for Visual Basic.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bdcbc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bdcbc-104">Syntax</span></span>  
  
```  
#Const constname = expression  
```  
  
## <a name="parts"></a><span data-ttu-id="bdcbc-105">Composants</span><span class="sxs-lookup"><span data-stu-id="bdcbc-105">Parts</span></span>  
 `constname`  
 <span data-ttu-id="bdcbc-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="bdcbc-106">Required.</span></span> <span data-ttu-id="bdcbc-107">Nom de la constante qui est définie.</span><span class="sxs-lookup"><span data-stu-id="bdcbc-107">Name of the constant being defined.</span></span>  
  
 `expression`  
 <span data-ttu-id="bdcbc-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="bdcbc-108">Required.</span></span> <span data-ttu-id="bdcbc-109">Littéral, autre constante de compilation conditionnelle ou toute combinaison qui comprend tout ou partie des opérateurs arithmétiques ou logiques à l’exception `Is`.</span><span class="sxs-lookup"><span data-stu-id="bdcbc-109">Literal, other conditional compiler constant, or any combination that includes any or all arithmetic or logical operators except `Is`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bdcbc-110">Notes</span><span class="sxs-lookup"><span data-stu-id="bdcbc-110">Remarks</span></span>  
 <span data-ttu-id="bdcbc-111">Constantes de compilation conditionnelle sont toujours privées pour le fichier dans lequel elles apparaissent.</span><span class="sxs-lookup"><span data-stu-id="bdcbc-111">Conditional compiler constants are always private to the file in which they appear.</span></span> <span data-ttu-id="bdcbc-112">Vous ne pouvez pas créer de constantes de compilation publiques à l’aide de la `#Const` directive ; vous pouvez les créer que dans l’interface utilisateur ou avec la `/define` option du compilateur.</span><span class="sxs-lookup"><span data-stu-id="bdcbc-112">You cannot create public compiler constants using the `#Const` directive; you can create them only in the user interface or with the `/define` compiler option.</span></span>  
  
 <span data-ttu-id="bdcbc-113">Vous pouvez utiliser uniquement des constantes de compilation conditionnelle et des littéraux dans `expression`.</span><span class="sxs-lookup"><span data-stu-id="bdcbc-113">You can use only conditional compiler constants and literals in `expression`.</span></span> <span data-ttu-id="bdcbc-114">À l’aide d’une constante standard définie avec `Const` provoque une erreur.</span><span class="sxs-lookup"><span data-stu-id="bdcbc-114">Using a standard constant defined with `Const` causes an error.</span></span> <span data-ttu-id="bdcbc-115">À l’inverse, vous pouvez utiliser des constantes définies avec le `#Const` mot clé uniquement pour la compilation conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="bdcbc-115">Conversely, you can use constants defined with the `#Const` keyword only for conditional compilation.</span></span> <span data-ttu-id="bdcbc-116">Constantes peuvent également être non, auquel cas ils ont une valeur de `Nothing`.</span><span class="sxs-lookup"><span data-stu-id="bdcbc-116">Constants can also be undefined, in which case they have a value of `Nothing`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bdcbc-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="bdcbc-117">Example</span></span>  
 <span data-ttu-id="bdcbc-118">Cet exemple utilise la directive `#Const`.</span><span class="sxs-lookup"><span data-stu-id="bdcbc-118">This example uses the `#Const` directive.</span></span>  
  
 [!code-vb[VbVbalrConditionalComp#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrConditionalComp/VB/Class1.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="bdcbc-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bdcbc-119">See also</span></span>

- [<span data-ttu-id="bdcbc-120">/define (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="bdcbc-120">/define (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/define.md)
- [<span data-ttu-id="bdcbc-121">#If...Then...#Else, directives</span><span class="sxs-lookup"><span data-stu-id="bdcbc-121">#If...Then...#Else Directives</span></span>](../../../visual-basic/language-reference/directives/if-then-else-directives.md)
- [<span data-ttu-id="bdcbc-122">Const (instruction)</span><span class="sxs-lookup"><span data-stu-id="bdcbc-122">Const Statement</span></span>](../../../visual-basic/language-reference/statements/const-statement.md)
- [<span data-ttu-id="bdcbc-123">Compilation conditionnelle</span><span class="sxs-lookup"><span data-stu-id="bdcbc-123">Conditional Compilation</span></span>](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)
- [<span data-ttu-id="bdcbc-124">If...Then...Else (instruction)</span><span class="sxs-lookup"><span data-stu-id="bdcbc-124">If...Then...Else Statement</span></span>](../../../visual-basic/language-reference/statements/if-then-else-statement.md)
