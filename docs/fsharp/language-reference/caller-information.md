---
title: 'Informations de l’appelant (F #)'
description: Décrit comment utiliser les attributs d’Argument appelant informations pour obtenir des informations de l’appelant à partir d’une méthode.
ms.date: 04/25/2017
ms.openlocfilehash: 0f2f4b16804d9156d234cc29d1f72ebe80a5b556
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44048676"
---
# <a name="caller-information"></a>Informations de l’appelant

À l'aide des attributs d'informations de l'appelant, vous pouvez obtenir des informations sur l'appelant d'une méthode. Vous pouvez obtenir le chemin d'accès du fichier de code source, le numéro de ligne dans le code source, puis le nom du membre de l'appelant. Ces informations sont utiles pour suivre, déboguer, et créer des outils de diagnostic.

Pour obtenir ces informations, vous utilisez les attributs qui sont appliqués aux paramètres facultatifs, qui a une valeur par défaut. Le tableau suivant répertorie les attributs d’informations de l’appelant qui sont définies dans le [System.Runtime.CompilerServices](/dotnet/api/system.runtime.compilerservices) espace de noms :

|Attribut|Description|Type|
|---------|-----------|----|
|[CallerFilePath](/dotnet/api/system.runtime.compilerservices.callerfilepathattribute)|Chemin d’accès complet du fichier source qui contient l’appelant. C’est le chemin d’accès au moment de la compilation.|`String`
|[CallerLineNumber](/dotnet/api/system.runtime.compilerservices.callerlinenumberattribute)|Numéro de ligne dans le fichier source dans lequel la méthode est appelée.|`Integer`|
|[CallerMemberName](/dotnet/api/system.runtime.compilerservices.callermembernameattribute)|Méthode ou nom de la propriété de l'appelant. Consultez la section des noms de membres plus loin dans cette rubrique.|`String`|

## <a name="example"></a>Exemple

L’exemple suivant montre comment vous pouvez utiliser ces attributs pour effectuer le suivi d’un appelant.

```fsharp
open System.Diagnostics
open System.Runtime.CompilerServices

type Tracer() =
    member __.DoTrace(msg: string,
                      [<CallerMemberName>] ?memberName: string,
                      [<CallerFilePath>] ?path: string
                      [<CallerLineNumber>] ?line: int) =
        Trace.WriteLine(sprintf "Message: %s" message)
        match (memberName, path, line) with
        | Some m, Some p, Some l ->
            Trace.WriteLine(sprintf "Member name: %s" m)
            Trace.WriteLine(sprintf "Source file path: %s" p)
            Trace.WriteLine(sprintf "Source line number: %d" l)
        | _,_,_ -> ()
```

## <a name="remarks"></a>Notes

Attributs d’informations de l’appelant peuvent uniquement être appliqués aux paramètres facultatifs. Vous devez fournir une valeur explicite pour chaque paramètre facultatif. Les attributs d’informations d’appelant contraindre le compilateur à écrire la valeur appropriée pour chaque paramètre facultatif décoré avec un attribut d’informations de l’appelant.

Les valeurs d'informations de l'appelant sont émises en tant que littéraux en langage intermédiaire (IL) au moment de la compilation. Contrairement aux résultats de la [StackTrace](/dotnet/api/system.diagnostics.stacktrace) propriété pour les exceptions, les résultats ne sont pas affectés par l’obfuscation.

Vous pouvez fournir explicitement les arguments facultatifs pour contrôler ou masquer des informations de l'appelant.

## <a name="member-names"></a>Noms de membres

Vous pouvez utiliser la [ `CallerMemberName` ](/dotnet/api/system.runtime.compilerservices.callermembernameattribute) attribut pour éviter de spécifier le nom du membre en tant qu’un `String` argument à la méthode appelée. À l’aide de cette technique, vous évitez le problème qui ne change pas la refactorisation renommer le `String` valeurs. Cet avantage est particulièrement utile pour les tâches suivantes :

* Utilisation du traçage et des programmes de diagnostic.
* Implémentation de la [INotifyPropertyChanged](/dotnet/api/system.componentmodel.inotifypropertychanged) interface lors de la liaison de données. Cette interface permet à la propriété d'un objet de signaler à un contrôle dépendant que la propriété a été modifiée, afin que ce contrôle puisse afficher les informations mises à jour. Sans le [ `CallerMemberName` ](/dotnet/api/system.runtime.compilerservices.callermembernameattribute) attribut, vous devez spécifier le nom de propriété comme un littéral.

Le graphique suivant montre le membre de noms qui sont retournés lorsque vous utilisez l’attribut CallerMemberName.

|Les appels se produisent à l'intérieur|Résultat de nom de membre|
|-------------------|------------------|
|Méthode, propriété ou événement|Le nom de la méthode, la propriété ou l'événement dont l'appel est originaire.|
|Constructeur|La chaîne « .ctor »|
|Constructeur statique|La chaîne « .cctor »|
|Destructeur|La chaîne « finalize »|
|Opérateurs définis par l'utilisateur ou conversions|Le nom généré pour le membre, par exemple, « op_Addition ».|
|Constructeur d'attribut|Le nom du membre auquel l'attribut est appliqué. Si l'attribut est un élément dans un membre (tel qu'un paramètre, une valeur de retour, ou un paramètre de type générique), le résultat est le nom du membre qui est associé à cet élément.|
|Aucun membre contenant (par exemple, niveau assembly ou attributs qui sont appliqués aux types)|Valeur par défaut du paramètre optionnel.|

## <a name="see-also"></a>Voir aussi

- [Attributs](attributes.md)  
- [Arguments nommés](parameters-and-arguments.md#named-arguments)  
- [Paramètres facultatifs](parameters-and-arguments.md#optional-parameters)  
