---
title: Numéro d'enregistrement incorrect
ms.date: 07/20/2015
f1_keywords:
- vbrID63
ms.assetid: 1fcc33f8-822a-4de9-a6e3-228ddb5824a6
ms.openlocfilehash: abd0a1467c0991a40b93e74a1d7a7889367fb8ca
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61977021"
---
# <a name="bad-record-number"></a>Numéro d'enregistrement incorrect
Le numéro d’enregistrement dans une instruction `a FileGet`, `FilePut`, `FileGetObject`ou `FilePutObject` est inférieur ou égal à zéro.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Vérifiez les calculs utilisés pour générer le numéro d’enregistrement. Vérifiez l’orthographe des variables contenant le numéro d’enregistrement ou utilisées dans le calcul des numéros d’enregistrement. Un nom de variable mal orthographié est déclaré implicitement et possède une valeur égale à zéro, sauf si vous avez utilisé `Option Explicit On` dans le module.  
  
## <a name="see-also"></a>Voir aussi

- [Option Explicit (instruction)](../../visual-basic/language-reference/statements/option-explicit-statement.md)
