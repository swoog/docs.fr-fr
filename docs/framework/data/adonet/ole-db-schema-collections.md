---
title: Collections de schémas OLE DB
ms.date: 03/30/2017
ms.assetid: 6380c36b-658e-4d67-91e8-7131ef4a7c2c
ms.openlocfilehash: 6c3441e86d4c5267418cf8002ba17d539c464d5c
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64645899"
---
# <a name="ole-db-schema-collections"></a><span data-ttu-id="dfa9b-102">Collections de schémas OLE DB</span><span class="sxs-lookup"><span data-stu-id="dfa9b-102">OLE DB Schema Collections</span></span>
<span data-ttu-id="dfa9b-103">Cette section traite de la prise en charge des collections de schémas pour les fournisseurs OLE DB de Microsoft SQL Server, Oracle et Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="dfa9b-103">This section discusses schema collection support for the OLE DB providers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-ole-db-provider"></a><span data-ttu-id="dfa9b-104">Fournisseur Microsoft SQL Server OLE DB</span><span class="sxs-lookup"><span data-stu-id="dfa9b-104">Microsoft SQL Server OLE DB Provider</span></span>  
 <span data-ttu-id="dfa9b-105">Le pilote OLE DB Microsoft SQL Server prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="dfa9b-105">The Microsoft SQL Server OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
- <span data-ttu-id="dfa9b-106">Tables</span><span class="sxs-lookup"><span data-stu-id="dfa9b-106">Tables</span></span>  
  
- <span data-ttu-id="dfa9b-107">Colonnes</span><span class="sxs-lookup"><span data-stu-id="dfa9b-107">Columns</span></span>  
  
- <span data-ttu-id="dfa9b-108">Procédures</span><span class="sxs-lookup"><span data-stu-id="dfa9b-108">Procedures</span></span>  
  
- <span data-ttu-id="dfa9b-109">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="dfa9b-109">ProcedureParameters</span></span>  
  
- <span data-ttu-id="dfa9b-110">Catalogue</span><span class="sxs-lookup"><span data-stu-id="dfa9b-110">Catalog</span></span>  
  
- <span data-ttu-id="dfa9b-111">Index</span><span class="sxs-lookup"><span data-stu-id="dfa9b-111">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="dfa9b-112">Tables</span><span class="sxs-lookup"><span data-stu-id="dfa9b-112">Tables</span></span>  
  
|<span data-ttu-id="dfa9b-113">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-113">ColumnName</span></span>|<span data-ttu-id="dfa9b-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="dfa9b-114">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dfa9b-115">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-115">TABLE_CATALOG</span></span>|<span data-ttu-id="dfa9b-116">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-116">String</span></span>|  
|<span data-ttu-id="dfa9b-117">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-117">TABLE_SCHEMA</span></span>|<span data-ttu-id="dfa9b-118">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-118">String</span></span>|  
|<span data-ttu-id="dfa9b-119">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-119">TABLE_NAME</span></span>|<span data-ttu-id="dfa9b-120">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-120">String</span></span>|  
|<span data-ttu-id="dfa9b-121">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-121">TABLE_TYPE</span></span>|<span data-ttu-id="dfa9b-122">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-122">String</span></span>|  
|<span data-ttu-id="dfa9b-123">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-123">TABLE_GUID</span></span>|<span data-ttu-id="dfa9b-124">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-124">Guid</span></span>|  
|<span data-ttu-id="dfa9b-125">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-125">DESCRIPTION</span></span>|<span data-ttu-id="dfa9b-126">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-126">String</span></span>|  
|<span data-ttu-id="dfa9b-127">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-127">TABLE_PROPID</span></span>|<span data-ttu-id="dfa9b-128">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-128">Int64</span></span>|  
|<span data-ttu-id="dfa9b-129">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="dfa9b-129">DATE_CREATED</span></span>|<span data-ttu-id="dfa9b-130">DateTime</span><span class="sxs-lookup"><span data-stu-id="dfa9b-130">DateTime</span></span>|  
|<span data-ttu-id="dfa9b-131">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="dfa9b-131">DATE_MODIFIED</span></span>|<span data-ttu-id="dfa9b-132">DateTime</span><span class="sxs-lookup"><span data-stu-id="dfa9b-132">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="dfa9b-133">Colonnes</span><span class="sxs-lookup"><span data-stu-id="dfa9b-133">Columns</span></span>  
  
|<span data-ttu-id="dfa9b-134">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-134">ColumnName</span></span>|<span data-ttu-id="dfa9b-135">Type de données</span><span class="sxs-lookup"><span data-stu-id="dfa9b-135">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dfa9b-136">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-136">TABLE_CATALOG</span></span>|<span data-ttu-id="dfa9b-137">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-137">String</span></span>|  
|<span data-ttu-id="dfa9b-138">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-138">TABLE_SCHEMA</span></span>|<span data-ttu-id="dfa9b-139">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-139">String</span></span>|  
|<span data-ttu-id="dfa9b-140">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-140">TABLE_NAME</span></span>|<span data-ttu-id="dfa9b-141">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-141">String</span></span>|  
|<span data-ttu-id="dfa9b-142">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-142">COLUMN_NAME</span></span>|<span data-ttu-id="dfa9b-143">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-143">String</span></span>|  
|<span data-ttu-id="dfa9b-144">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-144">COLUMN_GUID</span></span>|<span data-ttu-id="dfa9b-145">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-145">Guid</span></span>|  
|<span data-ttu-id="dfa9b-146">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-146">COLUMN_PROPID</span></span>|<span data-ttu-id="dfa9b-147">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-147">Int64</span></span>|  
|<span data-ttu-id="dfa9b-148">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-148">ORDINAL_POSITION</span></span>|<span data-ttu-id="dfa9b-149">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-149">Int64</span></span>|  
|<span data-ttu-id="dfa9b-150">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="dfa9b-150">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="dfa9b-151">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-151">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-152">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="dfa9b-152">COLUMN_DEFAULT</span></span>|<span data-ttu-id="dfa9b-153">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-153">String</span></span>|  
|<span data-ttu-id="dfa9b-154">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="dfa9b-154">COLUMN_FLAGS</span></span>|<span data-ttu-id="dfa9b-155">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-155">Int64</span></span>|  
|<span data-ttu-id="dfa9b-156">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-156">IS_NULLABLE</span></span>|<span data-ttu-id="dfa9b-157">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-157">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-158">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-158">DATA_TYPE</span></span>|<span data-ttu-id="dfa9b-159">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-159">Int32</span></span>|  
|<span data-ttu-id="dfa9b-160">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-160">TYPE_GUID</span></span>|<span data-ttu-id="dfa9b-161">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-161">Guid</span></span>|  
|<span data-ttu-id="dfa9b-162">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="dfa9b-162">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="dfa9b-163">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-163">Int64</span></span>|  
|<span data-ttu-id="dfa9b-164">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="dfa9b-164">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="dfa9b-165">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-165">Int64</span></span>|  
|<span data-ttu-id="dfa9b-166">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-166">NUMERIC_PRECISION</span></span>|<span data-ttu-id="dfa9b-167">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-167">Int32</span></span>|  
|<span data-ttu-id="dfa9b-168">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-168">NUMERIC_SCALE</span></span>|<span data-ttu-id="dfa9b-169">Int16</span><span class="sxs-lookup"><span data-stu-id="dfa9b-169">Int16</span></span>|  
|<span data-ttu-id="dfa9b-170">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-170">DATETIME_PRECISION</span></span>|<span data-ttu-id="dfa9b-171">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-171">Int64</span></span>|  
|<span data-ttu-id="dfa9b-172">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-172">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="dfa9b-173">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-173">String</span></span>|  
|<span data-ttu-id="dfa9b-174">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-174">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="dfa9b-175">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-175">String</span></span>|  
|<span data-ttu-id="dfa9b-176">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-176">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="dfa9b-177">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-177">String</span></span>|  
|<span data-ttu-id="dfa9b-178">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-178">COLLATION_CATALOG</span></span>|<span data-ttu-id="dfa9b-179">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-179">String</span></span>|  
|<span data-ttu-id="dfa9b-180">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-180">COLLATION_SCHEMA</span></span>|<span data-ttu-id="dfa9b-181">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-181">String</span></span>|  
|<span data-ttu-id="dfa9b-182">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-182">COLLATION_NAME</span></span>|<span data-ttu-id="dfa9b-183">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-183">String</span></span>|  
|<span data-ttu-id="dfa9b-184">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-184">DOMAIN_CATALOG</span></span>|<span data-ttu-id="dfa9b-185">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-185">String</span></span>|  
|<span data-ttu-id="dfa9b-186">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-186">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="dfa9b-187">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-187">String</span></span>|  
|<span data-ttu-id="dfa9b-188">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-188">DOMAIN_NAME</span></span>|<span data-ttu-id="dfa9b-189">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-189">String</span></span>|  
|<span data-ttu-id="dfa9b-190">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-190">DESCRIPTION</span></span>|<span data-ttu-id="dfa9b-191">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-191">String</span></span>|  
|<span data-ttu-id="dfa9b-192">COLUMN_LCID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-192">COLUMN_LCID</span></span>|<span data-ttu-id="dfa9b-193">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-193">Int32</span></span>|  
|<span data-ttu-id="dfa9b-194">COLUMN_COMPFLAGS</span><span class="sxs-lookup"><span data-stu-id="dfa9b-194">COLUMN_COMPFLAGS</span></span>|<span data-ttu-id="dfa9b-195">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-195">Int32</span></span>|  
|<span data-ttu-id="dfa9b-196">COLUMN_SORTID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-196">COLUMN_SORTID</span></span>|<span data-ttu-id="dfa9b-197">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-197">Int32</span></span>|  
|<span data-ttu-id="dfa9b-198">COLUMN_TDSCOLLATION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-198">COLUMN_TDSCOLLATION</span></span>|<span data-ttu-id="dfa9b-199">Byte[]</span><span class="sxs-lookup"><span data-stu-id="dfa9b-199">Byte[]</span></span>|  
|<span data-ttu-id="dfa9b-200">IS_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="dfa9b-200">IS_COMPUTED</span></span>|<span data-ttu-id="dfa9b-201">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-201">Boolean</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="dfa9b-202">Procédures</span><span class="sxs-lookup"><span data-stu-id="dfa9b-202">Procedures</span></span>  
  
|<span data-ttu-id="dfa9b-203">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-203">ColumnName</span></span>|<span data-ttu-id="dfa9b-204">Type de données</span><span class="sxs-lookup"><span data-stu-id="dfa9b-204">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dfa9b-205">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-205">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="dfa9b-206">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-206">String</span></span>|  
|<span data-ttu-id="dfa9b-207">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-207">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="dfa9b-208">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-208">String</span></span>|  
|<span data-ttu-id="dfa9b-209">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-209">PROCEDURE_NAME</span></span>|<span data-ttu-id="dfa9b-210">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-210">String</span></span>|  
|<span data-ttu-id="dfa9b-211">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-211">PROCEDURE_TYPE</span></span>|<span data-ttu-id="dfa9b-212">Int16</span><span class="sxs-lookup"><span data-stu-id="dfa9b-212">Int16</span></span>|  
|<span data-ttu-id="dfa9b-213">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-213">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="dfa9b-214">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-214">String</span></span>|  
|<span data-ttu-id="dfa9b-215">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-215">DESCRIPTION</span></span>|<span data-ttu-id="dfa9b-216">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-216">String</span></span>|  
|<span data-ttu-id="dfa9b-217">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="dfa9b-217">DATE_CREATED</span></span>|<span data-ttu-id="dfa9b-218">DateTime</span><span class="sxs-lookup"><span data-stu-id="dfa9b-218">DateTime</span></span>|  
|<span data-ttu-id="dfa9b-219">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="dfa9b-219">DATE_MODIFIED</span></span>|<span data-ttu-id="dfa9b-220">DateTime</span><span class="sxs-lookup"><span data-stu-id="dfa9b-220">DateTime</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="dfa9b-221">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="dfa9b-221">ProcedureParameters</span></span>  
  
|<span data-ttu-id="dfa9b-222">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-222">ColumnName</span></span>|<span data-ttu-id="dfa9b-223">Type de données</span><span class="sxs-lookup"><span data-stu-id="dfa9b-223">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dfa9b-224">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-224">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="dfa9b-225">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-225">String</span></span>|  
|<span data-ttu-id="dfa9b-226">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-226">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="dfa9b-227">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-227">String</span></span>|  
|<span data-ttu-id="dfa9b-228">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-228">PROCEDURE_NAME</span></span>|<span data-ttu-id="dfa9b-229">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-229">String</span></span>|  
|<span data-ttu-id="dfa9b-230">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-230">PARAMETER_NAME</span></span>|<span data-ttu-id="dfa9b-231">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-231">String</span></span>|  
|<span data-ttu-id="dfa9b-232">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-232">ORDINAL_POSITION</span></span>|<span data-ttu-id="dfa9b-233">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-233">Int32</span></span>|  
|<span data-ttu-id="dfa9b-234">PARAMETER_TYPE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-234">PARAMETER_TYPE</span></span>|<span data-ttu-id="dfa9b-235">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-235">Int32</span></span>|  
|<span data-ttu-id="dfa9b-236">PARAMETER_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="dfa9b-236">PARAMETER_HASDEFAULT</span></span>|<span data-ttu-id="dfa9b-237">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-237">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-238">PARAMETER_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="dfa9b-238">PARAMETER_DEFAULT</span></span>|<span data-ttu-id="dfa9b-239">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-239">String</span></span>|  
|<span data-ttu-id="dfa9b-240">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-240">IS_NULLABLE</span></span>|<span data-ttu-id="dfa9b-241">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-241">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-242">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-242">DATA_TYPE</span></span>|<span data-ttu-id="dfa9b-243">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-243">Int32</span></span>|  
|<span data-ttu-id="dfa9b-244">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="dfa9b-244">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="dfa9b-245">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-245">Int64</span></span>|  
|<span data-ttu-id="dfa9b-246">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="dfa9b-246">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="dfa9b-247">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-247">Int64</span></span>|  
|<span data-ttu-id="dfa9b-248">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-248">NUMERIC_PRECISION</span></span>|<span data-ttu-id="dfa9b-249">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-249">Int32</span></span>|  
|<span data-ttu-id="dfa9b-250">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-250">NUMERIC_SCALE</span></span>|<span data-ttu-id="dfa9b-251">Int16</span><span class="sxs-lookup"><span data-stu-id="dfa9b-251">Int16</span></span>|  
|<span data-ttu-id="dfa9b-252">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-252">DESCRIPTION</span></span>|<span data-ttu-id="dfa9b-253">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-253">String</span></span>|  
|<span data-ttu-id="dfa9b-254">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-254">TYPE_NAME</span></span>|<span data-ttu-id="dfa9b-255">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-255">String</span></span>|  
|<span data-ttu-id="dfa9b-256">LOCAL_TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-256">LOCAL_TYPE_NAME</span></span>|<span data-ttu-id="dfa9b-257">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-257">String</span></span>|  
  
### <a name="catalog"></a><span data-ttu-id="dfa9b-258">Catalogue</span><span class="sxs-lookup"><span data-stu-id="dfa9b-258">Catalog</span></span>  
  
|<span data-ttu-id="dfa9b-259">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-259">ColumnName</span></span>|<span data-ttu-id="dfa9b-260">Type de données</span><span class="sxs-lookup"><span data-stu-id="dfa9b-260">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dfa9b-261">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-261">CATALOG_NAME</span></span>|<span data-ttu-id="dfa9b-262">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-262">String</span></span>|  
|<span data-ttu-id="dfa9b-263">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-263">DESCRIPTION</span></span>|<span data-ttu-id="dfa9b-264">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-264">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="dfa9b-265">Index</span><span class="sxs-lookup"><span data-stu-id="dfa9b-265">Indexes</span></span>  
  
|<span data-ttu-id="dfa9b-266">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-266">ColumnName</span></span>|<span data-ttu-id="dfa9b-267">Type de données</span><span class="sxs-lookup"><span data-stu-id="dfa9b-267">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dfa9b-268">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-268">TABLE_CATALOG</span></span>|<span data-ttu-id="dfa9b-269">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-269">String</span></span>|  
|<span data-ttu-id="dfa9b-270">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-270">TABLE_SCHEMA</span></span>|<span data-ttu-id="dfa9b-271">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-271">String</span></span>|  
|<span data-ttu-id="dfa9b-272">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-272">TABLE_NAME</span></span>|<span data-ttu-id="dfa9b-273">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-273">String</span></span>|  
|<span data-ttu-id="dfa9b-274">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-274">INDEX_CATALOG</span></span>|<span data-ttu-id="dfa9b-275">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-275">String</span></span>|  
|<span data-ttu-id="dfa9b-276">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-276">INDEX_SCHEMA</span></span>|<span data-ttu-id="dfa9b-277">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-277">String</span></span>|  
|<span data-ttu-id="dfa9b-278">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-278">INDEX_NAME</span></span>|<span data-ttu-id="dfa9b-279">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-279">String</span></span>|  
|<span data-ttu-id="dfa9b-280">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="dfa9b-280">PRIMARY_KEY</span></span>|<span data-ttu-id="dfa9b-281">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-281">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-282">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-282">UNIQUE</span></span>|<span data-ttu-id="dfa9b-283">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-283">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-284">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="dfa9b-284">CLUSTERED</span></span>|<span data-ttu-id="dfa9b-285">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-285">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-286">TYPE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-286">TYPE</span></span>|<span data-ttu-id="dfa9b-287">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-287">Int32</span></span>|  
|<span data-ttu-id="dfa9b-288">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="dfa9b-288">FILL_FACTOR</span></span>|<span data-ttu-id="dfa9b-289">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-289">Int32</span></span>|  
|<span data-ttu-id="dfa9b-290">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-290">INITIAL_SIZE</span></span>|<span data-ttu-id="dfa9b-291">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-291">Int32</span></span>|  
|<span data-ttu-id="dfa9b-292">NULLS</span><span class="sxs-lookup"><span data-stu-id="dfa9b-292">NULLS</span></span>|<span data-ttu-id="dfa9b-293">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-293">Int32</span></span>|  
|<span data-ttu-id="dfa9b-294">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="dfa9b-294">SORT_BOOKMARKS</span></span>|<span data-ttu-id="dfa9b-295">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-295">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-296">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-296">AUTO_UPDATE</span></span>|<span data-ttu-id="dfa9b-297">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-297">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-298">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-298">NULL_COLLATION</span></span>|<span data-ttu-id="dfa9b-299">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-299">Int32</span></span>|  
|<span data-ttu-id="dfa9b-300">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-300">ORDINAL_POSITION</span></span>|<span data-ttu-id="dfa9b-301">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-301">Int64</span></span>|  
|<span data-ttu-id="dfa9b-302">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-302">COLUMN_NAME</span></span>|<span data-ttu-id="dfa9b-303">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-303">String</span></span>|  
|<span data-ttu-id="dfa9b-304">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-304">COLUMN_GUID</span></span>|<span data-ttu-id="dfa9b-305">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-305">Guid</span></span>|  
|<span data-ttu-id="dfa9b-306">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-306">COLUMN_PROPID</span></span>|<span data-ttu-id="dfa9b-307">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-307">Int64</span></span>|  
|<span data-ttu-id="dfa9b-308">COLLATION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-308">COLLATION</span></span>|<span data-ttu-id="dfa9b-309">Int16</span><span class="sxs-lookup"><span data-stu-id="dfa9b-309">Int16</span></span>|  
|<span data-ttu-id="dfa9b-310">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="dfa9b-310">CARDINALITY</span></span>|<span data-ttu-id="dfa9b-311">Decimal</span><span class="sxs-lookup"><span data-stu-id="dfa9b-311">Decimal</span></span>|  
|<span data-ttu-id="dfa9b-312">PAGES</span><span class="sxs-lookup"><span data-stu-id="dfa9b-312">PAGES</span></span>|<span data-ttu-id="dfa9b-313">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-313">Int32</span></span>|  
|<span data-ttu-id="dfa9b-314">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-314">FILTER_CONDITION</span></span>|<span data-ttu-id="dfa9b-315">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-315">String</span></span>|  
|<span data-ttu-id="dfa9b-316">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="dfa9b-316">INTEGRATED</span></span>|<span data-ttu-id="dfa9b-317">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-317">Boolean</span></span>|  
  
## <a name="microsoft-oracle-ole-db-provider"></a><span data-ttu-id="dfa9b-318">Fournisseur Microsoft Oracle OLE DB</span><span class="sxs-lookup"><span data-stu-id="dfa9b-318">Microsoft Oracle OLE DB Provider</span></span>  
 <span data-ttu-id="dfa9b-319">Le pilote Microsoft Oracle OLE DB prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="dfa9b-319">The Microsoft Oracle OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
- <span data-ttu-id="dfa9b-320">Tables</span><span class="sxs-lookup"><span data-stu-id="dfa9b-320">Tables</span></span>  
  
- <span data-ttu-id="dfa9b-321">Colonnes</span><span class="sxs-lookup"><span data-stu-id="dfa9b-321">Columns</span></span>  
  
- <span data-ttu-id="dfa9b-322">Procédures</span><span class="sxs-lookup"><span data-stu-id="dfa9b-322">Procedures</span></span>  
  
- <span data-ttu-id="dfa9b-323">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="dfa9b-323">ProcedureColumns</span></span>  
  
- <span data-ttu-id="dfa9b-324">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="dfa9b-324">ProcedureParameters</span></span>  
  
- <span data-ttu-id="dfa9b-325">Affichages</span><span class="sxs-lookup"><span data-stu-id="dfa9b-325">Views</span></span>  
  
- <span data-ttu-id="dfa9b-326">Index</span><span class="sxs-lookup"><span data-stu-id="dfa9b-326">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="dfa9b-327">Tables</span><span class="sxs-lookup"><span data-stu-id="dfa9b-327">Tables</span></span>  
  
|<span data-ttu-id="dfa9b-328">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-328">ColumnName</span></span>|<span data-ttu-id="dfa9b-329">Type de données</span><span class="sxs-lookup"><span data-stu-id="dfa9b-329">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dfa9b-330">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-330">TABLE_CATALOG</span></span>|<span data-ttu-id="dfa9b-331">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-331">String</span></span>|  
|<span data-ttu-id="dfa9b-332">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-332">TABLE_SCHEMA</span></span>|<span data-ttu-id="dfa9b-333">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-333">String</span></span>|  
|<span data-ttu-id="dfa9b-334">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-334">TABLE_NAME</span></span>|<span data-ttu-id="dfa9b-335">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-335">String</span></span>|  
|<span data-ttu-id="dfa9b-336">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-336">TABLE_TYPE</span></span>|<span data-ttu-id="dfa9b-337">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-337">String</span></span>|  
|<span data-ttu-id="dfa9b-338">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-338">TABLE_GUID</span></span>|<span data-ttu-id="dfa9b-339">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-339">Guid</span></span>|  
|<span data-ttu-id="dfa9b-340">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-340">DESCRIPTION</span></span>|<span data-ttu-id="dfa9b-341">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-341">String</span></span>|  
|<span data-ttu-id="dfa9b-342">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-342">TABLE_PROPID</span></span>|<span data-ttu-id="dfa9b-343">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-343">Int64</span></span>|  
|<span data-ttu-id="dfa9b-344">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="dfa9b-344">DATE_CREATED</span></span>|<span data-ttu-id="dfa9b-345">DateTime</span><span class="sxs-lookup"><span data-stu-id="dfa9b-345">DateTime</span></span>|  
|<span data-ttu-id="dfa9b-346">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="dfa9b-346">DATE_MODIFIED</span></span>|<span data-ttu-id="dfa9b-347">DateTime</span><span class="sxs-lookup"><span data-stu-id="dfa9b-347">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="dfa9b-348">Colonnes</span><span class="sxs-lookup"><span data-stu-id="dfa9b-348">Columns</span></span>  
  
|<span data-ttu-id="dfa9b-349">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-349">ColumnName</span></span>|<span data-ttu-id="dfa9b-350">Type de données</span><span class="sxs-lookup"><span data-stu-id="dfa9b-350">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dfa9b-351">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-351">TABLE_CATALOG</span></span>|<span data-ttu-id="dfa9b-352">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-352">String</span></span>|  
|<span data-ttu-id="dfa9b-353">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-353">TABLE_SCHEMA</span></span>|<span data-ttu-id="dfa9b-354">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-354">String</span></span>|  
|<span data-ttu-id="dfa9b-355">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-355">TABLE_NAME</span></span>|<span data-ttu-id="dfa9b-356">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-356">String</span></span>|  
|<span data-ttu-id="dfa9b-357">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-357">COLUMN_NAME</span></span>|<span data-ttu-id="dfa9b-358">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-358">String</span></span>|  
|<span data-ttu-id="dfa9b-359">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-359">COLUMN_GUID</span></span>|<span data-ttu-id="dfa9b-360">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-360">Guid</span></span>|  
|<span data-ttu-id="dfa9b-361">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-361">COLUMN_PROPID</span></span>|<span data-ttu-id="dfa9b-362">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-362">Int64</span></span>|  
|<span data-ttu-id="dfa9b-363">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-363">ORDINAL_POSITION</span></span>|<span data-ttu-id="dfa9b-364">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-364">Int64</span></span>|  
|<span data-ttu-id="dfa9b-365">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="dfa9b-365">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="dfa9b-366">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-366">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-367">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="dfa9b-367">COLUMN_DEFAULT</span></span>|<span data-ttu-id="dfa9b-368">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-368">String</span></span>|  
|<span data-ttu-id="dfa9b-369">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="dfa9b-369">COLUMN_FLAGS</span></span>|<span data-ttu-id="dfa9b-370">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-370">Int64</span></span>|  
|<span data-ttu-id="dfa9b-371">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-371">IS_NULLABLE</span></span>|<span data-ttu-id="dfa9b-372">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-372">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-373">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-373">DATA_TYPE</span></span>|<span data-ttu-id="dfa9b-374">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-374">Int32</span></span>|  
|<span data-ttu-id="dfa9b-375">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-375">TYPE_GUID</span></span>|<span data-ttu-id="dfa9b-376">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-376">Guid</span></span>|  
|<span data-ttu-id="dfa9b-377">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="dfa9b-377">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="dfa9b-378">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-378">Int64</span></span>|  
|<span data-ttu-id="dfa9b-379">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="dfa9b-379">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="dfa9b-380">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-380">Int64</span></span>|  
|<span data-ttu-id="dfa9b-381">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-381">NUMERIC_PRECISION</span></span>|<span data-ttu-id="dfa9b-382">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-382">Int32</span></span>|  
|<span data-ttu-id="dfa9b-383">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-383">NUMERIC_SCALE</span></span>|<span data-ttu-id="dfa9b-384">Int16</span><span class="sxs-lookup"><span data-stu-id="dfa9b-384">Int16</span></span>|  
|<span data-ttu-id="dfa9b-385">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-385">DATETIME_PRECISION</span></span>|<span data-ttu-id="dfa9b-386">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-386">Int64</span></span>|  
|<span data-ttu-id="dfa9b-387">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-387">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="dfa9b-388">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-388">String</span></span>|  
|<span data-ttu-id="dfa9b-389">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-389">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="dfa9b-390">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-390">String</span></span>|  
|<span data-ttu-id="dfa9b-391">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-391">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="dfa9b-392">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-392">String</span></span>|  
|<span data-ttu-id="dfa9b-393">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-393">COLLATION_CATALOG</span></span>|<span data-ttu-id="dfa9b-394">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-394">String</span></span>|  
|<span data-ttu-id="dfa9b-395">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-395">COLLATION_SCHEMA</span></span>|<span data-ttu-id="dfa9b-396">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-396">String</span></span>|  
|<span data-ttu-id="dfa9b-397">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-397">COLLATION_NAME</span></span>|<span data-ttu-id="dfa9b-398">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-398">String</span></span>|  
|<span data-ttu-id="dfa9b-399">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-399">DOMAIN_CATALOG</span></span>|<span data-ttu-id="dfa9b-400">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-400">String</span></span>|  
|<span data-ttu-id="dfa9b-401">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-401">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="dfa9b-402">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-402">String</span></span>|  
|<span data-ttu-id="dfa9b-403">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-403">DOMAIN_NAME</span></span>|<span data-ttu-id="dfa9b-404">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-404">String</span></span>|  
|<span data-ttu-id="dfa9b-405">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-405">DESCRIPTION</span></span>|<span data-ttu-id="dfa9b-406">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-406">String</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="dfa9b-407">Procédures</span><span class="sxs-lookup"><span data-stu-id="dfa9b-407">Procedures</span></span>  
  
|<span data-ttu-id="dfa9b-408">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-408">ColumnName</span></span>|<span data-ttu-id="dfa9b-409">Type de données</span><span class="sxs-lookup"><span data-stu-id="dfa9b-409">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dfa9b-410">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-410">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="dfa9b-411">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-411">String</span></span>|  
|<span data-ttu-id="dfa9b-412">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-412">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="dfa9b-413">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-413">String</span></span>|  
|<span data-ttu-id="dfa9b-414">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-414">PROCEDURE_NAME</span></span>|<span data-ttu-id="dfa9b-415">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-415">String</span></span>|  
|<span data-ttu-id="dfa9b-416">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-416">PROCEDURE_TYPE</span></span>|<span data-ttu-id="dfa9b-417">Int16</span><span class="sxs-lookup"><span data-stu-id="dfa9b-417">Int16</span></span>|  
|<span data-ttu-id="dfa9b-418">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-418">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="dfa9b-419">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-419">String</span></span>|  
|<span data-ttu-id="dfa9b-420">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-420">DESCRIPTION</span></span>|<span data-ttu-id="dfa9b-421">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-421">String</span></span>|  
|<span data-ttu-id="dfa9b-422">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="dfa9b-422">DATE_CREATED</span></span>|<span data-ttu-id="dfa9b-423">DateTime</span><span class="sxs-lookup"><span data-stu-id="dfa9b-423">DateTime</span></span>|  
|<span data-ttu-id="dfa9b-424">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="dfa9b-424">DATE_MODIFIED</span></span>|<span data-ttu-id="dfa9b-425">DateTime</span><span class="sxs-lookup"><span data-stu-id="dfa9b-425">DateTime</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="dfa9b-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="dfa9b-426">ProcedureColumns</span></span>  
  
|<span data-ttu-id="dfa9b-427">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-427">ColumnName</span></span>|<span data-ttu-id="dfa9b-428">Type de données</span><span class="sxs-lookup"><span data-stu-id="dfa9b-428">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dfa9b-429">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-429">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="dfa9b-430">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-430">String</span></span>|  
|<span data-ttu-id="dfa9b-431">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-431">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="dfa9b-432">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-432">String</span></span>|  
|<span data-ttu-id="dfa9b-433">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-433">PROCEDURE_NAME</span></span>|<span data-ttu-id="dfa9b-434">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-434">String</span></span>|  
|<span data-ttu-id="dfa9b-435">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-435">COLUMN_NAME</span></span>|<span data-ttu-id="dfa9b-436">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-436">String</span></span>|  
|<span data-ttu-id="dfa9b-437">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-437">COLUMN_GUID</span></span>|<span data-ttu-id="dfa9b-438">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-438">Guid</span></span>|  
|<span data-ttu-id="dfa9b-439">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-439">COLUMN_PROPID</span></span>|<span data-ttu-id="dfa9b-440">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-440">Int64</span></span>|  
|<span data-ttu-id="dfa9b-441">ROWSET_NUMBER</span><span class="sxs-lookup"><span data-stu-id="dfa9b-441">ROWSET_NUMBER</span></span>|<span data-ttu-id="dfa9b-442">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-442">Int64</span></span>|  
|<span data-ttu-id="dfa9b-443">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-443">ORDINAL_POSITION</span></span>|<span data-ttu-id="dfa9b-444">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-444">Int64</span></span>|  
|<span data-ttu-id="dfa9b-445">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-445">IS_NULLABLE</span></span>|<span data-ttu-id="dfa9b-446">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-446">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-447">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-447">DATA_TYPE</span></span>|<span data-ttu-id="dfa9b-448">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-448">Int32</span></span>|  
|<span data-ttu-id="dfa9b-449">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-449">TYPE_GUID</span></span>|<span data-ttu-id="dfa9b-450">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-450">Guid</span></span>|  
|<span data-ttu-id="dfa9b-451">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="dfa9b-451">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="dfa9b-452">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-452">Int64</span></span>|  
|<span data-ttu-id="dfa9b-453">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="dfa9b-453">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="dfa9b-454">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-454">Int64</span></span>|  
|<span data-ttu-id="dfa9b-455">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-455">NUMERIC_PRECISION</span></span>|<span data-ttu-id="dfa9b-456">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-456">Int32</span></span>|  
|<span data-ttu-id="dfa9b-457">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-457">NUMERIC_SCALE</span></span>|<span data-ttu-id="dfa9b-458">Int16</span><span class="sxs-lookup"><span data-stu-id="dfa9b-458">Int16</span></span>|  
|<span data-ttu-id="dfa9b-459">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-459">DESCRIPTION</span></span>|<span data-ttu-id="dfa9b-460">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-460">String</span></span>|  
|<span data-ttu-id="dfa9b-461">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="dfa9b-461">OVERLOAD</span></span>|<span data-ttu-id="dfa9b-462">Int16</span><span class="sxs-lookup"><span data-stu-id="dfa9b-462">Int16</span></span>|  
  
### <a name="views"></a><span data-ttu-id="dfa9b-463">Affichages</span><span class="sxs-lookup"><span data-stu-id="dfa9b-463">Views</span></span>  
  
|<span data-ttu-id="dfa9b-464">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-464">ColumnName</span></span>|<span data-ttu-id="dfa9b-465">Type de données</span><span class="sxs-lookup"><span data-stu-id="dfa9b-465">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dfa9b-466">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-466">TABLE_CATALOG</span></span>|<span data-ttu-id="dfa9b-467">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-467">String</span></span>|  
|<span data-ttu-id="dfa9b-468">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-468">TABLE_SCHEMA</span></span>|<span data-ttu-id="dfa9b-469">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-469">String</span></span>|  
|<span data-ttu-id="dfa9b-470">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-470">TABLE_NAME</span></span>|<span data-ttu-id="dfa9b-471">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-471">String</span></span>|  
|<span data-ttu-id="dfa9b-472">VIEW_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-472">VIEW_DEFINITION</span></span>|<span data-ttu-id="dfa9b-473">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-473">String</span></span>|  
|<span data-ttu-id="dfa9b-474">CHECK_OPTION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-474">CHECK_OPTION</span></span>|<span data-ttu-id="dfa9b-475">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-475">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-476">IS_UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-476">IS_UPDATABLE</span></span>|<span data-ttu-id="dfa9b-477">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-477">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-478">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-478">DESCRIPTION</span></span>|<span data-ttu-id="dfa9b-479">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-479">String</span></span>|  
|<span data-ttu-id="dfa9b-480">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="dfa9b-480">DATE_CREATED</span></span>|<span data-ttu-id="dfa9b-481">DateTime</span><span class="sxs-lookup"><span data-stu-id="dfa9b-481">DateTime</span></span>|  
|<span data-ttu-id="dfa9b-482">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="dfa9b-482">DATE_MODIFIED</span></span>|<span data-ttu-id="dfa9b-483">DateTime</span><span class="sxs-lookup"><span data-stu-id="dfa9b-483">DateTime</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="dfa9b-484">Index</span><span class="sxs-lookup"><span data-stu-id="dfa9b-484">Indexes</span></span>  
  
|<span data-ttu-id="dfa9b-485">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-485">ColumnName</span></span>|<span data-ttu-id="dfa9b-486">Type de données</span><span class="sxs-lookup"><span data-stu-id="dfa9b-486">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dfa9b-487">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-487">TABLE_CATALOG</span></span>|<span data-ttu-id="dfa9b-488">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-488">String</span></span>|  
|<span data-ttu-id="dfa9b-489">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-489">TABLE_SCHEMA</span></span>|<span data-ttu-id="dfa9b-490">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-490">String</span></span>|  
|<span data-ttu-id="dfa9b-491">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-491">TABLE_NAME</span></span>|<span data-ttu-id="dfa9b-492">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-492">String</span></span>|  
|<span data-ttu-id="dfa9b-493">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-493">INDEX_CATALOG</span></span>|<span data-ttu-id="dfa9b-494">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-494">String</span></span>|  
|<span data-ttu-id="dfa9b-495">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-495">INDEX_SCHEMA</span></span>|<span data-ttu-id="dfa9b-496">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-496">String</span></span>|  
|<span data-ttu-id="dfa9b-497">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-497">INDEX_NAME</span></span>|<span data-ttu-id="dfa9b-498">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-498">String</span></span>|  
|<span data-ttu-id="dfa9b-499">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="dfa9b-499">PRIMARY_KEY</span></span>|<span data-ttu-id="dfa9b-500">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-500">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-501">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-501">UNIQUE</span></span>|<span data-ttu-id="dfa9b-502">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-502">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-503">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="dfa9b-503">CLUSTERED</span></span>|<span data-ttu-id="dfa9b-504">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-504">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-505">TYPE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-505">TYPE</span></span>|<span data-ttu-id="dfa9b-506">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-506">Int32</span></span>|  
|<span data-ttu-id="dfa9b-507">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="dfa9b-507">FILL_FACTOR</span></span>|<span data-ttu-id="dfa9b-508">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-508">Int32</span></span>|  
|<span data-ttu-id="dfa9b-509">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-509">INITIAL_SIZE</span></span>|<span data-ttu-id="dfa9b-510">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-510">Int32</span></span>|  
|<span data-ttu-id="dfa9b-511">NULLS</span><span class="sxs-lookup"><span data-stu-id="dfa9b-511">NULLS</span></span>|<span data-ttu-id="dfa9b-512">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-512">Int32</span></span>|  
|<span data-ttu-id="dfa9b-513">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="dfa9b-513">SORT_BOOKMARKS</span></span>|<span data-ttu-id="dfa9b-514">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-514">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-515">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-515">AUTO_UPDATE</span></span>|<span data-ttu-id="dfa9b-516">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-516">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-517">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-517">NULL_COLLATION</span></span>|<span data-ttu-id="dfa9b-518">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-518">Int32</span></span>|  
|<span data-ttu-id="dfa9b-519">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-519">ORDINAL_POSITION</span></span>|<span data-ttu-id="dfa9b-520">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-520">Int64</span></span>|  
|<span data-ttu-id="dfa9b-521">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-521">COLUMN_NAME</span></span>|<span data-ttu-id="dfa9b-522">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-522">String</span></span>|  
|<span data-ttu-id="dfa9b-523">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-523">COLUMN_GUID</span></span>|<span data-ttu-id="dfa9b-524">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-524">Guid</span></span>|  
|<span data-ttu-id="dfa9b-525">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-525">COLUMN_PROPID</span></span>|<span data-ttu-id="dfa9b-526">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-526">Int64</span></span>|  
|<span data-ttu-id="dfa9b-527">COLLATION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-527">COLLATION</span></span>|<span data-ttu-id="dfa9b-528">Int16</span><span class="sxs-lookup"><span data-stu-id="dfa9b-528">Int16</span></span>|  
|<span data-ttu-id="dfa9b-529">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="dfa9b-529">CARDINALITY</span></span>|<span data-ttu-id="dfa9b-530">Decimal</span><span class="sxs-lookup"><span data-stu-id="dfa9b-530">Decimal</span></span>|  
|<span data-ttu-id="dfa9b-531">PAGES</span><span class="sxs-lookup"><span data-stu-id="dfa9b-531">PAGES</span></span>|<span data-ttu-id="dfa9b-532">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-532">Int32</span></span>|  
|<span data-ttu-id="dfa9b-533">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-533">FILTER_CONDITION</span></span>|<span data-ttu-id="dfa9b-534">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-534">String</span></span>|  
|<span data-ttu-id="dfa9b-535">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="dfa9b-535">INTEGRATED</span></span>|<span data-ttu-id="dfa9b-536">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-536">Boolean</span></span>|  
  
## <a name="microsoft-jet-ole-db-provider"></a><span data-ttu-id="dfa9b-537">Fournisseur Microsoft Jet OLE DB</span><span class="sxs-lookup"><span data-stu-id="dfa9b-537">Microsoft Jet OLE DB Provider</span></span>  
 <span data-ttu-id="dfa9b-538">Le pilote Microsoft Jet OLE DB prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="dfa9b-538">The Microsoft Jet OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
- <span data-ttu-id="dfa9b-539">Tables</span><span class="sxs-lookup"><span data-stu-id="dfa9b-539">Tables</span></span>  
  
- <span data-ttu-id="dfa9b-540">Colonnes</span><span class="sxs-lookup"><span data-stu-id="dfa9b-540">Columns</span></span>  
  
- <span data-ttu-id="dfa9b-541">Procédures</span><span class="sxs-lookup"><span data-stu-id="dfa9b-541">Procedures</span></span>  
  
- <span data-ttu-id="dfa9b-542">Affichages</span><span class="sxs-lookup"><span data-stu-id="dfa9b-542">Views</span></span>  
  
- <span data-ttu-id="dfa9b-543">Index</span><span class="sxs-lookup"><span data-stu-id="dfa9b-543">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="dfa9b-544">Tables</span><span class="sxs-lookup"><span data-stu-id="dfa9b-544">Tables</span></span>  
  
|<span data-ttu-id="dfa9b-545">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-545">ColumnName</span></span>|<span data-ttu-id="dfa9b-546">Type de données</span><span class="sxs-lookup"><span data-stu-id="dfa9b-546">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dfa9b-547">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-547">TABLE_CATALOG</span></span>|<span data-ttu-id="dfa9b-548">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-548">String</span></span>|  
|<span data-ttu-id="dfa9b-549">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-549">TABLE_SCHEMA</span></span>|<span data-ttu-id="dfa9b-550">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-550">String</span></span>|  
|<span data-ttu-id="dfa9b-551">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-551">TABLE_NAME</span></span>|<span data-ttu-id="dfa9b-552">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-552">String</span></span>|  
|<span data-ttu-id="dfa9b-553">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-553">TABLE_TYPE</span></span>|<span data-ttu-id="dfa9b-554">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-554">String</span></span>|  
|<span data-ttu-id="dfa9b-555">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-555">TABLE_GUID</span></span>|<span data-ttu-id="dfa9b-556">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-556">Guid</span></span>|  
|<span data-ttu-id="dfa9b-557">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-557">DESCRIPTION</span></span>|<span data-ttu-id="dfa9b-558">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-558">String</span></span>|  
|<span data-ttu-id="dfa9b-559">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-559">TABLE_PROPID</span></span>|<span data-ttu-id="dfa9b-560">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-560">Int64</span></span>|  
|<span data-ttu-id="dfa9b-561">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="dfa9b-561">DATE_CREATED</span></span>|<span data-ttu-id="dfa9b-562">DateTime</span><span class="sxs-lookup"><span data-stu-id="dfa9b-562">DateTime</span></span>|  
|<span data-ttu-id="dfa9b-563">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="dfa9b-563">DATE_MODIFIED</span></span>|<span data-ttu-id="dfa9b-564">DateTime</span><span class="sxs-lookup"><span data-stu-id="dfa9b-564">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="dfa9b-565">Colonnes</span><span class="sxs-lookup"><span data-stu-id="dfa9b-565">Columns</span></span>  
  
|<span data-ttu-id="dfa9b-566">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-566">ColumnName</span></span>|<span data-ttu-id="dfa9b-567">Type de données</span><span class="sxs-lookup"><span data-stu-id="dfa9b-567">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dfa9b-568">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-568">TABLE_CATALOG</span></span>|<span data-ttu-id="dfa9b-569">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-569">String</span></span>|  
|<span data-ttu-id="dfa9b-570">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-570">TABLE_SCHEMA</span></span>|<span data-ttu-id="dfa9b-571">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-571">String</span></span>|  
|<span data-ttu-id="dfa9b-572">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-572">TABLE_NAME</span></span>|<span data-ttu-id="dfa9b-573">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-573">String</span></span>|  
|<span data-ttu-id="dfa9b-574">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-574">COLUMN_NAME</span></span>|<span data-ttu-id="dfa9b-575">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-575">String</span></span>|  
|<span data-ttu-id="dfa9b-576">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-576">COLUMN_GUID</span></span>|<span data-ttu-id="dfa9b-577">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-577">Guid</span></span>|  
|<span data-ttu-id="dfa9b-578">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-578">COLUMN_PROPID</span></span>|<span data-ttu-id="dfa9b-579">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-579">Int64</span></span>|  
|<span data-ttu-id="dfa9b-580">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-580">ORDINAL_POSITION</span></span>|<span data-ttu-id="dfa9b-581">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-581">Int64</span></span>|  
|<span data-ttu-id="dfa9b-582">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="dfa9b-582">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="dfa9b-583">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-583">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-584">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="dfa9b-584">COLUMN_DEFAULT</span></span>|<span data-ttu-id="dfa9b-585">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-585">String</span></span>|  
|<span data-ttu-id="dfa9b-586">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="dfa9b-586">COLUMN_FLAGS</span></span>|<span data-ttu-id="dfa9b-587">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-587">Int64</span></span>|  
|<span data-ttu-id="dfa9b-588">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-588">IS_NULLABLE</span></span>|<span data-ttu-id="dfa9b-589">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-589">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-590">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-590">DATA_TYPE</span></span>|<span data-ttu-id="dfa9b-591">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-591">Int32</span></span>|  
|<span data-ttu-id="dfa9b-592">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-592">TYPE_GUID</span></span>|<span data-ttu-id="dfa9b-593">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-593">Guid</span></span>|  
|<span data-ttu-id="dfa9b-594">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="dfa9b-594">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="dfa9b-595">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-595">Int64</span></span>|  
|<span data-ttu-id="dfa9b-596">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="dfa9b-596">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="dfa9b-597">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-597">Int64</span></span>|  
|<span data-ttu-id="dfa9b-598">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-598">NUMERIC_PRECISION</span></span>|<span data-ttu-id="dfa9b-599">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-599">Int32</span></span>|  
|<span data-ttu-id="dfa9b-600">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-600">NUMERIC_SCALE</span></span>|<span data-ttu-id="dfa9b-601">Int16</span><span class="sxs-lookup"><span data-stu-id="dfa9b-601">Int16</span></span>|  
|<span data-ttu-id="dfa9b-602">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-602">DATETIME_PRECISION</span></span>|<span data-ttu-id="dfa9b-603">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-603">Int64</span></span>|  
|<span data-ttu-id="dfa9b-604">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-604">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="dfa9b-605">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-605">String</span></span>|  
|<span data-ttu-id="dfa9b-606">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-606">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="dfa9b-607">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-607">String</span></span>|  
|<span data-ttu-id="dfa9b-608">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-608">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="dfa9b-609">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-609">String</span></span>|  
|<span data-ttu-id="dfa9b-610">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-610">COLLATION_CATALOG</span></span>|<span data-ttu-id="dfa9b-611">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-611">String</span></span>|  
|<span data-ttu-id="dfa9b-612">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-612">COLLATION_SCHEMA</span></span>|<span data-ttu-id="dfa9b-613">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-613">String</span></span>|  
|<span data-ttu-id="dfa9b-614">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-614">COLLATION_NAME</span></span>|<span data-ttu-id="dfa9b-615">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-615">String</span></span>|  
|<span data-ttu-id="dfa9b-616">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-616">DOMAIN_CATALOG</span></span>|<span data-ttu-id="dfa9b-617">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-617">String</span></span>|  
|<span data-ttu-id="dfa9b-618">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-618">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="dfa9b-619">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-619">String</span></span>|  
|<span data-ttu-id="dfa9b-620">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-620">DOMAIN_NAME</span></span>|<span data-ttu-id="dfa9b-621">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-621">String</span></span>|  
|<span data-ttu-id="dfa9b-622">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-622">DESCRIPTION</span></span>|<span data-ttu-id="dfa9b-623">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-623">String</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="dfa9b-624">Procédures</span><span class="sxs-lookup"><span data-stu-id="dfa9b-624">Procedures</span></span>  
  
|<span data-ttu-id="dfa9b-625">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-625">ColumnName</span></span>|<span data-ttu-id="dfa9b-626">Type de données</span><span class="sxs-lookup"><span data-stu-id="dfa9b-626">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dfa9b-627">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-627">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="dfa9b-628">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-628">String</span></span>|  
|<span data-ttu-id="dfa9b-629">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-629">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="dfa9b-630">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-630">String</span></span>|  
|<span data-ttu-id="dfa9b-631">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-631">PROCEDURE_NAME</span></span>|<span data-ttu-id="dfa9b-632">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-632">String</span></span>|  
|<span data-ttu-id="dfa9b-633">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-633">PROCEDURE_TYPE</span></span>|<span data-ttu-id="dfa9b-634">Int16</span><span class="sxs-lookup"><span data-stu-id="dfa9b-634">Int16</span></span>|  
|<span data-ttu-id="dfa9b-635">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-635">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="dfa9b-636">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-636">String</span></span>|  
|<span data-ttu-id="dfa9b-637">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-637">DESCRIPTION</span></span>|<span data-ttu-id="dfa9b-638">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-638">String</span></span>|  
|<span data-ttu-id="dfa9b-639">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="dfa9b-639">DATE_CREATED</span></span>|<span data-ttu-id="dfa9b-640">DateTime</span><span class="sxs-lookup"><span data-stu-id="dfa9b-640">DateTime</span></span>|  
|<span data-ttu-id="dfa9b-641">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="dfa9b-641">DATE_MODIFIED</span></span>|<span data-ttu-id="dfa9b-642">DateTime</span><span class="sxs-lookup"><span data-stu-id="dfa9b-642">DateTime</span></span>|  
  
### <a name="views"></a><span data-ttu-id="dfa9b-643">Affichages</span><span class="sxs-lookup"><span data-stu-id="dfa9b-643">Views</span></span>  
  
|<span data-ttu-id="dfa9b-644">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-644">ColumnName</span></span>|<span data-ttu-id="dfa9b-645">Type de données</span><span class="sxs-lookup"><span data-stu-id="dfa9b-645">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dfa9b-646">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-646">TABLE_CATALOG</span></span>|<span data-ttu-id="dfa9b-647">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-647">String</span></span>|  
|<span data-ttu-id="dfa9b-648">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-648">TABLE_SCHEMA</span></span>|<span data-ttu-id="dfa9b-649">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-649">String</span></span>|  
|<span data-ttu-id="dfa9b-650">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-650">TABLE_NAME</span></span>|<span data-ttu-id="dfa9b-651">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-651">String</span></span>|  
|<span data-ttu-id="dfa9b-652">VIEW_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-652">VIEW_DEFINITION</span></span>|<span data-ttu-id="dfa9b-653">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-653">String</span></span>|  
|<span data-ttu-id="dfa9b-654">CHECK_OPTION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-654">CHECK_OPTION</span></span>|<span data-ttu-id="dfa9b-655">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-655">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-656">IS_UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-656">IS_UPDATABLE</span></span>|<span data-ttu-id="dfa9b-657">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-657">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-658">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-658">DESCRIPTION</span></span>|<span data-ttu-id="dfa9b-659">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-659">String</span></span>|  
|<span data-ttu-id="dfa9b-660">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="dfa9b-660">DATE_CREATED</span></span>|<span data-ttu-id="dfa9b-661">DateTime</span><span class="sxs-lookup"><span data-stu-id="dfa9b-661">DateTime</span></span>|  
|<span data-ttu-id="dfa9b-662">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="dfa9b-662">DATE_MODIFIED</span></span>|<span data-ttu-id="dfa9b-663">DateTime</span><span class="sxs-lookup"><span data-stu-id="dfa9b-663">DateTime</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="dfa9b-664">Index</span><span class="sxs-lookup"><span data-stu-id="dfa9b-664">Indexes</span></span>  
  
|<span data-ttu-id="dfa9b-665">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-665">ColumnName</span></span>|<span data-ttu-id="dfa9b-666">Type de données</span><span class="sxs-lookup"><span data-stu-id="dfa9b-666">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dfa9b-667">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-667">TABLE_CATALOG</span></span>|<span data-ttu-id="dfa9b-668">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-668">String</span></span>|  
|<span data-ttu-id="dfa9b-669">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-669">TABLE_SCHEMA</span></span>|<span data-ttu-id="dfa9b-670">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-670">String</span></span>|  
|<span data-ttu-id="dfa9b-671">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-671">TABLE_NAME</span></span>|<span data-ttu-id="dfa9b-672">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-672">String</span></span>|  
|<span data-ttu-id="dfa9b-673">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dfa9b-673">INDEX_CATALOG</span></span>|<span data-ttu-id="dfa9b-674">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-674">String</span></span>|  
|<span data-ttu-id="dfa9b-675">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dfa9b-675">INDEX_SCHEMA</span></span>|<span data-ttu-id="dfa9b-676">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-676">String</span></span>|  
|<span data-ttu-id="dfa9b-677">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-677">INDEX_NAME</span></span>|<span data-ttu-id="dfa9b-678">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-678">String</span></span>|  
|<span data-ttu-id="dfa9b-679">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="dfa9b-679">PRIMARY_KEY</span></span>|<span data-ttu-id="dfa9b-680">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-680">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-681">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-681">UNIQUE</span></span>|<span data-ttu-id="dfa9b-682">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-682">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-683">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="dfa9b-683">CLUSTERED</span></span>|<span data-ttu-id="dfa9b-684">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-684">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-685">TYPE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-685">TYPE</span></span>|<span data-ttu-id="dfa9b-686">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-686">Int32</span></span>|  
|<span data-ttu-id="dfa9b-687">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="dfa9b-687">FILL_FACTOR</span></span>|<span data-ttu-id="dfa9b-688">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-688">Int32</span></span>|  
|<span data-ttu-id="dfa9b-689">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-689">INITIAL_SIZE</span></span>|<span data-ttu-id="dfa9b-690">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-690">Int32</span></span>|  
|<span data-ttu-id="dfa9b-691">NULLS</span><span class="sxs-lookup"><span data-stu-id="dfa9b-691">NULLS</span></span>|<span data-ttu-id="dfa9b-692">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-692">Int32</span></span>|  
|<span data-ttu-id="dfa9b-693">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="dfa9b-693">SORT_BOOKMARKS</span></span>|<span data-ttu-id="dfa9b-694">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-694">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-695">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="dfa9b-695">AUTO_UPDATE</span></span>|<span data-ttu-id="dfa9b-696">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-696">Boolean</span></span>|  
|<span data-ttu-id="dfa9b-697">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-697">NULL_COLLATION</span></span>|<span data-ttu-id="dfa9b-698">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-698">Int32</span></span>|  
|<span data-ttu-id="dfa9b-699">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-699">ORDINAL_POSITION</span></span>|<span data-ttu-id="dfa9b-700">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-700">Int64</span></span>|  
|<span data-ttu-id="dfa9b-701">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="dfa9b-701">COLUMN_NAME</span></span>|<span data-ttu-id="dfa9b-702">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-702">String</span></span>|  
|<span data-ttu-id="dfa9b-703">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-703">COLUMN_GUID</span></span>|<span data-ttu-id="dfa9b-704">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-704">Guid</span></span>|  
|<span data-ttu-id="dfa9b-705">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="dfa9b-705">COLUMN_PROPID</span></span>|<span data-ttu-id="dfa9b-706">Int64</span><span class="sxs-lookup"><span data-stu-id="dfa9b-706">Int64</span></span>|  
|<span data-ttu-id="dfa9b-707">COLLATION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-707">COLLATION</span></span>|<span data-ttu-id="dfa9b-708">Int16</span><span class="sxs-lookup"><span data-stu-id="dfa9b-708">Int16</span></span>|  
|<span data-ttu-id="dfa9b-709">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="dfa9b-709">CARDINALITY</span></span>|<span data-ttu-id="dfa9b-710">Decimal</span><span class="sxs-lookup"><span data-stu-id="dfa9b-710">Decimal</span></span>|  
|<span data-ttu-id="dfa9b-711">PAGES</span><span class="sxs-lookup"><span data-stu-id="dfa9b-711">PAGES</span></span>|<span data-ttu-id="dfa9b-712">Int32</span><span class="sxs-lookup"><span data-stu-id="dfa9b-712">Int32</span></span>|  
|<span data-ttu-id="dfa9b-713">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="dfa9b-713">FILTER_CONDITION</span></span>|<span data-ttu-id="dfa9b-714">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dfa9b-714">String</span></span>|  
|<span data-ttu-id="dfa9b-715">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="dfa9b-715">INTEGRATED</span></span>|<span data-ttu-id="dfa9b-716">Booléen</span><span class="sxs-lookup"><span data-stu-id="dfa9b-716">Boolean</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="dfa9b-717">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfa9b-717">See also</span></span>

- [<span data-ttu-id="dfa9b-718">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="dfa9b-718">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
