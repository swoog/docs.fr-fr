---
title: L'accès à la propriété par défaut est ambigu entre le membre '<defaultpropertyname>' de l'interface héritée '<interfacename1>' et le membre '<defaultpropertyname>' de l'interface héritée '<interfacename2>'
ms.date: 07/20/2015
f1_keywords:
- vbc30686
- bc30686
helpviewer_keywords:
- BC30686
ms.assetid: 784fefec-ef57-48cf-b960-957df419b439
ms.openlocfilehash: a7079ff3b56b94cb969a77707dbd79b1d7dd4bb1
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55270587"
---
# <a name="default-property-access-is-ambiguous-between-the-inherited-interface-members-defaultpropertyname-of-interface-interfacename1-and-defaultpropertyname-of-interface-interfacename2"></a><span data-ttu-id="d9310-102">Accès à la propriété par défaut est ambigu entre les membres de l’interface héritée\<defaultpropertyname >' de l’interface '\<nom_interface1 >' et '\<defaultpropertyname >' de l’interface '\< nom_interface2 >'</span><span class="sxs-lookup"><span data-stu-id="d9310-102">Default property access is ambiguous between the inherited interface members '\<defaultpropertyname>' of interface '\<interfacename1>' and '\<defaultpropertyname>' of interface '\<interfacename2>'</span></span>
<span data-ttu-id="d9310-103">Une interface hérite de deux interfaces, chacun d’eux déclare une propriété par défaut avec le même nom.</span><span class="sxs-lookup"><span data-stu-id="d9310-103">An interface inherits from two interfaces, each of which declares a default property with the same name.</span></span> <span data-ttu-id="d9310-104">Le compilateur ne peut pas résoudre un accès à cette propriété par défaut sans qualification.</span><span class="sxs-lookup"><span data-stu-id="d9310-104">The compiler cannot resolve an access to this default property without qualification.</span></span> <span data-ttu-id="d9310-105">L'exemple suivant illustre ce comportement.</span><span class="sxs-lookup"><span data-stu-id="d9310-105">The following example illustrates this.</span></span>  
  
```  
Public Interface Iface1  
    Default Property prop(ByVal arg As Integer) As Integer  
End Interface  
Public Interface Iface2  
    Default Property prop(ByVal arg As Integer) As Integer  
End Interface  
Public Interface Iface3  
    Inherits Iface1, Iface2  
End Interface  
Public Class testClass  
    Public Sub accessDefaultProperty()  
        Dim testObj As Iface3  
        Dim testInt As Integer = testObj(1)  
    End Sub  
End Class  
```  
  
 <span data-ttu-id="d9310-106">Lorsque vous spécifiez `testObj(1)`, le compilateur tente de remédier à la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="d9310-106">When you specify `testObj(1)`, the compiler tries to resolve it to the default property.</span></span> <span data-ttu-id="d9310-107">Toutefois, il existe deux propriétés par défaut possibles en raison des interfaces héritées, le compilateur signale cette erreur.</span><span class="sxs-lookup"><span data-stu-id="d9310-107">However, there are two possible default properties because of the inherited interfaces, so the compiler signals this error.</span></span>  
  
 <span data-ttu-id="d9310-108">**ID d’erreur :** BC30686</span><span class="sxs-lookup"><span data-stu-id="d9310-108">**Error ID:** BC30686</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="d9310-109">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="d9310-109">To correct this error</span></span>  
  
-   <span data-ttu-id="d9310-110">Évitez d’hériter de tous les membres portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="d9310-110">Avoid inheriting any members with the same name.</span></span> <span data-ttu-id="d9310-111">Dans l’exemple précédent, si `testObj` n’a pas besoin des membres de, disons, `Iface2`, puis de le déclarer comme suit :</span><span class="sxs-lookup"><span data-stu-id="d9310-111">In the preceding example, if `testObj` does not need any of the members of, say, `Iface2`, then declare it as follows:</span></span>  
  
    ```  
    Dim testObj As Iface1  
    ```  
  
     <span data-ttu-id="d9310-112">ou</span><span class="sxs-lookup"><span data-stu-id="d9310-112">-or-</span></span>  
  
-   <span data-ttu-id="d9310-113">Implémentez l’interface qui hérite dans une classe.</span><span class="sxs-lookup"><span data-stu-id="d9310-113">Implement the inheriting interface in a class.</span></span> <span data-ttu-id="d9310-114">Vous pouvez implémenter chacune des propriétés héritées avec des noms différents.</span><span class="sxs-lookup"><span data-stu-id="d9310-114">Then you can implement each of the inherited properties with different names.</span></span> <span data-ttu-id="d9310-115">Toutefois, seule une d'entre elles peut être la propriété par défaut de la classe d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="d9310-115">However, only one of them can be the default property of the implementing class.</span></span> <span data-ttu-id="d9310-116">L'exemple suivant illustre ce comportement.</span><span class="sxs-lookup"><span data-stu-id="d9310-116">The following example illustrates this.</span></span>  
  
    ```  
    Public Class useIface3  
        Implements Iface3  
        Default Public Property prop1(ByVal arg As Integer) As Integer Implements Iface1.prop  
            ' Insert code to define Get and Set procedures for prop1.  
        End Property  
        Public Property prop2(ByVal arg As Integer) As Integer Implements Iface2.prop  
            ' Insert code to define Get and Set procedures for prop2.  
        End Property  
    End Class  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="d9310-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9310-117">See also</span></span>
- [<span data-ttu-id="d9310-118">Interfaces</span><span class="sxs-lookup"><span data-stu-id="d9310-118">Interfaces</span></span>](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
