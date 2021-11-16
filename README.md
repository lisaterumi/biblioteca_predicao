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
