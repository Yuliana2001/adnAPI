# ADN Mutante – API REST (AWS Lambda + DynamoDB)

Proyecto que implementa el desafío de detección de mutantes a partir de secuencias de ADN.  
La lógica está desarrollada en **Python** y se expone mediante **AWS API Gateway + Lambda + DynamoDB**.

---

## Descripción general

- Función principal: `is_mutant(dna: list[str]) -> bool`.
- El ADN es considerado mutante si contiene **más de una** secuencia de 4 letras iguales (`A`, `T`, `C`, `G`) en:
  - horizontal,
  - vertical,
  - diagonal principal,
  - diagonal inversa.

Sobre esta lógica se construyen dos endpoints:

- `POST /mutant` – verifica si un ADN es mutante.
- `GET /mutant/stats` – devuelve estadísticas de verificaciones.

URL base del despliegue:

```text
https://e10l15fn75.execute-api.us-east-2.amazonaws.com

## Endpoint POST /mutant

**URL**
POST https://e1015h7r5.execute-api.us-east-2.amazonaws.com/mutant



