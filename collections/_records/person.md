---
layout: record
record:
  description: This form outlines the required information for all service users,
    the data is to be collected once at enrolment.
  fields:
  - comments: null
    description: Person identifier provided in the person form. This can be a NINO
      or a unique provider ID. This must be unique for each individual supported on
      RTOF.
    dimensions: null
    foreign_keys: null
    id: unique_id
    latest_comments: null
    name: Unique person identifier
    primary_key: true
    sample_generator: null
    status: Decided
    type: string
    validation:
      required: true
  - comments: Minimum data collection required to understand enrolment
    description: UK National Insurance number. Must be unique. To be collected at
      enrolment into the program. All upper case and no spaces [regular expressions
      for NiNos]
    dimensions: null
    foreign_keys: null
    id: ni_number
    latest_comments: null
    name: NI Number
    primary_key: false
    sample_generator: null
    status: Decided
    type: NINO
    validation:
      required: true
      unique: true
  - comments: null
    description: This field is only relevant if a participant has a temporary NINO.
      In these cases, you should submit the temporary NINO, in this persons form,
      leaving the ni_number field blank, until the participant receives a permanent
      NINO. Once a permanent NINO has been received this form should be updated. All
      upper case and no spaces [regular expressions for NiNos]
    dimensions: null
    foreign_keys: null
    id: temp_ni_number
    latest_comments: null
    name: Temp NI number
    primary_key: false
    sample_generator: null
    status: Decided
    type: NINO
    validation:
      unique: true
  - comments: JF - 'Change to age' TR - 'Would be good to understand who (at HO?)
      wants age rather than age bracket - what's the purpose? Palladium and Ecorys
      both happy with bracketing and obviously it minimises the disclosiveness of
      the data.'
    description: Year of birth of participant. To be collected once at enrolment
    dimensions: null
    foreign_keys: null
    id: year_of_birth
    latest_comments: Deleted 'Month of birth' collection, just to collect age (year
      of birth) - to confirm if this satisfies HO requirements
    name: Year of birth
    primary_key: false
    sample_generator:
      args:
        end_date: -18y
        start_date: -65y
      method: date_between
    status: Pending consideration
    type: YYYY
    validation:
      required: true
  - comments: null
    description: Gender of participant. Must be one of the five categories provided.
      To be collected once at enrolment. Note there is a follow-up gender question
      as part of the baseline data collection.
    dimensions:
      dimensions:
      - description: null
        value: Man
      - description: null
        value: Woman
      - description: null
        value: Non-binary
      - description: null
        value: Other
      - description: null
        value: Prefer not to say
      id: gender
    foreign_keys: null
    id: gender
    latest_comments: null
    name: Gender
    primary_key: false
    sample_generator: null
    status: Pending consideration
    type: Categorical
    validation:
      dimension: gender
      required: true
  - comments: Confirm whether this should be string or list of LA's
    description: Local authority where participant was located once asylum status
      was granted. To be collected once at enrolment into the program.
    dimensions: null
    foreign_keys: null
    id: dispersal_area
    latest_comments: null
    name: Dispersal area
    primary_key: false
    sample_generator: null
    status: Decided
    type: String
    validation:
      required: true
  - comments: null
    description: Date of participant enrolment onto the program. Month and Year of
      enrolment required. To be collected once at enrolment.
    dimensions: null
    foreign_keys: null
    id: date_started_service
    latest_comments: null
    name: Date started with service
    primary_key: false
    sample_generator:
      args:
        end_date: -18y
        start_date: -65y
      method: date_between
    status: Decided
    type: Date
    validation:
      date_after: date_asylum_status_granted
      required: true
  id: person
---
