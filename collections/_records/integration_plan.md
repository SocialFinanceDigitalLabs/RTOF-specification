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
    latest_comments: null
    name: Unique person identifier
    primary_key: true
    sample_generator: null
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
    description: Selection of which integration outcome has been achieved. To be collected
      at each outcome submission.
    dimensions: null
    foreign_keys: null
    id: integration_outcome_type
    latest_comments: null
    name: Integration outcome type
    primary_key: true
    sample_generator: null
    status: Decided
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
  - comments: null
    description: Date of integration plan outcome achievement. To be collected at
      each outcome submission.
    dimensions: null
    foreign_keys: null
    id: integration_outcome_achieved_date
    latest_comments: null
    name: Date integration plan outcome acheived
    primary_key: false
    sample_generator:
      args:
        end_date: +2y
        start_date: +2m
      method: date_between
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
  - comments: TBC on categories - waiting for engagement with providers
    description: tbc. To be collected at each outcome submission.
    dimensions: null
    foreign_keys: null
    id: integration_social
    latest_comments: tbc - Ecorys to confirm categories after provider engagement
    name: Social bonds / bridges / links
    primary_key: false
    sample_generator: null
    status: Blocked
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
  - comments: TBC on categories - waiting for engagement with providers
    description: tbc. To be collected at each outcome submission.
    dimensions: null
    foreign_keys: null
    id: integration_comms_language
    latest_comments: tbc - Ecorys to confirm categories after provider engagement
    name: Language and communication
    primary_key: false
    sample_generator: null
    status: Blocked
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
  - comments: TBC on categories - waiting for engagement with providers
    description: tbc. To be collected at each outcome submission.
    dimensions: null
    foreign_keys: null
    id: integration_digital
    latest_comments: tbc - Ecorys to confirm categories after provider engagement
    name: Digital skills
    primary_key: false
    sample_generator: null
    status: Blocked
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
  id: integration_plan
---
