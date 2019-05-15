---
title: Introduction à COM Interop (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- interop assemblies
- COM interop [Visual Basic], about COM interop
ms.assetid: 8bd62e68-383d-407f-998b-29aa0ce0fd67
ms.openlocfilehash: 5eb862d75f8870da40af4cd817fa32a3d2781f38
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65592718"
---
# <a name="introduction-to-com-interop-visual-basic"></a>Introduction à COM Interop (Visual Basic)
Le composant COM (Object Model) permet un objet d’exposer ses fonctionnalités à d’autres composants et d’héberger des applications. Bien que les objets COM ont été essentiels à Windows de programmation de nombreuses années, les applications conçues pour le common language runtime (CLR) offrent de nombreux avantages.  
  
 Les applications .NET framework finira par remplacer celles développées avec COM. En attendant, vous devrez peut-être utiliser ou créer des objets COM à l’aide de Visual Studio. L’interopérabilité avec COM, ou *COM interop*, vous pouvez ainsi utiliser des objets COM existants lors de la transition vers le .NET Framework à votre propre rythme.  
  
 En utilisant le .NET Framework pour créer des composants COM, vous pouvez utiliser COM interop sans inscription. Cela vous permet de contrôler quelle version de DLL est activée lorsque plusieurs versions sont installée sur un ordinateur et permet aux utilisateurs finaux d’utiliser XCOPY ou FTP pour copier votre application dans un répertoire approprié sur leur ordinateur où il peut être exécuté. Pour plus d’informations, consultez [Registration-Free COM Interop](../../../framework/interop/registration-free-com-interop.md).  
  
## <a name="managed-code-and-data"></a>Le Code managé et des données  
 Le code développé pour le .NET Framework est appelé *du code managé*et contient des métadonnées qui sont utilisée par le CLR. Données utilisées par les applications .NET Framework sont appelées *les données managées* , car le runtime gère les tâches liées aux données telles que la vérification de type allocation et libération de la mémoire et l’exécution. Par défaut, Visual Basic .NET utilise des données et le code managé, mais vous pouvez accéder à du code non managé et les données des objets COM à l’aide des assemblys d’interopérabilité (décrites plus loin dans cette page).  
  
## <a name="assemblies"></a>Assemblys  
 Un assembly est le principal bloc de construction d’une application .NET Framework. C’est un ensemble de fonctionnalités qui sont générées, avec contrôle de version et déployées comme une unité de mise en œuvre unique contenant un ou plusieurs fichiers. Chaque assembly contient un manifeste d’assembly.  
  
## <a name="type-libraries-and-assembly-manifests"></a>Bibliothèques de types et les manifestes d’Assembly  
 Bibliothèques de types décrivent les caractéristiques des objets COM, tels que les noms des membres et types de données. Manifestes d’assembly exécutent la même fonction pour les applications .NET Framework. Ils incluent des informations sur les éléments suivants :  
  
- Identité de l’assembly, version, culture et signature numérique.  
  
- Fichiers qui composent l’implémentation de l’assembly.  
  
- Types et ressources qui composent l’assembly. Comprennent celles qui sont exportés à partir de celui-ci.  
  
- Dépendances de compilation des autres assemblys.  
  
- Autorisations requises pour l’assembly pour s’exécuter correctement.  
  
 Pour plus d’informations sur les assemblys et les manifestes d’assembly, consultez [assemblys dans .NET](../../../standard/assembly/index.md).  
  
### <a name="importing-and-exporting-type-libraries"></a>Importation et exportation de bibliothèques de types  
 Visual Studio contient un utilitaire, Tlbimp, qui vous permet d’importer des informations à partir d’une bibliothèque de types dans une application .NET Framework. Vous pouvez générer des bibliothèques de types provenant d’assemblys à l’aide de l’utilitaire Tlbexp.  
  
 Pour plus d’informations sur Tlbimp et Tlbexp, consultez [Tlbimp.exe (Type Library Importer)](../../../framework/tools/tlbimp-exe-type-library-importer.md) et [Tlbexp.exe (exportateur)](../../../framework/tools/tlbexp-exe-type-library-exporter.md).  
  
## <a name="interop-assemblies"></a>Assemblys PIA  
 Assemblys d’interopérabilité sont des assemblys .NET Framework qui géré de pont entre et membres de code non managé, mappage des membres de l’objet COM équivalent .NET Framework managés. Assemblys d’interopérabilité créés par Visual Basic .NET gèrent de nombreux détails de l’utilisation des objets COM, tels que le marshaling d’interopérabilité.  
  
## <a name="interoperability-marshaling"></a>Marshaling d’interopérabilité  
 Toutes les applications .NET Framework partagent un ensemble de types courants qui permettent l’interopérabilité des objets, quel que soit le langage de programmation qui est utilisé. Les paramètres et les valeurs de retour des objets COM utilisent parfois des types de données qui diffèrent de celles utilisées dans le code managé. *Marshaling d’interopérabilité* est le processus empaqueter des paramètres et valeurs de retour dans les types de données équivalents lors de leur déplacement vers et depuis des objets COM. Pour plus d’informations, consultez [Marshaling d’interopérabilité](../../../framework/interop/interop-marshaling.md).  
  
## <a name="see-also"></a>Voir aussi

- [COM Interop](../../../visual-basic/programming-guide/com-interop/index.md)
- [Procédure pas à pas : Implémentation de l’héritage avec les objets COM](../../../visual-basic/programming-guide/com-interop/walkthrough-implementing-inheritance-with-com-objects.md)
- [Interopération avec du code non managé](../../../framework/interop/index.md)
- [Dépannage des problèmes liés à l’interopérabilité](../../../visual-basic/programming-guide/com-interop/troubleshooting-interoperability.md)
- [Assemblys dans .NET](../../../standard/assembly/index.md)
- [Tlbimp.exe (importateur de bibliothèques de types)](../../../framework/tools/tlbimp-exe-type-library-importer.md)
- [Tlbexp.exe (exportateur de bibliothèques de types)](../../../framework/tools/tlbexp-exe-type-library-exporter.md)
- [Marshaling d'interopérabilité](../../../framework/interop/interop-marshaling.md)
- [COM Interop sans inscription](../../../framework/interop/registration-free-com-interop.md)
