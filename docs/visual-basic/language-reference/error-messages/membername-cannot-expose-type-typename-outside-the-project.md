---
title: '&#39;&lt;MemberName&gt; &#39; ne peut pas exposer le type &#39; &lt;typename&gt; &#39; en dehors du projet via &lt;containertype&gt; &#39; &lt;containertypename&gt;&#39;'
ms.date: 07/20/2015
f1_keywords:
- bc30909
- vbc30909
helpviewer_keywords:
- BC30909
ms.assetid: ffa7395d-e182-4087-8ce8-079810fdae54
ms.openlocfilehash: 39d316aca5ec306de4b1e43e2eb2d1495f5525d9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54672342"
---
# <a name="39ltmembernamegt39-cannot-expose-type-39lttypenamegt39-outside-the-project-through-ltcontainertypegt-39ltcontainertypenamegt39"></a><span data-ttu-id="aa3cf-102">&#39;&lt;MemberName&gt; &#39; ne peut pas exposer le type &#39; &lt;typename&gt; &#39; en dehors du projet via &lt;containertype&gt; &#39; &lt;containertypename&gt;&#39;</span><span class="sxs-lookup"><span data-stu-id="aa3cf-102">&#39;&lt;membername&gt;&#39; cannot expose type &#39;&lt;typename&gt;&#39; outside the project through &lt;containertype&gt; &#39;&lt;containertypename&gt;&#39;</span></span>
<span data-ttu-id="aa3cf-103">Une variable, un paramètre de procédure ou un retour de fonction est exposé en dehors de son conteneur, mais il est déclaré comme un type qui ne doit pas être exposé en dehors du conteneur.</span><span class="sxs-lookup"><span data-stu-id="aa3cf-103">A variable, procedure parameter, or function return is exposed outside its container, but it is declared as a type that must not be exposed outside the container.</span></span>  
  
 <span data-ttu-id="aa3cf-104">Le code squelette suivant montre une situation qui génère cette erreur.</span><span class="sxs-lookup"><span data-stu-id="aa3cf-104">The following skeleton code shows a situation that generates this error.</span></span>  
  
```  
Private Class privateClass  
End Class  
Public Class mainClass  
    Public exposedVar As New privateClass  
End Class  
```  
  
 <span data-ttu-id="aa3cf-105">Un type qui est déclaré `Protected`, `Friend`, `Protected Friend`, ou `Private` est destiné à un accès en dehors de son contexte de déclaration limité.</span><span class="sxs-lookup"><span data-stu-id="aa3cf-105">A type that is declared `Protected`, `Friend`, `Protected Friend`, or `Private` is intended to have limited access outside its declaration context.</span></span> <span data-ttu-id="aa3cf-106">À l’utiliser en tant que les données de type d’une variable avec un accès restreint moins serait en opposition avec cet effet.</span><span class="sxs-lookup"><span data-stu-id="aa3cf-106">Using it as the data type of a variable with less restricted access would defeat this purpose.</span></span> <span data-ttu-id="aa3cf-107">Dans le code squelette précédent, `exposedVar` est `Public` et exposera `privateClass` au code que vous ne devez pas y accéder.</span><span class="sxs-lookup"><span data-stu-id="aa3cf-107">In the preceding skeleton code, `exposedVar` is `Public` and would expose `privateClass` to code that should not have access to it.</span></span>  
  
 <span data-ttu-id="aa3cf-108">**ID d’erreur :** BC30909</span><span class="sxs-lookup"><span data-stu-id="aa3cf-108">**Error ID:** BC30909</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="aa3cf-109">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="aa3cf-109">To correct this error</span></span>  
  
-   <span data-ttu-id="aa3cf-110">Changement du niveau d’accès de la variable, un paramètre de procédure ou une fonction de retour pour être au moins aussi restrictif que le niveau d’accès de son type de données.</span><span class="sxs-lookup"><span data-stu-id="aa3cf-110">Change the access level of the variable, procedure parameter, or function return to be at least as restrictive as the access level of its data type.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aa3cf-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa3cf-111">See also</span></span>
- [<span data-ttu-id="aa3cf-112">Niveaux d’accès dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="aa3cf-112">Access levels in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
