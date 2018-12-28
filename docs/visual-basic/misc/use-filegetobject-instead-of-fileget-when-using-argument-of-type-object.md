---
title: Utilisez ’FileGetObject’ à la place de ’FileGet’ quand l’argument est de type ’Object’.
ms.date: 07/20/2015
ms.assetid: 090b8088-895a-482a-9362-606596bac304
ms.openlocfilehash: ddbe187ed1210d238448a5ff3feaee18beea1def
ms.sourcegitcommit: 0888d7b24f475c346a3f444de8d83ec1ca7cd234
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/22/2018
ms.locfileid: "53768009"
---
# <a name="use-filegetobject-instead-of-fileget-when-using-argument-of-type-object"></a>Utilisez ’FileGetObject’ à la place de ’FileGet’ quand l’argument est de type ’Object’.
La méthode `FileGet` comprend un argument de type `Object`. `FileGetObject` doit être utilisé à la place de `FileGet` pour éviter toute ambiguïté.  
  
 Notez que les fonctionnalités offertes par `My.Computer.Filesystem` proposent une plus grande facilité d’utilisation et des performances accrues par rapport à `FileGet` ou `FileGetObject`.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Remplacez `FileGet` par `FileGetObject`.  
  
2.  Effectuez un cast sur le type de l’argument `Object` pour en faire un type plus spécifique.  
  
## <a name="see-also"></a>Voir aussi  
   
 [My.Computer.FileSystem](xref:Microsoft.VisualBasic.FileIO.FileSystem)
