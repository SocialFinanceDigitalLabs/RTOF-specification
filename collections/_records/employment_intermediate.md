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
    sample_generator: null
    status: Decided
    type:
      description: A string
      id: string
    validation:
      required: true
      unique: true
  - comments: Date of completion of the final qualifying  outcome.
    description: Date of intermediate employment outcome achievement. To be collected
      once at intermediate employment outcome submission.
    dimensions: null
    foreign_keys: null
    id: date_intermediate_employment_outcome
    latest_comments: null
    name: Date achieved intermediate outcome
    primary_key: false
    sample_generator:
      args:
        end_date: +2y
        start_date: +2m
      method: date_between
    status: Decided
    type:
      description: A string
      id: Date
    validation:
      date_after: date_started_service
      required: true
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
    sample_generator: null
    status: Decided
    type:
      description: null
      id: List
    validation:
      dimension: employment_outcome_type
      required: true
  id: employment_intermediate
---
