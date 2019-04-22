---
title: L'attribut 'Extension' ne peut être appliqué qu'aux déclarations 'Module', 'Sub' ou 'Function'
ms.date: 07/20/2015
f1_keywords:
- bc36550
- vbc36550
helpviewer_keywords:
- BC36550
ms.assetid: 4387a51f-733c-45d7-abdb-eb64d4f51078
ms.openlocfilehash: a4561359e4d7cb0f6ebe44a5deb09b3374556ed8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58826182"
---
# <a name="extension-attribute-can-be-applied-only-to-module-sub-or-function-declarations"></a><span data-ttu-id="f7431-102">L'attribut 'Extension' ne peut être appliqué qu'aux déclarations 'Module', 'Sub' ou 'Function'</span><span class="sxs-lookup"><span data-stu-id="f7431-102">'Extension' attribute can be applied only to 'Module', 'Sub', or 'Function' declarations</span></span>
<span data-ttu-id="f7431-103">La seule façon d’étendre un type de données en Visual Basic consiste à définir une méthode d’extension à l’intérieur d’un module standard.</span><span class="sxs-lookup"><span data-stu-id="f7431-103">The only way to extend a data type in Visual Basic is to define an extension method inside a standard module.</span></span> <span data-ttu-id="f7431-104">La méthode d’extension peut être un `Sub` procédure ou un `Function` procédure.</span><span class="sxs-lookup"><span data-stu-id="f7431-104">The extension method can be a `Sub` procedure or a `Function` procedure.</span></span> <span data-ttu-id="f7431-105">Toutes les méthodes d’extension doivent être marqués avec l’attribut d’extension, `<Extension()>`, à partir de la <xref:System.Runtime.CompilerServices?displayProperty=nameWithType> espace de noms.</span><span class="sxs-lookup"><span data-stu-id="f7431-105">All extension methods must be marked with the extension attribute, `<Extension()>`, from the <xref:System.Runtime.CompilerServices?displayProperty=nameWithType> namespace.</span></span> <span data-ttu-id="f7431-106">Si vous le souhaitez, un module qui contient une méthode d’extension peut être marqué de la même façon.</span><span class="sxs-lookup"><span data-stu-id="f7431-106">Optionally, a module that contains an extension method may be marked in the same way.</span></span> <span data-ttu-id="f7431-107">Aucune autre utilisation de l’attribut d’extension n’est valide.</span><span class="sxs-lookup"><span data-stu-id="f7431-107">No other use of the extension attribute is valid.</span></span>  
  
 <span data-ttu-id="f7431-108">**ID d’erreur :** BC36550</span><span class="sxs-lookup"><span data-stu-id="f7431-108">**Error ID:** BC36550</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="f7431-109">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="f7431-109">To correct this error</span></span>  
  
-   <span data-ttu-id="f7431-110">Supprimez l’attribut d’extension.</span><span class="sxs-lookup"><span data-stu-id="f7431-110">Remove the extension attribute.</span></span>  
  
-   <span data-ttu-id="f7431-111">Reconcevez votre extension en tant que méthode, définie dans un module englobant.</span><span class="sxs-lookup"><span data-stu-id="f7431-111">Redesign your extension as a method, defined in an enclosing module.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f7431-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="f7431-112">Example</span></span>  
 <span data-ttu-id="f7431-113">L’exemple suivant définit un `Print` méthode pour le `String` type de données.</span><span class="sxs-lookup"><span data-stu-id="f7431-113">The following example defines a `Print` method for the `String` data type.</span></span>  
  
```  
Imports StringUtility  
Imports System.Runtime.CompilerServices  
Namespace StringUtility  
    <Extension()>   
    Module StringExtensions  
        <Extension()>   
        Public Sub Print (ByVal str As String)  
            Console.WriteLine(str)  
        End Sub  
    End Module  
End Namespace  
```  
  
## <a name="see-also"></a><span data-ttu-id="f7431-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7431-114">See also</span></span>

- [<span data-ttu-id="f7431-115">Vue d’ensemble des attributs</span><span class="sxs-lookup"><span data-stu-id="f7431-115">Attributes overview</span></span>](../../../visual-basic/programming-guide/concepts/attributes/index.md)
- [<span data-ttu-id="f7431-116">Méthodes d’extension</span><span class="sxs-lookup"><span data-stu-id="f7431-116">Extension Methods</span></span>](../../../visual-basic/programming-guide/language-features/procedures/extension-methods.md)
- [<span data-ttu-id="f7431-117">Module (instruction)</span><span class="sxs-lookup"><span data-stu-id="f7431-117">Module Statement</span></span>](../../../visual-basic/language-reference/statements/module-statement.md)
