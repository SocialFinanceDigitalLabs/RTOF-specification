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
  - comments: JF - 'Change to age' TR - 'Would be good to understand who (at HO?)
      wants age rather than age bracket - what's the purpose? Palladium and Ecorys
      both happy with bracketing and obviously it minimises the disclosiveness of
      the data.'
    description: Year of birth of participant. To be collected once at enrolment
    dimensions: null
    foreign_keys: null
    id: year_of_birth
    latest_comments: null
    name: Year of birth
    primary_key: false
    sample_generator:
      args:
        end_date: -18y
        start_date: -65y
      method: date_between
    status: Decided
    type:
      description: Represents a single (gregorian) year. Again, there is no JSON Schema
        equivalent, but this should be considered to have the same meaning as `gYear`
        in XML Schema Part 2. Encoded as an integer.
      id: year
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
    description: Gender of participant. Must be one of the five categories provided.
      To be collected once at enrolment. Note there is a follow-up gender question
      as part of the baseline data collection.
    dimensions: null
    foreign_keys: null
    id: gender
    latest_comments: null
    name: Gender
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
  - comments: Confirm whether this should be string or list of LA's
    description: Local authority where participant was located once asylum status
      was granted. To be collected once at enrolment into the program.
    dimensions: null
    foreign_keys: null
    id: dispersal_area
    latest_comments: null
    name: Dispersal area
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
  - comments: null
    description: Date of participant enrolment onto the program. Month and Year of
      enrolment required. To be collected once at enrolment.
    dimensions: null
    foreign_keys: null
    id: date_started_service
    latest_comments: null
    name: Date started with service
    primary_key: false
    sample_generator:
      args:
        end_date: -18y
        start_date: -65y
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
  id: person
---
