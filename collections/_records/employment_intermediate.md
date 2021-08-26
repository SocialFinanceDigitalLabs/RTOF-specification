---
layout: record
record:
  description: This form outlines the required data for participants who achieve the
    intermediate employment outcome. Data should be collected when achieving the intermediate
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
  - comments: Date of completion of the final qualifying  outcome.
    description: Date of intermediate employment outcome achievement. To be collected
      once at intermediate employment outcome submission.
    dimensions: null
    foreign_keys: null
    id: date_intermediate_employment_outcome
    latest_comments: null
    name: Date achieved intermediate outcome
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
  - comments: Selection of (at least) 3 intermediate outcomes achieved.
    description: Selection of at least 3 intermediate outcomes achieved from the provided
      list [link to list]. To be collected once at intermediate employment outcome
      submission.
    dimensions:
      dimensions:
      - description: Successful formal recognition and/or comparison of qualifications
          or skills
        value: qualifications or skills
      - description: Completion of relevant training course
        value: training course
      - description: Completion of 10 hours+ mentoring and/or coaching
        value: mentoring and/or coaching
      - description: Completion of 10 hours+ employability training
        value: employability
      - description: Volunteering - at least 10 days
        value: Volunteering
      - description: Work experience - at least 5 days
        value: work experience
      - description: Internship- maximum 10 days, unless paid for at the National
          Minimum Wage (or above) for people aged 18-22 or the National Living Wage
          (or above) for people aged 23+*
        value: Internship
      - description: Completion of sector-specific language training which is additional
          to the mainstream.
        value: sector-specific language training
      - description: Developed business plan for self-employment
        value: business plan for self-employment
      - description: Registered business for self-employment
        value: Registered business for self-employment
      - description: "another specified activity directly relevant to achieving the\
          \ individual\u2019s employment goals"
        value: another specified activity
      id: employment_outcome_type
    foreign_keys: null
    id: intermediate_employment_outcome_type
    latest_comments: null
    name: Type of intermediate outcome
    primary_key: false
    status: Decided
    type:
      description: Can contain multiple values. Can either be represented as a native
        list in formats that support them, such as JSON or XML, or encoded as a CSV
        string. If accompanied by a `dimension` validator, then each item in the list
        must be in the allowed values.
      id: list
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
  id: employment_intermediate
---
