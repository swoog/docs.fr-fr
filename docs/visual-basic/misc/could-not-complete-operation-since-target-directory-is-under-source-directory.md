---
title: Impossible d’achever l’opération, car le répertoire cible se situe sous le répertoire source
ms.date: 07/20/2015
f1_keywords:
- vbrIO_CyclicOperation
ms.assetid: 850d3a24-5d51-4ac8-a912-630efcd75278
ms.openlocfilehash: fca42f91f803a6b12535badcb25cc05cc3d23f6b
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64598471"
---
# <a name="could-not-complete-operation-since-target-directory-is-under-source-directory"></a>Impossible d’achever l’opération, car le répertoire cible se situe sous le répertoire source
Une opération cyclique a échoué. Les opérations cycliques se répètent et, par conséquent, ne peuvent pas s’achever. Par exemple, l’objet A peut essayer d’hériter de l’objet B qui hérite, à son tour, de l’objet A.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Lors d’un héritage, vérifiez qu’il n’existe aucune référence cyclique.  
  
## <a name="see-also"></a>Voir aussi

- [Types d’erreurs](../../visual-basic/programming-guide/language-features/error-types.md)
- [Utilisez des points d’arrêt dans le débogueur Visual Studio](/visualstudio/debugger/using-breakpoints)
