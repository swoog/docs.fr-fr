---
title: Impossible de faire référence à &#39; &lt;nom&gt; &#39; , car il est membre du champ valeurs &#39; &lt;nom&gt; &#39; de classe &#39; &lt;classname&gt; &#39;qui a &#39;System.MarshalByRefObject&#39; comme classe de base
ms.date: 07/20/2015
f1_keywords:
- vbc30310
- bc30310
helpviewer_keywords:
- BC30310
ms.assetid: 2aeb8872-7c87-4f01-98ef-9714ba3eebbe
ms.openlocfilehash: a6298c3e0f5102397d5cc3f237a186598c6b5ecc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54739295"
---
# <a name="cannot-refer-to-39ltnamegt39-because-it-is-a-member-of-the-value-typed-field-39ltnamegt39-of-class-39ltclassnamegt39-which-has-39systemmarshalbyrefobject39-as-a-base-class"></a><span data-ttu-id="8ae57-102">Impossible de faire référence à &#39; &lt;nom&gt; &#39; , car il est membre du champ valeurs &#39; &lt;nom&gt; &#39; de classe &#39; &lt;classname&gt; &#39;qui a &#39;System.MarshalByRefObject&#39; comme classe de base</span><span class="sxs-lookup"><span data-stu-id="8ae57-102">Cannot refer to &#39;&lt;name&gt;&#39; because it is a member of the value-typed field &#39;&lt;name&gt;&#39; of class &#39;&lt;classname&gt;&#39; which has &#39;System.MarshalByRefObject&#39; as a base class</span></span>
<span data-ttu-id="8ae57-103">Le `System.MarshalByRefObject` classe permet aux applications qui prennent en charge l’accès à distance à des objets entre les limites du domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="8ae57-103">The `System.MarshalByRefObject` class enables applications that support remote access to objects across application domain boundaries.</span></span> <span data-ttu-id="8ae57-104">Types doivent hériter la `MarshalByRejectObject` classe lorsque le type est utilisé au-delà des limites du domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="8ae57-104">Types must inherit from the `MarshalByRejectObject` class when the type is used across application domain boundaries.</span></span> <span data-ttu-id="8ae57-105">L’état de l’objet ne doit pas être copié, car les membres de l’objet ne sont pas utilisables en dehors du domaine d’application dans lequel ils ont été créés.</span><span class="sxs-lookup"><span data-stu-id="8ae57-105">The state of the object must not be copied because the members of the object are not usable outside the application domain in which they were created.</span></span>  
  
 <span data-ttu-id="8ae57-106">**ID d’erreur :** BC30310</span><span class="sxs-lookup"><span data-stu-id="8ae57-106">**Error ID:** BC30310</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="8ae57-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="8ae57-107">To correct this error</span></span>  
  
1.  <span data-ttu-id="8ae57-108">Vérification de la référence de s’assurer que le membre fait référence est valide.</span><span class="sxs-lookup"><span data-stu-id="8ae57-108">Check the reference to make sure the member being referred to is valid.</span></span>  
  
2.  <span data-ttu-id="8ae57-109">Qualifier explicitement le membre avec le `Me` mot clé.</span><span class="sxs-lookup"><span data-stu-id="8ae57-109">Explicitly qualify the member with the `Me` keyword.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8ae57-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ae57-110">See also</span></span>
- <xref:System.MarshalByRefObject>
- [<span data-ttu-id="8ae57-111">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="8ae57-111">Dim Statement</span></span>](../../../visual-basic/language-reference/statements/dim-statement.md)
