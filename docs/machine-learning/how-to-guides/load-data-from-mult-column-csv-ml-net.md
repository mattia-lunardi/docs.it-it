---
title: Caricare dati con più colonne da un file con estensione csv per l'elaborazione con Machine Learning - ML.NET
description: Informazioni su come caricare dati con molte colonne da un file con estensione csv per usarli nelle attività di creazione, training e assegnazione di punteggio per modelli di Machine Learning con ML.NET
ms.date: 02/06/2019
ms.custom: mvc,how-to
ms.openlocfilehash: b295653d1bd3a955c2e6da929dc8f2d4d0a4c14d
ms.sourcegitcommit: d2ccb199ae6bc5787b4762e9ea6d3f6fe88677af
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2019
ms.locfileid: "56091968"
---
# <a name="load-data-with-many-columns-from-a-csv-file-for-machine-learning-processing---mlnet"></a>Caricare dati con più colonne da un file con estensione csv per l'elaborazione con Machine Learning - ML.NET

`TextLoader` viene usato per caricare dati da file di testo. È necessario specificare le colonne di dati, i tipi delle colonne e la relativa posizione nel file di testo.

Quando il file di input contiene molte colonne dello stesso tipo e usate sempre insieme, leggerle come una *colonna vettore*. Questa strategia ha l'effetto di pulire lo schema di dati e consente quindi di evitare costi di prestazioni inutili, come illustrato nell'esempio seguente:

[File di esempio](https://github.com/dotnet/machinelearning/tree/master/test/data/generated_regression_dataset.csv):

```console
-2.75;0.77;-0.61;0.14;1.39;0.38;-0.53;-0.50;-2.13;-0.39;0.46;140.66
-0.61;-0.37;-0.12;0.55;-1.00;0.84;-0.02;1.30;-0.24;-0.50;-2.12;148.12
-0.85;-0.91;1.81;0.02;-0.78;-1.41;-1.09;-0.65;0.90;-0.37;-0.22;402.20
0.28;1.05;-0.24;0.30;-0.99;0.19;0.32;-0.95;-1.19;-0.63;0.75;443.51
```

Lettura del file tramite `TextLoader`:

```csharp
// Create a new context for ML.NET operations. It can be used for exception tracking and logging, 
// as a catalog of available operations and as the source of randomness.
var mlContext = new MLContext();

// Create the reader: define the data columns and where to find them in the text file.
var reader = mlContext.Data.CreateTextLoader(
    columns: new TextLoader.Column[]
    {
    // We read the first 10 values as a single float vector.
        new TextLoader.Column("FeatureVector",DataKind.R4,0,9),
        // Separately, read the target variable.
        new TextLoader.Column("Target",DataKind.R4,10)
    },
    // Default separator is tab, but we need a semicolon.
    separatorChar: ';',
    hasHeader: true
);

// Now read the file (remember though, readers are lazy, so the actual reading will happen when the data is accessed).
var data = reader.Read(dataPath);
```    