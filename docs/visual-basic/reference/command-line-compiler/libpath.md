---
title: -libpath
ms.date: 03/10/2018
helpviewer_keywords:
- libpath compiler option [Visual Basic]
- /libpath compiler option [Visual Basic]
- -libpath compiler option [Visual Basic]
ms.assetid: 5f1c26c9-3455-4e89-bdf3-b12d6c2e655b
ms.openlocfilehash: b7bfcb0f2034145822922126fe61efea8d8ef269
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61793924"
---
# <a name="-libpath"></a>-libpath
Spécifie l’emplacement des assemblys référencés.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-libpath:dirList  
```  
  
## <a name="arguments"></a>Arguments  
  
|Terme|Définition|  
|---|---|  
|`dirList`|Obligatoire. Délimitée par des points-virgules de liste de répertoires pour le compilateur doit vérifier si un assembly référencé est introuvable dans le répertoire de travail actuel (le répertoire à partir duquel vous appelez le compilateur) ou le répertoire du système du common language runtime. Si le nom du répertoire contient un espace, placez le nom entre guillemets ( » «).|  
  
## <a name="remarks"></a>Notes  
 Le `-libpath` option spécifie l’emplacement des assemblys référencés par le [-référence](../../../visual-basic/reference/command-line-compiler/reference.md) option.  
  
 Le compilateur recherche les références d’assembly qui ne sont pas complètes dans l’ordre suivant :  
  
1. Répertoire de travail actuel. Il s’agit du répertoire à partir duquel le compilateur est appelé.  
  
2. Répertoire système du common language runtime.  
  
3. Répertoires spécifiés par `/libpath`.  
  
4. Répertoires spécifiés par la variable d’environnement LIB.  
  
 Le `-libpath` option est additif ; en spécifiant davantage qu’une seule fois ajoute aux valeurs précédentes.  
  
 Utilisez `-reference` pour spécifier une référence d’assembly.  
  
|Pour définir /libpath dans Visual Studio un environnement de développement intégré|  
|---|  
|1.  Sélectionnez un projet dans l' **Explorateur de solutions**. Dans le menu **Projet**, cliquez sur **Propriétés**. <br />2.  Cliquez sur l’onglet **Références**.<br />3.  Cliquez sur le **référencer les chemins d’accès...**  bouton.<br />4.  Dans le **chemins d’accès de référence** boîte de dialogue, entrez le nom du répertoire dans le **dossier :** boîte.<br />5.  Cliquez sur **ajouter dossier**.|  
  
## <a name="example"></a>Exemple  
 Le code suivant compile `T2.vb` pour créer un fichier .exe. Le compilateur recherche dans le répertoire de travail, dans le répertoire racine du lecteur C: et dans le répertoire de nouveaux assemblys du lecteur C: pour références d’assembly.  
  
```console  
vbc -libpath:c:\;"c:\New Assemblies" -reference:t2.dll t2.vb  
```  
  
## <a name="see-also"></a>Voir aussi

- [Assemblys dans .NET](../../../standard/assembly/index.md)
- [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)
- [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
