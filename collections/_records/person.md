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
    name: Unique person identifier
    primary_key: true
    sample_generator: null
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
    name: NI Number
    primary_key: false
    sample_generator: null
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
    name: Temp NI number
    primary_key: false
    sample_generator: null
    type: NINO
    validation:
      unique: true
  - comments: null
    description: Date of birth of participant. To be collected once at enrolment
    dimensions: null
    foreign_keys: null
    id: date_of_birth
    name: Date of birth
    primary_key: false
    sample_generator:
      args:
        end_date: -18y
        start_date: -65y
      method: date_between
    type: YYYY-MM
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
    name: Gender
    primary_key: false
    sample_generator: null
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
    name: Dispersal area
    primary_key: false
    sample_generator: null
    type: String
    validation:
      required: true
  - comments: Categories TBC after engagement with the selected providers
    description: Where the participant was referred to your service from. Select one
      of the given options (if unknown please select 'Other'). To be collected at
      enrolment.
    dimensions:
      dimensions: []
      id: referral_source
    foreign_keys: null
    id: referral_source
    name: Referral source
    primary_key: false
    sample_generator: null
    type: Categorical
    validation:
      dimension: referral_source
      required: true
  - comments: null
    description: Date of participant enrolment onto the program. Month and Year of
      enrolment required. To be collected once at enrolment.
    dimensions: null
    foreign_keys: null
    id: date_started_service
    name: Date started with service
    primary_key: false
    sample_generator:
      args:
        end_date: -18y
        start_date: -65y
      method: date_between
    type: Date
    validation:
      date_after: date_asylum_status_granted
      required: true
  id: person
---
