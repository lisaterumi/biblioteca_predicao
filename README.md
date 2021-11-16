# biblioteca_predicao

Como chamar:

```
import predict_ner as predict

MODEL_DIR = [r"pucpr/eHelpBERTpt"]

Sentencas = 'Paciente recebeu medicação para febre e tosse. Paciente tomou omeprazol e referiu dor de cabeça.'
Sentencas = Sentencas.replace('.','.#')
sentencas = Sentencas.split('#')
print(sentencas)

result = predict.predictALLSentenceBERT(sentencas,MODEL_DIR)
print(result)


```
Resultado:

```
'Paciente':{'B-PatientorDisabledGroup'},'recebeu':{'O'},'medicação':{'B-TherapeuticorPreventiveProcedure'},'para':{'O'},'febre':{'B-SignorSymptom'},'e':{'O'},'tosse':{'B-SignorSymptom'},'.':{'O'},'Paciente':{'B-PatientorDisabledGroup'},'tomou':{'O'},'omeprazol':{'B-Chemicals&Drugs+<>+B-OrganicChemical+<>+B-PharmacologicSubstance'},'e':{'O'},'referiu':{'O'},'dor':{'B-SignorSymptom'},'de':{'I-SignorSymptom'},'cabeça':{'I-SignorSymptom'},'.':{'O'}
```
