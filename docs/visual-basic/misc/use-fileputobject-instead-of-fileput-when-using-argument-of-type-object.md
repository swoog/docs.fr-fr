---
title: Utilisez ’FilePutObject’ à la place de ’FilePut’ quand l’argument est de type ’Object’.
ms.date: 07/20/2015
f1_keywords:
- vbrUseFilePutObject
ms.assetid: d207b9b7-5898-4c13-8b03-9feefac5f726
ms.openlocfilehash: 3d793151905c61ee12eccdfdb5e9567a4924bb35
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54725556"
---
# <a name="use-fileputobject-instead-of-fileput-when-using-argument-of-type-object"></a>Utilisez ’FilePutObject’ à la place de ’FilePut’ quand l’argument est de type ’Object’.
La méthode `FilePut` comprend un argument de type `Object`. `FilePutObject` doit être utilisé à la place de `FilePut` pour éviter toute ambiguïté.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Remplacez `FilePut` par `FilePutObject`.  
  
-   Effectuez un cast sur le type de l’argument `Object` pour en faire un type plus spécifique.  
  
-   Utilisez les fonctionnalités disponibles dans l’objet `My.Computer.FileSystem` .  
  
## <a name="see-also"></a>Voir aussi

- [My.Computer.FileSystem](xref:Microsoft.VisualBasic.FileIO.FileSystem)
- [My.Computer.FileSystem.WriteAllBytes](xref:Microsoft.VisualBasic.MyServices.FileSystemProxy.WriteAllBytes%2A)
