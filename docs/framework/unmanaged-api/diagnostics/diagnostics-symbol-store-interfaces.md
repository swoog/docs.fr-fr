---
title: Interfaces du magasin de symboles de diagnostics
ms.date: 03/30/2017
helpviewer_keywords:
- unmanaged interfaces [.NET Framework], debugging
- diagnostics symbol store interfaces [.NET Framework]
- interfaces [.NET Framework], diagnostics symbol store
- unmanaged interfaces [.NET Framework], diagnostics symbol store
- debugging interfaces [.NET Framework]
- interfaces [.NET Framework debugging]
ms.assetid: f96987d5-e6a5-478b-ac5e-302e16545cce
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6fca7359888b8b73b2e1cf709ab708d71abf0db6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33435810"
---
# <a name="diagnostics-symbol-store-interfaces"></a><span data-ttu-id="dd261-102">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="dd261-102">Diagnostics Symbol Store Interfaces</span></span>
<span data-ttu-id="dd261-103">Cette rubrique décrit les interfaces non managées qui permettent un compilateur à générer des informations de symbole pour une utilisation par un débogueur.</span><span class="sxs-lookup"><span data-stu-id="dd261-103">This topic describes the unmanaged interfaces that enable a compiler to generate symbol information for use by a debugger.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="dd261-104">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="dd261-104">In This Section</span></span>  
 [<span data-ttu-id="dd261-105">IBindingDisplay, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-105">IBindingDisplay Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/ibindingdisplay-interface.md)  
 <span data-ttu-id="dd261-106">Fournit des méthodes qui affichent des informations de liaison en cours sur l’application en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="dd261-106">Provides methods that display current binding information about the running application.</span></span>  
  
 [<span data-ttu-id="dd261-107">IDebugAutoAttach, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-107">IDebugAutoAttach Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/idebugautoattach-interface.md)  
 <span data-ttu-id="dd261-108">Définit l’interface pour l’attachement automatique du débogueur appelé par serveur.</span><span class="sxs-lookup"><span data-stu-id="dd261-108">Defines the interface for a server-invoked debugger auto attach.</span></span>  
  
 [<span data-ttu-id="dd261-109">INotifyConnection2, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-109">INotifyConnection2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifyconnection2-interface.md)  
 <span data-ttu-id="dd261-110">Déclare des méthodes pour l’inscription et la désinscription d’une source de notification de connexion.</span><span class="sxs-lookup"><span data-stu-id="dd261-110">Declares methods for registering and unregistering a connection notification source.</span></span>  
  
 [<span data-ttu-id="dd261-111">INotifySink2, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-111">INotifySink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md)  
 <span data-ttu-id="dd261-112">Déclare des méthodes pour la notification de récepteur.</span><span class="sxs-lookup"><span data-stu-id="dd261-112">Declares methods for sink notification.</span></span>  
  
 [<span data-ttu-id="dd261-113">INotifySource2, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-113">INotifySource2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-interface.md)  
 <span data-ttu-id="dd261-114">Déclare une méthode pour définir des filtres de notification.</span><span class="sxs-lookup"><span data-stu-id="dd261-114">Declares a method for setting notification filters.</span></span>  
  
 [<span data-ttu-id="dd261-115">ISymENCUnmanagedMethod, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-115">ISymENCUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymencunmanagedmethod-interface.md)  
 <span data-ttu-id="dd261-116">Fournit des informations pour la fonctionnalité Modifier & Continuer.</span><span class="sxs-lookup"><span data-stu-id="dd261-116">Provides information for the Edit and Continue feature.</span></span>  
  
 [<span data-ttu-id="dd261-117">ISymUnmanagedAsyncMethod, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-117">ISymUnmanagedAsyncMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-interface.md)  
 <span data-ttu-id="dd261-118">Cette interface est le complément de la lecture à [isymunmanagedasyncmethodpropertieswriter, Interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md).</span><span class="sxs-lookup"><span data-stu-id="dd261-118">This interface is the reading complement to [ISymUnmanagedAsyncMethodPropertiesWriter Interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md).</span></span>  
  
 [<span data-ttu-id="dd261-119">ISymUnmanagedAsyncMethodPropertiesWriter, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-119">ISymUnmanagedAsyncMethodPropertiesWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md)  
 <span data-ttu-id="dd261-120">Permet la définition d’informations sur la méthode async facultatif par le symbole de méthode.</span><span class="sxs-lookup"><span data-stu-id="dd261-120">Allows definition of optional async method information per method symbol.</span></span> <span data-ttu-id="dd261-121">Doit utiliser avec une méthode ouverte (autrement dit, entre les appels à la [OpenMethod (méthode)](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openmethod-method.md)et le [CloseMethod, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-closemethod-method.md)).</span><span class="sxs-lookup"><span data-stu-id="dd261-121">Must use with an opened method (that is, between calls to the [OpenMethod Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openmethod-method.md)and the [CloseMethod Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-closemethod-method.md)).</span></span>  
  
 [<span data-ttu-id="dd261-122">ISymUnmanagedBinder, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-122">ISymUnmanagedBinder Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-interface.md)  
 <span data-ttu-id="dd261-123">Représente un classeur de symboles pour le code non managé.</span><span class="sxs-lookup"><span data-stu-id="dd261-123">Represents a symbol binder for unmanaged code.</span></span>  
  
 [<span data-ttu-id="dd261-124">ISymUnmanagedBinder2, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-124">ISymUnmanagedBinder2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder2-interface.md)  
 <span data-ttu-id="dd261-125">Représente un classeur de symboles pour le code non managé et étend la `ISymUnmanagedBinder` interface.</span><span class="sxs-lookup"><span data-stu-id="dd261-125">Represents a symbol binder for unmanaged code, and extends the `ISymUnmanagedBinder` interface.</span></span>  
  
 [<span data-ttu-id="dd261-126">ISymUnmanagedBinder3, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-126">ISymUnmanagedBinder3 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder3-interface.md)  
 <span data-ttu-id="dd261-127">Représente un classeur de symboles pour le code non managé et étend la `ISymUnmanagedBinder` interface.</span><span class="sxs-lookup"><span data-stu-id="dd261-127">Represents a symbol binder for unmanaged code, and extends the `ISymUnmanagedBinder` interface.</span></span>  
  
 [<span data-ttu-id="dd261-128">ISymUnmanagedConstant, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-128">ISymUnmanagedConstant Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-interface.md)  
 <span data-ttu-id="dd261-129">Fournit l’accès aux constantes non managées.</span><span class="sxs-lookup"><span data-stu-id="dd261-129">Provides access to unmanaged constants.</span></span>  
  
 [<span data-ttu-id="dd261-130">ISymUnmanagedDispose, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-130">ISymUnmanagedDispose Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddispose-interface.md)  
 <span data-ttu-id="dd261-131">Libère les ressources non managées.</span><span class="sxs-lookup"><span data-stu-id="dd261-131">Disposes of unmanaged resources.</span></span>  
  
 [<span data-ttu-id="dd261-132">ISymUnmanagedDocument, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-132">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)  
 <span data-ttu-id="dd261-133">Représente un document référencé par un magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="dd261-133">Represents a document referenced by a symbol store.</span></span>  
  
 [<span data-ttu-id="dd261-134">ISymUnmanagedDocumentWriter, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-134">ISymUnmanagedDocumentWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocumentwriter-interface.md)  
 <span data-ttu-id="dd261-135">Fournit des méthodes d'écriture dans un document référencé par un magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="dd261-135">Provides methods for writing to a document referenced by a symbol store.</span></span>  
  
 [<span data-ttu-id="dd261-136">ISymUnmanagedENCUpdate, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-136">ISymUnmanagedENCUpdate Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-interface.md)  
 <span data-ttu-id="dd261-137">Fournit des méthodes pour la fonctionnalité Modifier & Continuer.</span><span class="sxs-lookup"><span data-stu-id="dd261-137">Provides methods for the Edit and Continue feature.</span></span>  
  
 [<span data-ttu-id="dd261-138">ISymUnmanagedMethod, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-138">ISymUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md)  
 <span data-ttu-id="dd261-139">Représente une méthode dans le magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="dd261-139">Represents a method within the symbol store.</span></span>  
  
 [<span data-ttu-id="dd261-140">ISymUnmanagedNamespace, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-140">ISymUnmanagedNamespace Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagednamespace-interface.md)  
 <span data-ttu-id="dd261-141">Représente un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="dd261-141">Represents a namespace.</span></span>  
  
 [<span data-ttu-id="dd261-142">ISymUnmanagedReader, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-142">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)  
 <span data-ttu-id="dd261-143">Représente un lecteur de symboles qui fournit l’accès aux documents, des méthodes et des variables dans un magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="dd261-143">Represents a symbol reader that provides access to documents, methods, and variables within a symbol store.</span></span>  
  
 [<span data-ttu-id="dd261-144">ISymUnmanagedReader2, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-144">ISymUnmanagedReader2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader2-interface.md)  
 <span data-ttu-id="dd261-145">Obtient une méthode de lecteur de symboles étant donnée un jeton de méthode et un numéro de version de la modifier et copier.</span><span class="sxs-lookup"><span data-stu-id="dd261-145">Gets a symbol reader method given a method token and an edit-and-copy version number.</span></span>  
  
 [<span data-ttu-id="dd261-146">ISymUnmanagedReaderSymbolSearchInfo, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-146">ISymUnmanagedReaderSymbolSearchInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreadersymbolsearchinfo-interface.md)  
 <span data-ttu-id="dd261-147">Fournit des méthodes qui obtiennent des informations de la recherche de symbole.</span><span class="sxs-lookup"><span data-stu-id="dd261-147">Provides methods that get symbol search information.</span></span>  
  
 [<span data-ttu-id="dd261-148">ISymUnmanagedScope, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-148">ISymUnmanagedScope Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md)  
 <span data-ttu-id="dd261-149">Représente une portée lexicale dans une méthode.</span><span class="sxs-lookup"><span data-stu-id="dd261-149">Represents a lexical scope within a method.</span></span>  
  
 [<span data-ttu-id="dd261-150">ISymUnmanagedScope2, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-150">ISymUnmanagedScope2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope2-interface.md)  
 <span data-ttu-id="dd261-151">Représente une portée lexicale dans une méthode et étend la `ISymUnmanagedScope` interface avec des méthodes qui obtiennent des informations sur les constantes définies dans l’étendue...</span><span class="sxs-lookup"><span data-stu-id="dd261-151">Represents a lexical scope within a method, and extends the `ISymUnmanagedScope` interface with methods that get information about constants defined within the scope..</span></span>  
  
 [<span data-ttu-id="dd261-152">ISymUnmanagedSourceServerModule, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-152">ISymUnmanagedSourceServerModule Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsourceservermodule-interface.md)  
 <span data-ttu-id="dd261-153">Fournit des données du serveur source pour un module.</span><span class="sxs-lookup"><span data-stu-id="dd261-153">Provides source server data for a module.</span></span>  
  
 [<span data-ttu-id="dd261-154">ISymUnmanagedSymbolSearchInfo, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-154">ISymUnmanagedSymbolSearchInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-interface.md)  
 <span data-ttu-id="dd261-155">Fournit des méthodes qui obtiennent des informations sur le chemin de recherche.</span><span class="sxs-lookup"><span data-stu-id="dd261-155">Provides methods that get information about the search path.</span></span>  
  
 [<span data-ttu-id="dd261-156">ISymUnmanagedVariable, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-156">ISymUnmanagedVariable Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)  
 <span data-ttu-id="dd261-157">Représente une variable, comme un paramètre, une variable locale ou un champ.</span><span class="sxs-lookup"><span data-stu-id="dd261-157">Represents a variable, such as a parameter, a local variable, or a field.</span></span>  
  
 [<span data-ttu-id="dd261-158">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-158">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)  
 <span data-ttu-id="dd261-159">Représente un writer de symbole et fournit des méthodes pour définir des documents, les points de séquence, les portées lexicales et variables.</span><span class="sxs-lookup"><span data-stu-id="dd261-159">Represents a symbol writer, and provides methods to define documents, sequence points, lexical scopes, and variables.</span></span>  
  
 [<span data-ttu-id="dd261-160">ISymUnmanagedWriter2, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-160">ISymUnmanagedWriter2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-interface.md)  
 <span data-ttu-id="dd261-161">Représente un writer de symbole et fournit des méthodes pour définir des documents, les points de séquence, les portées lexicales et variables.</span><span class="sxs-lookup"><span data-stu-id="dd261-161">Represents a symbol writer, and provides methods to define documents, sequence points, lexical scopes, and variables.</span></span> <span data-ttu-id="dd261-162">Étend la `ISymUnmanagedWriter` interface.</span><span class="sxs-lookup"><span data-stu-id="dd261-162">Extends the `ISymUnmanagedWriter` interface.</span></span>  
  
 [<span data-ttu-id="dd261-163">ISymUnmanagedWriter3, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-163">ISymUnmanagedWriter3 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter3-interface.md)  
 <span data-ttu-id="dd261-164">Représente un writer de symbole et fournit des méthodes pour définir des documents, les points de séquence, les portées lexicales et variables.</span><span class="sxs-lookup"><span data-stu-id="dd261-164">Represents a symbol writer, and provides methods to define documents, sequence points, lexical scopes, and variables.</span></span> <span data-ttu-id="dd261-165">Étend la `ISymUnmanagedWriter` interface.</span><span class="sxs-lookup"><span data-stu-id="dd261-165">Extends the `ISymUnmanagedWriter` interface.</span></span>  
  
 [<span data-ttu-id="dd261-166">ISymUnmanagedWriter4, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-166">ISymUnmanagedWriter4 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter4-interface.md)  
 <span data-ttu-id="dd261-167">Isymunmanagedwriter4, interface.</span><span class="sxs-lookup"><span data-stu-id="dd261-167">ISymUnmanagedWriter4 interface.</span></span>  
  
 [<span data-ttu-id="dd261-168">ISymUnmanagedWriter5, interface</span><span class="sxs-lookup"><span data-stu-id="dd261-168">ISymUnmanagedWriter5 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-interface.md)  
 <span data-ttu-id="dd261-169">Isymunmanagedwriter5, interface.</span><span class="sxs-lookup"><span data-stu-id="dd261-169">ISymUnmanagedWriter5 interface.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="dd261-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dd261-170">Related Sections</span></span>  
 [<span data-ttu-id="dd261-171">Énumérations du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="dd261-171">Diagnostics Symbol Store Enumerations</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-enumerations.md)  
  
 [<span data-ttu-id="dd261-172">Structures du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="dd261-172">Diagnostics Symbol Store Structures</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-structures.md)  
  
 [<span data-ttu-id="dd261-173">Débogage</span><span class="sxs-lookup"><span data-stu-id="dd261-173">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
