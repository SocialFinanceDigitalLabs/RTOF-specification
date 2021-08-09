---
layout: record
record:
  description: This form outlines the required data for participants who achieve the
    housing sustainment outcome. Data should be collected when achieving the housing
    sustainment outcome.
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
    status: Decided
    type: string
    validation:
      required: true
      unique: true
  - comments: null
    description: Date of housing sustainment outcome achieved. To be collected once
      at housing sustainment outcome submission.
    dimensions: null
    foreign_keys: null
    id: housing_sustainment_date
    name: Date housing sustainment achieved
    primary_key: false
    sample_generator:
      args:
        end_date: +3y
        start_date: +1y
      method: date_between
    status: Decided
    type: Date
    validation:
      date_after: housing_entry_date
      required: true
  id: housing_sustain
---
