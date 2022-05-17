# Data Description

인간의 유전체 데이터를 활용한 암종 분류 모델 개발

해당 training dataset 중 하나 이상의 데이터셋을 활용하여 암종(cancer type)을 분류하는 모델 개발

학습 데이터 샘플의 암종(cancer type) 정보는 train_data_clinical_patient.csv 파일의 CANCER_TYPE_ACRONYM 컬럼에 있습니다.

모델 개발을 위한 기본적인 데이터 전처리가 필요하다면 마음껏 수행하시면 됩니다. 일부 환자는 임상정보 혹은 mutation, cna, rna-seq 데이터가 없을 수 있으며, 이 경우에는 학습 시 제외하고 사용하셔도 됩니다.

## File descriptions

### Train datasets

- **train_data_rna-seq.csv** - the training set (rna-seq) - 유전체 데이터
- **train_data_cna.csv** - the training set (cna) - copy number alteration 데이터
- **sample_submission.csv** - a sample submission file in the correct format (id와 expected 두개의 컬럼)
- **train_data_clinical_patient.csv** - the training set (임상정보) - 환자와 관련된 임상 데이터
- **train_data_mutations.csv** - the training set (돌연변이 정보) - 환자의 돌연변이 데이터
- expected value는 STAD, LUAD, LIHC, SKCM, COAD, LGG 총 6가지로 구성됨

### Test datasets

- **test_data_rna-seq_v1.csv** - the test set (rna-seq) - 유전체 데이터
- **test_data_cna_v1.csv** - the tes set (cna) - copy number alteration 데이터
- **test_data_clinical_patient_v1.csv** - the test set (임상정보) - 환자와 관련된 임상 데이터
- **test_data_mutations_v1.csv** - the test set (돌연변이 정보) - 환자의 돌연변이 데이터

학습 데이터로 모델을 만든 후 모델에 입력으로 사용했던 데이터와 같은 테스트 데이터로 환자별 암종을 분류하는 모델을 만들어 보세요.