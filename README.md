# DeepNetBim
*DeepNetBim*: *Deep* learning model for predicting HLA-epitope interaction based on *Net* work analysis by harnessing *B*inding and *im*munogenicity information

In DeepNetBim model, both binding intensity of HLA-peptide pairs and potential immunogenicity of epitopes which are capable of eliciting CD8+ T cell responses were considered. In addition, to improve model accuracy, network centrality metrics were extracted through network construction which proved to possess sufficient prediction power in comparison. Extensive tests on independent and benchmark datasets demonstrate that DeepNetBim can significantly outperform other well-known binding prediction tools. 

### Dependencies
DeepNetBim requires the following Python 3.0 modules:
- numpy 1.16.4
- pandas 0.24.2
- keras 2.2.4
- scipy 1.3.0
- sklearn 1.16.4

### 1. Input description 
The input data should meet the following format:

Columns  | Description
------------- | -------------
mhc | mhc class I molecules (e.g. HLA-A01:01)
sequence  | 9-mer peptides (e.g. RTFNEDLFR)

### 2. Implementation

It is noted that the following commands should be implemented under */src/ path. You can implement the code as following:
   ```sh
    python predict.py [inputfile]
   ```
For example:
   ```sh
    python predict.py ../data/sample.txt
   ```
  ### 3.Output description
  The output file is shown as */data/result_prediction.txt*. The description of output is shown as follows:
  
  Columns  | Description
------------- | -------------
mhc | mhc class I molecules 
sequence  | 9-mer peptides 
pred_affinity | the predicted transformed affinity (0 indicates week binding)
pred_immuno | the predicted immunogenic potential ( binary)
immuno_probability| the predicted immunogenic probability (continuous)


