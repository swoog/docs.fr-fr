---
title: Référence à l’assembly requise &#39; &lt;assemblyname&gt; &#39; contenant la classe de base &#39; &lt;classname&gt;&#39;
ms.date: 07/20/2015
f1_keywords:
- bc30007
- vbc30007
helpviewer_keywords:
- BC30007
ms.assetid: 5f34cf47-6c6e-4954-bd8e-d6b020b75fb7
ms.openlocfilehash: aabf4afb9f87f40d0e31ac7ccd725bfb285ddf37
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33593530"
---
# <a name="reference-required-to-assembly-39ltassemblynamegt39-containing-the-base-class-39ltclassnamegt39"></a>Référence à l’assembly requise &#39; &lt;assemblyname&gt; &#39; contenant la classe de base &#39; &lt;classname&gt;&#39;
Référence à l’assembly requise '\<nom_assembly >' contenant la classe de base\<nom_classe >'. Ajoutez-en une à votre projet.  
  
 La classe est définie dans une bibliothèque de liens dynamiques (DLL) ou un assembly qui n’est pas directement référencé dans votre projet. Le compilateur Visual Basic requiert une référence afin d’éviter toute ambiguïté au cas où la classe est définie dans plusieurs DLL ou assemblys.  
  
 **ID d’erreur :** BC30007  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Incluez le nom de la DLL ou de l’assembly non référencé dans vos références de projet.  
  
## <a name="see-also"></a>Voir aussi  
   
 [Gestion des références dans un projet](/visualstudio/ide/managing-references-in-a-project)  
 [Dépannage de références rompues](/visualstudio/ide/troubleshooting-broken-references)
