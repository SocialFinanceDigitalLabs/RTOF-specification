---
layout: record
record:
  description: This form outlines the required data for participants who are no longer
    engaged with the service. Data should be collected during the annual caseload
    review.
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
  - comments: description tbc - ask providers once, at the end of the programme, to
      go through list of participants and estimate whether, and when, participants
      stopped engaging.
    description: Date of last interaction with participant. Month and Year required.
      To be collected annually during annual caseload review.
    dimensions: null
    foreign_keys: null
    id: date_last_seen
    name: Date last seen
    primary_key: false
    sample_generator:
      args:
        end_date: null
        start_date: null
      method: date_between
    status: Decided
    type: Date
    validation:
      date_after: date_started_service
      required: true
  id: date_last_seen
---
