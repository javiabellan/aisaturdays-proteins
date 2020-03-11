# 🧬 Proteins AI-Saturdays 🧬
Code for the proteins properties prediction for the AI Saturdays Murcia

## Data

- ftp://ftp.uniprot.org/pub/databases/uniprot/current_release/knowledgebase/complete/
- ftp://ftp.uniprot.org/pub/databases/uniprot/current_release/uniref/

| Dataset 26/2/2020        | Num seqs.       | Comprimido | Descompr.     | Descripción                              |
|:------------------------:|----------------:|-----------:|--------------:|------------------------------------------|
| UniProtKB **Varsplic**   | **40.255**      | 8 MB       | **28** MB     | Para pruebas                             |
| UniProtKB **Swissprot**  | **561.911**     | 85 MB      | **264** MB    | Manually annotated and reviewed          |
| UniProtKB **TrEMBL**     | **177.754.527** | 39.2 GB    |               | Automatically annotated and not reviewed |
| **UniRef50**             | **39.178.216**  | 7.3 GB     |               | Hasta 50% de similaridad.                |
| **UniRef90**             | **107.153.647** | 23.1 GB    |               | Hasta 90% de similaridad.                |
| **UniRef100**            | **216.491.817** | 51.1 GB    |               | Todas.                                   |


## Models to try

- **Recurrent**: Unsupervised -> Predict next char
  - [ ] Simple RNN
  - [ ] GRU
  - [ ] LSTM
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
