---
title: L'exception de commentaire XML doit avoir un attribut 'cref'
ms.date: 07/20/2015
f1_keywords:
- bc42319
- vbc42319
helpviewer_keywords:
- BC42319
ms.assetid: 62eeeba3-6811-48be-b1ef-c2e4feda3177
ms.openlocfilehash: 91bde92e2184c90b14838a09a89a6d261447f139
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64662612"
---
# <a name="xml-comment-exception-must-have-a-cref-attribute"></a><span data-ttu-id="1406c-102">L'exception de commentaire XML doit avoir un attribut 'cref'</span><span class="sxs-lookup"><span data-stu-id="1406c-102">XML comment exception must have a 'cref' attribute</span></span>
<span data-ttu-id="1406c-103">Le \<exception > balise offre un moyen de documenter les exceptions qui peuvent être levées par une méthode.</span><span class="sxs-lookup"><span data-stu-id="1406c-103">The \<exception> tag provides a way to document the exceptions that may be thrown by a method.</span></span> <span data-ttu-id="1406c-104">Requis `cref` attribut désigne le nom d’un membre qui est vérifié par le Générateur de documentation.</span><span class="sxs-lookup"><span data-stu-id="1406c-104">The required `cref` attribute designates the name of a member, which is checked by the documentation generator.</span></span> <span data-ttu-id="1406c-105">Si le membre existe, elle est convertie en nom d’élément canonique dans le fichier de documentation.</span><span class="sxs-lookup"><span data-stu-id="1406c-105">If the member exists, it is translated to the canonical element name in the documentation file.</span></span>  
  
 <span data-ttu-id="1406c-106">**ID d’erreur :** BC42319</span><span class="sxs-lookup"><span data-stu-id="1406c-106">**Error ID:** BC42319</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="1406c-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="1406c-107">To correct this error</span></span>  
  
- <span data-ttu-id="1406c-108">Ajouter le `cref` attribut à l’exception comme suit :</span><span class="sxs-lookup"><span data-stu-id="1406c-108">Add the `cref` attribute to the exception as follows:</span></span>  
  
    ```  
    '''<exception cref="member">description</exception>  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="1406c-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1406c-109">See also</span></span>

- [<span data-ttu-id="1406c-110">\<exception></span><span class="sxs-lookup"><span data-stu-id="1406c-110">\<exception></span></span>](../../../visual-basic/language-reference/xmldoc/exception.md)
- [<span data-ttu-id="1406c-111">Guide pratique pour Créer une Documentation XML</span><span class="sxs-lookup"><span data-stu-id="1406c-111">How to: Create XML Documentation</span></span>](../../../visual-basic/programming-guide/program-structure/how-to-create-xml-documentation.md)
- [<span data-ttu-id="1406c-112">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="1406c-112">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
