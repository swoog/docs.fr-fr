---
title: La fonction ’Dir’ doit d’abord être appelée avec un argument ’Pathname’
ms.date: 07/20/2015
f1_keywords:
- vbrDIR_IllegalCall
ms.assetid: 7b5d149f-be91-4ac3-8262-86a360894e7d
ms.openlocfilehash: 828c715d9aaceef17d030113e7eda302f025ca9d
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55282585"
---
# <a name="dir-function-must-first-be-called-with-a-pathname-argument"></a>La fonction ’Dir’ doit d’abord être appelée avec un argument ’Pathname’
Un appel initial à la `Dir` fonction n’inclut pas le `PathName` argument. Le premier appel à `Dir` doit inclure un `PathName`, mais les appels suivants à `Dir` n’avez pas besoin d’inclure des paramètres permettant d’extraire l’élément suivant.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Fournir un `PathName` argument dans l’appel de fonction.  
  
## <a name="see-also"></a>Voir aussi
- <xref:Microsoft.VisualBasic.FileSystem.Dir%2A>
