---
title: Collections de schémas ODBC
ms.date: 03/30/2017
ms.assetid: 1bb126a5-ceec-4649-a4bc-8aa19e801046
ms.openlocfilehash: 072a9cd365031cd5660d1824bc229d459abc5af8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54525831"
---
# <a name="odbc-schema-collections"></a><span data-ttu-id="119cd-102">Collections de schémas ODBC</span><span class="sxs-lookup"><span data-stu-id="119cd-102">ODBC Schema Collections</span></span>
<span data-ttu-id="119cd-103">Cette section traite de la prise en charge des collections de schémas pour les pilotes ODBC Microsoft SQL Server, Oracle et Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="119cd-103">This section discusses schema collection support for the ODBC drivers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-odbc-driver"></a><span data-ttu-id="119cd-104">Pilote Microsoft SQL Server ODBC</span><span class="sxs-lookup"><span data-stu-id="119cd-104">Microsoft SQL Server ODBC Driver</span></span>  
 <span data-ttu-id="119cd-105">Le pilote ODBC de Microsoft SQL Server prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="119cd-105">The Microsoft SQL Server ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="119cd-106">Tables</span><span class="sxs-lookup"><span data-stu-id="119cd-106">Tables</span></span>  
  
-   <span data-ttu-id="119cd-107">Index</span><span class="sxs-lookup"><span data-stu-id="119cd-107">Indexes</span></span>  
  
-   <span data-ttu-id="119cd-108">Columns</span><span class="sxs-lookup"><span data-stu-id="119cd-108">Columns</span></span>  
  
-   <span data-ttu-id="119cd-109">Procédures</span><span class="sxs-lookup"><span data-stu-id="119cd-109">Procedures</span></span>  
  
-   <span data-ttu-id="119cd-110">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="119cd-110">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="119cd-111">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="119cd-111">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="119cd-112">Vues</span><span class="sxs-lookup"><span data-stu-id="119cd-112">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="119cd-113">Tables et vues</span><span class="sxs-lookup"><span data-stu-id="119cd-113">Tables and Views</span></span>  
  
|<span data-ttu-id="119cd-114">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="119cd-114">ColumnName</span></span>|<span data-ttu-id="119cd-115">Type de données</span><span class="sxs-lookup"><span data-stu-id="119cd-115">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="119cd-116">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="119cd-116">TABLE_CAT</span></span>|<span data-ttu-id="119cd-117">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-117">String</span></span>|  
|<span data-ttu-id="119cd-118">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="119cd-118">TABLE_SCHEM</span></span>|<span data-ttu-id="119cd-119">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-119">String</span></span>|  
|<span data-ttu-id="119cd-120">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-120">TABLE_NAME</span></span>|<span data-ttu-id="119cd-121">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-121">String</span></span>|  
|<span data-ttu-id="119cd-122">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-122">TABLE_TYPE</span></span>|<span data-ttu-id="119cd-123">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-123">String</span></span>|  
|<span data-ttu-id="119cd-124">REMARKS</span><span class="sxs-lookup"><span data-stu-id="119cd-124">REMARKS</span></span>|<span data-ttu-id="119cd-125">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-125">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="119cd-126">Index</span><span class="sxs-lookup"><span data-stu-id="119cd-126">Indexes</span></span>  
  
|<span data-ttu-id="119cd-127">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="119cd-127">ColumnName</span></span>|<span data-ttu-id="119cd-128">Type de données</span><span class="sxs-lookup"><span data-stu-id="119cd-128">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="119cd-129">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="119cd-129">TABLE_CAT</span></span>|<span data-ttu-id="119cd-130">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-130">String</span></span>|  
|<span data-ttu-id="119cd-131">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="119cd-131">TABLE_SCHEM</span></span>|<span data-ttu-id="119cd-132">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-132">String</span></span>|  
|<span data-ttu-id="119cd-133">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-133">TABLE_NAME</span></span>|<span data-ttu-id="119cd-134">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-134">String</span></span>|  
|<span data-ttu-id="119cd-135">NON_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="119cd-135">NON_UNIQUE</span></span>|<span data-ttu-id="119cd-136">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-136">Int16</span></span>|  
|<span data-ttu-id="119cd-137">INDEX_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="119cd-137">INDEX_QUALIFIER</span></span>|<span data-ttu-id="119cd-138">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-138">String</span></span>|  
|<span data-ttu-id="119cd-139">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-139">INDEX_NAME</span></span>|<span data-ttu-id="119cd-140">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-140">String</span></span>|  
|<span data-ttu-id="119cd-141">TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-141">TYPE</span></span>|<span data-ttu-id="119cd-142">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-142">Int16</span></span>|  
|<span data-ttu-id="119cd-143">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="119cd-143">ORDINAL_POSITION</span></span>|<span data-ttu-id="119cd-144">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-144">Int16</span></span>|  
|<span data-ttu-id="119cd-145">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-145">COLUMN_NAME</span></span>|<span data-ttu-id="119cd-146">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-146">String</span></span>|  
|<span data-ttu-id="119cd-147">ASC_OR_DESC</span><span class="sxs-lookup"><span data-stu-id="119cd-147">ASC_OR_DESC</span></span>|<span data-ttu-id="119cd-148">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-148">String</span></span>|  
|<span data-ttu-id="119cd-149">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="119cd-149">CARDINATLITY</span></span>|<span data-ttu-id="119cd-150">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-150">Int32</span></span>|  
|<span data-ttu-id="119cd-151">PAGES</span><span class="sxs-lookup"><span data-stu-id="119cd-151">PAGES</span></span>|<span data-ttu-id="119cd-152">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-152">Int32</span></span>|  
|<span data-ttu-id="119cd-153">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="119cd-153">FILTER_CONDITION</span></span>|<span data-ttu-id="119cd-154">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-154">String</span></span>|  
|<span data-ttu-id="119cd-155">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="119cd-155">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="119cd-156">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-156">String</span></span>|  
|<span data-ttu-id="119cd-157">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-157">SS_DATA_TYPE</span></span>|<span data-ttu-id="119cd-158">Byte</span><span class="sxs-lookup"><span data-stu-id="119cd-158">Byte</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="119cd-159">Columns</span><span class="sxs-lookup"><span data-stu-id="119cd-159">Columns</span></span>  
  
|<span data-ttu-id="119cd-160">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="119cd-160">ColumnName</span></span>|<span data-ttu-id="119cd-161">Type de données</span><span class="sxs-lookup"><span data-stu-id="119cd-161">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="119cd-162">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="119cd-162">TABLE_CAT</span></span>|<span data-ttu-id="119cd-163">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-163">String</span></span>|  
|<span data-ttu-id="119cd-164">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="119cd-164">TABLE_SCHEM</span></span>|<span data-ttu-id="119cd-165">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-165">String</span></span>|  
|<span data-ttu-id="119cd-166">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-166">TABLE_NAME</span></span>|<span data-ttu-id="119cd-167">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-167">String</span></span>|  
|<span data-ttu-id="119cd-168">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-168">COLUMN_NAME</span></span>|<span data-ttu-id="119cd-169">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-169">String</span></span>|  
|<span data-ttu-id="119cd-170">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-170">DATA_TYPE</span></span>|<span data-ttu-id="119cd-171">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-171">Int16</span></span>|  
|<span data-ttu-id="119cd-172">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-172">TYPE_NAME</span></span>|<span data-ttu-id="119cd-173">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-173">String</span></span>|  
|<span data-ttu-id="119cd-174">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="119cd-174">COLUMN_SIZE</span></span>|<span data-ttu-id="119cd-175">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-175">Int32</span></span>|  
|<span data-ttu-id="119cd-176">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="119cd-176">BUFFER_LENGTH</span></span>|<span data-ttu-id="119cd-177">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-177">Int32</span></span>|  
|<span data-ttu-id="119cd-178">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="119cd-178">DECIMAL_DIGITS</span></span>|<span data-ttu-id="119cd-179">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-179">Int16</span></span>|  
|<span data-ttu-id="119cd-180">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="119cd-180">NUM_PREC_RADIX</span></span>|<span data-ttu-id="119cd-181">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-181">Int16</span></span>|  
|<span data-ttu-id="119cd-182">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="119cd-182">NULLABLE</span></span>|<span data-ttu-id="119cd-183">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-183">Int16</span></span>|  
|<span data-ttu-id="119cd-184">REMARKS</span><span class="sxs-lookup"><span data-stu-id="119cd-184">REMARKS</span></span>|<span data-ttu-id="119cd-185">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-185">String</span></span>|  
|<span data-ttu-id="119cd-186">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="119cd-186">COLUMN_DEF</span></span>|<span data-ttu-id="119cd-187">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-187">String</span></span>|  
|<span data-ttu-id="119cd-188">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-188">SQL_DATA_TYPE</span></span>|<span data-ttu-id="119cd-189">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-189">Int16</span></span>|  
|<span data-ttu-id="119cd-190">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="119cd-190">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="119cd-191">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-191">Int16</span></span>|  
|<span data-ttu-id="119cd-192">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="119cd-192">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="119cd-193">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-193">Int32</span></span>|  
|<span data-ttu-id="119cd-194">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="119cd-194">ORDINAL_POSITION</span></span>|<span data-ttu-id="119cd-195">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-195">Int32</span></span>|  
|<span data-ttu-id="119cd-196">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="119cd-196">IS_NULLABLE</span></span>|<span data-ttu-id="119cd-197">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-197">String</span></span>|  
|<span data-ttu-id="119cd-198">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="119cd-198">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="119cd-199">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-199">String</span></span>|  
|<span data-ttu-id="119cd-200">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="119cd-200">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="119cd-201">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-201">String</span></span>|  
|<span data-ttu-id="119cd-202">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-202">SS_DATA_TYPE</span></span>|<span data-ttu-id="119cd-203">Byte</span><span class="sxs-lookup"><span data-stu-id="119cd-203">Byte</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="119cd-204">Procédures</span><span class="sxs-lookup"><span data-stu-id="119cd-204">Procedures</span></span>  
  
|<span data-ttu-id="119cd-205">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="119cd-205">ColumnName</span></span>|<span data-ttu-id="119cd-206">Type de données</span><span class="sxs-lookup"><span data-stu-id="119cd-206">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="119cd-207">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="119cd-207">PROCEDURE_CAT</span></span>|<span data-ttu-id="119cd-208">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-208">String</span></span>|  
|<span data-ttu-id="119cd-209">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="119cd-209">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="119cd-210">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-210">String</span></span>|  
|<span data-ttu-id="119cd-211">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-211">PROCEDURE_NAME</span></span>|<span data-ttu-id="119cd-212">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-212">String</span></span>|  
|<span data-ttu-id="119cd-213">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="119cd-213">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="119cd-214">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-214">Int32</span></span>|  
|<span data-ttu-id="119cd-215">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="119cd-215">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="119cd-216">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-216">Int32</span></span>|  
|<span data-ttu-id="119cd-217">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="119cd-217">NUM_RESULT_SETS</span></span>|<span data-ttu-id="119cd-218">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-218">Int32</span></span>|  
|<span data-ttu-id="119cd-219">REMARKS</span><span class="sxs-lookup"><span data-stu-id="119cd-219">REMARKS</span></span>|<span data-ttu-id="119cd-220">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-220">String</span></span>|  
|<span data-ttu-id="119cd-221">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-221">PROCEDURE_TYPE</span></span>|<span data-ttu-id="119cd-222">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-222">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="119cd-223">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="119cd-223">ProcedureColumns</span></span>  
  
|<span data-ttu-id="119cd-224">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="119cd-224">ColumnName</span></span>|<span data-ttu-id="119cd-225">Type de données</span><span class="sxs-lookup"><span data-stu-id="119cd-225">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="119cd-226">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="119cd-226">PROCEDURE_CAT</span></span>|<span data-ttu-id="119cd-227">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-227">String</span></span>|  
|<span data-ttu-id="119cd-228">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="119cd-228">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="119cd-229">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-229">String</span></span>|  
|<span data-ttu-id="119cd-230">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-230">PROCEDURE_NAME</span></span>|<span data-ttu-id="119cd-231">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-231">String</span></span>|  
|<span data-ttu-id="119cd-232">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-232">COLUMN_NAME</span></span>|<span data-ttu-id="119cd-233">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-233">String</span></span>|  
|<span data-ttu-id="119cd-234">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-234">COLUMN_TYPE</span></span>|<span data-ttu-id="119cd-235">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-235">Int16</span></span>|  
|<span data-ttu-id="119cd-236">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-236">DATA_TYPE</span></span>|<span data-ttu-id="119cd-237">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-237">Int16</span></span>|  
|<span data-ttu-id="119cd-238">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-238">TYPE_NAME</span></span>|<span data-ttu-id="119cd-239">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-239">String</span></span>|  
|<span data-ttu-id="119cd-240">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="119cd-240">COLUMN_SIZE</span></span>|<span data-ttu-id="119cd-241">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-241">Int32</span></span>|  
|<span data-ttu-id="119cd-242">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="119cd-242">BUFFER_LENGTH</span></span>|<span data-ttu-id="119cd-243">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-243">Int32</span></span>|  
|<span data-ttu-id="119cd-244">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="119cd-244">DECIMAL_DIGITS</span></span>|<span data-ttu-id="119cd-245">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-245">Int16</span></span>|  
|<span data-ttu-id="119cd-246">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="119cd-246">NUM_PREC_RADIX</span></span>|<span data-ttu-id="119cd-247">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-247">Int16</span></span>|  
|<span data-ttu-id="119cd-248">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="119cd-248">NULLABLE</span></span>|<span data-ttu-id="119cd-249">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-249">Int16</span></span>|  
|<span data-ttu-id="119cd-250">REMARKS</span><span class="sxs-lookup"><span data-stu-id="119cd-250">REMARKS</span></span>|<span data-ttu-id="119cd-251">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-251">String</span></span>|  
|<span data-ttu-id="119cd-252">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="119cd-252">COLUMN_DEF</span></span>|<span data-ttu-id="119cd-253">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-253">String</span></span>|  
|<span data-ttu-id="119cd-254">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-254">SQL_DATA_TYPE</span></span>|<span data-ttu-id="119cd-255">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-255">Int16</span></span>|  
|<span data-ttu-id="119cd-256">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="119cd-256">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="119cd-257">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-257">Int16</span></span>|  
|<span data-ttu-id="119cd-258">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="119cd-258">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="119cd-259">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-259">Int32</span></span>|  
|<span data-ttu-id="119cd-260">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="119cd-260">ORDINAL_POSITION</span></span>|<span data-ttu-id="119cd-261">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-261">Int32</span></span>|  
|<span data-ttu-id="119cd-262">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="119cd-262">IS_NULLABLE</span></span>|<span data-ttu-id="119cd-263">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-263">String</span></span>|  
|<span data-ttu-id="119cd-264">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="119cd-264">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="119cd-265">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-265">String</span></span>|  
|<span data-ttu-id="119cd-266">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="119cd-266">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="119cd-267">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-267">String</span></span>|  
|<span data-ttu-id="119cd-268">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-268">SS_DATA_TYPE</span></span>|<span data-ttu-id="119cd-269">Byte</span><span class="sxs-lookup"><span data-stu-id="119cd-269">Byte</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="119cd-270">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="119cd-270">ProcedureParameters</span></span>  
  
|<span data-ttu-id="119cd-271">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="119cd-271">ColumnName</span></span>|<span data-ttu-id="119cd-272">Type de données</span><span class="sxs-lookup"><span data-stu-id="119cd-272">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="119cd-273">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="119cd-273">PROCEDURE_CAT</span></span>|<span data-ttu-id="119cd-274">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-274">String</span></span>|  
|<span data-ttu-id="119cd-275">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="119cd-275">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="119cd-276">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-276">String</span></span>|  
|<span data-ttu-id="119cd-277">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-277">PROCEDURE_NAME</span></span>|<span data-ttu-id="119cd-278">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-278">String</span></span>|  
|<span data-ttu-id="119cd-279">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-279">COLUMN_NAME</span></span>|<span data-ttu-id="119cd-280">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-280">String</span></span>|  
|<span data-ttu-id="119cd-281">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-281">COLUMN_TYPE</span></span>|<span data-ttu-id="119cd-282">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-282">Int16</span></span>|  
|<span data-ttu-id="119cd-283">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-283">DATA_TYPE</span></span>|<span data-ttu-id="119cd-284">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-284">Int16</span></span>|  
|<span data-ttu-id="119cd-285">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-285">TYPE_NAME</span></span>|<span data-ttu-id="119cd-286">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-286">String</span></span>|  
|<span data-ttu-id="119cd-287">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="119cd-287">COLUMN_SIZE</span></span>|<span data-ttu-id="119cd-288">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-288">Int32</span></span>|  
|<span data-ttu-id="119cd-289">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="119cd-289">BUFFER_LENGTH</span></span>|<span data-ttu-id="119cd-290">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-290">Int32</span></span>|  
|<span data-ttu-id="119cd-291">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="119cd-291">DECIMAL_DIGITS</span></span>|<span data-ttu-id="119cd-292">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-292">Int16</span></span>|  
|<span data-ttu-id="119cd-293">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="119cd-293">NUM_PREC_RADIX</span></span>|<span data-ttu-id="119cd-294">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-294">Int16</span></span>|  
|<span data-ttu-id="119cd-295">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="119cd-295">NULLABLE</span></span>|<span data-ttu-id="119cd-296">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-296">Int16</span></span>|  
|<span data-ttu-id="119cd-297">REMARKS</span><span class="sxs-lookup"><span data-stu-id="119cd-297">REMARKS</span></span>|<span data-ttu-id="119cd-298">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-298">String</span></span>|  
|<span data-ttu-id="119cd-299">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="119cd-299">COLUMN_DEF</span></span>|<span data-ttu-id="119cd-300">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-300">String</span></span>|  
|<span data-ttu-id="119cd-301">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-301">SQL_DATA_TYPE</span></span>|<span data-ttu-id="119cd-302">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-302">Int16</span></span>|  
|<span data-ttu-id="119cd-303">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="119cd-303">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="119cd-304">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-304">Int16</span></span>|  
|<span data-ttu-id="119cd-305">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="119cd-305">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="119cd-306">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-306">Int32</span></span>|  
|<span data-ttu-id="119cd-307">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="119cd-307">ORDINAL_POSITION</span></span>|<span data-ttu-id="119cd-308">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-308">Int32</span></span>|  
|<span data-ttu-id="119cd-309">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="119cd-309">IS_NULLABLE</span></span>|<span data-ttu-id="119cd-310">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-310">String</span></span>|  
|<span data-ttu-id="119cd-311">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="119cd-311">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="119cd-312">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-312">String</span></span>|  
|<span data-ttu-id="119cd-313">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="119cd-313">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="119cd-314">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-314">String</span></span>|  
|<span data-ttu-id="119cd-315">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-315">SS_DATA_TYPE</span></span>|<span data-ttu-id="119cd-316">Byte</span><span class="sxs-lookup"><span data-stu-id="119cd-316">Byte</span></span>|  
  
## <a name="microsoft-oracle-odbc-driver"></a><span data-ttu-id="119cd-317">Pilote Microsoft Oracle ODBC</span><span class="sxs-lookup"><span data-stu-id="119cd-317">Microsoft Oracle ODBC Driver</span></span>  
 <span data-ttu-id="119cd-318">Le pilote Microsoft SQL Server Oracle ODBC prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="119cd-318">The Microsoft SQL Server Oracle ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="119cd-319">Tables</span><span class="sxs-lookup"><span data-stu-id="119cd-319">Tables</span></span>  
  
-   <span data-ttu-id="119cd-320">Columns</span><span class="sxs-lookup"><span data-stu-id="119cd-320">Columns</span></span>  
  
-   <span data-ttu-id="119cd-321">Procédures</span><span class="sxs-lookup"><span data-stu-id="119cd-321">Procedures</span></span>  
  
-   <span data-ttu-id="119cd-322">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="119cd-322">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="119cd-323">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="119cd-323">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="119cd-324">Vues</span><span class="sxs-lookup"><span data-stu-id="119cd-324">Views</span></span>  
  
-   <span data-ttu-id="119cd-325">Index</span><span class="sxs-lookup"><span data-stu-id="119cd-325">Indexes</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="119cd-326">Tables et vues</span><span class="sxs-lookup"><span data-stu-id="119cd-326">Tables and Views</span></span>  
  
|<span data-ttu-id="119cd-327">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="119cd-327">ColumnName</span></span>|<span data-ttu-id="119cd-328">Type de données</span><span class="sxs-lookup"><span data-stu-id="119cd-328">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="119cd-329">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="119cd-329">TABLE_QUALIFIER</span></span>|<span data-ttu-id="119cd-330">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-330">String</span></span>|  
|<span data-ttu-id="119cd-331">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="119cd-331">TABLE_OWNER</span></span>|<span data-ttu-id="119cd-332">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-332">String</span></span>|  
|<span data-ttu-id="119cd-333">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-333">TABLE_NAME</span></span>|<span data-ttu-id="119cd-334">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-334">String</span></span>|  
|<span data-ttu-id="119cd-335">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-335">TABLE_TYPE</span></span>|<span data-ttu-id="119cd-336">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-336">String</span></span>|  
|<span data-ttu-id="119cd-337">REMARKS</span><span class="sxs-lookup"><span data-stu-id="119cd-337">REMARKS</span></span>|<span data-ttu-id="119cd-338">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-338">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="119cd-339">Columns</span><span class="sxs-lookup"><span data-stu-id="119cd-339">Columns</span></span>  
  
|<span data-ttu-id="119cd-340">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="119cd-340">ColumnName</span></span>|<span data-ttu-id="119cd-341">Type de données</span><span class="sxs-lookup"><span data-stu-id="119cd-341">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="119cd-342">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="119cd-342">TABLE_QUALIFIER</span></span>|<span data-ttu-id="119cd-343">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-343">String</span></span>|  
|<span data-ttu-id="119cd-344">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="119cd-344">TABLE_OWNER</span></span>|<span data-ttu-id="119cd-345">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-345">String</span></span>|  
|<span data-ttu-id="119cd-346">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-346">TABLE_NAME</span></span>|<span data-ttu-id="119cd-347">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-347">String</span></span>|  
|<span data-ttu-id="119cd-348">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-348">COLUMN_NAME</span></span>|<span data-ttu-id="119cd-349">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-349">String</span></span>|  
|<span data-ttu-id="119cd-350">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-350">DATA_TYPE</span></span>|<span data-ttu-id="119cd-351">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-351">Int16</span></span>|  
|<span data-ttu-id="119cd-352">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-352">TYPE_NAME</span></span>|<span data-ttu-id="119cd-353">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-353">String</span></span>|  
|<span data-ttu-id="119cd-354">PRECISION</span><span class="sxs-lookup"><span data-stu-id="119cd-354">PRECISION</span></span>|<span data-ttu-id="119cd-355">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-355">Int32</span></span>|  
|<span data-ttu-id="119cd-356">LENGTH</span><span class="sxs-lookup"><span data-stu-id="119cd-356">LENGTH</span></span>|<span data-ttu-id="119cd-357">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-357">Int32</span></span>|  
|<span data-ttu-id="119cd-358">SCALE</span><span class="sxs-lookup"><span data-stu-id="119cd-358">SCALE</span></span>|<span data-ttu-id="119cd-359">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-359">Int16</span></span>|  
|<span data-ttu-id="119cd-360">RADIX</span><span class="sxs-lookup"><span data-stu-id="119cd-360">RADIX</span></span>|<span data-ttu-id="119cd-361">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-361">Int16</span></span>|  
|<span data-ttu-id="119cd-362">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="119cd-362">NULLABLE</span></span>|<span data-ttu-id="119cd-363">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-363">Int16</span></span>|  
|<span data-ttu-id="119cd-364">REMARKS</span><span class="sxs-lookup"><span data-stu-id="119cd-364">REMARKS</span></span>|<span data-ttu-id="119cd-365">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-365">String</span></span>|  
|<span data-ttu-id="119cd-366">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="119cd-366">ORDINAL_POSITION</span></span>|<span data-ttu-id="119cd-367">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-367">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="119cd-368">Procédures</span><span class="sxs-lookup"><span data-stu-id="119cd-368">Procedures</span></span>  
  
|<span data-ttu-id="119cd-369">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="119cd-369">ColumnName</span></span>|<span data-ttu-id="119cd-370">Type de données</span><span class="sxs-lookup"><span data-stu-id="119cd-370">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="119cd-371">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="119cd-371">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="119cd-372">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-372">String</span></span>|  
|<span data-ttu-id="119cd-373">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="119cd-373">PROCEDURE_OWNER</span></span>|<span data-ttu-id="119cd-374">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-374">String</span></span>|  
|<span data-ttu-id="119cd-375">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-375">PROCEDURE_NAME</span></span>|<span data-ttu-id="119cd-376">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-376">String</span></span>|  
|<span data-ttu-id="119cd-377">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="119cd-377">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="119cd-378">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-378">Int16</span></span>|  
|<span data-ttu-id="119cd-379">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="119cd-379">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="119cd-380">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-380">Int16</span></span>|  
|<span data-ttu-id="119cd-381">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="119cd-381">NUM_RESULT_SETS</span></span>|<span data-ttu-id="119cd-382">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-382">Int16</span></span>|  
|<span data-ttu-id="119cd-383">REMARKS</span><span class="sxs-lookup"><span data-stu-id="119cd-383">REMARKS</span></span>|<span data-ttu-id="119cd-384">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-384">String</span></span>|  
|<span data-ttu-id="119cd-385">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-385">PROCEDURE_TYPE</span></span>|<span data-ttu-id="119cd-386">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-386">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="119cd-387">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="119cd-387">ProcedureColumns</span></span>  
  
|<span data-ttu-id="119cd-388">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="119cd-388">ColumnName</span></span>|<span data-ttu-id="119cd-389">Type de données</span><span class="sxs-lookup"><span data-stu-id="119cd-389">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="119cd-390">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="119cd-390">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="119cd-391">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-391">String</span></span>|  
|<span data-ttu-id="119cd-392">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="119cd-392">PROCEDURE_OWNER</span></span>|<span data-ttu-id="119cd-393">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-393">String</span></span>|  
|<span data-ttu-id="119cd-394">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-394">PROCEDURE_NAME</span></span>|<span data-ttu-id="119cd-395">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-395">String</span></span>|  
|<span data-ttu-id="119cd-396">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-396">COLUMN_NAME</span></span>|<span data-ttu-id="119cd-397">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-397">String</span></span>|  
|<span data-ttu-id="119cd-398">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-398">COLUMN_TYPE</span></span>|<span data-ttu-id="119cd-399">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-399">Int16</span></span>|  
|<span data-ttu-id="119cd-400">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-400">DATA_TYPE</span></span>|<span data-ttu-id="119cd-401">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-401">Int16</span></span>|  
|<span data-ttu-id="119cd-402">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-402">TYPE_NAME</span></span>|<span data-ttu-id="119cd-403">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-403">String</span></span>|  
|<span data-ttu-id="119cd-404">PRECISION</span><span class="sxs-lookup"><span data-stu-id="119cd-404">PRECISION</span></span>|<span data-ttu-id="119cd-405">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-405">Int32</span></span>|  
|<span data-ttu-id="119cd-406">LENGTH</span><span class="sxs-lookup"><span data-stu-id="119cd-406">LENGTH</span></span>|<span data-ttu-id="119cd-407">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-407">Int32</span></span>|  
|<span data-ttu-id="119cd-408">SCALE</span><span class="sxs-lookup"><span data-stu-id="119cd-408">SCALE</span></span>|<span data-ttu-id="119cd-409">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-409">Int16</span></span>|  
|<span data-ttu-id="119cd-410">RADIX</span><span class="sxs-lookup"><span data-stu-id="119cd-410">RADIX</span></span>|<span data-ttu-id="119cd-411">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-411">Int16</span></span>|  
|<span data-ttu-id="119cd-412">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="119cd-412">NULLABLE</span></span>|<span data-ttu-id="119cd-413">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-413">Int16</span></span>|  
|<span data-ttu-id="119cd-414">REMARKS</span><span class="sxs-lookup"><span data-stu-id="119cd-414">REMARKS</span></span>|<span data-ttu-id="119cd-415">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-415">String</span></span>|  
|<span data-ttu-id="119cd-416">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="119cd-416">OVERLOAD</span></span>|<span data-ttu-id="119cd-417">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-417">Int32</span></span>|  
|<span data-ttu-id="119cd-418">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="119cd-418">ORDINAL_POSITION</span></span>|<span data-ttu-id="119cd-419">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-419">Int32</span></span>|  
  
## <a name="microsoft-jet-odbc-driver"></a><span data-ttu-id="119cd-420">Pilote Microsoft Jet ODBC</span><span class="sxs-lookup"><span data-stu-id="119cd-420">Microsoft Jet ODBC Driver</span></span>  
 <span data-ttu-id="119cd-421">Le pilote Microsoft Jet ODBC prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="119cd-421">The Microsoft Jet ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="119cd-422">Tables</span><span class="sxs-lookup"><span data-stu-id="119cd-422">Tables</span></span>  
  
-   <span data-ttu-id="119cd-423">Index</span><span class="sxs-lookup"><span data-stu-id="119cd-423">Indexes</span></span>  
  
-   <span data-ttu-id="119cd-424">Columns</span><span class="sxs-lookup"><span data-stu-id="119cd-424">Columns</span></span>  
  
-   <span data-ttu-id="119cd-425">Procédures</span><span class="sxs-lookup"><span data-stu-id="119cd-425">Procedures</span></span>  
  
-   <span data-ttu-id="119cd-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="119cd-426">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="119cd-427">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="119cd-427">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="119cd-428">Vues</span><span class="sxs-lookup"><span data-stu-id="119cd-428">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="119cd-429">Tables et vues</span><span class="sxs-lookup"><span data-stu-id="119cd-429">Tables and Views</span></span>  
  
|<span data-ttu-id="119cd-430">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="119cd-430">ColumnName</span></span>|<span data-ttu-id="119cd-431">Type de données</span><span class="sxs-lookup"><span data-stu-id="119cd-431">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="119cd-432">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="119cd-432">TABLE_QUALIFIER</span></span>|<span data-ttu-id="119cd-433">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-433">String</span></span>|  
|<span data-ttu-id="119cd-434">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="119cd-434">TABLE_OWNER</span></span>|<span data-ttu-id="119cd-435">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-435">String</span></span>|  
|<span data-ttu-id="119cd-436">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-436">TABLE_NAME</span></span>|<span data-ttu-id="119cd-437">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-437">String</span></span>|  
|<span data-ttu-id="119cd-438">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-438">TABLE_TYPE</span></span>|<span data-ttu-id="119cd-439">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-439">String</span></span>|  
|<span data-ttu-id="119cd-440">REMARKS</span><span class="sxs-lookup"><span data-stu-id="119cd-440">REMARKS</span></span>|<span data-ttu-id="119cd-441">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-441">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="119cd-442">Columns</span><span class="sxs-lookup"><span data-stu-id="119cd-442">Columns</span></span>  
  
|<span data-ttu-id="119cd-443">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="119cd-443">ColumnName</span></span>|<span data-ttu-id="119cd-444">Type de données</span><span class="sxs-lookup"><span data-stu-id="119cd-444">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="119cd-445">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="119cd-445">TABLE_QUALIFIER</span></span>|<span data-ttu-id="119cd-446">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-446">String</span></span>|  
|<span data-ttu-id="119cd-447">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="119cd-447">TABLE_OWNER</span></span>|<span data-ttu-id="119cd-448">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-448">String</span></span>|  
|<span data-ttu-id="119cd-449">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-449">TABLE_NAME</span></span>|<span data-ttu-id="119cd-450">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-450">String</span></span>|  
|<span data-ttu-id="119cd-451">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-451">COLUMN_NAME</span></span>|<span data-ttu-id="119cd-452">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-452">String</span></span>|  
|<span data-ttu-id="119cd-453">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-453">DATA_TYPE</span></span>|<span data-ttu-id="119cd-454">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-454">Int16</span></span>|  
|<span data-ttu-id="119cd-455">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-455">TYPE_NAME</span></span>|<span data-ttu-id="119cd-456">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-456">String</span></span>|  
|<span data-ttu-id="119cd-457">PRECISION</span><span class="sxs-lookup"><span data-stu-id="119cd-457">PRECISION</span></span>|<span data-ttu-id="119cd-458">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-458">Int32</span></span>|  
|<span data-ttu-id="119cd-459">LENGTH</span><span class="sxs-lookup"><span data-stu-id="119cd-459">LENGTH</span></span>|<span data-ttu-id="119cd-460">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-460">Int32</span></span>|  
|<span data-ttu-id="119cd-461">SCALE</span><span class="sxs-lookup"><span data-stu-id="119cd-461">SCALE</span></span>|<span data-ttu-id="119cd-462">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-462">Int16</span></span>|  
|<span data-ttu-id="119cd-463">RADIX</span><span class="sxs-lookup"><span data-stu-id="119cd-463">RADIX</span></span>|<span data-ttu-id="119cd-464">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-464">Int16</span></span>|  
|<span data-ttu-id="119cd-465">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="119cd-465">NULLABLE</span></span>|<span data-ttu-id="119cd-466">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-466">Int16</span></span>|  
|<span data-ttu-id="119cd-467">REMARKS</span><span class="sxs-lookup"><span data-stu-id="119cd-467">REMARKS</span></span>|<span data-ttu-id="119cd-468">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-468">String</span></span>|  
|<span data-ttu-id="119cd-469">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="119cd-469">ORDINAL_POSITION</span></span>|<span data-ttu-id="119cd-470">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-470">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="119cd-471">Procédures</span><span class="sxs-lookup"><span data-stu-id="119cd-471">Procedures</span></span>  
  
|<span data-ttu-id="119cd-472">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="119cd-472">ColumnName</span></span>|<span data-ttu-id="119cd-473">Type de données</span><span class="sxs-lookup"><span data-stu-id="119cd-473">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="119cd-474">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="119cd-474">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="119cd-475">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-475">String</span></span>|  
|<span data-ttu-id="119cd-476">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="119cd-476">PROCEDURE_OWNER</span></span>|<span data-ttu-id="119cd-477">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-477">String</span></span>|  
|<span data-ttu-id="119cd-478">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-478">PROCEDURE_NAME</span></span>|<span data-ttu-id="119cd-479">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-479">String</span></span>|  
|<span data-ttu-id="119cd-480">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="119cd-480">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="119cd-481">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-481">Int16</span></span>|  
|<span data-ttu-id="119cd-482">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="119cd-482">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="119cd-483">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-483">Int16</span></span>|  
|<span data-ttu-id="119cd-484">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="119cd-484">NUM_RESULT_SETS</span></span>|<span data-ttu-id="119cd-485">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-485">Int16</span></span>|  
|<span data-ttu-id="119cd-486">REMARKS</span><span class="sxs-lookup"><span data-stu-id="119cd-486">REMARKS</span></span>|<span data-ttu-id="119cd-487">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-487">String</span></span>|  
|<span data-ttu-id="119cd-488">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-488">PROCEDURE_TYPE</span></span>|<span data-ttu-id="119cd-489">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-489">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="119cd-490">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="119cd-490">ProcedureColumns</span></span>  
  
|<span data-ttu-id="119cd-491">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="119cd-491">ColumnName</span></span>|<span data-ttu-id="119cd-492">Type de données</span><span class="sxs-lookup"><span data-stu-id="119cd-492">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="119cd-493">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="119cd-493">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="119cd-494">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-494">String</span></span>|  
|<span data-ttu-id="119cd-495">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="119cd-495">PROCEDURE_OWNER</span></span>|<span data-ttu-id="119cd-496">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-496">String</span></span>|  
|<span data-ttu-id="119cd-497">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-497">PROCEDURE_NAME</span></span>|<span data-ttu-id="119cd-498">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-498">String</span></span>|  
|<span data-ttu-id="119cd-499">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-499">COLUMN_NAME</span></span>|<span data-ttu-id="119cd-500">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-500">String</span></span>|  
|<span data-ttu-id="119cd-501">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-501">COLUMN_TYPE</span></span>|<span data-ttu-id="119cd-502">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-502">Int16</span></span>|  
|<span data-ttu-id="119cd-503">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-503">DATA_TYPE</span></span>|<span data-ttu-id="119cd-504">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-504">Int16</span></span>|  
|<span data-ttu-id="119cd-505">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-505">TYPE_NAME</span></span>|<span data-ttu-id="119cd-506">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-506">String</span></span>|  
|<span data-ttu-id="119cd-507">PRECISION</span><span class="sxs-lookup"><span data-stu-id="119cd-507">PRECISION</span></span>|<span data-ttu-id="119cd-508">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-508">Int32</span></span>|  
|<span data-ttu-id="119cd-509">LENGTH</span><span class="sxs-lookup"><span data-stu-id="119cd-509">LENGTH</span></span>|<span data-ttu-id="119cd-510">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-510">Int32</span></span>|  
|<span data-ttu-id="119cd-511">SCALE</span><span class="sxs-lookup"><span data-stu-id="119cd-511">SCALE</span></span>|<span data-ttu-id="119cd-512">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-512">Int16</span></span>|  
|<span data-ttu-id="119cd-513">RADIX</span><span class="sxs-lookup"><span data-stu-id="119cd-513">RADIX</span></span>|<span data-ttu-id="119cd-514">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-514">Int16</span></span>|  
|<span data-ttu-id="119cd-515">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="119cd-515">NULLABLE</span></span>|<span data-ttu-id="119cd-516">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-516">Int16</span></span>|  
|<span data-ttu-id="119cd-517">REMARKS</span><span class="sxs-lookup"><span data-stu-id="119cd-517">REMARKS</span></span>|<span data-ttu-id="119cd-518">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-518">String</span></span>|  
|<span data-ttu-id="119cd-519">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="119cd-519">OVERLOAD</span></span>|<span data-ttu-id="119cd-520">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-520">Int32</span></span>|  
|<span data-ttu-id="119cd-521">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="119cd-521">ORDINAL_POSITION</span></span>|<span data-ttu-id="119cd-522">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-522">Int32</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="119cd-523">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="119cd-523">ProcedureParameters</span></span>  
  
|<span data-ttu-id="119cd-524">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="119cd-524">ColumnName</span></span>|<span data-ttu-id="119cd-525">Type de données</span><span class="sxs-lookup"><span data-stu-id="119cd-525">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="119cd-526">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="119cd-526">PROCEDURE_CAT</span></span>|<span data-ttu-id="119cd-527">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-527">String</span></span>|  
|<span data-ttu-id="119cd-528">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="119cd-528">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="119cd-529">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-529">String</span></span>|  
|<span data-ttu-id="119cd-530">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-530">PROCEDURE_NAME</span></span>|<span data-ttu-id="119cd-531">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-531">String</span></span>|  
|<span data-ttu-id="119cd-532">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-532">COLUMN_NAME</span></span>|<span data-ttu-id="119cd-533">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-533">String</span></span>|  
|<span data-ttu-id="119cd-534">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-534">COLUMN_TYPE</span></span>|<span data-ttu-id="119cd-535">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-535">Int16</span></span>|  
|<span data-ttu-id="119cd-536">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-536">DATA_TYPE</span></span>|<span data-ttu-id="119cd-537">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-537">Int16</span></span>|  
|<span data-ttu-id="119cd-538">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="119cd-538">TYPE_NAME</span></span>|<span data-ttu-id="119cd-539">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-539">String</span></span>|  
|<span data-ttu-id="119cd-540">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="119cd-540">COLUMN_SIZE</span></span>|<span data-ttu-id="119cd-541">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-541">Int32</span></span>|  
|<span data-ttu-id="119cd-542">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="119cd-542">BUFFER_LENGTH</span></span>|<span data-ttu-id="119cd-543">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-543">Int32</span></span>|  
|<span data-ttu-id="119cd-544">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="119cd-544">DECIMAL_DIGITS</span></span>|<span data-ttu-id="119cd-545">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-545">Int16</span></span>|  
|<span data-ttu-id="119cd-546">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="119cd-546">NUM_PREC_RADIX</span></span>|<span data-ttu-id="119cd-547">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-547">Int16</span></span>|  
|<span data-ttu-id="119cd-548">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="119cd-548">NULLABLE</span></span>|<span data-ttu-id="119cd-549">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-549">Int16</span></span>|  
|<span data-ttu-id="119cd-550">REMARKS</span><span class="sxs-lookup"><span data-stu-id="119cd-550">REMARKS</span></span>|<span data-ttu-id="119cd-551">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-551">String</span></span>|  
|<span data-ttu-id="119cd-552">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="119cd-552">COLUMN_DEF</span></span>|<span data-ttu-id="119cd-553">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-553">String</span></span>|  
|<span data-ttu-id="119cd-554">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="119cd-554">SQL_DATA_TYPE</span></span>|<span data-ttu-id="119cd-555">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-555">Int16</span></span>|  
|<span data-ttu-id="119cd-556">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="119cd-556">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="119cd-557">Int16</span><span class="sxs-lookup"><span data-stu-id="119cd-557">Int16</span></span>|  
|<span data-ttu-id="119cd-558">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="119cd-558">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="119cd-559">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-559">Int32</span></span>|  
|<span data-ttu-id="119cd-560">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="119cd-560">ORDINAL_POSITION</span></span>|<span data-ttu-id="119cd-561">Int32</span><span class="sxs-lookup"><span data-stu-id="119cd-561">Int32</span></span>|  
|<span data-ttu-id="119cd-562">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="119cd-562">IS_NULLABLE</span></span>|<span data-ttu-id="119cd-563">Chaîne</span><span class="sxs-lookup"><span data-stu-id="119cd-563">String</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="119cd-564">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="119cd-564">See also</span></span>
- [<span data-ttu-id="119cd-565">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="119cd-565">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
