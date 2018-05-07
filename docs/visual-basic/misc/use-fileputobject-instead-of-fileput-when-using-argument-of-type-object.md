---
title: Utilisez &#39;FilePutObject&#39; au lieu de &#39;FilePut&#39; quand l’argument de type &#39;objet&#39;
ms.date: 07/20/2015
f1_keywords:
- vbrUseFilePutObject
ms.assetid: d207b9b7-5898-4c13-8b03-9feefac5f726
ms.openlocfilehash: 529352d98c175981c20861205ce04c8a2ebcdca9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="use-39fileputobject39-instead-of-39fileput39-when-using-argument-of-type-39object39"></a>Utilisez &#39;FilePutObject&#39; au lieu de &#39;FilePut&#39; quand l’argument de type &#39;objet&#39;
Le `FilePut` méthode inclut un argument de type `Object`. `FilePutObject` doit être utilisé à la place de `FilePut` pour éviter toute ambiguïté.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Remplacez `FilePut` par `FilePutObject`.  
  
-   Effectuez un cast sur le type de l’argument `Object` pour en faire un type plus spécifique.  
  
-   Utilisez les fonctionnalités disponibles dans l’objet `My.Computer.FileSystem` .  
  
## <a name="see-also"></a>Voir aussi  
   
 [My.Computer.FileSystem](xref:Microsoft.VisualBasic.FileIO.FileSystem)  
 [My.Computer.FileSystem.WriteAllBytes](xref:Microsoft.VisualBasic.MyServices.FileSystemProxy.WriteAllBytes%2A)
