---
title: Utilisez &#39;FileGetObject&#39; au lieu de &#39;FileGet&#39; quand l’argument de type &#39;objet&#39;
ms.date: 07/20/2015
ms.assetid: 090b8088-895a-482a-9362-606596bac304
ms.openlocfilehash: 2edb80f6df95774e0ea5a7b51e57925845d7ba75
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33640415"
---
# <a name="use-39filegetobject39-instead-of-39fileget39-when-using-argument-of-type-39object39"></a>Utilisez &#39;FileGetObject&#39; au lieu de &#39;FileGet&#39; quand l’argument de type &#39;objet&#39;
La méthode `FileGet` comprend un argument de type `Object`. `FileGetObject` doit être utilisé à la place de `FileGet` pour éviter toute ambiguïté.  
  
 Notez que les fonctionnalités offertes par `My.Computer.Filesystem` proposent une plus grande facilité d’utilisation et des performances accrues par rapport à `FileGet` ou `FileGetObject`.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Remplacez `FileGet` par `FileGetObject`.  
  
2.  Effectuez un cast sur le type de l’argument `Object` pour en faire un type plus spécifique.  
  
## <a name="see-also"></a>Voir aussi  
   
 [My.Computer.FileSystem](xref:Microsoft.VisualBasic.FileIO.FileSystem)
