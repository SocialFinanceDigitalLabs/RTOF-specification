---
layout: record
record:
  description: 'This form outlines the required baseline data for all service users,
    the data is to be collected across interactions with participants and submitted
    either when submitting form: integration_plan or within 3 months after enrolment.'
  fields:
  - comments: Minimum data collection required to understand enrolment
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
  - comments: To ensure we use the same categories HO use for data collection
    description: Nationality of participant. A list of nationalities are provided.
      Must select one of the given categories, please see nationality descriptions
      to link with the relevant code. To be collected once and submitted within 3
      months of enrolment.
    dimensions: null
    foreign_keys: null
    id: nationality
    latest_comments: null
    name: Nationality
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
  - comments: The categories for this are still to be decided and will be a product
      of engagement with frontline providers during mobilistion.
    description: The referral source that led the participant to RTOF.
    dimensions: null
    foreign_keys: null
    id: referral_source
    latest_comments: Categories tbc after provider engagement
    name: Referral source
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
  - comments: null
    description: Do you identify as transgender? A question which follows on from
      the question in the person data form, with 'identify as transgender', 'do not
      identify as transgender' or 'prefer not to say'. To be collected once and submitted
      within 3 months of enrolment.
    dimensions: null
    foreign_keys: null
    id: transgender
    latest_comments: tbc with Ecorys, Palladium and HO
    name: Transgender
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
    description: Selection of either single or couple. Couple includes living with
      more than one individual. To be collected once and submitted within 3 months
      of enrolment.
    dimensions: null
    foreign_keys: null
    id: living_status
    latest_comments: tbc with Ecorys, Palladium and HO
    name: Living status
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
    description: Do you currently have any dependents in the UK? Yes / No to understand
      whether the participant has any depedents curently in the UK. To be collected
      once and submitted within 3 months of enrolment.
    dimensions: null
    foreign_keys: null
    id: current_dependents_uk
    latest_comments: tbc with Ecorys, Palladium and HO
    name: Current dependents in UK
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
    description: If answered Yes to 'current dependents UK'. Selection of each option
      that applies to the participant. To be collected once and submitted within 3
      months of enrolment.
    dimensions: null
    foreign_keys: null
    id: current_number_of_dependents_uk
    latest_comments: tbc with Ecorys, Palladium and HO
    name: Current dependents in UK
    primary_key: false
    sample_generator: null
    status: Pending consideration
    type:
      description: Can contain multiple values. Can either be represented as a native
        list in formats that support them, such as JSON or XML, or encoded as a CSV
        string. If accompanied by a `dimension` validator, then each item in the list
        must be in the allowed values.
      id: list
    validation:
    - args:
      - help: The ID of the category that this list has to be a member of.
        name: category_id
        type: string
      description: 'Only used for fields of type categorical, this validator ensures
        that the provided value is part of category

        list identified.

        '
      id: dimension
  - comments: To confirm alternative collection route if an integration plan is not
      submitted [eg. Provider caseload review]
    description: Date participant entered the UK, relating to their latest and current
      arrival. To be collected once and submitted within 3 months of enrolment.
    dimensions: null
    foreign_keys: null
    id: date_arrived_in_uk
    latest_comments: null
    name: Date arrived in UK
    primary_key: false
    sample_generator:
      args:
        end_date: -2m
        start_date: -2y
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
  - comments: Can we use HO data for this - to check with HO.
    description: Date participant was granted asylum status, relating to their latest
      and current asylum status. To be collected once and submitted within 3 months
      of enrolment.
    dimensions: null
    foreign_keys: null
    id: date_asylum_status_granted
    latest_comments: null
    name: Date asylum status granted
    primary_key: false
    sample_generator:
      args:
        end_date: -2m
        start_date: -1y
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
  - comments: https://esol.britishcouncil.org/sites/default/files/attachments/informational-page/ESOL%20level%20descriptors.pdf
    description: The language level of participant when entering RTOF. Selection of
      one of the specified category, further information on these levels can be found
      here [https://esol.britishcouncil.org/sites/default/files/attachments/informational-page/ESOL%20level%20descriptors.pdf].
      To be collected once and submitted within 3 months of enrolment.
    dimensions: null
    foreign_keys: null
    id: language_level_on_entry
    latest_comments: null
    name: Language level on entry
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
  - comments: To provide a relevant link to equivalent qualification levels around
      the world (https://www.gov.uk/what-different-qualification-levels-mean/list-of-qualification-levels)
    description: The highest level of qualification of participant when entering RTOF.
      Selection of one of the specified category, these refer to [https://www.gov.uk/what-different-qualification-levels-mean/list-of-qualification-levels#:~:text=Level%205%20qualifications%20are%3A,higher%20national%20diploma%20(%20HND%20)].
      To be collected once and submitted within 3 months of enrolment.
    dimensions: null
    foreign_keys: null
    id: highest_qualification_achieved
    latest_comments: null
    name: Highest qualification  level achieved
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
    description: This should only be submitted if the response to the field "highest
      qualification level achieved" was "unknown"
    dimensions: null
    foreign_keys: null
    id: age_finished_study
    latest_comments: tbc with Ecorys, Palladium and HO
    name: Age when finished study
    primary_key: false
    sample_generator: null
    status: Pending consideration
    type:
      description: An integer as defined by the JSON Schema `integer` type.
      id: integer
    validation: []
  - comments: Simple yes / no selection. To confirm whether this refers to 'ever employed
      in home country' or 'within a given time period before arriving in the UK' [explain
      use case of question - understanding if work in UK is comparable to prior experience]
    description: When participant left home country were they in any form of employment
      - yes / no response. To be collected once and submitted within 3 months of enrolment.
    dimensions: null
    foreign_keys: null
    id: employed_in_home_country
    latest_comments: null
    name: Employed in home country
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
  - comments: To confirm word limit (and possibly add a suggestion ie. Teacher)
    description: If answered 'Yes' to employed in home country field, state job role
      [e.g. teacher] of their last employment. Max word count 10 words. To be collected
      once and submitted within 3 months of enrolment.
    dimensions: null
    foreign_keys: null
    id: occupation_type
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
      - help: The number of characters
        name: characters
        type: integer
      description: 'Maximum number of unicode characters in string.

        '
      id: character_limit
  - comments: To confirm word limit (and possibly add a suggestion ie. Education)
    description: If answered 'Yes' to employed in home country field, state the sector
      [eg. education] of their last employment. Max word count 10 words. To be collected
      once and submitted within 3 months of enrolment.
    dimensions: null
    foreign_keys: null
    id: occupation_sector
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
      - help: The number of characters
        name: characters
        type: integer
      description: 'Maximum number of unicode characters in string.

        '
      id: character_limit
  - comments: null
    description: All participants to be asked what their employment goals. This can
      be sector, job role or employment-type. To be collected once and submitted within
      3 months of enrolment.
    dimensions: null
    foreign_keys: null
    id: occupation_goal
    latest_comments: tbc with Ecorys, Palladium and HO
    name: Occupation goal at baseline
    primary_key: false
    sample_generator: null
    status: Pending consideration
    type:
      description: A string of Unicode characters as defined by the JSON Schema `string`
        type.
      id: string
    validation:
    - args:
      - help: The number of characters
        name: characters
        type: integer
      description: 'Maximum number of unicode characters in string.

        '
      id: character_limit
  - comments: 'JF: Why not capture <8 hrs/week? Does this Q relate to status in home
      country? Suggest change ''unpaid work...'' to voluntary work (to include either
      for family or not) Clarify that sick/disabled relates to reason for unemployment
      (if this is the case) These comments also apply to other references to emplyment
      type'
    description: Selection of a single category describing the employment status of
      the participant prior to entering RTOF. To be collected once and submitted within
      3 months of enrolment.
    dimensions: null
    foreign_keys: null
    id: economic_status
    latest_comments: tbc with James W (Ecorys) to confirm requirements of the VfM
      assessment
    name: Main economic status at baseline
    primary_key: false
    sample_generator: null
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
  - comments: Ecorys to provide details. To be collected once and submitted within
      3 months of enrolment.
    description: tbc
    dimensions: null
    foreign_keys: null
    id: housing_baseline_accommodation
    latest_comments: tbc by Ecorys re. Value for Money assessment
    name: Accommodation type
    primary_key: false
    sample_generator: null
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
  id: baseline
---
