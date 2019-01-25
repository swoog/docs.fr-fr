---
title: Référence à l’assembly requise &#39; &lt;assemblyname&gt; &#39; contenant la classe de base &#39; &lt;classname&gt;&#39;
ms.date: 07/20/2015
f1_keywords:
- bc30007
- vbc30007
helpviewer_keywords:
- BC30007
ms.assetid: 5f34cf47-6c6e-4954-bd8e-d6b020b75fb7
ms.openlocfilehash: f2aa8f1f05ce15bd25992b7f1851854952108813
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54506267"
---
# <a name="reference-required-to-assembly-39ltassemblynamegt39-containing-the-base-class-39ltclassnamegt39"></a><span data-ttu-id="05787-102">Référence à l’assembly requise &#39; &lt;assemblyname&gt; &#39; contenant la classe de base &#39; &lt;classname&gt;&#39;</span><span class="sxs-lookup"><span data-stu-id="05787-102">Reference required to assembly &#39;&lt;assemblyname&gt;&#39; containing the base class &#39;&lt;classname&gt;&#39;</span></span>
<span data-ttu-id="05787-103">Référence à l’assembly requise '\<nom_assembly >' contenant la classe de base\<nom_classe >'.</span><span class="sxs-lookup"><span data-stu-id="05787-103">Reference required to assembly '\<assemblyname>' containing the base class '\<classname>'.</span></span> <span data-ttu-id="05787-104">Ajoutez-en une à votre projet.</span><span class="sxs-lookup"><span data-stu-id="05787-104">Add one to your project.</span></span>  
  
 <span data-ttu-id="05787-105">La classe est définie dans une bibliothèque de liens dynamiques (DLL) ou un assembly qui n’est pas directement référencé dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="05787-105">The class is defined in a dynamic-link library (DLL) or assembly that is not directly referenced in your project.</span></span> <span data-ttu-id="05787-106">Le compilateur Visual Basic requiert une référence pour éviter toute ambiguïté au cas où la classe est définie dans plusieurs DLL ou assemblys.</span><span class="sxs-lookup"><span data-stu-id="05787-106">The Visual Basic compiler requires a reference to avoid ambiguity in case the class is defined in more than one DLL or assembly.</span></span>  
  
 <span data-ttu-id="05787-107">**ID d’erreur :** BC30007</span><span class="sxs-lookup"><span data-stu-id="05787-107">**Error ID:** BC30007</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="05787-108">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="05787-108">To correct this error</span></span>  
  
-   <span data-ttu-id="05787-109">Incluez le nom de la DLL ou de l’assembly non référencé dans vos références de projet.</span><span class="sxs-lookup"><span data-stu-id="05787-109">Include the name of the unreferenced DLL or assembly in your project references.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="05787-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05787-110">See also</span></span>

- [<span data-ttu-id="05787-111">Gestion des références dans un projet</span><span class="sxs-lookup"><span data-stu-id="05787-111">Managing references in a project</span></span>](/visualstudio/ide/managing-references-in-a-project)
- [<span data-ttu-id="05787-112">Dépannage de références rompues</span><span class="sxs-lookup"><span data-stu-id="05787-112">Troubleshooting Broken References</span></span>](/visualstudio/ide/troubleshooting-broken-references)
