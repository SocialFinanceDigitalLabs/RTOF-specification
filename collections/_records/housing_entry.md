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
  - comments: null
    description: Date of housing entry outcome achieved. To be collected once at entry
      to housing outcome submission.
    dimensions: null
    foreign_keys: null
    id: housing_entry_date
    latest_comments: null
    name: Date of housing entry
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
    status: Work in progress
    type:
      description: Restricted to a set of fixed values. Represented as a string, this
        type must have a `dimension` validator indicating the set of allowed values.
      id: categorical
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
      - help: The ID of the category that this list has to be a member of.
        name: category_id
        type: string
      description: 'Only used for fields of type categorical, this validator ensures
        that the provided value is part of category

        list identified.

        '
      id: dimension
  id: housing_entry
---
