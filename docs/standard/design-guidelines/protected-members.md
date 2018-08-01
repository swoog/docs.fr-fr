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
ms.openlocfilehash: 5d4d334d9809f374442e19807d3b249a17a1d9df
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33571083"
---
# <a name="protected-members"></a><span data-ttu-id="cacef-102">Membres protégés</span><span class="sxs-lookup"><span data-stu-id="cacef-102">Protected Members</span></span>
<span data-ttu-id="cacef-103">Les membres protégés par eux-mêmes ne fournissent pas de n’importe quel d’extensibilité, mais elles peuvent rendre les extensibilité via le sous-classement plus puissant.</span><span class="sxs-lookup"><span data-stu-id="cacef-103">Protected members by themselves do not provide any extensibility, but they can make extensibility through subclassing more powerful.</span></span> <span data-ttu-id="cacef-104">Ils peuvent être utilisés pour exposer les options de personnalisation avancée sans compliquer inutilement de l’interface publique principale.</span><span class="sxs-lookup"><span data-stu-id="cacef-104">They can be used to expose advanced customization options without unnecessarily complicating the main public interface.</span></span>  
  
 <span data-ttu-id="cacef-105">Concepteurs de Framework doivent être prudent avec les membres protégés, car le nom « protégé » peut donner un sentiment de sécurité.</span><span class="sxs-lookup"><span data-stu-id="cacef-105">Framework designers need to be careful with protected members because the name "protected" can give a false sense of security.</span></span> <span data-ttu-id="cacef-106">Toute personne est en mesure de sous-classe d’une classe unsealed et les membres de l’accès protégé, et par conséquent, les mêmes défensives pratiques de codage utilisés pour les membres publics s’appliquent à des membres protégés.</span><span class="sxs-lookup"><span data-stu-id="cacef-106">Anyone is able to subclass an unsealed class and access protected members, and so all the same defensive coding practices used for public members apply to protected members.</span></span>  
  
 <span data-ttu-id="cacef-107">**✓ CONSIDER** à l’aide de membres pour la personnalisation avancée protégés.</span><span class="sxs-lookup"><span data-stu-id="cacef-107">**✓ CONSIDER** using protected members for advanced customization.</span></span>  
  
 <span data-ttu-id="cacef-108">**✓ DO** considérer les membres protégés dans les classes unsealed comme public à des fins de sécurité, la documentation et compatibilité analysis.</span><span class="sxs-lookup"><span data-stu-id="cacef-108">**✓ DO** treat protected members in unsealed classes as public for the purpose of security, documentation, and compatibility analysis.</span></span>  
  
 <span data-ttu-id="cacef-109">Toute personne peut hériter d’une classe et accéder aux membres protégés.</span><span class="sxs-lookup"><span data-stu-id="cacef-109">Anyone can inherit from a class and access the protected members.</span></span>  
  
 <span data-ttu-id="cacef-110">*Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*</span><span class="sxs-lookup"><span data-stu-id="cacef-110">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="cacef-111">*Réimprimées avec l’autorisation de Pearson éducation, Inc. à partir de [règles de conception d’infrastructure : Conventions, idiomes et des modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="cacef-111">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cacef-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cacef-112">See Also</span></span>  
 [<span data-ttu-id="cacef-113">Règles de conception de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="cacef-113">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
 [<span data-ttu-id="cacef-114">Conception en vue de l’extensibilité</span><span class="sxs-lookup"><span data-stu-id="cacef-114">Designing for Extensibility</span></span>](../../../docs/standard/design-guidelines/designing-for-extensibility.md)
