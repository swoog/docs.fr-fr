---
title: Membres protégés
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- members [.NET Framework], protected
- protected members
- classes [.NET Framework], unsealed
- classes [.NET Framework], protected members
- unsealed classes
- customizing class behavior
ms.assetid: aa0b58ee-3956-494d-ab48-471ae5db8740
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4574dffc3f9dd1b60d655bfde33a4ddc1a81d350
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44140942"
---
# <a name="protected-members"></a><span data-ttu-id="d7717-102">Membres protégés</span><span class="sxs-lookup"><span data-stu-id="d7717-102">Protected Members</span></span>
<span data-ttu-id="d7717-103">Membres protégés par eux-mêmes ne fournissent pas de n’importe quel d’extensibilité, mais qu’ils puissent prendre extensibilité via sous-classement plus puissant.</span><span class="sxs-lookup"><span data-stu-id="d7717-103">Protected members by themselves do not provide any extensibility, but they can make extensibility through subclassing more powerful.</span></span> <span data-ttu-id="d7717-104">Ils peuvent être utilisés pour exposent des options de personnalisation avancée sans compliquer inutilement l’interface publique principale.</span><span class="sxs-lookup"><span data-stu-id="d7717-104">They can be used to expose advanced customization options without unnecessarily complicating the main public interface.</span></span>  
  
 <span data-ttu-id="d7717-105">Concepteurs de Framework doivent être prudent avec les membres protégés, car le nom « protégé » peut donner un faux sentiment de sécurité.</span><span class="sxs-lookup"><span data-stu-id="d7717-105">Framework designers need to be careful with protected members because the name "protected" can give a false sense of security.</span></span> <span data-ttu-id="d7717-106">Toute personne est en mesure de sous-classe d’une classe unsealed et les membres de l’accès protégé, et par conséquent, les mêmes pratiques de codage défensifs utilisés pour les membres publics s’appliquent aux membres protégés.</span><span class="sxs-lookup"><span data-stu-id="d7717-106">Anyone is able to subclass an unsealed class and access protected members, and so all the same defensive coding practices used for public members apply to protected members.</span></span>  
  
 <span data-ttu-id="d7717-107">**✓ CONSIDER** à l’aide de membres pour la personnalisation avancée protégés.</span><span class="sxs-lookup"><span data-stu-id="d7717-107">**✓ CONSIDER** using protected members for advanced customization.</span></span>  
  
 <span data-ttu-id="d7717-108">**✓ DO** considérer les membres protégés dans les classes unsealed comme public à des fins de sécurité, la documentation et compatibilité analysis.</span><span class="sxs-lookup"><span data-stu-id="d7717-108">**✓ DO** treat protected members in unsealed classes as public for the purpose of security, documentation, and compatibility analysis.</span></span>  
  
 <span data-ttu-id="d7717-109">Toute personne peut hériter d’une classe et accéder aux membres protégés.</span><span class="sxs-lookup"><span data-stu-id="d7717-109">Anyone can inherit from a class and access the protected members.</span></span>  
  
 <span data-ttu-id="d7717-110">*Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*</span><span class="sxs-lookup"><span data-stu-id="d7717-110">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="d7717-111">*Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="d7717-111">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d7717-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7717-112">See also</span></span>

- [<span data-ttu-id="d7717-113">Règles de conception de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="d7717-113">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
- [<span data-ttu-id="d7717-114">Conception en vue de l’extensibilité</span><span class="sxs-lookup"><span data-stu-id="d7717-114">Designing for Extensibility</span></span>](../../../docs/standard/design-guidelines/designing-for-extensibility.md)
