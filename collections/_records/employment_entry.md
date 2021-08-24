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
      description: A string
      id: string
    validation:
      required: true
  - comments: null
    description: Employment entry can either be an employment outcome or self-employment
      outcome. To be collected once at entry to employment outcome submission.
    dimensions:
      dimensions:
      - description: null
        value: Employment
      - description: null
        value: Self-employment
      id: employment_entry_outcome_type
    foreign_keys: null
    id: employment_entry_outcome_type
    latest_comments: null
    name: Type of employment entry outcome
    primary_key: false
    sample_generator: null
    status: Decided
    type:
      description: null
      id: Categorical
    validation:
      dimension: employment_entry_outcome_type
      required: true
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
      description: A string
      id: Date
    validation:
      date_after: date_started_service
      required: true
  - comments: null
    description: Selection of a single category describing the type of employment
      participant is entering for the employment outcome achievement. To be collected
      once at entry to employment outcome submission.
    dimensions:
      dimensions:
      - description: null
        value: PT 0-15 hours per week
      - description: null
        value: PT 16-30 hours per week
      - description: null
        value: FT 31 hours +
      - description: null
        value: Government employment & training programme
      id: employment_entry_details
    foreign_keys: null
    id: employment_entry_details
    latest_comments: tbc - same comments as baseline 'economic_status', categories
      to align
    name: Details of paid employment
    primary_key: false
    sample_generator: null
    status: Pending consideration
    type:
      description: null
      id: Categorical
    validation:
      dimension: employment_entry_details
      required: true
  - comments: null
    description: State participants employment type for the achievement of entry to
      employment outcome. To be collected once at entry to employment outcome submission.
    dimensions: null
    foreign_keys: null
    id: employment_entry_occupation
    latest_comments: null
    name: Occupation type
    primary_key: false
    sample_generator: null
    status: Decided
    type:
      description: null
      id: Free Text (short)
    validation:
      character_limit: 255
      required: true
  - comments: null
    description: State the participants employment sector for the achievement of entry
      to employment outcome. To be collected once at entry to employment outcome submission.
    dimensions: null
    foreign_keys: null
    id: employment_entry_sector
    latest_comments: null
    name: Sector
    primary_key: false
    sample_generator: null
    status: Decided
    type:
      description: null
      id: Free Text (short)
    validation:
      character_limit: 255
      required: true
  id: employment_entry
---
