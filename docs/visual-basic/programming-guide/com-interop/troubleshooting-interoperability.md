---
title: Dépannage des problèmes liés à l'interopérabilité (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- interop, deploying assemblies
- assemblies [Visual Basic]
- interop, installing assemblies that share components
- COM objects, troubleshooting
- interop, sharing components
- troubleshooting interoperability [Visual Basic]
- interoperability, troubleshooting
- COM interop [Visual Basic], troubleshooting
- assemblies [Visual Basic], deploying
- troubleshooting Visual Basic, interoperability
- interop assemblies
- interoperability, sharing components
- shared components, using with assemblies
ms.assetid: b324cc1e-b03c-4f39-aea6-6a6d5bfd0e37
ms.openlocfilehash: 413c9331611d3406c13df58f25db1ef0255339b6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54517667"
---
# <a name="troubleshooting-interoperability-visual-basic"></a>Dépannage des problèmes liés à l'interopérabilité (Visual Basic)
Lorsque vous interagissez entre COM et le code managé de la [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)], vous pouvez rencontrer un ou plusieurs des problèmes courants suivants.  
  
##  <a name="vbconinteroperabilitymarshalinganchor1"></a> Marshaling d’interopérabilité  
 Dans certains cas, vous devrez peut-être utiliser des types de données qui ne sont pas dans le cadre de la [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)]. Assemblys d’interopérabilité gèrent l’essentiel du travail pour les objets COM, mais vous devrez peut-être contrôler les types de données qui sont utilisés lorsque les objets managés sont exposées à COM. Par exemple, les structures de bibliothèques de classes doivent indiquer le `BStr` type sur les chaînes envoyées à des objets COM créés par Visual Basic 6.0 et versions antérieures non managé. Dans ce cas, vous pouvez utiliser le <xref:System.Runtime.InteropServices.MarshalAsAttribute> attribut pour que les types managés à exposer en tant que types non managés.  
  
##  <a name="vbconinteroperabilitymarshalinganchor2"></a> Exportation de chaînes de longueur fixe au Code non managé  
 Dans Visual Basic 6.0 et versions antérieures, les chaînes sont exportés vers des objets COM en tant que séquence d’octets sans caractère null de fin. Pour la compatibilité avec d’autres langages, Visual Basic .NET inclut un caractère de fin lors de l’exportation de chaînes. La meilleure façon de résoudre cette incompatibilité consiste à exporter les chaînes qui ne possèdent pas le caractère de fin en tant que tableaux de `Byte` ou `Char`.  
  
##  <a name="vbconinteroperabilitymarshalinganchor3"></a> Exportation de hiérarchies d’héritage  
 Aplatissent les hiérarchies lorsqu’elle est exposée en tant qu’objets COM de classe managée. Par exemple, si vous définissez une classe de base avec un membre, puis héritez de la classe de base dans une classe dérivée qui est exposée en tant qu’objet COM, les clients qui utilisent la classe dérivée dans l’objet COM ne sera pas en mesure d’utiliser les membres hérités. Les membres de classe de base est accessible à partir d’objets COM uniquement en tant qu’instances d’une classe de base, puis uniquement si la classe de base est également créée comme un objet COM.  
  
## <a name="overloaded-methods"></a>Méthodes surchargées  
 Bien que vous pouvez créer des méthodes surchargées avec Visual Basic, ils ne sont pas pris en charge par COM. Lorsqu’une classe qui contient des méthodes surchargées est exposée en tant qu’objet COM, les nouveaux noms de méthode sont générés pour les méthodes surchargées.  
  
 Par exemple, considérons une classe qui a deux surcharges de la `Synch` (méthode). Lorsque la classe est exposée comme un objet COM, les nouveaux noms de méthode générée peut être `Synch` et `Synch_2`.  
  
 Le changement de nom peut provoquer deux problèmes pour les consommateurs de l’objet COM.  
  
1.  Les clients ne l’espériez les noms de méthode générée.  
  
2.  Les noms de méthode générée dans la classe exposée comme un objet COM peuvent changer lorsque de nouvelles surcharges sont ajoutées à la classe ou de sa classe de base. Cela peut entraîner des problèmes de versioning.  
  
 Pour résoudre les problèmes, attribuez un nom unique, au lieu d’utiliser la surcharge, lorsque vous développez des objets qui seront exposées en tant qu’objets COM à chaque méthode.  
  
##  <a name="vbconinteroperabilitymarshalinganchor4"></a> Utilisation d’objets COM via les assemblys d’interopérabilité  
 Vous utilisez des assemblys PIA presque comme si elles étaient des remplacements de code managé pour les objets COM qu’ils représentent. Toutefois, comme ce sont des wrappers et des objets COM réels pas, il existe certaines différences entre l’utilisation d’assemblys d’interopérabilité et d’assemblys standards. Ces différences comprennent l’exposition des classes et des types de données pour les paramètres et valeurs de retour.  
  
##  <a name="vbconinteroperabilitymarshalinganchor5"></a> Les classes exposées en tant que les deux Interfaces et Classes  
 Contrairement aux classes dans les assemblys standards, les classes COM sont exposés dans les assemblys PIA en tant qu’une interface et une classe qui représente la classe COM. Nom de l’interface est identique à celle de la classe COM. Le nom de la classe d’interopérabilité est identique à celui de la classe COM d’origine, mais avec le mot « Class » est ajouté. Par exemple, supposons que vous avez un projet avec une référence à un assembly d’interopérabilité pour un objet COM. Si la classe COM est nommée `MyComClass`, IntelliSense et l’Explorateur d’objets affichent une interface nommée `MyComClass` et une classe nommée `MyComClassClass`.  
  
##  <a name="vbconinteroperabilitymarshalinganchor6"></a> Création d’Instances d’une classe .NET Framework  
 En règle générale, vous créez une instance d’un [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] classe à l’aide de la `New` instruction avec un nom de classe. Avoir une classe COM représentée par un assembly d’interopérabilité est le seul cas dans lequel vous pouvez utiliser la `New` instruction avec une interface. Sauf si vous utilisez la classe COM avec un `Inherits` instruction, vous pouvez utiliser l’interface comme vous le feriez pour une classe. Le code suivant montre comment créer un `Command` objet dans un projet qui a une référence à l’objet COM de la bibliothèque Microsoft ActiveX Data Objects 2.8 :  
  
 [!code-vb[VbVbalrInterop#20](../../../visual-basic/programming-guide/com-interop/codesnippet/VisualBasic/troubleshooting-interoperability_1.vb)]  
  
 Toutefois, si vous utilisez la classe COM comme base pour une classe dérivée, vous devez utiliser la classe d’interopérabilité qui représente la classe COM, comme dans le code suivant :  
  
 [!code-vb[VbVbalrInterop#21](../../../visual-basic/programming-guide/com-interop/codesnippet/VisualBasic/troubleshooting-interoperability_2.vb)]  
  
> [!NOTE]
>  Assemblys PIA implémentent implicitement les interfaces qui représentent des classes COM. Vous ne devez pas essayer d’utiliser le `Implements` entraîne d’instruction pour implémenter ces interfaces ou une erreur.  
  
##  <a name="vbconinteroperabilitymarshalinganchor7"></a> Types de données pour les paramètres et valeurs de retour  
 Contrairement aux membres des assemblys standard, les membres de l’assembly d’interopérabilité peuvent avoir des types de données qui diffèrent de ceux utilisés dans la déclaration d’objet d’origine. Bien que les assemblys PIA convertissent implicitement les types de COM pour les types common language runtime compatible, vous devez prêter attention aux types de données qui sont utilisées par les deux côtés pour empêcher les erreurs d’exécution. Par exemple, dans les objets COM créés dans Visual Basic 6.0 et versions antérieures, les valeurs de type `Integer` supposent la [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] type équivalent, `Short`. Il est recommandé d’utiliser l’Explorateur d’objets pour examiner les caractéristiques des membres importés avant de les utiliser.  
  
##  <a name="vbconinteroperabilitymarshalinganchor8"></a> Méthodes COM de niveau module  
 La plupart des objets COM sont utilisés en créant une instance d’une classe COM en utilisant le `New` mot clé, puis en appelant les méthodes de l’objet. Une exception à cette règle concerne les objets COM qui contiennent `AppObj` ou `GlobalMultiUse` classes COM. Ces classes sont semblables aux méthodes au niveau du module dans les classes Visual Basic .NET. Visual Basic 6.0 et les versions antérieures créent implicitement des instances de ces objets pour vous la première fois que vous appelez une de leurs méthodes. Par exemple, dans Visual Basic 6.0, vous pouvez ajouter une référence à la bibliothèque d’objets Microsoft DAO 3.6 et appeler le `DBEngine` méthode sans d’abord créer une instance :  
  
```vb  
Dim db As DAO.Database  
' Open the database.  
Set db = DBEngine.OpenDatabase("C:\nwind.mdb")  
' Use the database object.  
```  
  
 Visual Basic .NET nécessite toujours créer les instances des objets COM avant de pouvoir utiliser leurs méthodes. Pour utiliser ces méthodes dans Visual Basic, déclarez une variable de la classe souhaitée et utilisez le mot clé new pour assigner l’objet à la variable objet. Le `Shared` mot clé peut être utilisé lorsque vous souhaitez vous assurer que qu’une seule instance de la classe est créée.  
  
 [!code-vb[VbVbalrInterop#23](../../../visual-basic/programming-guide/com-interop/codesnippet/VisualBasic/troubleshooting-interoperability_3.vb)]  
  
##  <a name="vbconinteroperabilitymarshalinganchor9"></a> Erreurs non gérées dans les gestionnaires d’événements  
 Un problème d’interopérabilité courant concerne les erreurs dans les gestionnaires d’événements qui gèrent les événements déclenchés par des objets COM. Ces erreurs sont ignorées, sauf si vous recherchez spécifiquement les erreurs à l’aide de `On Error` ou `Try...Catch...Finally` instructions. Par exemple, l’exemple suivant provient d’un projet Visual Basic .NET qui a une référence à l’objet COM de la bibliothèque Microsoft ActiveX Data Objects 2.8.  
  
 [!code-vb[VbVbalrInterop#24](../../../visual-basic/programming-guide/com-interop/codesnippet/VisualBasic/troubleshooting-interoperability_4.vb)]  
  
 Cet exemple génère une erreur comme prévu. Toutefois, si vous essayez du même exemple sans le `Try...Catch...Finally` bloc, l’erreur est ignorée comme si vous avez utilisé le `OnError Resume Next` instruction. Sans gestion des erreurs, la division par zéro échoue sans avertissement. Étant donné que ces erreurs ne déclenchent jamais d’erreurs d’exception non gérée, il est important que vous utilisez une forme de gestion des exceptions dans les gestionnaires d’événements qui gèrent des événements à partir des objets COM.  
  
### <a name="understanding-com-interop-errors"></a>Compréhension des erreurs COM interop  
 Sans gestion des erreurs, les appels interop génèrent souvent des erreurs qui fournissent des informations de peu. Si possible, utilisez structurées gestion des erreurs pour fournir plus d’informations sur les problèmes lorsqu’ils se produisent. Cela peut être particulièrement utile lorsque vous déboguez des applications. Exemple :  
  
 [!code-vb[VbVbalrInterop#25](../../../visual-basic/programming-guide/com-interop/codesnippet/VisualBasic/troubleshooting-interoperability_5.vb)]  
  
 Vous trouverez des informations telles que la description d’erreur, HRESULT et la source des erreurs COM en examinant le contenu de l’objet exception.  
  
##  <a name="vbconinteroperabilitymarshalinganchor10"></a> Problèmes de contrôle ActiveX  
 La plupart des contrôles ActiveX qui fonctionnent avec Visual Basic 6.0 fonctionne avec Visual Basic .NET sans difficultés. Les principales exceptions sont les contrôles conteneurs, ou des contrôles qui contiennent visuellement des autres contrôles. Voici quelques exemples de contrôles plus anciens qui ne fonctionnent pas correctement avec Visual Studio :  
  
-   Contrôle Frame de Microsoft Forms 2.0  
  
-   Contrôle Up-Down, également connu sous le contrôle de sélection numérique  
  
-   Contrôle Sheridan Tab.  
  
 Il existe peu de solutions pour les problèmes de contrôle ActiveX non pris en charge. Vous pouvez migrer des contrôles existants à Visual Studio si vous possédez le code source d’origine. Sinon, vous pouvez vérifier avec les éditeurs de logiciels pour la mise à jour. Versions compatibles avec NET des contrôles pour remplacer non pris en charge les contrôles ActiveX.  
  
##  <a name="vbconinteroperabilitymarshalinganchor11"></a> Transmission des propriétés en lecture seule de contrôles ByRef  
 Visual Basic .NET génère parfois des erreurs COM par exemple, « Error 0x800A017F CTL_E_SETNOTSUPPORTED » lorsque vous transmettez `ReadOnly` propriétés de certains anciens contrôles ActiveX comme `ByRef` paramètres à d’autres procédures. Les appels de procédure similaires à partir de Visual Basic 6.0 ne génèrent pas d’erreur et les paramètres sont traités comme si vous les passés par valeur. Le message d’erreur Visual Basic .NET indique que vous essayez de modifier une propriété qui n’a pas de propriété `Set` procédure.  
  
 Si vous avez accès à la procédure appelée, vous pouvez éviter cette erreur à l’aide de la `ByVal` mot clé pour déclarer des paramètres qui acceptent `ReadOnly` propriétés. Exemple :  
  
 [!code-vb[VbVbalrInterop#26](../../../visual-basic/programming-guide/com-interop/codesnippet/VisualBasic/troubleshooting-interoperability_6.vb)]  
  
 Si vous n’avez pas accès au code source pour la procédure appelée, vous pouvez forcer la propriété à être passés par valeur en ajoutant un jeu supplémentaire de crochets autour de la procédure d’appel. Par exemple, dans un projet qui a une référence à l’objet COM de la bibliothèque Microsoft ActiveX Data Objects 2.8, vous pouvez utiliser :  
  
 [!code-vb[VbVbalrInterop#27](../../../visual-basic/programming-guide/com-interop/codesnippet/VisualBasic/troubleshooting-interoperability_7.vb)]  
  
##  <a name="vbconinteroperabilitymarshalinganchor12"></a> Déploiement d’assemblys exposant l’interopérabilité  
 Déploiement d’assemblys qui exposent les interfaces COM présente des défis uniques. Par exemple, un problème potentiel se produit lorsque des applications distinctes référencent le même assembly COM. Cette situation est courante lorsqu’une nouvelle version d’un assembly est installée et une autre application utilise toujours l’ancienne version de l’assembly. Si vous désinstallez un assembly partageant une DLL, vous pouvez involontairement rendre non disponible aux autres assemblys.  
  
 Pour éviter ce problème, vous devez installer les assemblys partagés pour le Global Assembly Cache (GAC) et utiliser un module de fusion pour le composant. Si vous ne pouvez pas installer l’application dans le GAC, il doit être installé dans un sous-répertoire spécifique à la version du répertoire CommonFilesFolder.  
  
 Dans le répertoire avec l’application appelante, les assemblys qui ne sont pas partagés doivent être placés côte à côte.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Runtime.InteropServices.MarshalAsAttribute>
- [COM Interop](../../../visual-basic/programming-guide/com-interop/index.md)
- [Tlbimp.exe (importateur de bibliothèques de types)](../../../framework/tools/tlbimp-exe-type-library-importer.md)
- [Tlbexp.exe (exportateur de bibliothèques de types)](../../../framework/tools/tlbexp-exe-type-library-exporter.md)
- [Procédure pas à pas : Implémentation de l’héritage avec les objets COM](../../../visual-basic/programming-guide/com-interop/walkthrough-implementing-inheritance-with-com-objects.md)
- [Inherits (instruction)](../../../visual-basic/language-reference/statements/inherits-statement.md)
- [Global Assembly Cache](../../../framework/app-domains/gac.md)
