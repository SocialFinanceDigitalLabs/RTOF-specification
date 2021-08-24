---
layout: record
record:
  description: This form outlines the required data for participants who achieve the
    employment OR self-employment entry outcome. A participant can only achieve either
    the employment or self-employment outcome. Data should be collected when achieving
    the employment entry outcome.
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
  - comments: null
    description: Employment entry can either be an employment outcome or self-employment
      outcome. To be collected once at entry to employment outcome submission.
    dimensions: null
    foreign_keys: null
    id: employment_entry_outcome_type
    latest_comments: null
    name: Type of employment entry outcome
    primary_key: false
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
    description: Date of employment entry submission. To be collected once at entry
      to employment outcome submission.
    dimensions: null
    foreign_keys: null
    id: date_employment_entry
    latest_comments: null
    name: Date entered employment
    primary_key: false
    sample_generator:
      args:
        end_date: null
        start_date: null
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
  - comments: null
    description: Selection of a single category describing the type of employment
      participant is entering for the employment outcome achievement. To be collected
      once at entry to employment outcome submission.
    dimensions: null
    foreign_keys: null
    id: employment_entry_details
    latest_comments: tbc - same comments as baseline 'economic_status', categories
      to align
    name: Details of paid employment
    primary_key: false
    sample_generator: null
    status: Pending consideration
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
    description: State participants employment type for the achievement of entry to
      employment outcome. To be collected once at entry to employment outcome submission.
      For some providers this may be a categorical data field - please confirm with
      your nominated data lead.
    dimensions: null
    foreign_keys: null
    id: employment_entry_occupation
    latest_comments: null
    name: Occupation type
    primary_key: false
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
      - help: The number of characters
        name: characters
        type: integer
      description: 'Maximum number of unicode characters in string.

        '
      id: character_limit
  - comments: null
    description: State the participants employment sector for the achievement of entry
      to employment outcome. To be collected once at entry to employment outcome submission.
      For some providers this may be a categorical data field - please confirm with
      your nominated data lead.
    dimensions: null
    foreign_keys: null
    id: employment_entry_sector
    latest_comments: null
    name: Sector
    primary_key: false
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
      - help: The number of characters
        name: characters
        type: integer
      description: 'Maximum number of unicode characters in string.

        '
      id: character_limit
  id: employment_entry
---
