---
title: "'<attribute>' ne peut pas être appliqué, car le format du GUID '<number>' n'est pas correct"
ms.date: 07/20/2015
f1_keywords:
- vbc32500
- bc32500
helpviewer_keywords:
- BC32500
ms.assetid: 6fa34c55-368e-4d7d-b488-07a3fffe045f
ms.openlocfilehash: d27c326b6a88271ba4abf0144e71027f6671b17e
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59330673"
---
# <a name="attribute-cannot-be-applied-because-the-format-of-the-guid-number-is-not-correct"></a>«\<attribut >' ne peut pas être appliqué, car le format du GUID '\<nombre >' n’est pas correct
Un `COMClassAttribute` bloc d’attributs Spécifie un identificateur global unique (GUID) qui n’est pas conforme au format approprié. `COMClassAttribute` utilise les GUID pour identifier de manière unique la classe, l’interface et l’événement de création.  
  
 Un GUID se compose de 16 octets, dont les huit premiers sont numériques et les huit derniers sont binaires. Il est généré par les utilitaires Microsoft tels que uuidgen.exe et est garanti être unique dans l’espace et de temps.  
  
 **ID d’erreur :** BC32500  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Déterminer le GUID ou le GUID nécessaire pour identifier l’objet COM approprié.  
  
2. Vérifiez que les chaînes de GUID présentées au bloc d’attributs `COMClassAttribute` sont copiées correctement.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Guid>
- [Vue d’ensemble des attributs](../../../visual-basic/programming-guide/concepts/attributes/index.md)
