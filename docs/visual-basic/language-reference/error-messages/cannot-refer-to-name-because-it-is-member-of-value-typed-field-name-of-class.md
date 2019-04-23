---
title: Impossible de faire référence à '<name>', car il est membre du champ de valeurs '<name>' de la classe '<classname>', qui a 'System.MarshalByRefObject' comme classe de base
ms.date: 07/20/2015
f1_keywords:
- vbc30310
- bc30310
helpviewer_keywords:
- BC30310
ms.assetid: 2aeb8872-7c87-4f01-98ef-9714ba3eebbe
ms.openlocfilehash: 78b0a3131b6e77ed257f200523ecebd4dfce3691
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59316542"
---
# <a name="cannot-refer-to-name-because-it-is-a-member-of-the-value-typed-field-name-of-class-classname-which-has-systemmarshalbyrefobject-as-a-base-class"></a><span data-ttu-id="554ea-102">Ne peut pas faire référence à '\<nom >', car il est membre du champ de valeurs '\<nom >' de la classe\<nom_classe >' qui a 'System.MarshalByRefObject' comme classe de base</span><span class="sxs-lookup"><span data-stu-id="554ea-102">Cannot refer to '\<name>' because it is a member of the value-typed field '\<name>' of class '\<classname>' which has 'System.MarshalByRefObject' as a base class</span></span>
<span data-ttu-id="554ea-103">Le `System.MarshalByRefObject` classe permet aux applications qui prennent en charge l’accès à distance à des objets entre les limites du domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="554ea-103">The `System.MarshalByRefObject` class enables applications that support remote access to objects across application domain boundaries.</span></span> <span data-ttu-id="554ea-104">Types doivent hériter la `MarshalByRejectObject` classe lorsque le type est utilisé au-delà des limites du domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="554ea-104">Types must inherit from the `MarshalByRejectObject` class when the type is used across application domain boundaries.</span></span> <span data-ttu-id="554ea-105">L’état de l’objet ne doit pas être copié, car les membres de l’objet ne sont pas utilisables en dehors du domaine d’application dans lequel ils ont été créés.</span><span class="sxs-lookup"><span data-stu-id="554ea-105">The state of the object must not be copied because the members of the object are not usable outside the application domain in which they were created.</span></span>  
  
 <span data-ttu-id="554ea-106">**ID d’erreur :** BC30310</span><span class="sxs-lookup"><span data-stu-id="554ea-106">**Error ID:** BC30310</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="554ea-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="554ea-107">To correct this error</span></span>  
  
1. <span data-ttu-id="554ea-108">Vérification de la référence de s’assurer que le membre fait référence est valide.</span><span class="sxs-lookup"><span data-stu-id="554ea-108">Check the reference to make sure the member being referred to is valid.</span></span>  
  
2. <span data-ttu-id="554ea-109">Qualifier explicitement le membre avec le `Me` mot clé.</span><span class="sxs-lookup"><span data-stu-id="554ea-109">Explicitly qualify the member with the `Me` keyword.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="554ea-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="554ea-110">See also</span></span>

- <xref:System.MarshalByRefObject>
- [<span data-ttu-id="554ea-111">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="554ea-111">Dim Statement</span></span>](../../../visual-basic/language-reference/statements/dim-statement.md)
