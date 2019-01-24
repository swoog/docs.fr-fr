---
title: Instances d'objets par défaut fournies par My.Forms et My.WebServices (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- My.WebServices object [Visual Basic], developing applications
- My.Forms object [Visual Basic], developing applications
- rapid application development (RAD), My.Forms
- rapid application development (RAD), My.WebServices
ms.assetid: de930027-9108-4f0c-b97c-5e7db4d6ef79
ms.openlocfilehash: 9285e88e3dc9fd8b3731416b1c40811188d6a33d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54563598"
---
# <a name="default-object-instances-provided-by-myforms-and-mywebservices-visual-basic"></a><span data-ttu-id="ccefb-102">Instances d'objets par défaut fournies par My.Forms et My.WebServices (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ccefb-102">Default Object Instances Provided by My.Forms and My.WebServices (Visual Basic)</span></span>
<span data-ttu-id="ccefb-103">Le [My.Forms](../../../visual-basic/language-reference/objects/my-forms-object.md) et [My.WebServices](../../../visual-basic/language-reference/objects/my-webservices-object.md) objets fournissent l’accès aux formulaires, sources de données et services Web XML utilisés par votre application.</span><span class="sxs-lookup"><span data-stu-id="ccefb-103">The [My.Forms](../../../visual-basic/language-reference/objects/my-forms-object.md) and [My.WebServices](../../../visual-basic/language-reference/objects/my-webservices-object.md) objects provide access to forms, data sources, and XML Web services used by your application.</span></span> <span data-ttu-id="ccefb-104">Pour ce font, ils fournissent des collections de *instances par défaut* de chacun de ces objets.</span><span class="sxs-lookup"><span data-stu-id="ccefb-104">They do this by providing collections of *default instances* of each of these objects.</span></span>  
  
## <a name="default-instances"></a><span data-ttu-id="ccefb-105">Instances par défaut</span><span class="sxs-lookup"><span data-stu-id="ccefb-105">Default Instances</span></span>  
 <span data-ttu-id="ccefb-106">Une instance par défaut est une instance de la classe qui est fournie par le runtime et ne doit pas être déclaré et instancié à l’aide de la `Dim` et `New` instructions.</span><span class="sxs-lookup"><span data-stu-id="ccefb-106">A default instance is an instance of the class that is provided by the runtime and does not need to be declared and instantiated using the `Dim` and `New` statements.</span></span> <span data-ttu-id="ccefb-107">L’exemple suivant montre comment déclarer et instancier une instance d’un <xref:System.Windows.Forms.Form> classe appelée `Form1`, et la façon dont vous êtes maintenant en mesure d’obtenir une instance par défaut de ce <xref:System.Windows.Forms.Form> classe via `My.Forms`.</span><span class="sxs-lookup"><span data-stu-id="ccefb-107">The following example demonstrates how you might have declared and instantiated an instance of a <xref:System.Windows.Forms.Form> class called `Form1`, and how you are now able to get a default instance of this <xref:System.Windows.Forms.Form> class through `My.Forms`.</span></span>  
  
 [!code-vb[VbVbcnMy#5](../../../visual-basic/developing-apps/development-with-my/codesnippet/VisualBasic/default-object-instances-provided-by-my-forms-and-my-webservices_1.vb)]  
  
 [!code-vb[VbVbcnMy#6](../../../visual-basic/developing-apps/development-with-my/codesnippet/VisualBasic/default-object-instances-provided-by-my-forms-and-my-webservices_2.vb)]  
  
 <span data-ttu-id="ccefb-108">Le `My.Forms` objet retourne une collection d’instances par défaut pour chaque `Form` classe qui existe dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="ccefb-108">The `My.Forms` object returns a collection of default instances for every `Form` class that exists in your project.</span></span> <span data-ttu-id="ccefb-109">De même, `My.WebServices` fournit une instance par défaut de la classe proxy pour chaque service Web que vous avez créé une référence dans votre application.</span><span class="sxs-lookup"><span data-stu-id="ccefb-109">Similarly, `My.WebServices` provides a default instance of the proxy class for every Web service that you have created a reference to in your application.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ccefb-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccefb-110">See also</span></span>
- [<span data-ttu-id="ccefb-111">My.Forms (objet)</span><span class="sxs-lookup"><span data-stu-id="ccefb-111">My.Forms Object</span></span>](../../../visual-basic/language-reference/objects/my-forms-object.md)
- [<span data-ttu-id="ccefb-112">My.WebServices (objet)</span><span class="sxs-lookup"><span data-stu-id="ccefb-112">My.WebServices Object</span></span>](../../../visual-basic/language-reference/objects/my-webservices-object.md)
- [<span data-ttu-id="ccefb-113">Comment My dépend du type de projet</span><span class="sxs-lookup"><span data-stu-id="ccefb-113">How My Depends on Project Type</span></span>](../../../visual-basic/developing-apps/development-with-my/how-my-depends-on-project-type.md)
