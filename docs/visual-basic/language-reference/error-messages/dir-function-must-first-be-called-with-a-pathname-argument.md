---
title: La fonction ’Dir’ doit d’abord être appelée avec un argument ’Pathname’
ms.date: 07/20/2015
f1_keywords:
- vbrDIR_IllegalCall
ms.assetid: 7b5d149f-be91-4ac3-8262-86a360894e7d
ms.openlocfilehash: d255b8dddd098835764f72b8a166eaa08b0353df
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61803452"
---
# <a name="dir-function-must-first-be-called-with-a-pathname-argument"></a>La fonction ’Dir’ doit d’abord être appelée avec un argument ’Pathname’
Un appel initial à la `Dir` fonction n’inclut pas le `PathName` argument. Le premier appel à `Dir` doit inclure un `PathName`, mais les appels suivants à `Dir` n’avez pas besoin d’inclure des paramètres permettant d’extraire l’élément suivant.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Fournir un `PathName` argument dans l’appel de fonction.  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.FileSystem.Dir%2A>
