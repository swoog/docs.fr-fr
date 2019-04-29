---
title: Le nom '<name>' n'est pas déclaré
ms.date: 10/10/2018
f1_keywords:
- bc30451
- vbc30451
helpviewer_keywords:
- BC30451
ms.assetid: 765f099b-e21e-47c6-a906-a065444e56b3
ms.openlocfilehash: 3aadc49f91021409123550ba2712f1acf5b99d83
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61651023"
---
# <a name="name-name-is-not-declared"></a><span data-ttu-id="01e1b-102">Nom de «\<nom >' n’est pas déclaré</span><span class="sxs-lookup"><span data-stu-id="01e1b-102">Name '\<name>' is not declared</span></span>
<span data-ttu-id="01e1b-103">Une instruction fait référence à un élément de programmation, mais le compilateur ne peut pas trouver un élément portant ce nom exact.</span><span class="sxs-lookup"><span data-stu-id="01e1b-103">A statement refers to a programming element, but the compiler cannot find an element with that exact name.</span></span>  
  
 <span data-ttu-id="01e1b-104">**ID d’erreur :** BC30451</span><span class="sxs-lookup"><span data-stu-id="01e1b-104">**Error ID:** BC30451</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="01e1b-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="01e1b-105">To correct this error</span></span>  
  
1. <span data-ttu-id="01e1b-106">Vérifiez l’orthographe du nom dans l’instruction de référence.</span><span class="sxs-lookup"><span data-stu-id="01e1b-106">Check the spelling of the name in the referring statement.</span></span> <span data-ttu-id="01e1b-107">Visual Basic respecte la casse, mais toute autre variation dans l’orthographe est considérée comme un nom complètement différent.</span><span class="sxs-lookup"><span data-stu-id="01e1b-107">Visual Basic is case-insensitive, but any other variation in the spelling is regarded as a completely different name.</span></span> <span data-ttu-id="01e1b-108">Notez que le caractère de soulignement (`_`) fait partie du nom et donc de l’orthographe.</span><span class="sxs-lookup"><span data-stu-id="01e1b-108">Note that the underscore (`_`) is part of the name and therefore part of the spelling.</span></span>  
  
2. <span data-ttu-id="01e1b-109">Vérifiez que vous disposez de l’opérateur d’accès au membre (`.`) entre un objet et son membre.</span><span class="sxs-lookup"><span data-stu-id="01e1b-109">Check that you have the member access operator (`.`) between an object and its member.</span></span> <span data-ttu-id="01e1b-110">Par exemple, si vous disposez d’un contrôle <xref:System.Windows.Forms.TextBox> dont le nom est `TextBox1`, pour accéder à sa propriété <xref:System.Windows.Forms.TextBoxBase.Text%2A> , vous devez taper `TextBox1.Text`.</span><span class="sxs-lookup"><span data-stu-id="01e1b-110">For example, if you have a <xref:System.Windows.Forms.TextBox> control named `TextBox1`, to access its <xref:System.Windows.Forms.TextBoxBase.Text%2A> property you should type `TextBox1.Text`.</span></span> <span data-ttu-id="01e1b-111">Si, au lieu de cela, vous tapez `TextBox1Text`, vous créez un nom différent.</span><span class="sxs-lookup"><span data-stu-id="01e1b-111">If instead you type `TextBox1Text`, you have created a different name.</span></span>  
  
3. <span data-ttu-id="01e1b-112">Si l’orthographe est correcte et que la syntaxe n’importe quel objet d’accès de membre est correcte, vérifiez que l’élément a été déclaré.</span><span class="sxs-lookup"><span data-stu-id="01e1b-112">If the spelling is correct and the syntax of any object member access is correct, verify that the element has been declared.</span></span> <span data-ttu-id="01e1b-113">Pour plus d’informations, consultez [Declared Elements](../../programming-guide/language-features/declared-elements/index.md).</span><span class="sxs-lookup"><span data-stu-id="01e1b-113">For more information, see [Declared Elements](../../programming-guide/language-features/declared-elements/index.md).</span></span>  
  
4. <span data-ttu-id="01e1b-114">Si l’élément de programmation a été déclaré, vérifiez qu’il est dans la portée.</span><span class="sxs-lookup"><span data-stu-id="01e1b-114">If the programming element has been declared, check that it is in scope.</span></span> <span data-ttu-id="01e1b-115">Si l’instruction de référence est en dehors de la région déclarant l’élément de programmation, vous devrez peut-être qualifier le nom d’élément.</span><span class="sxs-lookup"><span data-stu-id="01e1b-115">If the referring statement is outside the region declaring the programming element, you might need to qualify the element name.</span></span> <span data-ttu-id="01e1b-116">Pour plus d'informations, consultez [Scope in Visual Basic](../../programming-guide/language-features/declared-elements/scope.md).</span><span class="sxs-lookup"><span data-stu-id="01e1b-116">For more information, see [Scope in Visual Basic](../../programming-guide/language-features/declared-elements/scope.md).</span></span>  

5. <span data-ttu-id="01e1b-117">Si vous n’utilisez pas un type qualifié complet ou le nom de type et de membre (par exemple, votre code fait référence à une propriété en tant que `MethodInfo.Name` au lieu de `System.Reflection.MethodInfo.Name`), ajoutez un [Imports, instruction](../statements/imports-statement-net-namespace-and-type.md).</span><span class="sxs-lookup"><span data-stu-id="01e1b-117">If you are not using a fully qualified type or type and member name (for example, your code refers to a property as `MethodInfo.Name` instead of `System.Reflection.MethodInfo.Name`), add an [Imports statement](../statements/imports-statement-net-namespace-and-type.md).</span></span>

6. <span data-ttu-id="01e1b-118">Si vous essayez de compiler un projet de SDK-style (un projet avec un \*fichier .vbproj qui commence par la ligne `<Project Sdk="Microsoft.NET.Sdk">`) et le message d’erreur fait référence à un type ou membre dans l’assembly Microsoft.VisualBasic.dll, configurez votre application Compilez avec une référence à la bibliothèque Runtime Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="01e1b-118">If you are attempting to compile an SDK-style project (a project with a \*.vbproj file that begins with the line `<Project Sdk="Microsoft.NET.Sdk">`), and the error message refers to a type or member in the Microsoft.VisualBasic.dll assembly, configure your application to compile with a reference to the Visual Basic Runtime Library.</span></span> <span data-ttu-id="01e1b-119">Par défaut, un sous-ensemble de la bibliothèque est incorporé dans votre assembly dans un projet de style SDK.</span><span class="sxs-lookup"><span data-stu-id="01e1b-119">By default, a subset of the library is embedded in your assembly in an SDK-style project.</span></span>

   <span data-ttu-id="01e1b-120">Par exemple, l’exemple suivant compilation échoue, car le <xref:Microsoft.VisualBasic.CompilerServices.Conversions.ToInteger%2A?displayProperty=fullName> méthode ne peut pas être trouvée.</span><span class="sxs-lookup"><span data-stu-id="01e1b-120">For example, the following example fails to compile because the <xref:Microsoft.VisualBasic.CompilerServices.Conversions.ToInteger%2A?displayProperty=fullName> method cannot be found.</span></span> <span data-ttu-id="01e1b-121">Il n’est pas incorporé dans le sous-ensemble du Runtime Visual Basic inclus avec votre application.</span><span class="sxs-lookup"><span data-stu-id="01e1b-121">It is not embedded in the subset of the Visual Basic Runtime included with your application.</span></span>  

   [!code-vb[BC30451](~/samples/snippets/visualbasic/language-reference/error-messages/bc30451/program1.vb)]

   <span data-ttu-id="01e1b-122">Pour résoudre cette erreur, ajoutez le `<VBRuntime>Default</VBRuntime>` élément aux projets `<PropertyGroup>` section, comme le montre de fichier de projet Visual Basic suivant.</span><span class="sxs-lookup"><span data-stu-id="01e1b-122">To address this error, add the `<VBRuntime>Default</VBRuntime>` element to the projects `<PropertyGroup>` section, as the following Visual Basic project file shows.</span></span>

   [!code-vb[BC30451](~/samples/snippets/visualbasic/language-reference/error-messages/bc30451/vbruntime.vbproj?highlight=6)]

## <a name="see-also"></a><span data-ttu-id="01e1b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01e1b-123">See also</span></span>

- [<span data-ttu-id="01e1b-124">Liste des déclarations et des constantes</span><span class="sxs-lookup"><span data-stu-id="01e1b-124">Declarations and Constants Summary</span></span>](../../../visual-basic/language-reference/keywords/declarations-and-constants-summary.md)
- [<span data-ttu-id="01e1b-125">Conventions d’affectation de noms de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="01e1b-125">Visual Basic Naming Conventions</span></span>](../../../visual-basic/programming-guide/program-structure/naming-conventions.md)
- [<span data-ttu-id="01e1b-126">Noms d’éléments déclarés</span><span class="sxs-lookup"><span data-stu-id="01e1b-126">Declared Element Names</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md)
- [<span data-ttu-id="01e1b-127">Références aux éléments déclarés</span><span class="sxs-lookup"><span data-stu-id="01e1b-127">References to Declared Elements</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)
