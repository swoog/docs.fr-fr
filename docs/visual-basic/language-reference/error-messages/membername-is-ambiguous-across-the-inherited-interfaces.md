---
title: "'<membername>' est ambigu dans les interfaces héritées '<interfacename1>' et '<interfacename2>'"
ms.date: 07/20/2015
f1_keywords:
- vbc30685
- bc30685
helpviewer_keywords:
- BC30685
ms.assetid: 756add7a-23d5-4b4f-a48d-8297d6459c73
ms.openlocfilehash: 71f8cb96c9981bbfc55236ea815fa5f5cb0e8aaf
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64622648"
---
# <a name="membername-is-ambiguous-across-the-inherited-interfaces-interfacename1-and-interfacename2"></a><span data-ttu-id="1cb96-102">«\<nom_membre >' est ambigu dans les interfaces héritées'\<nom_interface1 >' et '\<nom_interface2 > »</span><span class="sxs-lookup"><span data-stu-id="1cb96-102">'\<membername>' is ambiguous across the inherited interfaces '\<interfacename1>' and '\<interfacename2>'</span></span>
<span data-ttu-id="1cb96-103">L’interface hérite de deux ou plusieurs membres portant le même nom plusieurs interfaces.</span><span class="sxs-lookup"><span data-stu-id="1cb96-103">The interface inherits two or more members with the same name from multiple interfaces.</span></span>  
  
 <span data-ttu-id="1cb96-104">**ID d’erreur :** BC30685</span><span class="sxs-lookup"><span data-stu-id="1cb96-104">**Error ID:** BC30685</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="1cb96-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="1cb96-105">To correct this error</span></span>  
  
- <span data-ttu-id="1cb96-106">Castez la valeur de l’interface de base que vous souhaitez utiliser. par exemple :</span><span class="sxs-lookup"><span data-stu-id="1cb96-106">Cast the value to the base interface that you want to use; for example:</span></span>  
  
    ```  
    Interface Left  
        Sub MySub()  
    End Interface  
  
    Interface Right  
        Sub MySub()  
    End Interface  
  
    Interface LeftRight  
        Inherits Left, Right  
    End Interface  
  
    Module test  
        Sub Main()  
            Dim x As LeftRight  
            ' x.MySub()  'x is ambiguous.  
            CType(x, Left).MySub() ' Cast to base type.  
            CType(x, Right).MySub() ' Call the other base type.  
        End Sub  
    End Module  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="1cb96-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cb96-107">See also</span></span>

- [<span data-ttu-id="1cb96-108">Interfaces</span><span class="sxs-lookup"><span data-stu-id="1cb96-108">Interfaces</span></span>](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
