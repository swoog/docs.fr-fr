---
title: Une référence à l'assembly '<assemblyname>' contenant la classe de base '<classname>' est requise
ms.date: 07/20/2015
f1_keywords:
- bc30007
- vbc30007
helpviewer_keywords:
- BC30007
ms.assetid: 5f34cf47-6c6e-4954-bd8e-d6b020b75fb7
ms.openlocfilehash: 8218a3325d5d47bf85aacab1724221d233d92ba4
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64661702"
---
# <a name="reference-required-to-assembly-assemblyname-containing-the-base-class-classname"></a>Référence à l’assembly requise '\<nom_assembly >' contenant la classe de base\<nom_classe >'
Référence à l’assembly requise '\<nom_assembly >' contenant la classe de base\<nom_classe >'. Ajoutez-en une à votre projet.  
  
 La classe est définie dans une bibliothèque de liens dynamiques (DLL) ou un assembly qui n’est pas directement référencé dans votre projet. Le compilateur Visual Basic requiert une référence pour éviter toute ambiguïté au cas où la classe est définie dans plusieurs DLL ou assemblys.  
  
 **ID d’erreur :** BC30007  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Incluez le nom de la DLL ou de l’assembly non référencé dans vos références de projet.  
  
## <a name="see-also"></a>Voir aussi

- [Gestion des références dans un projet](/visualstudio/ide/managing-references-in-a-project)
- [Dépannage de références rompues](/visualstudio/ide/troubleshooting-broken-references)
