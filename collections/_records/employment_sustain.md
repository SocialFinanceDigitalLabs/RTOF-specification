---
layout: record
record:
  description: This form outlines the required data for participants who achieve the
    employment sustainment outcome. Data should be collected when achieving the employment
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
    latest_comments: null
    name: Unique person identifier
    primary_key: true
    sample_generator: null
    status: Decided
    type: string
    validation:
      required: true
      unique: true
  - comments: null
    description: Date of employment sustainment outcome achieved. This can be either
      be for the self-employment or employment route. To be collected once at employment
      sustained outcome submission.
    dimensions: null
    foreign_keys: null
    id: employment_sustainment_date
    latest_comments: null
    name: Date employment sustainment outcome achieved
    primary_key: false
    sample_generator:
      args:
        end_date: +3y
        start_date: +1y
      method: date_between
    status: Decided
    type: Date
    validation:
      date_after: date_employment_entry
      required: true
  id: employment_sustain
---
