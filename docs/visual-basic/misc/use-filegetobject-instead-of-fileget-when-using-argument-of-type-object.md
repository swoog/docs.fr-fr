---
title: Utilisez ’FileGetObject’ à la place de ’FileGet’ quand l’argument est de type ’Object’.
ms.date: 07/20/2015
ms.assetid: 090b8088-895a-482a-9362-606596bac304
ms.openlocfilehash: 60eaabc686070aced908116728f06d4e82b5cecb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54723392"
---
# <a name="use-filegetobject-instead-of-fileget-when-using-argument-of-type-object"></a>Utilisez ’FileGetObject’ à la place de ’FileGet’ quand l’argument est de type ’Object’.
La méthode `FileGet` comprend un argument de type `Object`. `FileGetObject` doit être utilisé à la place de `FileGet` pour éviter toute ambiguïté.  
  
 Notez que les fonctionnalités offertes par `My.Computer.Filesystem` proposent une plus grande facilité d’utilisation et des performances accrues par rapport à `FileGet` ou `FileGetObject`.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Remplacez `FileGet` par `FileGetObject`.  
  
2.  Effectuez un cast sur le type de l’argument `Object` pour en faire un type plus spécifique.  
  
## <a name="see-also"></a>Voir aussi

- [My.Computer.FileSystem](xref:Microsoft.VisualBasic.FileIO.FileSystem)
