---
title: "'<interfacename>. <membername>'est déjà implémenté par la classe de base'<baseclassname>'. Réimplémentation de <type> supposé"
ms.date: 07/20/2015
f1_keywords:
- vbc42015
- bc42015
helpviewer_keywords:
- BC42015
ms.assetid: 658c070a-113e-4bd8-b294-12c243191160
ms.openlocfilehash: 64bd7771820c2a4073350b7a5189d3a32c4775be
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61921327"
---
# <a name="interfacenamemembername-is-already-implemented-by-the-base-class-baseclassname-re-implementation-of-type-assumed"></a><span data-ttu-id="b0097-103">'\<nom_interface >. \<nom_membre >' est déjà implémenté par la classe de base\<nom_classe_de_base >'.</span><span class="sxs-lookup"><span data-stu-id="b0097-103">'\<interfacename>.\<membername>' is already implemented by the base class '\<baseclassname>'.</span></span> <span data-ttu-id="b0097-104">Réimplémentation de \<type > supposé</span><span class="sxs-lookup"><span data-stu-id="b0097-104">Re-implementation of \<type> assumed</span></span>
<span data-ttu-id="b0097-105">Une propriété, une procédure ou un événement dans une classe dérivée utilise une `Implements` clause qui spécifie un membre d’interface qui est déjà implémenté dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="b0097-105">A property, procedure, or event in a derived class uses an `Implements` clause specifying an interface member that is already implemented in the base class.</span></span>  
  
 <span data-ttu-id="b0097-106">Une classe dérivée peut réimplémenter un membre d’interface qui est implémenté par sa classe de base.</span><span class="sxs-lookup"><span data-stu-id="b0097-106">A derived class can reimplement an interface member that is implemented by its base class.</span></span> <span data-ttu-id="b0097-107">La substitution de l’implémentation de la classe de base est une procédure différente.</span><span class="sxs-lookup"><span data-stu-id="b0097-107">This is not the same as overriding the base class implementation.</span></span> <span data-ttu-id="b0097-108">Pour plus d’informations, consultez [Implements](../../../visual-basic/language-reference/statements/implements-clause.md).</span><span class="sxs-lookup"><span data-stu-id="b0097-108">For more information, see [Implements](../../../visual-basic/language-reference/statements/implements-clause.md).</span></span>  
  
 <span data-ttu-id="b0097-109">Par défaut, ce message est un avertissement.</span><span class="sxs-lookup"><span data-stu-id="b0097-109">By default, this message is a warning.</span></span> <span data-ttu-id="b0097-110">Pour plus d’informations sur le masquage des avertissements ou leur traitement en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span><span class="sxs-lookup"><span data-stu-id="b0097-110">For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
 <span data-ttu-id="b0097-111">**ID d’erreur :** BC42015</span><span class="sxs-lookup"><span data-stu-id="b0097-111">**Error ID:** BC42015</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="b0097-112">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="b0097-112">To correct this error</span></span>  
  
- <span data-ttu-id="b0097-113">Si vous comptez réimplémenter le membre d’interface, aucune mesure n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b0097-113">If you intend to reimplement the interface member, you do not need to take any action.</span></span> <span data-ttu-id="b0097-114">Code de votre classe dérivée accède au membre réimplémenté, sauf si vous utilisez le `MyBase` mot clé pour accéder à l’implémentation de classe de base.</span><span class="sxs-lookup"><span data-stu-id="b0097-114">Code in your derived class accesses the reimplemented member unless you use the `MyBase` keyword to access the base class implementation.</span></span>  
  
- <span data-ttu-id="b0097-115">Si vous ne comptez pas réimplémenter le membre d’interface, supprimez la clause `Implements` de la déclaration de la propriété, de la procédure ou de l’événement.</span><span class="sxs-lookup"><span data-stu-id="b0097-115">If you do not intend to reimplement the interface member, remove the `Implements` clause from the property, procedure, or event declaration.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b0097-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0097-116">See also</span></span>

- [<span data-ttu-id="b0097-117">Interfaces</span><span class="sxs-lookup"><span data-stu-id="b0097-117">Interfaces</span></span>](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
