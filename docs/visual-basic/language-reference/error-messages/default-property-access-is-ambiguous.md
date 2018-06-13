---
title: Accès à la propriété par défaut est ambigu entre les membres de l’interface héritée &#39; &lt;defaultpropertyname&gt; &#39; d’interface &#39; &lt;nom_interface1&gt; &#39; et &#39; &lt;defaultpropertyname&gt; &#39; d’interface &#39; &lt;nom_interface2&gt;&#39;
ms.date: 07/20/2015
f1_keywords:
- vbc30686
- bc30686
helpviewer_keywords:
- BC30686
ms.assetid: 784fefec-ef57-48cf-b960-957df419b439
ms.openlocfilehash: 65a10067284cad3bf56ecdc441ebefa0a740ef53
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33590853"
---
# <a name="default-property-access-is-ambiguous-between-the-inherited-interface-members-39ltdefaultpropertynamegt39-of-interface-39ltinterfacename1gt39-and-39ltdefaultpropertynamegt39-of-interface-39ltinterfacename2gt39"></a>Accès à la propriété par défaut est ambigu entre les membres de l’interface héritée &#39; &lt;defaultpropertyname&gt; &#39; d’interface &#39; &lt;nom_interface1&gt; &#39; et &#39; &lt;defaultpropertyname&gt; &#39; d’interface &#39; &lt;nom_interface2&gt;&#39;
Une interface hérite de deux interfaces, chacun d’eux déclare une propriété par défaut avec le même nom. Le compilateur ne peut pas résoudre un accès à cette propriété par défaut sans qualification. L'exemple suivant illustre ce comportement.  
  
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
  
 Lorsque vous spécifiez `testObj(1)`, le compilateur tente de résoudre la propriété par défaut. Toutefois, il existe deux propriétés par défaut possibles en raison des interfaces héritées, le compilateur signale cette erreur.  
  
 **ID d’erreur :** BC30686  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Évitez d’hériter de tous les membres portant le même nom. Dans l’exemple précédent, si `testObj` n’a pas besoin des membres de, par exemple, `Iface2`, puis de le déclarer comme suit :  
  
    ```  
    Dim testObj As Iface1  
    ```  
  
     - ou -  
  
-   Implémentez l’interface qui hérite dans une classe. Vous pouvez implémenter chacune des propriétés héritées avec des noms différents. Toutefois, un seul d'entre eux peut être la propriété par défaut de la classe d’implémentation. L'exemple suivant illustre ce comportement.  
  
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
  
## <a name="see-also"></a>Voir aussi  
 [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
