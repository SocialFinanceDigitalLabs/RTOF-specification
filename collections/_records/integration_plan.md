---
layout: record
record:
  description: This form outlines the required data for participants who achieve each
    integration plan outcome - one submission for each creation, 6-month progress
    and 12-month progress. Data should be collected when achieving each integration
    plan outcome.
  fields:
  - comments: null
    description: Person identifier provided in the person form. This can be a NINO
      or a unique provider ID. This must be unique for each individual supported on
      RTOF.
    dimensions: null
    foreign_keys:
    - field: unique_id
      record: person
    id: unique_id
    name: Unique person identifier
    primary_key: true
    sample_generator: null
    type: string
    validation:
      required: true
      unique: true
  - comments: null
    description: Date of integration plan outcome achievement. To be collected at
      each outcome submission.
    dimensions: null
    foreign_keys: null
    id: integration_outcome_achieved_date
    name: Date integration plan outcome acheived
    primary_key: true
    sample_generator:
      args:
        end_date: +2y
        start_date: +2m
      method: date_between
    type: Date
    validation:
      date_after: date_started_service
      required: true
  - comments: null
    description: Selection of which integration outcome has been achieved. To be collected
      at each outcome submission.
    dimensions:
      dimensions:
      - description: null
        value: Creation
      - description: null
        value: 6 month
      - description: null
        value: 12 month
      id: integration_outcome_type
    foreign_keys: null
    id: integration_outcome_type
    name: Integration outcome type
    primary_key: false
    sample_generator: null
    type: Categorical
    validation:
      dimension: integration_outcome_type
      required: true
  - comments: TBC on categories - waiting for engagement with providers
    description: tbc. To be collected at each outcome submission.
    dimensions:
      dimensions:
      - description: null
        value: tbc
      id: integration_social
    foreign_keys: null
    id: integration_social
    name: Social bonds / bridges / links
    primary_key: false
    sample_generator: null
    type: Categorical
    validation:
      dimension: integration_social
      required: true
  - comments: TBC on categories - waiting for engagement with providers
    description: tbc. To be collected at each outcome submission.
    dimensions:
      dimensions:
      - description: null
        value: tbc
      id: integration_comms_language
    foreign_keys: null
    id: integration_comms_language
    name: Language and communication
    primary_key: false
    sample_generator: null
    type: Categorical
    validation:
      dimension: integration_comms_language
      required: true
  - comments: TBC on categories - waiting for engagement with providers
    description: tbc. To be collected at each outcome submission.
    dimensions:
      dimensions:
      - description: null
        value: tbc
      id: integration_digital
    foreign_keys: null
    id: integration_digital
    name: Digital skills
    primary_key: false
    sample_generator: null
    type: Categorical
    validation:
      dimension: integration_digital
      required: true
  id: integration_plan
---
