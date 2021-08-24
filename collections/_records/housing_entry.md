---
layout: record
record:
  description: This form outlines the required data for participants who achieve the
    housing entry outcome. Data should be collected when achieving the housing entry
    outcome.
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
    latest_comments: null
    name: Unique person identifier
    primary_key: true
    sample_generator: null
    status: Decided
    type:
      description: A string
      id: string
    validation:
      required: true
      unique: true
  - comments: null
    description: Date of housing entry outcome achieved. To be collected once at entry
      to housing outcome submission.
    dimensions: null
    foreign_keys: null
    id: housing_entry_date
    latest_comments: null
    name: Date of housing entry
    primary_key: false
    sample_generator:
      args:
        end_date: +2y
        start_date: +6m
      method: date_between
    status: Decided
    type:
      description: A string
      id: Date
    validation:
      date_after: date_started_service
      required: true
  - comments: tbc - once selected, the categories will align with baseline collection
    description: tbc
    dimensions:
      dimensions:
      - description: null
        value: tbc
      id: housing_entry_accomodation
    foreign_keys: null
    id: housing_entry_accomodation
    latest_comments: tbc - same comments as 'housing_baseline_accommodation', categories
      to align
    name: Accomodation type
    primary_key: false
    sample_generator: null
    status: Work in progress
    type:
      description: null
      id: Categorical
    validation:
      dimension: housing_entry_accomodation
      required: true
  id: housing_entry
---
