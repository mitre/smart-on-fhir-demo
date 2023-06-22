# Example queries

This file contains example queries using Synthea data provided by the API endpoint `https://api.logicahealth.org/FHIRResearchSynthea/open`.

## Get MedicationRequests for a given Patient

    https://api.logicahealth.org/FHIRResearchSynthea/open/MedicationRequest?subject=53844

## Chaining

        https://api.logicahealth.org/FHIRResearchSynthea/open/MedicationRequest?subject:Patient.name=Brande998

## Reverse chaining

`195662009` is "Acute viral pharyngitis (disorder)"

    https://api.logicahealth.org/FHIRResearchSynthea/open/Patient?_has:Condition:subject:code=195662009
