# 🧬 Proteins AI-Saturdays 🧬
Code for the proteins properties prediction for the AI Saturdays Murcia

## Pasos

1. Con datasets pequeños -> Entrenar de forma no supervisada (sólo las secuencias)
    - Redes recurrentes -> Predecir el siguinete aminoácido (ver ULMFiT)
    - Transformers -> Predecir el aminoacido oculto (ver BERT)
    - Transformers -> Predecir si amonoácido real o no (ver ELECTRA)
    - Comparar cuales son los mejores modelos.
    - Hecer exploratorio con reducción dimensional.
    - Introducir los datos de los dominios.
2. Con datasets pequeños -> Entrenar de forma supervisada (alguna tarea de clasificación de la proteina)
    - ¿Qué es interesante predecir? Preguntar a Alvaro y Estaban.
3. Repetir lo anterior con datasets más grandes

## Data



| Dataset 26/2/2020        | Num seqs.       | Comprimido | Descompr.     | Descripción                              |
|:------------------------:|----------------:|-----------:|--------------:|------------------------------------------|
| UniProtKB **Varsplic**   | **40.255**      | 8 MB       | **28** MB     | Para pruebas pequeñas                    |
| UniProtKB **Swissprot**  | **561.911**     | 85 MB      | **264** MB    | Manually annotated and reviewed          |
| UniProtKB **TrEMBL**     | **177.754.527** | 39.2 GB    |               | Automatically annotated and not reviewed |
| **UniRef50**             | **39.178.216**  | 7.3 GB     |               | Hasta 50% de similaridad.                |
| **UniRef90**             | **107.153.647** | 23.1 GB    |               | Hasta 90% de similaridad.                |
| **UniRef100**            | **216.491.817** | 51.1 GB    |               | Todas.                                   |
| **UniParc**              | **310.472.414** | 62.3 GB    |               | Todo de todo.                            |

- Enlaces
  - **UniProtKB**: ftp://ftp.uniprot.org/pub/databases/uniprot/current_release/knowledgebase/complete/
  - **UniRef**: ftp://ftp.uniprot.org/pub/databases/uniprot/current_release/uniref/
  - **UniParc**: ftp://ftp.uniprot.org/pub/databases/uniprot/current_release/uniparc/


## Modelos a probar

- **Recurrent**: Unsupervised -> Predict next char
  - [ ] Simple RNN
  - [ ] GRU
  - [ ] LSTM
    - Con [DropConnect](https://es.coursera.org/lecture/competitive-data-science/hyperparameter-tuning-iii-Hg3xw)
  - [ ] mLSTM
  - [ ] [AWD-LSTM](https://arxiv.org/abs/1708.02182): Regular LSTM with extra dropouts. Used in [ULMFiT](https://arxiv.org/abs/1801.06146)
  - [ ] [QRNN](https://arxiv.org/abs/1611.01576): Quasi-Recurrent Neural Networks. Used in [MultiFiT](https://arxiv.org/abs/1909.04761)
- **Transformers**: Unsupervised -> Predict masked char or [ELECTRA](https://openreview.net/pdf?id=r1xMH1BtvB)
  - [ ] Simple transformer
  - [ ] [BERT](https://arxiv.org/abs/1810.04805)
  - [ ] [Transformer-XL](https://arxiv.org/abs/1901.02860)
  - [ ] [RoBERTa](https://arxiv.org/abs/1907.11692)
  - [ ] [BART](https://arxiv.org/abs/1910.13461)
  - [ ] [Reformer](https://arxiv.org/abs/2001.04451)
  

# Papers

- Transformers
  - Biological Structure and Function Emerge ... (abr 2019, FAIR)
    - [paper](https://www.biorxiv.org/content/10.1101/622803v1) 
  - [ProGen](https://twitter.com/RichardSocher/status/1237842037744910336) (mar 2020)
    - [Blog](https://blog.einstein.ai/progen/)
    - [Paper](https://www.biorxiv.org/content/10.1101/2020.03.07.982272v1)
