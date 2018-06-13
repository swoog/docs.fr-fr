---
title: Propriété par défaut &#39; &lt;nom_propriété1&gt; &#39; est en conflit avec la propriété par défaut &#39; &lt;propertyname2&gt; &#39; dans &#39; &lt;classname&gt; &#39;et devrait donc être déclaré &#39;ombres&#39;
ms.date: 07/20/2015
f1_keywords:
- vbc40007
- bc40007
helpviewer_keywords:
- BC40007
ms.assetid: 692ccf76-5715-4f11-a972-84cf9de30bc1
ms.openlocfilehash: b305f7a59a9865ebeb6b6f53607757b719fb4d41
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33586622"
---
# <a name="default-property-39ltpropertyname1gt39-conflicts-with-default-property-39ltpropertyname2gt39-in-39ltclassnamegt39-and-so-should-be-declared-39shadows39"></a><span data-ttu-id="9776f-102">Propriété par défaut &#39; &lt;nom_propriété1&gt; &#39; est en conflit avec la propriété par défaut &#39; &lt;propertyname2&gt; &#39; dans &#39; &lt;classname&gt; &#39;et devrait donc être déclaré &#39;ombres&#39;</span><span class="sxs-lookup"><span data-stu-id="9776f-102">Default property &#39;&lt;propertyname1&gt;&#39; conflicts with default property &#39;&lt;propertyname2&gt;&#39; in &#39;&lt;classname&gt;&#39; and so should be declared &#39;Shadows&#39;</span></span>
<span data-ttu-id="9776f-103">Une propriété est déclarée avec le même nom qu’une propriété définie dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="9776f-103">A property is declared with the same name as a property defined in the base class.</span></span> <span data-ttu-id="9776f-104">Dans ce cas, la propriété de cette classe doit occulter la propriété de classe de base.</span><span class="sxs-lookup"><span data-stu-id="9776f-104">In this situation, the property in this class should shadow the base class property.</span></span>  
  
 <span data-ttu-id="9776f-105">Ce message est un avertissement.</span><span class="sxs-lookup"><span data-stu-id="9776f-105">This message is a warning.</span></span> <span data-ttu-id="9776f-106">`Shadows` est supposé par défaut.</span><span class="sxs-lookup"><span data-stu-id="9776f-106">`Shadows` is assumed by default.</span></span> <span data-ttu-id="9776f-107">Pour plus d’informations sur le masquage des avertissements ou le traitement des avertissements en tant qu’erreurs, consultez [configuration des avertissements en Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span><span class="sxs-lookup"><span data-stu-id="9776f-107">For more information about hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
 <span data-ttu-id="9776f-108">**ID d’erreur :** BC40007</span><span class="sxs-lookup"><span data-stu-id="9776f-108">**Error ID:** BC40007</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="9776f-109">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="9776f-109">To correct this error</span></span>  
  
-   <span data-ttu-id="9776f-110">Ajouter le `Shadows` mot clé à la déclaration ou modifiez le nom de la propriété déclarée.</span><span class="sxs-lookup"><span data-stu-id="9776f-110">Add the `Shadows` keyword to the declaration, or change the name of the property being declared.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9776f-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9776f-111">See Also</span></span>  
 [<span data-ttu-id="9776f-112">Shadows</span><span class="sxs-lookup"><span data-stu-id="9776f-112">Shadows</span></span>](../../../visual-basic/language-reference/modifiers/shadows.md)  
 [<span data-ttu-id="9776f-113">Occultation dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9776f-113">Shadowing in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md)
