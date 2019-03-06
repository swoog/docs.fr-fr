---
title: Icorprofilerinfo6::enumngenmodulemethodsinliningthismethod, méthode
ms.date: 03/30/2017
ms.assetid: b933dfe6-7833-40cb-aad8-40842dc3034f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 67ae413ae8944757fc90bcde752b9a5fe53cc68f
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57365319"
---
# <a name="icorprofilerinfo6enumngenmodulemethodsinliningthismethod-method"></a>Icorprofilerinfo6::enumngenmodulemethodsinliningthismethod, méthode

Retourne un énumérateur pour toutes les méthodes qui sont définis dans un module NGen donné et un inline une méthode donnée.

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT EnumNgenModuleMethodsInliningThisMethod(
        [in] ModuleID inlinersModuleId,
        [in] ModuleID inlineeModuleId,
        [in] mdMethodDef inlineeMethodId,
        [out] BOOL *incompleteData,
        [out] ICorProfilerMethodEnum** ppEnum
);
```

## <a name="parameters"></a>Paramètres

`inlinersModuleId`\
[in] L’identificateur d’un module NGen.

`inlineeModuleId`\
[in] L’identificateur d’un module qui définit `inlineeMethodId`. Pour plus d'informations, consultez la section Notes.

`inlineeMethodId`\
[in] L’identificateur d’une méthode inline. Pour plus d'informations, consultez la section Notes.

`incompleteData`\
[out] Un indicateur qui indique si `ppEnum` contient toutes les méthodes d’incorporation (inlining) une méthode donnée.  Pour plus d'informations, consultez la section Notes.

`ppEnum`\
[out] Un pointeur vers l’adresse d’un énumérateur

## <a name="remarks"></a>Notes

`inlineeModuleId` et `inlineeMethodId` forment l’identificateur complet de la méthode qui peut être inline. Par exemple, supposons que le module `A` définit une méthode `Simple.Add`:

```csharp
Simple.Add(int a, int b)
{ return a + b; }
```

et le module B définit `Fancy.AddTwice`:

```csharp
Fancy.AddTwice(int a, int b)
{ return Simple.Add(a,b) + Simple.Add(a,b); }
```

Supposons également que `Fancy.AddTwice` inlines l’appel à `SimpleAdd`. Un profileur peut utiliser cet énumérateur pour rechercher toutes les méthodes définies dans le module B qui inline `Simple.Add`, et le résultat serait énumérer `AddTwice`.  `inlineeModuleId` est l’identificateur de module `A`, et `inlineeMethodId` est l’identificateur de `Simple.Add(int a, int b)`.

Si `incompleteData` a la valeur true après la fonction est retournée, l’énumérateur ne contient pas toutes les méthodes d’incorporation (inlining) une méthode donnée. Cela peut se produire lorsque l’une ou des dépendances plus directes ou indirectes du module de personnes n’ont pas encore été chargés. Si un profileur doit obtenir les données précises, il doit réessayer plus tard lorsque plusieurs modules sont chargés, de préférence à chaque chargement de module.

Le `EnumNgenModuleMethodsInliningThisMethod` méthode peut être utilisée pour contourner les limitations sur incorporation (inlining) pour ReJIT. ReJIT permet un profileur de modifier l’implémentation d’une méthode et puis créez un nouveau code pour celui-ci à la volée. Par exemple, nous pourrions modifier `Simple.Add` comme suit :

```csharp
Simple.Add(int a, int b)
{ return 42; }
```

Toutefois, car `Fancy.AddTwice` a déjà inline `Simple.Add`, il continue à avoir le même comportement qu’avant. Pour contourner cette limitation, l’appelant doit rechercher toutes les méthodes dans tous les modules en ligne `Simple.Add` et utiliser `ICorProfilerInfo5::RequestRejit` sur chacune de ces méthodes. Lorsque les méthodes sont recompilés, ils ont le nouveau comportement `Simple.Add` au lieu de l’ancien comportement.

## <a name="requirements"></a>Spécifications

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).

**En-tête :** CorProf.idl, CorProf.h

**Bibliothèque :** CorGuids.lib

**Versions du .NET Framework :** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]

## <a name="see-also"></a>Voir aussi

- [ICorProfilerInfo6, interface](icorprofilerinfo6-interface.md)