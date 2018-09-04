---
title: Trasformazioni dati
description: Esplorare le diverse trasformazioni dati supportate in ML.NET.
ms.date: 08/08/2018
author: jralexander
ms.author: johalex
ms.openlocfilehash: 3c483f4a263052eb15435775a47f514893eee049
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/02/2018
ms.locfileid: "43397143"
---
# <a name="data-transforms"></a><span data-ttu-id="a63a1-103">Trasformazioni dati</span><span class="sxs-lookup"><span data-stu-id="a63a1-103">Data transforms</span></span>

<span data-ttu-id="a63a1-104">Le tabelle seguenti contengono informazioni su tutte le trasformazioni dati supportate in ML.NET (selezionare il tipo di trasformazione dati per passare alla tabella corrispondente):</span><span class="sxs-lookup"><span data-stu-id="a63a1-104">The following tables contain information about all of the data transforms supported in ML.NET (select the data transform type to navigate to the corresponding table):</span></span>

* [<span data-ttu-id="a63a1-105">Categorie</span><span class="sxs-lookup"><span data-stu-id="a63a1-105">Categorical</span></span>](#categorical)
* [<span data-ttu-id="a63a1-106">Combinatori e separatori</span><span class="sxs-lookup"><span data-stu-id="a63a1-106">Combiners and segregators</span></span>](#combiners-and-segregators)
* [<span data-ttu-id="a63a1-107">Selezione funzionalità</span><span class="sxs-lookup"><span data-stu-id="a63a1-107">Feature selection</span></span>](#feature-selection)
* [<span data-ttu-id="a63a1-108">Algoritmi di estrazione funzionalità</span><span class="sxs-lookup"><span data-stu-id="a63a1-108">Featurizers</span></span>](#featurizers)
* [<span data-ttu-id="a63a1-109">Analisi etichette</span><span class="sxs-lookup"><span data-stu-id="a63a1-109">Label parsing</span></span>](#label-parsing)
* [<span data-ttu-id="a63a1-110">Valori mancanti</span><span class="sxs-lookup"><span data-stu-id="a63a1-110">Missing Values</span></span>](#missing-values)
* [<span data-ttu-id="a63a1-111">Normalizzazione</span><span class="sxs-lookup"><span data-stu-id="a63a1-111">Normalization</span></span>](#normalization)
* [<span data-ttu-id="a63a1-112">Filtri di riga</span><span class="sxs-lookup"><span data-stu-id="a63a1-112">Row filters</span></span>](#row-filters)
* [<span data-ttu-id="a63a1-113">Schema</span><span class="sxs-lookup"><span data-stu-id="a63a1-113">Schema</span></span>](#schema)
* [<span data-ttu-id="a63a1-114">Elaborazione testo ed estrazione funzionalità</span><span class="sxs-lookup"><span data-stu-id="a63a1-114">Text processing and featurization</span></span>](#text-processing-and-featurization)
* [<span data-ttu-id="a63a1-115">Varie</span><span class="sxs-lookup"><span data-stu-id="a63a1-115">Miscellaneous</span></span>](#miscellaneous)

> [!NOTE]
> <span data-ttu-id="a63a1-116">ML.NET è attualmente in anteprima.</span><span class="sxs-lookup"><span data-stu-id="a63a1-116">ML.NET is currently in Preview.</span></span> <span data-ttu-id="a63a1-117">Non tutte le trasformazioni dati sono attualmente supportate.</span><span class="sxs-lookup"><span data-stu-id="a63a1-117">Not all data transforms are currently supported.</span></span> <span data-ttu-id="a63a1-118">Per inviare una richiesta per una determinata trasformazione, aprire un problema nel repository GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/issues).</span><span class="sxs-lookup"><span data-stu-id="a63a1-118">To submit a request for a certain transform, open an issue in the [dotnet/machinelearning](https://github.com/dotnet/machinelearning/issues) GitHub repository.</span></span>

## <a name="categorical"></a><span data-ttu-id="a63a1-119">Categorie</span><span class="sxs-lookup"><span data-stu-id="a63a1-119">Categorical</span></span>

| <span data-ttu-id="a63a1-120">Transform</span><span class="sxs-lookup"><span data-stu-id="a63a1-120">Transform</span></span> | <span data-ttu-id="a63a1-121">Definizione</span><span class="sxs-lookup"><span data-stu-id="a63a1-121">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.CategoricalHashOneHotVectorizer> | <span data-ttu-id="a63a1-122">Codifica la variabile categorica con la codifica basata su hash.</span><span class="sxs-lookup"><span data-stu-id="a63a1-122">Encodes the categorical variable with hash-based encoding.</span></span> |
| <xref:Microsoft.ML.Transforms.CategoricalOneHotVectorizer> | <span data-ttu-id="a63a1-123">Codifica la variabile categorica con la codifica one-hot in base a un dizionario di termini.</span><span class="sxs-lookup"><span data-stu-id="a63a1-123">Encodes the categorical variable with one-hot encoding based on a term dictionary.</span></span> |

## <a name="combiners-and-segregators"></a><span data-ttu-id="a63a1-124">Combinatori e separatori</span><span class="sxs-lookup"><span data-stu-id="a63a1-124">Combiners and segregators</span></span>

| <span data-ttu-id="a63a1-125">Transform</span><span class="sxs-lookup"><span data-stu-id="a63a1-125">Transform</span></span> | <span data-ttu-id="a63a1-126">Definizione</span><span class="sxs-lookup"><span data-stu-id="a63a1-126">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.CombinerByContiguousGroupId> | <span data-ttu-id="a63a1-127">Raggruppa i valori di una colonna scalare in un vettore in base a un ID gruppo contiguo.</span><span class="sxs-lookup"><span data-stu-id="a63a1-127">Groups values of a scalar column into a vector based on a contiguous group ID.</span></span> |
| <xref:Microsoft.ML.Transforms.FeatureCombiner> | <span data-ttu-id="a63a1-128">Combina tutte le funzionalità in una colonna funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a63a1-128">Combines all the features into one feature column.</span></span> |
| <xref:Microsoft.ML.Transforms.ManyHeterogeneousModelCombiner> | <span data-ttu-id="a63a1-129">Combina una sequenza di oggetti TransformModel e un oggetto PredictorModel in un singolo oggetto PredictorModel.</span><span class="sxs-lookup"><span data-stu-id="a63a1-129">Combines a sequence of TransformModels and a PredictorModel into a single PredictorModel.</span></span> |
| <xref:Microsoft.ML.Transforms.ModelCombiner> | <span data-ttu-id="a63a1-130">Combina una sequenza di oggetti TransformModel in un singolo modello.</span><span class="sxs-lookup"><span data-stu-id="a63a1-130">Combines a sequence of TransformModels into a single model.</span></span> |
| <xref:Microsoft.ML.Transforms.Segregator> | <span data-ttu-id="a63a1-131">Separa le colonne vettore in sequenze di righe, operazione inversa del raggruppamento trasformazione.</span><span class="sxs-lookup"><span data-stu-id="a63a1-131">Ungroups vector columns into sequences of rows; the inverse of Group transform.</span></span> |
| <xref:Microsoft.ML.Transforms.TwoHeterogeneousModelCombiner> | <span data-ttu-id="a63a1-132">Combina un oggetto TransformModel e un oggetto PredictorModel in un singolo oggetto PredictorModel.</span><span class="sxs-lookup"><span data-stu-id="a63a1-132">Combines a TransformModel and a PredictorModel into a single PredictorModel.</span></span> |

## <a name="feature-selection"></a><span data-ttu-id="a63a1-133">Selezione funzionalità</span><span class="sxs-lookup"><span data-stu-id="a63a1-133">Feature selection</span></span>

| <span data-ttu-id="a63a1-134">Transform</span><span class="sxs-lookup"><span data-stu-id="a63a1-134">Transform</span></span> | <span data-ttu-id="a63a1-135">Definizione</span><span class="sxs-lookup"><span data-stu-id="a63a1-135">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.FeatureSelectorByCount> | <span data-ttu-id="a63a1-136">Seleziona gli slot per i quali il conteggio dei valori non predefiniti è maggiore o uguale a una determinata soglia.</span><span class="sxs-lookup"><span data-stu-id="a63a1-136">Selects the slots for which the count of non-default values is greater than or equal to a threshold.</span></span> |
| <xref:Microsoft.ML.Transforms.FeatureSelectorByMutualInformation> | <span data-ttu-id="a63a1-137">Seleziona gli slot top k in tutte le colonne specificate ordinate in base alle relative informazioni reciproche con la colonna etichetta.</span><span class="sxs-lookup"><span data-stu-id="a63a1-137">Selects the top k slots across all specified columns ordered by their mutual information with the label column.</span></span> |

## <a name="featurizers"></a><span data-ttu-id="a63a1-138">Algoritmi di estrazione funzionalità</span><span class="sxs-lookup"><span data-stu-id="a63a1-138">Featurizers</span></span>

| <span data-ttu-id="a63a1-139">Transform</span><span class="sxs-lookup"><span data-stu-id="a63a1-139">Transform</span></span> | <span data-ttu-id="a63a1-140">Definizione</span><span class="sxs-lookup"><span data-stu-id="a63a1-140">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.HashConverter> | <span data-ttu-id="a63a1-141">Converte i valori colonna in hash.</span><span class="sxs-lookup"><span data-stu-id="a63a1-141">Converts column values into hashes.</span></span> <span data-ttu-id="a63a1-142">Questa trasformazione accetta input numerici e di testo, sia con colonne singole che vettoriali.</span><span class="sxs-lookup"><span data-stu-id="a63a1-142">This transform accepts both numeric and text inputs, both single and vector-valued columns.</span></span> |
| <xref:Microsoft.ML.Transforms.TreeLeafFeaturizer> | <span data-ttu-id="a63a1-143">Esegue il training di un ensemble di alberi o lo carica da un file, quindi esegue il mapping di un vettore delle caratteristiche numerico a tre output: 1.</span><span class="sxs-lookup"><span data-stu-id="a63a1-143">Trains a tree ensemble, or loads it from a file, then maps a numeric feature vector to three outputs: 1.</span></span> <span data-ttu-id="a63a1-144">Un vettore che contiene i singoli output dell'albero dell'ensemble di alberi.</span><span class="sxs-lookup"><span data-stu-id="a63a1-144">A vector containing the individual tree outputs of the tree ensemble.</span></span> <span data-ttu-id="a63a1-145">2.</span><span class="sxs-lookup"><span data-stu-id="a63a1-145">2.</span></span> <span data-ttu-id="a63a1-146">Un vettore che indica le foglie su cui si basa il vettore delle caratteristiche nell'ensemble di alberi.</span><span class="sxs-lookup"><span data-stu-id="a63a1-146">A vector indicating the leaves that the feature vector falls on in the tree ensemble.</span></span> <span data-ttu-id="a63a1-147">3.</span><span class="sxs-lookup"><span data-stu-id="a63a1-147">3.</span></span> <span data-ttu-id="a63a1-148">Un vettore che indica i percorsi su cui si basa il vettore delle caratteristiche nell'ensemble di alberi.</span><span class="sxs-lookup"><span data-stu-id="a63a1-148">A vector indicating the paths that the feature vector falls on in the tree ensemble.</span></span> <span data-ttu-id="a63a1-149">Se vengono specificati sia un file di modello che un algoritmo di training, il vettore userà il file di modello.</span><span class="sxs-lookup"><span data-stu-id="a63a1-149">If both a model file and a trainer are specified, the vector will use the model file.</span></span> <span data-ttu-id="a63a1-150">Se non viene specificato alcun elemento, il vettore eseguirà il training di un modello FastTree predefinito.</span><span class="sxs-lookup"><span data-stu-id="a63a1-150">If neither are specified, the vector will train a default FastTree model.</span></span> <span data-ttu-id="a63a1-151">In questo modo è possibile gestire le etichette chiave eseguendo il training di un modello di regressione rispetto ai relativi indici permutati facoltativamente.</span><span class="sxs-lookup"><span data-stu-id="a63a1-151">This can handle key labels by training a regression model towards their optionally permuted indices.</span></span> |

## <a name="label-parsing"></a><span data-ttu-id="a63a1-152">Analisi etichette</span><span class="sxs-lookup"><span data-stu-id="a63a1-152">Label parsing</span></span>

| <span data-ttu-id="a63a1-153">Transform</span><span class="sxs-lookup"><span data-stu-id="a63a1-153">Transform</span></span> | <span data-ttu-id="a63a1-154">Definizione</span><span class="sxs-lookup"><span data-stu-id="a63a1-154">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.Dictionarizer> | <span data-ttu-id="a63a1-155">Converte i valori di input (parole, numeri e così via) da indicizzare in un dizionario.</span><span class="sxs-lookup"><span data-stu-id="a63a1-155">Converts input values (words, numbers, etc.) to index in a dictionary.</span></span> |
| <xref:Microsoft.ML.Transforms.LabelColumnKeyBooleanConverter> | <span data-ttu-id="a63a1-156">Trasforma l'etichetta in chiave o bool (se necessario) per renderla appropriata per la classificazione.</span><span class="sxs-lookup"><span data-stu-id="a63a1-156">Transforms the label to either key or bool (if needed) to make it suitable for classification.</span></span> |
| <xref:Microsoft.ML.Transforms.LabelIndicator> | <span data-ttu-id="a63a1-157">Remapper di etichette usato da OVA.</span><span class="sxs-lookup"><span data-stu-id="a63a1-157">Label remapper used by OVA.</span></span> |
| <xref:Microsoft.ML.Transforms.LabelToFloatConverter> | <span data-ttu-id="a63a1-158">Trasforma l'etichetta in float per renderla appropriata per la regressione.</span><span class="sxs-lookup"><span data-stu-id="a63a1-158">Transforms the label to float to make it suitable for regression.</span></span> |
| <xref:Microsoft.ML.Transforms.PredictedLabelColumnOriginalValueConverter> | <span data-ttu-id="a63a1-159">Trasforma una colonna etichetta stimata nei relativi valori originali, a meno che non sia di tipo bool.</span><span class="sxs-lookup"><span data-stu-id="a63a1-159">Transforms a predicted label column to its original values, unless it is of type bool.</span></span> |

## <a name="missing-values"></a><span data-ttu-id="a63a1-160">Valori mancanti</span><span class="sxs-lookup"><span data-stu-id="a63a1-160">Missing Values</span></span>

| <span data-ttu-id="a63a1-161">Transform</span><span class="sxs-lookup"><span data-stu-id="a63a1-161">Transform</span></span> | <span data-ttu-id="a63a1-162">Definizione</span><span class="sxs-lookup"><span data-stu-id="a63a1-162">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.MissingValueHandler> | <span data-ttu-id="a63a1-163">Consente di gestire i valori mancanti sostituendoli con il valore predefinito o con il valore medio/min/max (solo per le colonne non di testo).</span><span class="sxs-lookup"><span data-stu-id="a63a1-163">Handle missing values by replacing them with either the default value or the mean/min/max value (for non-text columns only).</span></span> <span data-ttu-id="a63a1-164">È possibile facoltativamente concatenare una colonna indicatore, se il tipo di colonna di input è numerico.</span><span class="sxs-lookup"><span data-stu-id="a63a1-164">An indicator column can optionally be concatenated, if the input column type is numeric.</span></span> |
| <xref:Microsoft.ML.Transforms.MissingValueIndicator> | <span data-ttu-id="a63a1-165">Consente di creare una colonna di output booleana con lo stesso numero di slot della colonna di input in cui il valore di output è true se manca il valore nella colonna di input.</span><span class="sxs-lookup"><span data-stu-id="a63a1-165">Create a boolean output column with the same number of slots as the input column, where the output value is true if the value in the input column is missing.</span></span> |
| <xref:Microsoft.ML.Transforms.MissingValuesDropper> | <span data-ttu-id="a63a1-166">Rimuove le righe NA dalle colonne vettore.</span><span class="sxs-lookup"><span data-stu-id="a63a1-166">Removes NAs from vector columns.</span></span> |
| <xref:Microsoft.ML.Transforms.MissingValuesRowDropper> | <span data-ttu-id="a63a1-167">Esclude tramite filtro le righe contenenti valori mancanti.</span><span class="sxs-lookup"><span data-stu-id="a63a1-167">Filters out rows that contain missing values.</span></span> |
| <xref:Microsoft.ML.Transforms.MissingValueSubstitutor> | <span data-ttu-id="a63a1-168">Consente di creare una colonna di output dello stesso tipo e dimensioni della colonna di input, in cui i valori mancanti vengono sostituiti con il valore predefinito o con il valore medio/min/max (solo per le colonne non di testo).</span><span class="sxs-lookup"><span data-stu-id="a63a1-168">Create an output column of the same type and size of the input column, where missing values are replaced with either the default value or the mean/min/max value (for non-text columns only).</span></span> |

## <a name="normalization"></a><span data-ttu-id="a63a1-169">Normalization</span><span class="sxs-lookup"><span data-stu-id="a63a1-169">Normalization</span></span>

| <span data-ttu-id="a63a1-170">Transform</span><span class="sxs-lookup"><span data-stu-id="a63a1-170">Transform</span></span> | <span data-ttu-id="a63a1-171">Definizione</span><span class="sxs-lookup"><span data-stu-id="a63a1-171">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.BinNormalizer> | <span data-ttu-id="a63a1-172">I valori vengono assegnati in bin di isodensità e viene eseguito il mapping di un valore ai relativi elementi bin_number/number_of_bins.</span><span class="sxs-lookup"><span data-stu-id="a63a1-172">The values are assigned into equidensity bins and a value is mapped to its bin_number / number_of_bins.</span></span> |
| <xref:Microsoft.ML.Transforms.ConditionalNormalizer> | <span data-ttu-id="a63a1-173">Normalizza le colonne solo se necessario.</span><span class="sxs-lookup"><span data-stu-id="a63a1-173">Normalize the columns only if needed.</span></span> |
| <xref:Microsoft.ML.Transforms.GlobalContrastNormalizer> | <span data-ttu-id="a63a1-174">Esegue una normalizzazione del contrasto globale nei valori di input: Y = (s \* X - M) / D, dove s è una scala, M è la media e D è la norma L2 o la deviazione standard.</span><span class="sxs-lookup"><span data-stu-id="a63a1-174">Performs a global contrast normalization on input values: Y = (s \* X - M) / D, where s is a scale, M is mean and D is either L2 norm or standard deviation.</span></span> | 
| <xref:Microsoft.ML.Transforms.LogMeanVarianceNormalizer> | <span data-ttu-id="a63a1-175">Normalizza i dati in base alla media calcolata e alla varianza del logaritmo dei dati.</span><span class="sxs-lookup"><span data-stu-id="a63a1-175">Normalizes the data based on the computed mean and variance of the logarithm of the data.</span></span> |
| <xref:Microsoft.ML.Transforms.LpNormalizer> | <span data-ttu-id="a63a1-176">Normalizza i vettori (righe) singolarmente ridimensionandoli in base a una norma unitaria (L2, L1 o LInf).</span><span class="sxs-lookup"><span data-stu-id="a63a1-176">Normalize vectors (rows) individually by rescaling them to the unit norm (L2, L1 or LInf).</span></span> <span data-ttu-id="a63a1-177">Esegue l'operazione seguente su un vettore X: Y = (X - M) / D, in cui M è la media e D è la norma L2, la norma L1 o la norma LInf.</span><span class="sxs-lookup"><span data-stu-id="a63a1-177">Performs the following operation on a vector X: Y = (X - M) / D, where M is mean and D is either the L2 norm, the L1 norm, or the LInf norm.</span></span> |
| <xref:Microsoft.ML.Transforms.MeanVarianceNormalizer> | <span data-ttu-id="a63a1-178">Normalizza i dati in base alla media calcolata e alla varianza dei dati.</span><span class="sxs-lookup"><span data-stu-id="a63a1-178">Normalizes the data based on the computed mean and variance of the data.</span></span> |
| <xref:Microsoft.ML.Transforms.MinMaxNormalizer> | <span data-ttu-id="a63a1-179">Normalizza i dati in base ai valori minimo e massimo osservati dei dati.</span><span class="sxs-lookup"><span data-stu-id="a63a1-179">Normalizes the data based on the observed minimum and maximum values of the data.</span></span> |
| <xref:Microsoft.ML.Transforms.SupervisedBinNormalizer> | <span data-ttu-id="a63a1-180">Analogo a <xref:Microsoft.ML.Transforms.BinNormalizer>, ma calcola i bin in base alla correlazione con la colonna etichetta e non l'isodensità.</span><span class="sxs-lookup"><span data-stu-id="a63a1-180">Similar to <xref:Microsoft.ML.Transforms.BinNormalizer>, but calculates bins based on correlation with the label column, not equidensity.</span></span> <span data-ttu-id="a63a1-181">Il nuovo valore è bin_number/number_of_bins.</span><span class="sxs-lookup"><span data-stu-id="a63a1-181">The new value is bin_number / number_of_bins.</span></span> |

## <a name="row-filters"></a><span data-ttu-id="a63a1-182">Filtri di riga</span><span class="sxs-lookup"><span data-stu-id="a63a1-182">Row Filters</span></span>

| <span data-ttu-id="a63a1-183">Transform</span><span class="sxs-lookup"><span data-stu-id="a63a1-183">Transform</span></span> | <span data-ttu-id="a63a1-184">Definizione</span><span class="sxs-lookup"><span data-stu-id="a63a1-184">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.RowRangeFilter> | <span data-ttu-id="a63a1-185">Filtra una vista dati in una colonna di tipo Single, Double o Key (contigua).</span><span class="sxs-lookup"><span data-stu-id="a63a1-185">Filters a dataview on a column of type Single, Double or Key (contiguous).</span></span> <span data-ttu-id="a63a1-186">Mantiene i valori che sono compresi nell'intervallo min/max specificato.</span><span class="sxs-lookup"><span data-stu-id="a63a1-186">Keeps the values that are in the specified min/max range.</span></span> <span data-ttu-id="a63a1-187">Le righe NaN vengono sempre escluse tramite filtro. Se l'input è di tipo Key, i valori min/max vengono considerati percentuali del numero di valori.</span><span class="sxs-lookup"><span data-stu-id="a63a1-187">NaNs are always filtered out. If the input is a Key type, the min/max are considered percentages of the number of values.</span></span> |
| <xref:Microsoft.ML.Transforms.RowSkipAndTakeFilter> | <span data-ttu-id="a63a1-188">Consente di limitare l'input a un subset di righe in un offset facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a63a1-188">Allows limiting input to a subset of rows at an optional offset.</span></span> <span data-ttu-id="a63a1-189">Può essere usato per implementare il paging dei dati.</span><span class="sxs-lookup"><span data-stu-id="a63a1-189">Can be used to implement data paging.</span></span> |
| <xref:Microsoft.ML.Transforms.RowSkipFilter> | <span data-ttu-id="a63a1-190">Consente di limitare l'input a un subset di righe ignorando un numero di righe.</span><span class="sxs-lookup"><span data-stu-id="a63a1-190">Allows limiting input to a subset of rows by skipping a number of rows.</span></span> |
| <xref:Microsoft.ML.Transforms.RowTakeFilter> | <span data-ttu-id="a63a1-191">Consente di limitare l'input a un subset di righe accettando le prime N righe.</span><span class="sxs-lookup"><span data-stu-id="a63a1-191">Allows limiting input to a subset of rows by taking N first rows.</span></span> |

## <a name="schema"></a><span data-ttu-id="a63a1-192">Schema</span><span class="sxs-lookup"><span data-stu-id="a63a1-192">Schema</span></span>

| <span data-ttu-id="a63a1-193">Transform</span><span class="sxs-lookup"><span data-stu-id="a63a1-193">Transform</span></span> | <span data-ttu-id="a63a1-194">Definizione</span><span class="sxs-lookup"><span data-stu-id="a63a1-194">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.ColumnConcatenator> | <span data-ttu-id="a63a1-195">Concatena due colonne dello stesso tipo di elemento.</span><span class="sxs-lookup"><span data-stu-id="a63a1-195">Concatenates two columns of the same item type.</span></span> |
| <xref:Microsoft.ML.Transforms.ColumnCopier> | <span data-ttu-id="a63a1-196">Duplica le colonne dal set di dati.</span><span class="sxs-lookup"><span data-stu-id="a63a1-196">Duplicates columns from the dataset.</span></span>|
| <xref:Microsoft.ML.Transforms.ColumnDropper> | <span data-ttu-id="a63a1-197">Elimina le colonne dal set di dati.</span><span class="sxs-lookup"><span data-stu-id="a63a1-197">Drops columns from the dataset.</span></span> |
| <xref:Microsoft.ML.Transforms.ColumnSelector> | <span data-ttu-id="a63a1-198">Seleziona un set di colonne, eliminando tutte le altre.</span><span class="sxs-lookup"><span data-stu-id="a63a1-198">Selects a set of columns, dropping all others.</span></span> |
| <xref:Microsoft.ML.Transforms.ColumnTypeConverter> | <span data-ttu-id="a63a1-199">Converte una colonna in un tipo diverso, usando le conversioni standard.</span><span class="sxs-lookup"><span data-stu-id="a63a1-199">Converts a column to a different type, using standard conversions.</span></span> |
| <xref:Microsoft.ML.Transforms.KeyToTextConverter> | <span data-ttu-id="a63a1-200">KeyToValueTransform utilizza i metadati KeyValues per eseguire il mapping degli indici di chiave ai valori corrispondenti nei metadati KeyValues.</span><span class="sxs-lookup"><span data-stu-id="a63a1-200">KeyToValueTransform utilizes KeyValues metadata to map key indices to the corresponding values in the KeyValues metadata.</span></span> |
| <xref:Microsoft.ML.Transforms.NGramTranslator> | <span data-ttu-id="a63a1-201">Produce un elenco di conteggi di n-grammi (sequenze di valori consecutivi di lunghezza 1-n) in un vettore specifico di chiavi.</span><span class="sxs-lookup"><span data-stu-id="a63a1-201">Produces a bag of counts of ngrams (sequences of consecutive values of length 1-n) in a given vector of keys.</span></span> <span data-ttu-id="a63a1-202">Tale operazione viene eseguita creando un dizionario di n-grammi e usando l'ID nel dizionario come indice nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="a63a1-202">It does so by building a dictionary of ngrams and using the id in the dictionary as the index in the bag.</span></span> | 
| <xref:Microsoft.ML.Transforms.OptionalColumnCreator> | <span data-ttu-id="a63a1-203">Se dopo la deserializzazione la colonna di origine non esiste, creare una colonna con il tipo corretto e i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="a63a1-203">If the source column does not exist after deserialization, create a column with the right type and default values.</span></span> |

## <a name="text-processing-and-featurization"></a><span data-ttu-id="a63a1-204">Elaborazione testo ed estrazione funzionalità</span><span class="sxs-lookup"><span data-stu-id="a63a1-204">Text processing and featurization</span></span>

| <span data-ttu-id="a63a1-205">Transform</span><span class="sxs-lookup"><span data-stu-id="a63a1-205">Transform</span></span> | <span data-ttu-id="a63a1-206">Definizione</span><span class="sxs-lookup"><span data-stu-id="a63a1-206">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.CharacterTokenizer> | <span data-ttu-id="a63a1-207">Tokenizer orientato ai caratteri in cui il testo viene considerato una sequenza di caratteri.</span><span class="sxs-lookup"><span data-stu-id="a63a1-207">Character-oriented tokenizer where text is considered a sequence of characters.</span></span> |
| <xref:Microsoft.ML.Transforms.TextFeaturizer> | <span data-ttu-id="a63a1-208">Una trasformazione che converte una raccolta di documenti di testo in vettori delle caratteristiche numerici.</span><span class="sxs-lookup"><span data-stu-id="a63a1-208">A transform that turns a collection of text documents into numerical feature vectors.</span></span> <span data-ttu-id="a63a1-209">I vettori delle caratteristiche sono conteggi normalizzati di n-grammi (parola e/o carattere) in un determinato testo in formato token.</span><span class="sxs-lookup"><span data-stu-id="a63a1-209">The feature vectors are normalized counts of (word and/or character) ngrams in a given tokenized text.</span></span> |
| <xref:Microsoft.ML.Transforms.TextToKeyConverter> | <span data-ttu-id="a63a1-210">Converte i valori di input (parole, numeri e così via) da indicizzare in un dizionario.</span><span class="sxs-lookup"><span data-stu-id="a63a1-210">Converts input values (words, numbers, etc.) to index in a dictionary.</span></span> |
| <xref:Microsoft.ML.Transforms.WordEmbeddings> | <span data-ttu-id="a63a1-211">Una trasformazione che converte i vettori di token di testo in vettori numerici usando un modello con pre-training.</span><span class="sxs-lookup"><span data-stu-id="a63a1-211">A transform that converts vectors of text tokens into numeric vectors using a pre-trained model.</span></span> <span data-ttu-id="a63a1-212">Per altre informazioni sulla tecnica, vedere la pagina di Wikipedia [Word embedding](https://en.wikipedia.org/wiki/Word_embedding).</span><span class="sxs-lookup"><span data-stu-id="a63a1-212">For more information about the technique, see the [Word embedding](https://en.wikipedia.org/wiki/Word_embedding) Wikipedia page.</span></span> |
| <xref:Microsoft.ML.Transforms.WordTokenizer> | <span data-ttu-id="a63a1-213">L'input per questa trasformazione è testo e l'output è un vettore di testo che contiene le parole (token) nel testo originale.</span><span class="sxs-lookup"><span data-stu-id="a63a1-213">The input to this transform is text, and the output is a vector of text containing the words (tokens) in the original text.</span></span> <span data-ttu-id="a63a1-214">Il separatore è uno spazio, ma è possibile specificare qualsiasi altro carattere (o più caratteri).</span><span class="sxs-lookup"><span data-stu-id="a63a1-214">The separator is space, but any other character (or multiple characters) can be specified.</span></span> |

## <a name="miscellaneous"></a><span data-ttu-id="a63a1-215">Varie</span><span class="sxs-lookup"><span data-stu-id="a63a1-215">Miscellaneous</span></span>

| <span data-ttu-id="a63a1-216">Transform</span><span class="sxs-lookup"><span data-stu-id="a63a1-216">Transform</span></span> | <span data-ttu-id="a63a1-217">Definizione</span><span class="sxs-lookup"><span data-stu-id="a63a1-217">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.ApproximateBootstrapSampler> | <span data-ttu-id="a63a1-218">Campionamento bootstrap approssimativo.</span><span class="sxs-lookup"><span data-stu-id="a63a1-218">Approximate bootstrap sampling.</span></span> |
| <xref:Microsoft.ML.Transforms.BinaryPredictionScoreColumnsRenamer> | <span data-ttu-id="a63a1-219">Per la stima binaria rinomina le colonne PredictedLabel e Score per includere il nome della classe positiva.</span><span class="sxs-lookup"><span data-stu-id="a63a1-219">For binary prediction, renames the PredictedLabel and Score columns to include the name of the positive class.</span></span>|
| <xref:Microsoft.ML.Transforms.DataCache> | <span data-ttu-id="a63a1-220">Memorizza nella cache usando l'opzione cache specificata.</span><span class="sxs-lookup"><span data-stu-id="a63a1-220">Caches using the specified cache option.</span></span> |
| <xref:Microsoft.ML.Transforms.DatasetScorer> | <span data-ttu-id="a63a1-221">Assegna un punteggio a un set di dati con un modello predittivo.</span><span class="sxs-lookup"><span data-stu-id="a63a1-221">Scores a dataset with a predictor model.</span></span> |
| <xref:Microsoft.ML.Transforms.DatasetTransformScorer> | <span data-ttu-id="a63a1-222">Assegna un punteggio a un set di dati con un modello di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="a63a1-222">Scores a dataset with a transform model.</span></span> |
| <xref:Microsoft.ML.Transforms.NoOperation> | <span data-ttu-id="a63a1-223">Non effettua alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="a63a1-223">Does nothing.</span></span> |
| <xref:Microsoft.ML.Transforms.RandomNumberGenerator> | <span data-ttu-id="a63a1-224">Aggiunge una colonna con una sequenza di numeri generata.</span><span class="sxs-lookup"><span data-stu-id="a63a1-224">Adds a column with a generated number sequence.</span></span> |
| <xref:Microsoft.ML.Transforms.ScoreColumnSelector> | <span data-ttu-id="a63a1-225">Seleziona solo le ultime colonne punteggio e le colonne aggiuntive specificate negli argomenti.</span><span class="sxs-lookup"><span data-stu-id="a63a1-225">Selects only the last score columns and the extra columns specified in the arguments.</span></span> |
| <xref:Microsoft.ML.Transforms.Scorer> | <span data-ttu-id="a63a1-226">Trasforma il modello predittivo in un modello di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="a63a1-226">Turns the predictor model into a transform model.</span></span> |
| <xref:Microsoft.ML.Transforms.SentimentAnalyzer> | <span data-ttu-id="a63a1-227">Usa un modello di sentiment con pre-training per assegnare un punteggio alle stringhe di input.</span><span class="sxs-lookup"><span data-stu-id="a63a1-227">Uses a pretrained sentiment model to score input strings.</span></span> |
| <xref:Microsoft.ML.Transforms.TrainTestDatasetSplitter> | <span data-ttu-id="a63a1-228">Suddivide il set di dati in set di training e di test.</span><span class="sxs-lookup"><span data-stu-id="a63a1-228">Splits the dataset into train and test sets.</span></span> |