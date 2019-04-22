---
title: Me, My, MyBase et MyClass dans Visual Basic
ms.date: 07/20/2015
f1_keywords:
- MyClass
- vb.Me
- MyBase
- vb.MyBase
- Me
- vb.MyClass
- vb.This
- vb.My
helpviewer_keywords:
- My object
- self-reference [Visual Basic], Me keyword
- MyClass keyword [Visual Basic], relationship to similar programming elements
- Me keyword [Visual Basic], relationship to similar programming elements
- Me keyword [Visual Basic], referring to the current instance of an object
- Me keyword [Visual Basic]
- self-reference
- current instance [Visual Basic], Me keyword
- MyBase keyword [Visual Basic], relationship to similar programming elements
ms.assetid: f8e241ae-b1ed-4886-9aa0-08c632154029
ms.openlocfilehash: a8df6e48fd5bce9bb28d8aef7e031f36741ad0ad
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58813390"
---
# <a name="me-my-mybase-and-myclass-in-visual-basic"></a><span data-ttu-id="6b4b9-102">Me, My, MyBase et MyClass dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6b4b9-102">Me, My, MyBase, and MyClass in Visual Basic</span></span>
<span data-ttu-id="6b4b9-103">`Me`, `My`, `MyBase`, et `MyClass` en Visual Basic ont des noms similaires, mais à des fins différentes.</span><span class="sxs-lookup"><span data-stu-id="6b4b9-103">`Me`, `My`, `MyBase`, and `MyClass` in Visual Basic have similar names, but different purposes.</span></span> <span data-ttu-id="6b4b9-104">Cette rubrique décrit chacune de ces entités afin de les distinguer.</span><span class="sxs-lookup"><span data-stu-id="6b4b9-104">This topic describes each of these entities in order to distinguish them.</span></span>  
  
## <a name="me"></a><span data-ttu-id="6b4b9-105">Me</span><span class="sxs-lookup"><span data-stu-id="6b4b9-105">Me</span></span>  
 <span data-ttu-id="6b4b9-106">Le `Me` mot clé permet de faire référence à l’instance spécifique d’une classe ou structure dans laquelle le code est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="6b4b9-106">The `Me` keyword provides a way to refer to the specific instance of a class or structure in which the code is currently executing.</span></span> <span data-ttu-id="6b4b9-107">`Me` se comporte comme une variable objet ou une variable de structure faisant référence à l’instance actuelle.</span><span class="sxs-lookup"><span data-stu-id="6b4b9-107">`Me` behaves like either an object variable or a structure variable referring to the current instance.</span></span> <span data-ttu-id="6b4b9-108">À l’aide de `Me` est particulièrement utile pour transmettre des informations sur l’instance en cours d’exécution d’une classe ou une structure à une procédure dans une autre classe, structure ou module.</span><span class="sxs-lookup"><span data-stu-id="6b4b9-108">Using `Me` is particularly useful for passing information about the currently executing instance of a class or structure to a procedure in another class, structure, or module.</span></span>  
  
 <span data-ttu-id="6b4b9-109">Par exemple, supposons que vous avez la procédure suivante dans un module.</span><span class="sxs-lookup"><span data-stu-id="6b4b9-109">For example, suppose you have the following procedure in a module.</span></span>  
  
```  
Sub ChangeFormColor(FormName As Form)  
   Randomize()  
   FormName.BackColor = Color.FromArgb(Rnd() * 256, Rnd() * 256, Rnd() * 256)  
End Sub  
```  
  
 <span data-ttu-id="6b4b9-110">Vous pouvez appeler cette procédure et passer l’instance actuelle de la <xref:System.Windows.Forms.Form> classe en tant qu’argument à l’aide de l’instruction suivante.</span><span class="sxs-lookup"><span data-stu-id="6b4b9-110">You can call this procedure and pass the current instance of the <xref:System.Windows.Forms.Form> class as an argument by using the following statement.</span></span>  
  
```  
ChangeFormColor(Me)  
```  
  
## <a name="my"></a><span data-ttu-id="6b4b9-111">My</span><span class="sxs-lookup"><span data-stu-id="6b4b9-111">My</span></span>  
 <span data-ttu-id="6b4b9-112">Le `My` fonctionnalité offre un accès facile et intuitif à un nombre de [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] classes, l’activation de l’utilisateur de Visual Basic interagir avec l’ordinateur, application, paramètres, ressources et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="6b4b9-112">The `My` feature provides easy and intuitive access to a number of [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] classes, enabling the Visual Basic user to interact with the computer, application, settings, resources, and so on.</span></span>  
  
## <a name="mybase"></a><span data-ttu-id="6b4b9-113">MyBase</span><span class="sxs-lookup"><span data-stu-id="6b4b9-113">MyBase</span></span>  
 <span data-ttu-id="6b4b9-114">Le `MyBase` mot clé se comporte comme une variable objet faisant référence à la classe de base de l’instance actuelle d’une classe.</span><span class="sxs-lookup"><span data-stu-id="6b4b9-114">The `MyBase` keyword behaves like an object variable referring to the base class of the current instance of a class.</span></span> <span data-ttu-id="6b4b9-115">`MyBase` est couramment utilisé pour accéder aux membres de classe de base qui sont substitués ou occultés dans une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="6b4b9-115">`MyBase` is commonly used to access base class members that are overridden or shadowed in a derived class.</span></span> <span data-ttu-id="6b4b9-116">`MyBase.New` est utilisé pour appeler explicitement un constructeur de classe de base à partir d’un constructeur de classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="6b4b9-116">`MyBase.New` is used to explicitly call a base class constructor from a derived class constructor.</span></span>  
  
## <a name="myclass"></a><span data-ttu-id="6b4b9-117">MyClass</span><span class="sxs-lookup"><span data-stu-id="6b4b9-117">MyClass</span></span>  
 <span data-ttu-id="6b4b9-118">Le `MyClass` mot clé se comporte comme une variable objet faisant référence à l’instance actuelle d’une classe implémentée à l’origine.</span><span class="sxs-lookup"><span data-stu-id="6b4b9-118">The `MyClass` keyword behaves like an object variable referring to the current instance of a class as originally implemented.</span></span> <span data-ttu-id="6b4b9-119">`MyClass` est similaire à `Me`, mais tous les appels de méthode sur celui-ci sont traités comme si la méthode était `NotOverridable`.</span><span class="sxs-lookup"><span data-stu-id="6b4b9-119">`MyClass` is similar to `Me`, but all method calls on it are treated as if the method were `NotOverridable`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6b4b9-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b4b9-120">See also</span></span>

- [<span data-ttu-id="6b4b9-121">Éléments fondamentaux de l’héritage</span><span class="sxs-lookup"><span data-stu-id="6b4b9-121">Inheritance Basics</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)
