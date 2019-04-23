---
title: Collections de schémas OLE DB
ms.date: 03/30/2017
ms.assetid: 6380c36b-658e-4d67-91e8-7131ef4a7c2c
ms.openlocfilehash: 6dc187b0a876d9e167a74f2381db156dde2764fe
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59164682"
---
# <a name="ole-db-schema-collections"></a><span data-ttu-id="c679b-102">Collections de schémas OLE DB</span><span class="sxs-lookup"><span data-stu-id="c679b-102">OLE DB Schema Collections</span></span>
<span data-ttu-id="c679b-103">Cette section traite de la prise en charge des collections de schémas pour les fournisseurs OLE DB de Microsoft SQL Server, Oracle et Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="c679b-103">This section discusses schema collection support for the OLE DB providers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-ole-db-provider"></a><span data-ttu-id="c679b-104">Fournisseur Microsoft SQL Server OLE DB</span><span class="sxs-lookup"><span data-stu-id="c679b-104">Microsoft SQL Server OLE DB Provider</span></span>  
 <span data-ttu-id="c679b-105">Le pilote OLE DB Microsoft SQL Server prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="c679b-105">The Microsoft SQL Server OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="c679b-106">Tables</span><span class="sxs-lookup"><span data-stu-id="c679b-106">Tables</span></span>  
  
-   <span data-ttu-id="c679b-107">Colonnes</span><span class="sxs-lookup"><span data-stu-id="c679b-107">Columns</span></span>  
  
-   <span data-ttu-id="c679b-108">Procédures</span><span class="sxs-lookup"><span data-stu-id="c679b-108">Procedures</span></span>  
  
-   <span data-ttu-id="c679b-109">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="c679b-109">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="c679b-110">Catalogue</span><span class="sxs-lookup"><span data-stu-id="c679b-110">Catalog</span></span>  
  
-   <span data-ttu-id="c679b-111">Index</span><span class="sxs-lookup"><span data-stu-id="c679b-111">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="c679b-112">Tables</span><span class="sxs-lookup"><span data-stu-id="c679b-112">Tables</span></span>  
  
|<span data-ttu-id="c679b-113">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c679b-113">ColumnName</span></span>|<span data-ttu-id="c679b-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="c679b-114">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c679b-115">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-115">TABLE_CATALOG</span></span>|<span data-ttu-id="c679b-116">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-116">String</span></span>|  
|<span data-ttu-id="c679b-117">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-117">TABLE_SCHEMA</span></span>|<span data-ttu-id="c679b-118">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-118">String</span></span>|  
|<span data-ttu-id="c679b-119">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-119">TABLE_NAME</span></span>|<span data-ttu-id="c679b-120">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-120">String</span></span>|  
|<span data-ttu-id="c679b-121">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c679b-121">TABLE_TYPE</span></span>|<span data-ttu-id="c679b-122">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-122">String</span></span>|  
|<span data-ttu-id="c679b-123">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-123">TABLE_GUID</span></span>|<span data-ttu-id="c679b-124">GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-124">Guid</span></span>|  
|<span data-ttu-id="c679b-125">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c679b-125">DESCRIPTION</span></span>|<span data-ttu-id="c679b-126">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-126">String</span></span>|  
|<span data-ttu-id="c679b-127">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="c679b-127">TABLE_PROPID</span></span>|<span data-ttu-id="c679b-128">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-128">Int64</span></span>|  
|<span data-ttu-id="c679b-129">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="c679b-129">DATE_CREATED</span></span>|<span data-ttu-id="c679b-130">DateTime</span><span class="sxs-lookup"><span data-stu-id="c679b-130">DateTime</span></span>|  
|<span data-ttu-id="c679b-131">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="c679b-131">DATE_MODIFIED</span></span>|<span data-ttu-id="c679b-132">DateTime</span><span class="sxs-lookup"><span data-stu-id="c679b-132">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="c679b-133">Colonnes</span><span class="sxs-lookup"><span data-stu-id="c679b-133">Columns</span></span>  
  
|<span data-ttu-id="c679b-134">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c679b-134">ColumnName</span></span>|<span data-ttu-id="c679b-135">Type de données</span><span class="sxs-lookup"><span data-stu-id="c679b-135">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c679b-136">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-136">TABLE_CATALOG</span></span>|<span data-ttu-id="c679b-137">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-137">String</span></span>|  
|<span data-ttu-id="c679b-138">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-138">TABLE_SCHEMA</span></span>|<span data-ttu-id="c679b-139">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-139">String</span></span>|  
|<span data-ttu-id="c679b-140">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-140">TABLE_NAME</span></span>|<span data-ttu-id="c679b-141">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-141">String</span></span>|  
|<span data-ttu-id="c679b-142">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-142">COLUMN_NAME</span></span>|<span data-ttu-id="c679b-143">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-143">String</span></span>|  
|<span data-ttu-id="c679b-144">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-144">COLUMN_GUID</span></span>|<span data-ttu-id="c679b-145">GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-145">Guid</span></span>|  
|<span data-ttu-id="c679b-146">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="c679b-146">COLUMN_PROPID</span></span>|<span data-ttu-id="c679b-147">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-147">Int64</span></span>|  
|<span data-ttu-id="c679b-148">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c679b-148">ORDINAL_POSITION</span></span>|<span data-ttu-id="c679b-149">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-149">Int64</span></span>|  
|<span data-ttu-id="c679b-150">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="c679b-150">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="c679b-151">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-151">Boolean</span></span>|  
|<span data-ttu-id="c679b-152">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c679b-152">COLUMN_DEFAULT</span></span>|<span data-ttu-id="c679b-153">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-153">String</span></span>|  
|<span data-ttu-id="c679b-154">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="c679b-154">COLUMN_FLAGS</span></span>|<span data-ttu-id="c679b-155">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-155">Int64</span></span>|  
|<span data-ttu-id="c679b-156">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c679b-156">IS_NULLABLE</span></span>|<span data-ttu-id="c679b-157">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-157">Boolean</span></span>|  
|<span data-ttu-id="c679b-158">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c679b-158">DATA_TYPE</span></span>|<span data-ttu-id="c679b-159">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-159">Int32</span></span>|  
|<span data-ttu-id="c679b-160">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-160">TYPE_GUID</span></span>|<span data-ttu-id="c679b-161">GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-161">Guid</span></span>|  
|<span data-ttu-id="c679b-162">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c679b-162">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="c679b-163">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-163">Int64</span></span>|  
|<span data-ttu-id="c679b-164">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c679b-164">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="c679b-165">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-165">Int64</span></span>|  
|<span data-ttu-id="c679b-166">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="c679b-166">NUMERIC_PRECISION</span></span>|<span data-ttu-id="c679b-167">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-167">Int32</span></span>|  
|<span data-ttu-id="c679b-168">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="c679b-168">NUMERIC_SCALE</span></span>|<span data-ttu-id="c679b-169">Int16</span><span class="sxs-lookup"><span data-stu-id="c679b-169">Int16</span></span>|  
|<span data-ttu-id="c679b-170">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="c679b-170">DATETIME_PRECISION</span></span>|<span data-ttu-id="c679b-171">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-171">Int64</span></span>|  
|<span data-ttu-id="c679b-172">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-172">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="c679b-173">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-173">String</span></span>|  
|<span data-ttu-id="c679b-174">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-174">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="c679b-175">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-175">String</span></span>|  
|<span data-ttu-id="c679b-176">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-176">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="c679b-177">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-177">String</span></span>|  
|<span data-ttu-id="c679b-178">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-178">COLLATION_CATALOG</span></span>|<span data-ttu-id="c679b-179">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-179">String</span></span>|  
|<span data-ttu-id="c679b-180">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-180">COLLATION_SCHEMA</span></span>|<span data-ttu-id="c679b-181">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-181">String</span></span>|  
|<span data-ttu-id="c679b-182">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-182">COLLATION_NAME</span></span>|<span data-ttu-id="c679b-183">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-183">String</span></span>|  
|<span data-ttu-id="c679b-184">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-184">DOMAIN_CATALOG</span></span>|<span data-ttu-id="c679b-185">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-185">String</span></span>|  
|<span data-ttu-id="c679b-186">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-186">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="c679b-187">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-187">String</span></span>|  
|<span data-ttu-id="c679b-188">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-188">DOMAIN_NAME</span></span>|<span data-ttu-id="c679b-189">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-189">String</span></span>|  
|<span data-ttu-id="c679b-190">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c679b-190">DESCRIPTION</span></span>|<span data-ttu-id="c679b-191">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-191">String</span></span>|  
|<span data-ttu-id="c679b-192">COLUMN_LCID</span><span class="sxs-lookup"><span data-stu-id="c679b-192">COLUMN_LCID</span></span>|<span data-ttu-id="c679b-193">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-193">Int32</span></span>|  
|<span data-ttu-id="c679b-194">COLUMN_COMPFLAGS</span><span class="sxs-lookup"><span data-stu-id="c679b-194">COLUMN_COMPFLAGS</span></span>|<span data-ttu-id="c679b-195">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-195">Int32</span></span>|  
|<span data-ttu-id="c679b-196">COLUMN_SORTID</span><span class="sxs-lookup"><span data-stu-id="c679b-196">COLUMN_SORTID</span></span>|<span data-ttu-id="c679b-197">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-197">Int32</span></span>|  
|<span data-ttu-id="c679b-198">COLUMN_TDSCOLLATION</span><span class="sxs-lookup"><span data-stu-id="c679b-198">COLUMN_TDSCOLLATION</span></span>|<span data-ttu-id="c679b-199">Byte[]</span><span class="sxs-lookup"><span data-stu-id="c679b-199">Byte[]</span></span>|  
|<span data-ttu-id="c679b-200">IS_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="c679b-200">IS_COMPUTED</span></span>|<span data-ttu-id="c679b-201">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-201">Boolean</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="c679b-202">Procédures</span><span class="sxs-lookup"><span data-stu-id="c679b-202">Procedures</span></span>  
  
|<span data-ttu-id="c679b-203">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c679b-203">ColumnName</span></span>|<span data-ttu-id="c679b-204">Type de données</span><span class="sxs-lookup"><span data-stu-id="c679b-204">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c679b-205">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-205">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="c679b-206">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-206">String</span></span>|  
|<span data-ttu-id="c679b-207">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-207">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="c679b-208">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-208">String</span></span>|  
|<span data-ttu-id="c679b-209">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-209">PROCEDURE_NAME</span></span>|<span data-ttu-id="c679b-210">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-210">String</span></span>|  
|<span data-ttu-id="c679b-211">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c679b-211">PROCEDURE_TYPE</span></span>|<span data-ttu-id="c679b-212">Int16</span><span class="sxs-lookup"><span data-stu-id="c679b-212">Int16</span></span>|  
|<span data-ttu-id="c679b-213">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="c679b-213">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="c679b-214">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-214">String</span></span>|  
|<span data-ttu-id="c679b-215">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c679b-215">DESCRIPTION</span></span>|<span data-ttu-id="c679b-216">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-216">String</span></span>|  
|<span data-ttu-id="c679b-217">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="c679b-217">DATE_CREATED</span></span>|<span data-ttu-id="c679b-218">DateTime</span><span class="sxs-lookup"><span data-stu-id="c679b-218">DateTime</span></span>|  
|<span data-ttu-id="c679b-219">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="c679b-219">DATE_MODIFIED</span></span>|<span data-ttu-id="c679b-220">DateTime</span><span class="sxs-lookup"><span data-stu-id="c679b-220">DateTime</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="c679b-221">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="c679b-221">ProcedureParameters</span></span>  
  
|<span data-ttu-id="c679b-222">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c679b-222">ColumnName</span></span>|<span data-ttu-id="c679b-223">Type de données</span><span class="sxs-lookup"><span data-stu-id="c679b-223">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c679b-224">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-224">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="c679b-225">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-225">String</span></span>|  
|<span data-ttu-id="c679b-226">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-226">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="c679b-227">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-227">String</span></span>|  
|<span data-ttu-id="c679b-228">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-228">PROCEDURE_NAME</span></span>|<span data-ttu-id="c679b-229">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-229">String</span></span>|  
|<span data-ttu-id="c679b-230">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-230">PARAMETER_NAME</span></span>|<span data-ttu-id="c679b-231">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-231">String</span></span>|  
|<span data-ttu-id="c679b-232">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c679b-232">ORDINAL_POSITION</span></span>|<span data-ttu-id="c679b-233">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-233">Int32</span></span>|  
|<span data-ttu-id="c679b-234">PARAMETER_TYPE</span><span class="sxs-lookup"><span data-stu-id="c679b-234">PARAMETER_TYPE</span></span>|<span data-ttu-id="c679b-235">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-235">Int32</span></span>|  
|<span data-ttu-id="c679b-236">PARAMETER_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="c679b-236">PARAMETER_HASDEFAULT</span></span>|<span data-ttu-id="c679b-237">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-237">Boolean</span></span>|  
|<span data-ttu-id="c679b-238">PARAMETER_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c679b-238">PARAMETER_DEFAULT</span></span>|<span data-ttu-id="c679b-239">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-239">String</span></span>|  
|<span data-ttu-id="c679b-240">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c679b-240">IS_NULLABLE</span></span>|<span data-ttu-id="c679b-241">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-241">Boolean</span></span>|  
|<span data-ttu-id="c679b-242">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c679b-242">DATA_TYPE</span></span>|<span data-ttu-id="c679b-243">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-243">Int32</span></span>|  
|<span data-ttu-id="c679b-244">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c679b-244">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="c679b-245">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-245">Int64</span></span>|  
|<span data-ttu-id="c679b-246">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c679b-246">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="c679b-247">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-247">Int64</span></span>|  
|<span data-ttu-id="c679b-248">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="c679b-248">NUMERIC_PRECISION</span></span>|<span data-ttu-id="c679b-249">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-249">Int32</span></span>|  
|<span data-ttu-id="c679b-250">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="c679b-250">NUMERIC_SCALE</span></span>|<span data-ttu-id="c679b-251">Int16</span><span class="sxs-lookup"><span data-stu-id="c679b-251">Int16</span></span>|  
|<span data-ttu-id="c679b-252">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c679b-252">DESCRIPTION</span></span>|<span data-ttu-id="c679b-253">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-253">String</span></span>|  
|<span data-ttu-id="c679b-254">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-254">TYPE_NAME</span></span>|<span data-ttu-id="c679b-255">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-255">String</span></span>|  
|<span data-ttu-id="c679b-256">LOCAL_TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-256">LOCAL_TYPE_NAME</span></span>|<span data-ttu-id="c679b-257">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-257">String</span></span>|  
  
### <a name="catalog"></a><span data-ttu-id="c679b-258">Catalogue</span><span class="sxs-lookup"><span data-stu-id="c679b-258">Catalog</span></span>  
  
|<span data-ttu-id="c679b-259">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c679b-259">ColumnName</span></span>|<span data-ttu-id="c679b-260">Type de données</span><span class="sxs-lookup"><span data-stu-id="c679b-260">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c679b-261">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-261">CATALOG_NAME</span></span>|<span data-ttu-id="c679b-262">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-262">String</span></span>|  
|<span data-ttu-id="c679b-263">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c679b-263">DESCRIPTION</span></span>|<span data-ttu-id="c679b-264">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-264">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="c679b-265">Index</span><span class="sxs-lookup"><span data-stu-id="c679b-265">Indexes</span></span>  
  
|<span data-ttu-id="c679b-266">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c679b-266">ColumnName</span></span>|<span data-ttu-id="c679b-267">Type de données</span><span class="sxs-lookup"><span data-stu-id="c679b-267">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c679b-268">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-268">TABLE_CATALOG</span></span>|<span data-ttu-id="c679b-269">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-269">String</span></span>|  
|<span data-ttu-id="c679b-270">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-270">TABLE_SCHEMA</span></span>|<span data-ttu-id="c679b-271">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-271">String</span></span>|  
|<span data-ttu-id="c679b-272">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-272">TABLE_NAME</span></span>|<span data-ttu-id="c679b-273">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-273">String</span></span>|  
|<span data-ttu-id="c679b-274">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-274">INDEX_CATALOG</span></span>|<span data-ttu-id="c679b-275">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-275">String</span></span>|  
|<span data-ttu-id="c679b-276">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-276">INDEX_SCHEMA</span></span>|<span data-ttu-id="c679b-277">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-277">String</span></span>|  
|<span data-ttu-id="c679b-278">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-278">INDEX_NAME</span></span>|<span data-ttu-id="c679b-279">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-279">String</span></span>|  
|<span data-ttu-id="c679b-280">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="c679b-280">PRIMARY_KEY</span></span>|<span data-ttu-id="c679b-281">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-281">Boolean</span></span>|  
|<span data-ttu-id="c679b-282">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="c679b-282">UNIQUE</span></span>|<span data-ttu-id="c679b-283">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-283">Boolean</span></span>|  
|<span data-ttu-id="c679b-284">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="c679b-284">CLUSTERED</span></span>|<span data-ttu-id="c679b-285">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-285">Boolean</span></span>|  
|<span data-ttu-id="c679b-286">TYPE</span><span class="sxs-lookup"><span data-stu-id="c679b-286">TYPE</span></span>|<span data-ttu-id="c679b-287">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-287">Int32</span></span>|  
|<span data-ttu-id="c679b-288">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="c679b-288">FILL_FACTOR</span></span>|<span data-ttu-id="c679b-289">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-289">Int32</span></span>|  
|<span data-ttu-id="c679b-290">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="c679b-290">INITIAL_SIZE</span></span>|<span data-ttu-id="c679b-291">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-291">Int32</span></span>|  
|<span data-ttu-id="c679b-292">NULLS</span><span class="sxs-lookup"><span data-stu-id="c679b-292">NULLS</span></span>|<span data-ttu-id="c679b-293">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-293">Int32</span></span>|  
|<span data-ttu-id="c679b-294">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c679b-294">SORT_BOOKMARKS</span></span>|<span data-ttu-id="c679b-295">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-295">Boolean</span></span>|  
|<span data-ttu-id="c679b-296">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="c679b-296">AUTO_UPDATE</span></span>|<span data-ttu-id="c679b-297">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-297">Boolean</span></span>|  
|<span data-ttu-id="c679b-298">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="c679b-298">NULL_COLLATION</span></span>|<span data-ttu-id="c679b-299">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-299">Int32</span></span>|  
|<span data-ttu-id="c679b-300">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c679b-300">ORDINAL_POSITION</span></span>|<span data-ttu-id="c679b-301">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-301">Int64</span></span>|  
|<span data-ttu-id="c679b-302">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-302">COLUMN_NAME</span></span>|<span data-ttu-id="c679b-303">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-303">String</span></span>|  
|<span data-ttu-id="c679b-304">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-304">COLUMN_GUID</span></span>|<span data-ttu-id="c679b-305">GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-305">Guid</span></span>|  
|<span data-ttu-id="c679b-306">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="c679b-306">COLUMN_PROPID</span></span>|<span data-ttu-id="c679b-307">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-307">Int64</span></span>|  
|<span data-ttu-id="c679b-308">COLLATION</span><span class="sxs-lookup"><span data-stu-id="c679b-308">COLLATION</span></span>|<span data-ttu-id="c679b-309">Int16</span><span class="sxs-lookup"><span data-stu-id="c679b-309">Int16</span></span>|  
|<span data-ttu-id="c679b-310">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="c679b-310">CARDINALITY</span></span>|<span data-ttu-id="c679b-311">Decimal</span><span class="sxs-lookup"><span data-stu-id="c679b-311">Decimal</span></span>|  
|<span data-ttu-id="c679b-312">PAGES</span><span class="sxs-lookup"><span data-stu-id="c679b-312">PAGES</span></span>|<span data-ttu-id="c679b-313">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-313">Int32</span></span>|  
|<span data-ttu-id="c679b-314">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="c679b-314">FILTER_CONDITION</span></span>|<span data-ttu-id="c679b-315">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-315">String</span></span>|  
|<span data-ttu-id="c679b-316">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="c679b-316">INTEGRATED</span></span>|<span data-ttu-id="c679b-317">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-317">Boolean</span></span>|  
  
## <a name="microsoft-oracle-ole-db-provider"></a><span data-ttu-id="c679b-318">Fournisseur Microsoft Oracle OLE DB</span><span class="sxs-lookup"><span data-stu-id="c679b-318">Microsoft Oracle OLE DB Provider</span></span>  
 <span data-ttu-id="c679b-319">Le pilote Microsoft Oracle OLE DB prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="c679b-319">The Microsoft Oracle OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="c679b-320">Tables</span><span class="sxs-lookup"><span data-stu-id="c679b-320">Tables</span></span>  
  
-   <span data-ttu-id="c679b-321">Colonnes</span><span class="sxs-lookup"><span data-stu-id="c679b-321">Columns</span></span>  
  
-   <span data-ttu-id="c679b-322">Procédures</span><span class="sxs-lookup"><span data-stu-id="c679b-322">Procedures</span></span>  
  
-   <span data-ttu-id="c679b-323">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="c679b-323">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="c679b-324">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="c679b-324">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="c679b-325">Affichages</span><span class="sxs-lookup"><span data-stu-id="c679b-325">Views</span></span>  
  
-   <span data-ttu-id="c679b-326">Index</span><span class="sxs-lookup"><span data-stu-id="c679b-326">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="c679b-327">Tables</span><span class="sxs-lookup"><span data-stu-id="c679b-327">Tables</span></span>  
  
|<span data-ttu-id="c679b-328">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c679b-328">ColumnName</span></span>|<span data-ttu-id="c679b-329">Type de données</span><span class="sxs-lookup"><span data-stu-id="c679b-329">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c679b-330">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-330">TABLE_CATALOG</span></span>|<span data-ttu-id="c679b-331">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-331">String</span></span>|  
|<span data-ttu-id="c679b-332">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-332">TABLE_SCHEMA</span></span>|<span data-ttu-id="c679b-333">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-333">String</span></span>|  
|<span data-ttu-id="c679b-334">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-334">TABLE_NAME</span></span>|<span data-ttu-id="c679b-335">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-335">String</span></span>|  
|<span data-ttu-id="c679b-336">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c679b-336">TABLE_TYPE</span></span>|<span data-ttu-id="c679b-337">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-337">String</span></span>|  
|<span data-ttu-id="c679b-338">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-338">TABLE_GUID</span></span>|<span data-ttu-id="c679b-339">GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-339">Guid</span></span>|  
|<span data-ttu-id="c679b-340">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c679b-340">DESCRIPTION</span></span>|<span data-ttu-id="c679b-341">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-341">String</span></span>|  
|<span data-ttu-id="c679b-342">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="c679b-342">TABLE_PROPID</span></span>|<span data-ttu-id="c679b-343">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-343">Int64</span></span>|  
|<span data-ttu-id="c679b-344">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="c679b-344">DATE_CREATED</span></span>|<span data-ttu-id="c679b-345">DateTime</span><span class="sxs-lookup"><span data-stu-id="c679b-345">DateTime</span></span>|  
|<span data-ttu-id="c679b-346">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="c679b-346">DATE_MODIFIED</span></span>|<span data-ttu-id="c679b-347">DateTime</span><span class="sxs-lookup"><span data-stu-id="c679b-347">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="c679b-348">Colonnes</span><span class="sxs-lookup"><span data-stu-id="c679b-348">Columns</span></span>  
  
|<span data-ttu-id="c679b-349">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c679b-349">ColumnName</span></span>|<span data-ttu-id="c679b-350">Type de données</span><span class="sxs-lookup"><span data-stu-id="c679b-350">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c679b-351">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-351">TABLE_CATALOG</span></span>|<span data-ttu-id="c679b-352">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-352">String</span></span>|  
|<span data-ttu-id="c679b-353">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-353">TABLE_SCHEMA</span></span>|<span data-ttu-id="c679b-354">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-354">String</span></span>|  
|<span data-ttu-id="c679b-355">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-355">TABLE_NAME</span></span>|<span data-ttu-id="c679b-356">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-356">String</span></span>|  
|<span data-ttu-id="c679b-357">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-357">COLUMN_NAME</span></span>|<span data-ttu-id="c679b-358">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-358">String</span></span>|  
|<span data-ttu-id="c679b-359">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-359">COLUMN_GUID</span></span>|<span data-ttu-id="c679b-360">GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-360">Guid</span></span>|  
|<span data-ttu-id="c679b-361">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="c679b-361">COLUMN_PROPID</span></span>|<span data-ttu-id="c679b-362">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-362">Int64</span></span>|  
|<span data-ttu-id="c679b-363">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c679b-363">ORDINAL_POSITION</span></span>|<span data-ttu-id="c679b-364">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-364">Int64</span></span>|  
|<span data-ttu-id="c679b-365">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="c679b-365">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="c679b-366">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-366">Boolean</span></span>|  
|<span data-ttu-id="c679b-367">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c679b-367">COLUMN_DEFAULT</span></span>|<span data-ttu-id="c679b-368">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-368">String</span></span>|  
|<span data-ttu-id="c679b-369">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="c679b-369">COLUMN_FLAGS</span></span>|<span data-ttu-id="c679b-370">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-370">Int64</span></span>|  
|<span data-ttu-id="c679b-371">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c679b-371">IS_NULLABLE</span></span>|<span data-ttu-id="c679b-372">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-372">Boolean</span></span>|  
|<span data-ttu-id="c679b-373">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c679b-373">DATA_TYPE</span></span>|<span data-ttu-id="c679b-374">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-374">Int32</span></span>|  
|<span data-ttu-id="c679b-375">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-375">TYPE_GUID</span></span>|<span data-ttu-id="c679b-376">GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-376">Guid</span></span>|  
|<span data-ttu-id="c679b-377">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c679b-377">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="c679b-378">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-378">Int64</span></span>|  
|<span data-ttu-id="c679b-379">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c679b-379">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="c679b-380">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-380">Int64</span></span>|  
|<span data-ttu-id="c679b-381">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="c679b-381">NUMERIC_PRECISION</span></span>|<span data-ttu-id="c679b-382">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-382">Int32</span></span>|  
|<span data-ttu-id="c679b-383">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="c679b-383">NUMERIC_SCALE</span></span>|<span data-ttu-id="c679b-384">Int16</span><span class="sxs-lookup"><span data-stu-id="c679b-384">Int16</span></span>|  
|<span data-ttu-id="c679b-385">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="c679b-385">DATETIME_PRECISION</span></span>|<span data-ttu-id="c679b-386">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-386">Int64</span></span>|  
|<span data-ttu-id="c679b-387">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-387">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="c679b-388">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-388">String</span></span>|  
|<span data-ttu-id="c679b-389">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-389">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="c679b-390">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-390">String</span></span>|  
|<span data-ttu-id="c679b-391">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-391">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="c679b-392">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-392">String</span></span>|  
|<span data-ttu-id="c679b-393">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-393">COLLATION_CATALOG</span></span>|<span data-ttu-id="c679b-394">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-394">String</span></span>|  
|<span data-ttu-id="c679b-395">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-395">COLLATION_SCHEMA</span></span>|<span data-ttu-id="c679b-396">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-396">String</span></span>|  
|<span data-ttu-id="c679b-397">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-397">COLLATION_NAME</span></span>|<span data-ttu-id="c679b-398">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-398">String</span></span>|  
|<span data-ttu-id="c679b-399">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-399">DOMAIN_CATALOG</span></span>|<span data-ttu-id="c679b-400">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-400">String</span></span>|  
|<span data-ttu-id="c679b-401">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-401">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="c679b-402">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-402">String</span></span>|  
|<span data-ttu-id="c679b-403">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-403">DOMAIN_NAME</span></span>|<span data-ttu-id="c679b-404">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-404">String</span></span>|  
|<span data-ttu-id="c679b-405">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c679b-405">DESCRIPTION</span></span>|<span data-ttu-id="c679b-406">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-406">String</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="c679b-407">Procédures</span><span class="sxs-lookup"><span data-stu-id="c679b-407">Procedures</span></span>  
  
|<span data-ttu-id="c679b-408">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c679b-408">ColumnName</span></span>|<span data-ttu-id="c679b-409">Type de données</span><span class="sxs-lookup"><span data-stu-id="c679b-409">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c679b-410">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-410">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="c679b-411">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-411">String</span></span>|  
|<span data-ttu-id="c679b-412">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-412">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="c679b-413">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-413">String</span></span>|  
|<span data-ttu-id="c679b-414">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-414">PROCEDURE_NAME</span></span>|<span data-ttu-id="c679b-415">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-415">String</span></span>|  
|<span data-ttu-id="c679b-416">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c679b-416">PROCEDURE_TYPE</span></span>|<span data-ttu-id="c679b-417">Int16</span><span class="sxs-lookup"><span data-stu-id="c679b-417">Int16</span></span>|  
|<span data-ttu-id="c679b-418">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="c679b-418">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="c679b-419">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-419">String</span></span>|  
|<span data-ttu-id="c679b-420">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c679b-420">DESCRIPTION</span></span>|<span data-ttu-id="c679b-421">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-421">String</span></span>|  
|<span data-ttu-id="c679b-422">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="c679b-422">DATE_CREATED</span></span>|<span data-ttu-id="c679b-423">DateTime</span><span class="sxs-lookup"><span data-stu-id="c679b-423">DateTime</span></span>|  
|<span data-ttu-id="c679b-424">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="c679b-424">DATE_MODIFIED</span></span>|<span data-ttu-id="c679b-425">DateTime</span><span class="sxs-lookup"><span data-stu-id="c679b-425">DateTime</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="c679b-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="c679b-426">ProcedureColumns</span></span>  
  
|<span data-ttu-id="c679b-427">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c679b-427">ColumnName</span></span>|<span data-ttu-id="c679b-428">Type de données</span><span class="sxs-lookup"><span data-stu-id="c679b-428">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c679b-429">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-429">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="c679b-430">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-430">String</span></span>|  
|<span data-ttu-id="c679b-431">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-431">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="c679b-432">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-432">String</span></span>|  
|<span data-ttu-id="c679b-433">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-433">PROCEDURE_NAME</span></span>|<span data-ttu-id="c679b-434">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-434">String</span></span>|  
|<span data-ttu-id="c679b-435">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-435">COLUMN_NAME</span></span>|<span data-ttu-id="c679b-436">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-436">String</span></span>|  
|<span data-ttu-id="c679b-437">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-437">COLUMN_GUID</span></span>|<span data-ttu-id="c679b-438">GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-438">Guid</span></span>|  
|<span data-ttu-id="c679b-439">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="c679b-439">COLUMN_PROPID</span></span>|<span data-ttu-id="c679b-440">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-440">Int64</span></span>|  
|<span data-ttu-id="c679b-441">ROWSET_NUMBER</span><span class="sxs-lookup"><span data-stu-id="c679b-441">ROWSET_NUMBER</span></span>|<span data-ttu-id="c679b-442">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-442">Int64</span></span>|  
|<span data-ttu-id="c679b-443">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c679b-443">ORDINAL_POSITION</span></span>|<span data-ttu-id="c679b-444">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-444">Int64</span></span>|  
|<span data-ttu-id="c679b-445">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c679b-445">IS_NULLABLE</span></span>|<span data-ttu-id="c679b-446">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-446">Boolean</span></span>|  
|<span data-ttu-id="c679b-447">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c679b-447">DATA_TYPE</span></span>|<span data-ttu-id="c679b-448">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-448">Int32</span></span>|  
|<span data-ttu-id="c679b-449">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-449">TYPE_GUID</span></span>|<span data-ttu-id="c679b-450">GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-450">Guid</span></span>|  
|<span data-ttu-id="c679b-451">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c679b-451">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="c679b-452">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-452">Int64</span></span>|  
|<span data-ttu-id="c679b-453">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c679b-453">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="c679b-454">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-454">Int64</span></span>|  
|<span data-ttu-id="c679b-455">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="c679b-455">NUMERIC_PRECISION</span></span>|<span data-ttu-id="c679b-456">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-456">Int32</span></span>|  
|<span data-ttu-id="c679b-457">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="c679b-457">NUMERIC_SCALE</span></span>|<span data-ttu-id="c679b-458">Int16</span><span class="sxs-lookup"><span data-stu-id="c679b-458">Int16</span></span>|  
|<span data-ttu-id="c679b-459">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c679b-459">DESCRIPTION</span></span>|<span data-ttu-id="c679b-460">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-460">String</span></span>|  
|<span data-ttu-id="c679b-461">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="c679b-461">OVERLOAD</span></span>|<span data-ttu-id="c679b-462">Int16</span><span class="sxs-lookup"><span data-stu-id="c679b-462">Int16</span></span>|  
  
### <a name="views"></a><span data-ttu-id="c679b-463">Affichages</span><span class="sxs-lookup"><span data-stu-id="c679b-463">Views</span></span>  
  
|<span data-ttu-id="c679b-464">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c679b-464">ColumnName</span></span>|<span data-ttu-id="c679b-465">Type de données</span><span class="sxs-lookup"><span data-stu-id="c679b-465">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c679b-466">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-466">TABLE_CATALOG</span></span>|<span data-ttu-id="c679b-467">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-467">String</span></span>|  
|<span data-ttu-id="c679b-468">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-468">TABLE_SCHEMA</span></span>|<span data-ttu-id="c679b-469">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-469">String</span></span>|  
|<span data-ttu-id="c679b-470">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-470">TABLE_NAME</span></span>|<span data-ttu-id="c679b-471">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-471">String</span></span>|  
|<span data-ttu-id="c679b-472">VIEW_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="c679b-472">VIEW_DEFINITION</span></span>|<span data-ttu-id="c679b-473">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-473">String</span></span>|  
|<span data-ttu-id="c679b-474">CHECK_OPTION</span><span class="sxs-lookup"><span data-stu-id="c679b-474">CHECK_OPTION</span></span>|<span data-ttu-id="c679b-475">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-475">Boolean</span></span>|  
|<span data-ttu-id="c679b-476">IS_UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="c679b-476">IS_UPDATABLE</span></span>|<span data-ttu-id="c679b-477">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-477">Boolean</span></span>|  
|<span data-ttu-id="c679b-478">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c679b-478">DESCRIPTION</span></span>|<span data-ttu-id="c679b-479">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-479">String</span></span>|  
|<span data-ttu-id="c679b-480">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="c679b-480">DATE_CREATED</span></span>|<span data-ttu-id="c679b-481">DateTime</span><span class="sxs-lookup"><span data-stu-id="c679b-481">DateTime</span></span>|  
|<span data-ttu-id="c679b-482">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="c679b-482">DATE_MODIFIED</span></span>|<span data-ttu-id="c679b-483">DateTime</span><span class="sxs-lookup"><span data-stu-id="c679b-483">DateTime</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="c679b-484">Index</span><span class="sxs-lookup"><span data-stu-id="c679b-484">Indexes</span></span>  
  
|<span data-ttu-id="c679b-485">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c679b-485">ColumnName</span></span>|<span data-ttu-id="c679b-486">Type de données</span><span class="sxs-lookup"><span data-stu-id="c679b-486">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c679b-487">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-487">TABLE_CATALOG</span></span>|<span data-ttu-id="c679b-488">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-488">String</span></span>|  
|<span data-ttu-id="c679b-489">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-489">TABLE_SCHEMA</span></span>|<span data-ttu-id="c679b-490">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-490">String</span></span>|  
|<span data-ttu-id="c679b-491">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-491">TABLE_NAME</span></span>|<span data-ttu-id="c679b-492">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-492">String</span></span>|  
|<span data-ttu-id="c679b-493">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-493">INDEX_CATALOG</span></span>|<span data-ttu-id="c679b-494">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-494">String</span></span>|  
|<span data-ttu-id="c679b-495">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-495">INDEX_SCHEMA</span></span>|<span data-ttu-id="c679b-496">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-496">String</span></span>|  
|<span data-ttu-id="c679b-497">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-497">INDEX_NAME</span></span>|<span data-ttu-id="c679b-498">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-498">String</span></span>|  
|<span data-ttu-id="c679b-499">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="c679b-499">PRIMARY_KEY</span></span>|<span data-ttu-id="c679b-500">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-500">Boolean</span></span>|  
|<span data-ttu-id="c679b-501">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="c679b-501">UNIQUE</span></span>|<span data-ttu-id="c679b-502">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-502">Boolean</span></span>|  
|<span data-ttu-id="c679b-503">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="c679b-503">CLUSTERED</span></span>|<span data-ttu-id="c679b-504">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-504">Boolean</span></span>|  
|<span data-ttu-id="c679b-505">TYPE</span><span class="sxs-lookup"><span data-stu-id="c679b-505">TYPE</span></span>|<span data-ttu-id="c679b-506">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-506">Int32</span></span>|  
|<span data-ttu-id="c679b-507">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="c679b-507">FILL_FACTOR</span></span>|<span data-ttu-id="c679b-508">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-508">Int32</span></span>|  
|<span data-ttu-id="c679b-509">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="c679b-509">INITIAL_SIZE</span></span>|<span data-ttu-id="c679b-510">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-510">Int32</span></span>|  
|<span data-ttu-id="c679b-511">NULLS</span><span class="sxs-lookup"><span data-stu-id="c679b-511">NULLS</span></span>|<span data-ttu-id="c679b-512">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-512">Int32</span></span>|  
|<span data-ttu-id="c679b-513">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c679b-513">SORT_BOOKMARKS</span></span>|<span data-ttu-id="c679b-514">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-514">Boolean</span></span>|  
|<span data-ttu-id="c679b-515">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="c679b-515">AUTO_UPDATE</span></span>|<span data-ttu-id="c679b-516">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-516">Boolean</span></span>|  
|<span data-ttu-id="c679b-517">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="c679b-517">NULL_COLLATION</span></span>|<span data-ttu-id="c679b-518">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-518">Int32</span></span>|  
|<span data-ttu-id="c679b-519">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c679b-519">ORDINAL_POSITION</span></span>|<span data-ttu-id="c679b-520">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-520">Int64</span></span>|  
|<span data-ttu-id="c679b-521">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-521">COLUMN_NAME</span></span>|<span data-ttu-id="c679b-522">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-522">String</span></span>|  
|<span data-ttu-id="c679b-523">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-523">COLUMN_GUID</span></span>|<span data-ttu-id="c679b-524">GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-524">Guid</span></span>|  
|<span data-ttu-id="c679b-525">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="c679b-525">COLUMN_PROPID</span></span>|<span data-ttu-id="c679b-526">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-526">Int64</span></span>|  
|<span data-ttu-id="c679b-527">COLLATION</span><span class="sxs-lookup"><span data-stu-id="c679b-527">COLLATION</span></span>|<span data-ttu-id="c679b-528">Int16</span><span class="sxs-lookup"><span data-stu-id="c679b-528">Int16</span></span>|  
|<span data-ttu-id="c679b-529">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="c679b-529">CARDINALITY</span></span>|<span data-ttu-id="c679b-530">Decimal</span><span class="sxs-lookup"><span data-stu-id="c679b-530">Decimal</span></span>|  
|<span data-ttu-id="c679b-531">PAGES</span><span class="sxs-lookup"><span data-stu-id="c679b-531">PAGES</span></span>|<span data-ttu-id="c679b-532">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-532">Int32</span></span>|  
|<span data-ttu-id="c679b-533">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="c679b-533">FILTER_CONDITION</span></span>|<span data-ttu-id="c679b-534">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-534">String</span></span>|  
|<span data-ttu-id="c679b-535">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="c679b-535">INTEGRATED</span></span>|<span data-ttu-id="c679b-536">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-536">Boolean</span></span>|  
  
## <a name="microsoft-jet-ole-db-provider"></a><span data-ttu-id="c679b-537">Fournisseur Microsoft Jet OLE DB</span><span class="sxs-lookup"><span data-stu-id="c679b-537">Microsoft Jet OLE DB Provider</span></span>  
 <span data-ttu-id="c679b-538">Le pilote Microsoft Jet OLE DB prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="c679b-538">The Microsoft Jet OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="c679b-539">Tables</span><span class="sxs-lookup"><span data-stu-id="c679b-539">Tables</span></span>  
  
-   <span data-ttu-id="c679b-540">Colonnes</span><span class="sxs-lookup"><span data-stu-id="c679b-540">Columns</span></span>  
  
-   <span data-ttu-id="c679b-541">Procédures</span><span class="sxs-lookup"><span data-stu-id="c679b-541">Procedures</span></span>  
  
-   <span data-ttu-id="c679b-542">Affichages</span><span class="sxs-lookup"><span data-stu-id="c679b-542">Views</span></span>  
  
-   <span data-ttu-id="c679b-543">Index</span><span class="sxs-lookup"><span data-stu-id="c679b-543">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="c679b-544">Tables</span><span class="sxs-lookup"><span data-stu-id="c679b-544">Tables</span></span>  
  
|<span data-ttu-id="c679b-545">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c679b-545">ColumnName</span></span>|<span data-ttu-id="c679b-546">Type de données</span><span class="sxs-lookup"><span data-stu-id="c679b-546">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c679b-547">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-547">TABLE_CATALOG</span></span>|<span data-ttu-id="c679b-548">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-548">String</span></span>|  
|<span data-ttu-id="c679b-549">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-549">TABLE_SCHEMA</span></span>|<span data-ttu-id="c679b-550">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-550">String</span></span>|  
|<span data-ttu-id="c679b-551">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-551">TABLE_NAME</span></span>|<span data-ttu-id="c679b-552">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-552">String</span></span>|  
|<span data-ttu-id="c679b-553">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c679b-553">TABLE_TYPE</span></span>|<span data-ttu-id="c679b-554">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-554">String</span></span>|  
|<span data-ttu-id="c679b-555">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-555">TABLE_GUID</span></span>|<span data-ttu-id="c679b-556">GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-556">Guid</span></span>|  
|<span data-ttu-id="c679b-557">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c679b-557">DESCRIPTION</span></span>|<span data-ttu-id="c679b-558">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-558">String</span></span>|  
|<span data-ttu-id="c679b-559">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="c679b-559">TABLE_PROPID</span></span>|<span data-ttu-id="c679b-560">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-560">Int64</span></span>|  
|<span data-ttu-id="c679b-561">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="c679b-561">DATE_CREATED</span></span>|<span data-ttu-id="c679b-562">DateTime</span><span class="sxs-lookup"><span data-stu-id="c679b-562">DateTime</span></span>|  
|<span data-ttu-id="c679b-563">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="c679b-563">DATE_MODIFIED</span></span>|<span data-ttu-id="c679b-564">DateTime</span><span class="sxs-lookup"><span data-stu-id="c679b-564">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="c679b-565">Colonnes</span><span class="sxs-lookup"><span data-stu-id="c679b-565">Columns</span></span>  
  
|<span data-ttu-id="c679b-566">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c679b-566">ColumnName</span></span>|<span data-ttu-id="c679b-567">Type de données</span><span class="sxs-lookup"><span data-stu-id="c679b-567">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c679b-568">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-568">TABLE_CATALOG</span></span>|<span data-ttu-id="c679b-569">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-569">String</span></span>|  
|<span data-ttu-id="c679b-570">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-570">TABLE_SCHEMA</span></span>|<span data-ttu-id="c679b-571">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-571">String</span></span>|  
|<span data-ttu-id="c679b-572">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-572">TABLE_NAME</span></span>|<span data-ttu-id="c679b-573">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-573">String</span></span>|  
|<span data-ttu-id="c679b-574">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-574">COLUMN_NAME</span></span>|<span data-ttu-id="c679b-575">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-575">String</span></span>|  
|<span data-ttu-id="c679b-576">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-576">COLUMN_GUID</span></span>|<span data-ttu-id="c679b-577">GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-577">Guid</span></span>|  
|<span data-ttu-id="c679b-578">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="c679b-578">COLUMN_PROPID</span></span>|<span data-ttu-id="c679b-579">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-579">Int64</span></span>|  
|<span data-ttu-id="c679b-580">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c679b-580">ORDINAL_POSITION</span></span>|<span data-ttu-id="c679b-581">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-581">Int64</span></span>|  
|<span data-ttu-id="c679b-582">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="c679b-582">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="c679b-583">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-583">Boolean</span></span>|  
|<span data-ttu-id="c679b-584">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c679b-584">COLUMN_DEFAULT</span></span>|<span data-ttu-id="c679b-585">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-585">String</span></span>|  
|<span data-ttu-id="c679b-586">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="c679b-586">COLUMN_FLAGS</span></span>|<span data-ttu-id="c679b-587">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-587">Int64</span></span>|  
|<span data-ttu-id="c679b-588">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c679b-588">IS_NULLABLE</span></span>|<span data-ttu-id="c679b-589">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-589">Boolean</span></span>|  
|<span data-ttu-id="c679b-590">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c679b-590">DATA_TYPE</span></span>|<span data-ttu-id="c679b-591">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-591">Int32</span></span>|  
|<span data-ttu-id="c679b-592">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-592">TYPE_GUID</span></span>|<span data-ttu-id="c679b-593">GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-593">Guid</span></span>|  
|<span data-ttu-id="c679b-594">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c679b-594">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="c679b-595">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-595">Int64</span></span>|  
|<span data-ttu-id="c679b-596">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c679b-596">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="c679b-597">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-597">Int64</span></span>|  
|<span data-ttu-id="c679b-598">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="c679b-598">NUMERIC_PRECISION</span></span>|<span data-ttu-id="c679b-599">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-599">Int32</span></span>|  
|<span data-ttu-id="c679b-600">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="c679b-600">NUMERIC_SCALE</span></span>|<span data-ttu-id="c679b-601">Int16</span><span class="sxs-lookup"><span data-stu-id="c679b-601">Int16</span></span>|  
|<span data-ttu-id="c679b-602">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="c679b-602">DATETIME_PRECISION</span></span>|<span data-ttu-id="c679b-603">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-603">Int64</span></span>|  
|<span data-ttu-id="c679b-604">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-604">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="c679b-605">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-605">String</span></span>|  
|<span data-ttu-id="c679b-606">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-606">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="c679b-607">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-607">String</span></span>|  
|<span data-ttu-id="c679b-608">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-608">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="c679b-609">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-609">String</span></span>|  
|<span data-ttu-id="c679b-610">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-610">COLLATION_CATALOG</span></span>|<span data-ttu-id="c679b-611">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-611">String</span></span>|  
|<span data-ttu-id="c679b-612">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-612">COLLATION_SCHEMA</span></span>|<span data-ttu-id="c679b-613">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-613">String</span></span>|  
|<span data-ttu-id="c679b-614">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-614">COLLATION_NAME</span></span>|<span data-ttu-id="c679b-615">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-615">String</span></span>|  
|<span data-ttu-id="c679b-616">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-616">DOMAIN_CATALOG</span></span>|<span data-ttu-id="c679b-617">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-617">String</span></span>|  
|<span data-ttu-id="c679b-618">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-618">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="c679b-619">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-619">String</span></span>|  
|<span data-ttu-id="c679b-620">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-620">DOMAIN_NAME</span></span>|<span data-ttu-id="c679b-621">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-621">String</span></span>|  
|<span data-ttu-id="c679b-622">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c679b-622">DESCRIPTION</span></span>|<span data-ttu-id="c679b-623">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-623">String</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="c679b-624">Procédures</span><span class="sxs-lookup"><span data-stu-id="c679b-624">Procedures</span></span>  
  
|<span data-ttu-id="c679b-625">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c679b-625">ColumnName</span></span>|<span data-ttu-id="c679b-626">Type de données</span><span class="sxs-lookup"><span data-stu-id="c679b-626">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c679b-627">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-627">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="c679b-628">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-628">String</span></span>|  
|<span data-ttu-id="c679b-629">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-629">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="c679b-630">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-630">String</span></span>|  
|<span data-ttu-id="c679b-631">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-631">PROCEDURE_NAME</span></span>|<span data-ttu-id="c679b-632">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-632">String</span></span>|  
|<span data-ttu-id="c679b-633">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c679b-633">PROCEDURE_TYPE</span></span>|<span data-ttu-id="c679b-634">Int16</span><span class="sxs-lookup"><span data-stu-id="c679b-634">Int16</span></span>|  
|<span data-ttu-id="c679b-635">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="c679b-635">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="c679b-636">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-636">String</span></span>|  
|<span data-ttu-id="c679b-637">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c679b-637">DESCRIPTION</span></span>|<span data-ttu-id="c679b-638">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-638">String</span></span>|  
|<span data-ttu-id="c679b-639">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="c679b-639">DATE_CREATED</span></span>|<span data-ttu-id="c679b-640">DateTime</span><span class="sxs-lookup"><span data-stu-id="c679b-640">DateTime</span></span>|  
|<span data-ttu-id="c679b-641">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="c679b-641">DATE_MODIFIED</span></span>|<span data-ttu-id="c679b-642">DateTime</span><span class="sxs-lookup"><span data-stu-id="c679b-642">DateTime</span></span>|  
  
### <a name="views"></a><span data-ttu-id="c679b-643">Affichages</span><span class="sxs-lookup"><span data-stu-id="c679b-643">Views</span></span>  
  
|<span data-ttu-id="c679b-644">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c679b-644">ColumnName</span></span>|<span data-ttu-id="c679b-645">Type de données</span><span class="sxs-lookup"><span data-stu-id="c679b-645">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c679b-646">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-646">TABLE_CATALOG</span></span>|<span data-ttu-id="c679b-647">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-647">String</span></span>|  
|<span data-ttu-id="c679b-648">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-648">TABLE_SCHEMA</span></span>|<span data-ttu-id="c679b-649">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-649">String</span></span>|  
|<span data-ttu-id="c679b-650">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-650">TABLE_NAME</span></span>|<span data-ttu-id="c679b-651">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-651">String</span></span>|  
|<span data-ttu-id="c679b-652">VIEW_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="c679b-652">VIEW_DEFINITION</span></span>|<span data-ttu-id="c679b-653">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-653">String</span></span>|  
|<span data-ttu-id="c679b-654">CHECK_OPTION</span><span class="sxs-lookup"><span data-stu-id="c679b-654">CHECK_OPTION</span></span>|<span data-ttu-id="c679b-655">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-655">Boolean</span></span>|  
|<span data-ttu-id="c679b-656">IS_UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="c679b-656">IS_UPDATABLE</span></span>|<span data-ttu-id="c679b-657">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-657">Boolean</span></span>|  
|<span data-ttu-id="c679b-658">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c679b-658">DESCRIPTION</span></span>|<span data-ttu-id="c679b-659">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-659">String</span></span>|  
|<span data-ttu-id="c679b-660">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="c679b-660">DATE_CREATED</span></span>|<span data-ttu-id="c679b-661">DateTime</span><span class="sxs-lookup"><span data-stu-id="c679b-661">DateTime</span></span>|  
|<span data-ttu-id="c679b-662">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="c679b-662">DATE_MODIFIED</span></span>|<span data-ttu-id="c679b-663">DateTime</span><span class="sxs-lookup"><span data-stu-id="c679b-663">DateTime</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="c679b-664">Index</span><span class="sxs-lookup"><span data-stu-id="c679b-664">Indexes</span></span>  
  
|<span data-ttu-id="c679b-665">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c679b-665">ColumnName</span></span>|<span data-ttu-id="c679b-666">Type de données</span><span class="sxs-lookup"><span data-stu-id="c679b-666">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c679b-667">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-667">TABLE_CATALOG</span></span>|<span data-ttu-id="c679b-668">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-668">String</span></span>|  
|<span data-ttu-id="c679b-669">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-669">TABLE_SCHEMA</span></span>|<span data-ttu-id="c679b-670">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-670">String</span></span>|  
|<span data-ttu-id="c679b-671">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-671">TABLE_NAME</span></span>|<span data-ttu-id="c679b-672">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-672">String</span></span>|  
|<span data-ttu-id="c679b-673">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c679b-673">INDEX_CATALOG</span></span>|<span data-ttu-id="c679b-674">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-674">String</span></span>|  
|<span data-ttu-id="c679b-675">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c679b-675">INDEX_SCHEMA</span></span>|<span data-ttu-id="c679b-676">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-676">String</span></span>|  
|<span data-ttu-id="c679b-677">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-677">INDEX_NAME</span></span>|<span data-ttu-id="c679b-678">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-678">String</span></span>|  
|<span data-ttu-id="c679b-679">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="c679b-679">PRIMARY_KEY</span></span>|<span data-ttu-id="c679b-680">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-680">Boolean</span></span>|  
|<span data-ttu-id="c679b-681">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="c679b-681">UNIQUE</span></span>|<span data-ttu-id="c679b-682">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-682">Boolean</span></span>|  
|<span data-ttu-id="c679b-683">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="c679b-683">CLUSTERED</span></span>|<span data-ttu-id="c679b-684">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-684">Boolean</span></span>|  
|<span data-ttu-id="c679b-685">TYPE</span><span class="sxs-lookup"><span data-stu-id="c679b-685">TYPE</span></span>|<span data-ttu-id="c679b-686">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-686">Int32</span></span>|  
|<span data-ttu-id="c679b-687">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="c679b-687">FILL_FACTOR</span></span>|<span data-ttu-id="c679b-688">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-688">Int32</span></span>|  
|<span data-ttu-id="c679b-689">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="c679b-689">INITIAL_SIZE</span></span>|<span data-ttu-id="c679b-690">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-690">Int32</span></span>|  
|<span data-ttu-id="c679b-691">NULLS</span><span class="sxs-lookup"><span data-stu-id="c679b-691">NULLS</span></span>|<span data-ttu-id="c679b-692">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-692">Int32</span></span>|  
|<span data-ttu-id="c679b-693">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c679b-693">SORT_BOOKMARKS</span></span>|<span data-ttu-id="c679b-694">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-694">Boolean</span></span>|  
|<span data-ttu-id="c679b-695">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="c679b-695">AUTO_UPDATE</span></span>|<span data-ttu-id="c679b-696">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-696">Boolean</span></span>|  
|<span data-ttu-id="c679b-697">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="c679b-697">NULL_COLLATION</span></span>|<span data-ttu-id="c679b-698">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-698">Int32</span></span>|  
|<span data-ttu-id="c679b-699">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c679b-699">ORDINAL_POSITION</span></span>|<span data-ttu-id="c679b-700">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-700">Int64</span></span>|  
|<span data-ttu-id="c679b-701">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c679b-701">COLUMN_NAME</span></span>|<span data-ttu-id="c679b-702">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-702">String</span></span>|  
|<span data-ttu-id="c679b-703">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-703">COLUMN_GUID</span></span>|<span data-ttu-id="c679b-704">GUID</span><span class="sxs-lookup"><span data-stu-id="c679b-704">Guid</span></span>|  
|<span data-ttu-id="c679b-705">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="c679b-705">COLUMN_PROPID</span></span>|<span data-ttu-id="c679b-706">Int64</span><span class="sxs-lookup"><span data-stu-id="c679b-706">Int64</span></span>|  
|<span data-ttu-id="c679b-707">COLLATION</span><span class="sxs-lookup"><span data-stu-id="c679b-707">COLLATION</span></span>|<span data-ttu-id="c679b-708">Int16</span><span class="sxs-lookup"><span data-stu-id="c679b-708">Int16</span></span>|  
|<span data-ttu-id="c679b-709">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="c679b-709">CARDINALITY</span></span>|<span data-ttu-id="c679b-710">Decimal</span><span class="sxs-lookup"><span data-stu-id="c679b-710">Decimal</span></span>|  
|<span data-ttu-id="c679b-711">PAGES</span><span class="sxs-lookup"><span data-stu-id="c679b-711">PAGES</span></span>|<span data-ttu-id="c679b-712">Int32</span><span class="sxs-lookup"><span data-stu-id="c679b-712">Int32</span></span>|  
|<span data-ttu-id="c679b-713">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="c679b-713">FILTER_CONDITION</span></span>|<span data-ttu-id="c679b-714">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c679b-714">String</span></span>|  
|<span data-ttu-id="c679b-715">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="c679b-715">INTEGRATED</span></span>|<span data-ttu-id="c679b-716">Booléen</span><span class="sxs-lookup"><span data-stu-id="c679b-716">Boolean</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c679b-717">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c679b-717">See also</span></span>

- [<span data-ttu-id="c679b-718">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="c679b-718">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
