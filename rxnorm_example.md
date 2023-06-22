# RXNorm example

## FHIR API

### Request

    GET https://api.logicahealth.org/FHIRResearchSynthea/open/MedicationRequest?subject=390665

### Response

Returns MedicationRequests with the following RXNorm codes:

- 316672
- 562251
- 996740
- 997223

## RXNorm API

### Request

    GET https://rxnav.nlm.nih.gov/REST/interaction/list.json?rxcuis=316672+562251+996740+997223

### Response

```json
{
  "nlmDisclaimer": "It is not the intention of NLM to provide specific medical advice, but rather to provide users with information to better understand their health and their medications. NLM urges you to consult with a qualified physician for advice about medications.",
  "fullInteractionTypeGroup": [
    {
      "sourceDisclaimer": "DrugBank is intended for educational and scientific research purposes only and you expressly acknowledge and agree that use of DrugBank is at your sole risk. The accuracy of DrugBank information is not guaranteed and reliance on DrugBank shall be at your sole risk. DrugBank is not intended as a substitute for professional medical advice, diagnosis or treatment..[www.drugbank.ca]",
      "sourceName": "DrugBank",
      "fullInteractionType": [
        {
          "comment": "Drug1 (rxcui = 562251, name = amoxicillin 250 MG / clavulanate 125 MG Oral Tablet, tty = SCD). Drug2 (rxcui = 996740, name = memantine hydrochloride 2 MG/ML Oral Solution, tty = SCD). Drug1 is resolved to amoxicillin, Drug2 is resolved to memantine and interaction asserted in DrugBank between Amoxicillin and Memantine. Drug1 is resolved to amoxicillin anhydrous, Drug2 is resolved to memantine and interaction asserted in DrugBank between Amoxicillin and Memantine.",
          "minConcept": [
            {
              "rxcui": "562251",
              "name": "amoxicillin 250 MG / clavulanate 125 MG Oral Tablet",
              "tty": "SCD"
            },
            {
              "rxcui": "996740",
              "name": "memantine hydrochloride 2 MG/ML Oral Solution",
              "tty": "SCD"
            }
          ],
          "interactionPair": [
            {
              "interactionConcept": [
                {
                  "minConceptItem": {
                    "rxcui": "1297882",
                    "name": "amoxicillin anhydrous",
                    "tty": "PIN"
                  },
                  "sourceConceptItem": {
                    "id": "DB01060",
                    "name": "Amoxicillin",
                    "url": "https://go.drugbank.com/drugs/DB01060#interactions"
                  }
                },
                {
                  "minConceptItem": {
                    "rxcui": "6719",
                    "name": "memantine",
                    "tty": "IN"
                  },
                  "sourceConceptItem": {
                    "id": "DB01043",
                    "name": "Memantine",
                    "url": "https://go.drugbank.com/drugs/DB01043#interactions"
                  }
                }
              ],
              "severity": "N/A",
              "description": "Memantine may decrease the excretion rate of Amoxicillin which could result in a higher serum level."
            },
            {
              "interactionConcept": [
                {
                  "minConceptItem": {
                    "rxcui": "723",
                    "name": "amoxicillin",
                    "tty": "IN"
                  },
                  "sourceConceptItem": {
                    "id": "DB01060",
                    "name": "Amoxicillin",
                    "url": "https://go.drugbank.com/drugs/DB01060#interactions"
                  }
                },
                {
                  "minConceptItem": {
                    "rxcui": "6719",
                    "name": "memantine",
                    "tty": "IN"
                  },
                  "sourceConceptItem": {
                    "id": "DB01043",
                    "name": "Memantine",
                    "url": "https://go.drugbank.com/drugs/DB01043#interactions"
                  }
                }
              ],
              "severity": "N/A",
              "description": "Memantine may decrease the excretion rate of Amoxicillin which could result in a higher serum level."
            }
          ]
        },
        {
          "comment": "Drug1 (rxcui = 316672, name = simvastatin 10 MG, tty = SCDC). Drug2 (rxcui = 997223, name = donepezil hydrochloride 10 MG Oral Tablet, tty = SCD). Drug1 is resolved to simvastatin, Drug2 is resolved to donepezil and interaction asserted in DrugBank between Simvastatin and Donepezil.",
          "minConcept": [
            {
              "rxcui": "316672",
              "name": "simvastatin 10 MG",
              "tty": "SCDC"
            },
            {
              "rxcui": "997223",
              "name": "donepezil hydrochloride 10 MG Oral Tablet",
              "tty": "SCD"
            }
          ],
          "interactionPair": [
            {
              "interactionConcept": [
                {
                  "minConceptItem": {
                    "rxcui": "36567",
                    "name": "simvastatin",
                    "tty": "IN"
                  },
                  "sourceConceptItem": {
                    "id": "DB00641",
                    "name": "Simvastatin",
                    "url": "https://go.drugbank.com/drugs/DB00641#interactions"
                  }
                },
                {
                  "minConceptItem": {
                    "rxcui": "135447",
                    "name": "donepezil",
                    "tty": "IN"
                  },
                  "sourceConceptItem": {
                    "id": "DB00843",
                    "name": "Donepezil",
                    "url": "https://go.drugbank.com/drugs/DB00843#interactions"
                  }
                }
              ],
              "severity": "N/A",
              "description": "The metabolism of Donepezil can be decreased when combined with Simvastatin."
            }
          ]
        }
      ]
    }
  ]
}
```
