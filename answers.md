full_name                Direct PII           Drop                       Directly identifies the individual
email                    Direct PII           Drop                       High-risk should removed leaks.
date_of_birth            Indirect PII         Mask                       Can be used for re-identification. Convert to "Age Group" (e.g., 20-30) instead.
zip_code                 Indirect PII         Mask                       Keep only the first 3 digits to provide general location without pinpointing a home.
job_title                Indirect PII         Pseudonymize               Replace specific titles with generic categories to prevent identity "leaks."
diagnosis_notes          Indirect PII         Pseudonymize               Notes often contain names or specific dates; must be scrubbed of identifiers.
