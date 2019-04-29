---
title: Sécurité et conditions de concurrence
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- security [.NET Framework], race conditions
- race conditions
- secure coding, race conditions
- code security, race conditions
ms.assetid: ea3edb80-b2e8-4e85-bfed-311b20cb59b6
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 57ceaedc7c38ae70a0db5a7fd584a765a7474aff
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61933807"
---
# <a name="security-and-race-conditions"></a>Sécurité et conditions de concurrence
Un autre problème concerne le risque de failles de sécurité exploité par les conditions de concurrence. Il existe plusieurs façons dans lequel cela peut se produire. Les sous-rubriques qui suivent décrivent certains des principaux pièges que le développeur doit éviter.  
  
## <a name="race-conditions-in-the-dispose-method"></a>Conditions de concurrence dans la méthode Dispose  
 Si d’une classe **Dispose** (méthode) (pour plus d’informations, consultez [Garbage Collection](../../../docs/standard/garbage-collection/index.md)) est non synchronisé, il est possible que le code de nettoyage à l’intérieur de **Dispose** peut être exécuté plus de une fois, comme illustré dans l’exemple suivant.  
  
```vb  
Sub Dispose()  
    If Not (myObj Is Nothing) Then  
       Cleanup(myObj)  
       myObj = Nothing  
    End If  
End Sub  
```  
  
```csharp  
void Dispose()   
{  
    if (myObj != null)   
    {  
        Cleanup(myObj);  
        myObj = null;  
    }  
}  
```  
  
 Étant donné que cela **Dispose** implémentation n’est pas synchronisée, il est possible pour `Cleanup` doit être appelée par tout d’abord un thread, puis un deuxième thread avant `_myObj` a la valeur **null**. S’il s’agit d’un problème de sécurité varie selon que se passe-t-il lorsque le `Cleanup` code s’exécute. Un problème majeur avec non synchronisés **Dispose** implémentations implique l’utilisation des descripteurs de ressources tels que les fichiers. Suppression inappropriée peut entraîner le handle incorrect à utiliser, ce qui entraîne souvent des failles de sécurité.  
  
## <a name="race-conditions-in-constructors"></a>Conditions de concurrence dans les constructeurs  
 Dans certaines applications, il est parfois possible d’autres threads peuvent accéder aux membres de classe avant l’exécution complète de leurs constructeurs de classe. Vous devez examiner tous les constructeurs de classe pour vous assurer qu’il n’y a aucun problème de sécurité si cela doit se produire ou synchroniser des threads si nécessaire.  
  
## <a name="race-conditions-with-cached-objects"></a>Conditions de concurrence avec les objets mis en cache  
 Le code qui met en cache les informations de sécurité ou utilise la sécurité d’accès du code [Assert](../../../docs/framework/misc/using-the-assert-method.md) opération peut également être vulnérable aux conditions de concurrence critique si d’autres parties de la classe ne sont pas correctement synchronisées, comme illustré dans l’exemple suivant.  
  
```vb  
Sub SomeSecureFunction()  
    If SomeDemandPasses() Then  
        fCallersOk = True  
        DoOtherWork()  
        fCallersOk = False  
    End If  
End Sub  
  
Sub DoOtherWork()  
    If fCallersOK Then  
        DoSomethingTrusted()  
    Else  
        DemandSomething()  
        DoSomethingTrusted()  
    End If  
End Sub  
```  
  
```csharp  
void SomeSecureFunction()   
{  
    if (SomeDemandPasses())   
    {  
        fCallersOk = true;  
        DoOtherWork();  
        fCallersOk = false;  
    }  
}  
void DoOtherWork()   
{  
    if (fCallersOK)   
    {  
        DoSomethingTrusted();  
    }  
    else   
    {  
        DemandSomething();  
        DoSomethingTrusted();  
    }  
}  
```  
  
 S’il existe des autres chemins d’accès aux `DoOtherWork` qui peut être appelée à partir d’un autre thread avec le même objet, un appelant non fiable peut ignorer une demande.  
  
 Si votre code met en cache les informations de sécurité, veillez à consulter pour cette vulnérabilité.  
  
## <a name="race-conditions-in-finalizers"></a>Conditions de concurrence critique dans des finaliseurs  
 Conditions de concurrence peuvent également se produire dans un objet qui fait référence à une ressource statique ou non managée qu’il libère ensuite dans son finaliseur. Si plusieurs objets partagent une ressource qui est manipulée dans un finaliseur de classe, les objets doivent synchroniser tous les accès à cette ressource.  
  
## <a name="see-also"></a>Voir aussi

- [Instructions de codage sécurisé](../../../docs/standard/security/secure-coding-guidelines.md)
