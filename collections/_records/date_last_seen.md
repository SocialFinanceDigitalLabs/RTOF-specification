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
    latest_comments: null
    name: Unique person identifier
    primary_key: true
    status: Decided
    type:
      description: A string of Unicode characters as defined by the JSON Schema `string`
        type.
      id: string
    validation:
    - args:
      - help: true/false value indicating if the current field is required
        name: enabled
        type: boolean
      description: 'A field with ''required: true'' must be present in the data record,
        and must have a non-blank value. It is short-hand

        for ''notnull: true'' and ''notblank: true''.

        '
      id: required
    - args:
      - help: true/false value indicating if the current field is required
        name: enabled
        type: boolean
      description: 'A field with ''unique: true'' should be unique within the dataset
        for this provider.

        '
      id: unique
  - comments: description tbc - ask providers once, at the end of the programme, to
      go through list of participants and estimate whether, and when, participants
      stopped engaging.
    description: Date of last interaction with participant. Month and Year required.
      To be collected annually during annual caseload review.
    dimensions: null
    foreign_keys: null
    id: date_last_seen
    latest_comments: null
    name: Date last seen
    primary_key: false
    status: Decided
    type:
      description: Represents a single date. JSON Schema has no direct date representation,
        but can be considered a restriction on string to match the ISO-8601 format,
        e.g. 2021-07-20
      id: date
    validation:
    - args:
      - help: true/false value indicating if the current field is required
        name: enabled
        type: boolean
      description: 'A field with ''required: true'' must be present in the data record,
        and must have a non-blank value. It is short-hand

        for ''notnull: true'' and ''notblank: true''.

        '
      id: required
    - args:
      - help: The ID of the field that this date has to be after
        items:
          type: string
        name: field_id
        type: array
      description: 'Only used for fields of type date, this validator ensures that
        the provided value is after the date indicated. When

        multiple

        '
      id: date_after
  id: date_last_seen
---
