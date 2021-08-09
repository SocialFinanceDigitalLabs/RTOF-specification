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
    type: string
    validation:
      required: true
  - comments: To ensure we use the same categories HO use for data collection
    description: Nationality of participant. A list of nationalities are provided.
      Must select one of the given categories, please see nationality descriptions
      to link with the relevant code. To be collected once and submitted within 3
      months of enrolment.
    dimensions:
      dimensions:
      - description: Andorra
        value: AD
      - description: United Arab Emirates
        value: AE
      - description: Afghanistan
        value: AF
      - description: Antigua and Barbuda
        value: AG
      - description: Anguilla
        value: AI
      - description: Albania
        value: AL
      - description: Armenia
        value: AM
      - description: Angola
        value: AO
      - description: Antarctica
        value: AQ
      - description: Argentina
        value: AR
      - description: American Samoa
        value: AS
      - description: Austria
        value: AT
      - description: Australia
        value: AU
      - description: Aruba
        value: AW
      - description: "\xC5land Islands"
        value: AX
      - description: Azerbaijan
        value: AZ
      - description: Bosnia and Herzegovina
        value: BA
      - description: Barbados
        value: BB
      - description: Bangladesh
        value: BD
      - description: Belgium
        value: BE
      - description: Burkina Faso
        value: BF
      - description: Bulgaria
        value: BG
      - description: Bahrain
        value: BH
      - description: Burundi
        value: BI
      - description: Benin
        value: BJ
      - description: "Saint Barth\xE9lemy"
        value: BL
      - description: Bermuda
        value: BM
      - description: Brunei
        value: BN
      - description: Bolivia
        value: BO
      - description: Caribbean Netherlands
        value: BQ
      - description: Brazil
        value: BR
      - description: Bahamas
        value: BS
      - description: Bhutan
        value: BT
      - description: Bouvet Island
        value: BV
      - description: Botswana
        value: BW
      - description: Belarus
        value: BY
      - description: Belize
        value: BZ
      - description: Canada
        value: CA
      - description: Cocos (Keeling) Islands
        value: CC
      - description: Democratic Republic of the Congo
        value: CD
      - description: Central African Republic
        value: CF
      - description: Congo (Republic of)
        value: CG
      - description: Switzerland
        value: CH
      - description: "C\xF4te d'Ivoire (Ivory Coast)"
        value: CI
      - description: Cook Islands
        value: CK
      - description: Chile
        value: CL
      - description: Cameroon
        value: CM
      - description: China
        value: CN
      - description: Colombia
        value: CO
      - description: Costa Rica
        value: CR
      - description: Cuba
        value: CU
      - description: Cape Verde
        value: CV
      - description: "Cura\xE7ao"
        value: CW
      - description: Christmas Island
        value: CX
      - description: Cyprus
        value: CY
      - description: Czech Republic
        value: CZ
      - description: Germany
        value: DE
      - description: Djibouti
        value: DJ
      - description: Denmark
        value: DK
      - description: Dominica
        value: DM
      - description: Dominican Republic
        value: DO
      - description: Algeria
        value: DZ
      - description: Ecuador
        value: EC
      - description: Estonia
        value: EE
      - description: Egypt
        value: EG
      - description: Western Saharan
        value: EH
      - description: Eritrea
        value: ER
      - description: Spain
        value: ES
      - description: Ethiopia
        value: ET
      - description: Finland
        value: FI
      - description: Fiji
        value: FJ
      - description: Falkland Islands
        value: FK
      - description: Micronesia
        value: FM
      - description: Faroe Islands
        value: FO
      - description: France
        value: FR
      - description: Gabon
        value: GA
      - description: United Kingdom
        value: GB
      - description: Grenada
        value: GD
      - description: Georgia
        value: GE
      - description: French Guiana
        value: GF
      - description: Guernsey
        value: GG
      - description: Ghana
        value: GH
      - description: Gibraltar
        value: GI
      - description: Greenland
        value: GL
      - description: Gambia
        value: GM
      - description: Guinea
        value: GN
      - description: Guadeloupe
        value: GP
      - description: Equatorial Guinea
        value: GQ
      - description: Greece
        value: GR
      - description: South Georgia and the South Sandwich Islands
        value: GS
      - description: Guatemala
        value: GT
      - description: Guam
        value: GU
      - description: Guinea-Bissau
        value: GW
      - description: Guyana
        value: GY
      - description: Hong Kong
        value: HK
      - description: Heard and McDonald Islands
        value: HM
      - description: Honduras
        value: HN
      - description: Croatia
        value: HR
      - description: Haiti
        value: HT
      - description: Hungary
        value: HU
      - description: Indonesia
        value: ID
      - description: Ireland
        value: IE
      - description: Israel
        value: IL
      - description: Isle of Man
        value: IM
      - description: India
        value: IN
      - description: British Indian Ocean Territory
        value: IO
      - description: Iraq
        value: IQ
      - description: Iran
        value: IR
      - description: Iceland
        value: IS
      - description: Italy
        value: IT
      - description: Jersey
        value: JE
      - description: Jamaica
        value: JM
      - description: Jordan
        value: JO
      - description: Japan
        value: JP
      - description: Kenya
        value: KE
      - description: Kyrgyzstan
        value: KG
      - description: Cambodia
        value: KH
      - description: Kiribati
        value: KI
      - description: Comoros
        value: KM
      - description: Saint Kitts and Nevis
        value: KN
      - description: North Korea
        value: KP
      - description: South Korea
        value: KR
      - description: Kuwait
        value: KW
      - description: Cayman Islands
        value: KY
      - description: Kazakhstan
        value: KZ
      - description: Laos
        value: LA
      - description: Lebanon
        value: LB
      - description: Saint Lucia
        value: LC
      - description: Liechtenstein
        value: LI
      - description: Sri Lanka
        value: LK
      - description: Liberia
        value: LR
      - description: Lesotho
        value: LS
      - description: Lithuania
        value: LT
      - description: Luxembourg
        value: LU
      - description: Latvia
        value: LV
      - description: Libya
        value: LY
      - description: Morocco
        value: MA
      - description: Monaco
        value: MC
      - description: Moldova
        value: MD
      - description: Montenegro
        value: ME
      - description: Saint Martin (France)
        value: MF
      - description: Madagascar
        value: MG
      - description: Marshall Islands
        value: MH
      - description: Macedonia
        value: MK
      - description: Mali
        value: ML
      - description: Burma (Republic of the Union of Myanmar)
        value: MM
      - description: Mongolia
        value: MN
      - description: Macau
        value: MO
      - description: Northern Mariana Islands
        value: MP
      - description: Martinique
        value: MQ
      - description: Mauritania
        value: MR
      - description: Montserrat
        value: MS
      - description: Malta
        value: MT
      - description: Mauritius
        value: MU
      - description: Maldives
        value: MV
      - description: Malawi
        value: MW
      - description: Mexico
        value: MX
      - description: Malaysia
        value: MY
      - description: Mozambique
        value: MZ
      - description: Namibia
        value: NA
      - description: New Caledonia
        value: NC
      - description: Niger
        value: NE
      - description: Norfolk Island
        value: NF
      - description: Nigeria
        value: NG
      - description: Nicaragua
        value: NI
      - description: Netherlands
        value: NL
      - description: Norway
        value: 'NO'
      - description: Nepal
        value: NP
      - description: Nauru
        value: NR
      - description: Niue
        value: NU
      - description: New Zealand
        value: NZ
      - description: Oman
        value: OM
      - description: Panama
        value: PA
      - description: Peru
        value: PE
      - description: French Polynesia
        value: PF
      - description: Papua New Guinea
        value: PG
      - description: Philippines
        value: PH
      - description: Pakistan
        value: PK
      - description: Poland
        value: PL
      - description: St. Pierre and Miquelon
        value: PM
      - description: Pitcairn
        value: PN
      - description: Puerto Rico
        value: PR
      - description: Palestine
        value: PS
      - description: Portugal
        value: PT
      - description: Palau
        value: PW
      - description: Paraguay
        value: PY
      - description: Qatar
        value: QA
      - description: "R\xE9union"
        value: RE
      - description: Romania
        value: RO
      - description: Serbia
        value: RS
      - description: Russian Federation
        value: RU
      - description: Rwanda
        value: RW
      - description: Saudi Arabia
        value: SA
      - description: Solomon Islands
        value: SB
      - description: Seychelles
        value: SC
      - description: Sudan
        value: SD
      - description: Sweden
        value: SE
      - description: Singapore
        value: SG
      - description: Saint Helena
        value: SH
      - description: Slovenia
        value: SI
      - description: Svalbard and Jan Mayen Islands
        value: SJ
      - description: Slovakia
        value: SK
      - description: Sierra Leone
        value: SL
      - description: San Marino
        value: SM
      - description: Senegal
        value: SN
      - description: Somalia
        value: SO
      - description: Suriname
        value: SR
      - description: South Sudan
        value: SS
      - description: "S\xE3o Tome and Pr\xEDncipe"
        value: ST
      - description: El Salvador
        value: SV
      - description: Saint Martin (Netherlands)
        value: SX
      - description: Syria
        value: SY
      - description: Swaziland
        value: SZ
      - description: Turks and Caicos Islands
        value: TC
      - description: Chad
        value: TD
      - description: French Southern Territories
        value: TF
      - description: Togo
        value: TG
      - description: Thailand
        value: TH
      - description: Tajikistan
        value: TJ
      - description: Tokelau
        value: TK
      - description: Timor-Leste
        value: TL
      - description: Turkmenistan
        value: TM
      - description: Tunisia
        value: TN
      - description: Tonga
        value: TO
      - description: Turkey
        value: TR
      - description: Trinidad and Tobago
        value: TT
      - description: Tuvalu
        value: TV
      - description: Taiwan
        value: TW
      - description: Tanzania
        value: TZ
      - description: Ukraine
        value: UA
      - description: Uganda
        value: UG
      - description: United States Minor Outlying Islands
        value: UM
      - description: United States of America
        value: US
      - description: Uruguay
        value: UY
      - description: Uzbekistan
        value: UZ
      - description: Vatican
        value: VA
      - description: Saint Vincent and Grenadines
        value: VC
      - description: Venezuela
        value: VE
      - description: British Virgin Islands
        value: VG
      - description: United States Virgin Islands
        value: VI
      - description: Vietnam
        value: VN
      - description: Vanuatu
        value: VU
      - description: Wallis and Futuna Islands
        value: WF
      - description: Samoa
        value: WS
      - description: Yemen
        value: YE
      - description: Mayotte
        value: YT
      - description: South Africa
        value: ZA
      - description: Zambia
        value: ZM
      - description: Zimbabwe
        value: ZW
      id: nationality
    foreign_keys: null
    id: nationality
    latest_comments: null
    name: Nationality
    primary_key: false
    sample_generator: null
    status: Decided
    type: Categorical
    validation:
      dimension: nationality
      required: true
  - comments: The categories for this are still to be decided and will be a product
      of engagement with frontline providers during mobilistion.
    description: The referral source that led the participant to RTOF.
    dimensions:
      dimensions: []
      id: referral_source
    foreign_keys: null
    id: referral_source
    latest_comments: Categories tbc after provider engagement
    name: Referral source
    primary_key: false
    sample_generator: null
    status: Blocked
    type: Categorical
    validation:
      dimension: referral_source
      required: true
  - comments: null
    description: Do you identify as transgender? A question which follows on from
      the question in the person data form, with 'identify as transgender', 'do not
      identify as transgender' or 'prefer not to say'. To be collected once and submitted
      within 3 months of enrolment.
    dimensions:
      dimensions:
      - description: null
        value: Identify as transgender
      - description: null
        value: Do not identify as Transgender
      - description: null
        value: Prefer not to say
      id: transgender
    foreign_keys: null
    id: transgender
    latest_comments: tbc with Ecorys, Palladium and HO
    name: Transgender
    primary_key: false
    sample_generator: null
    status: Pending consideration
    type: Categorical
    validation:
      dimension: transgender
      required: true
  - comments: null
    description: Selection of either single or couple. Couple includes living with
      more than one individual. To be collected once and submitted within 3 months
      of enrolment.
    dimensions:
      dimensions:
      - description: null
        value: Single
      - description: null
        value: Couple
      id: living_status
    foreign_keys: null
    id: living_status
    latest_comments: tbc with Ecorys, Palladium and HO
    name: Living status
    primary_key: false
    sample_generator: null
    status: Pending consideration
    type: Categorical
    validation:
      dimension: living_status
      required: true
  - comments: null
    description: Do you currently have any dependents in the UK? Yes / No to understand
      whether the participant has any depedents curently in the UK. To be collected
      once and submitted within 3 months of enrolment.
    dimensions:
      dimensions:
      - description: null
        value: 'Yes'
      - description: null
        value: 'No'
      id: current_dependents_uk
    foreign_keys: null
    id: current_dependents_uk
    latest_comments: tbc with Ecorys, Palladium and HO
    name: Current dependents in UK
    primary_key: false
    sample_generator: null
    status: pending consideration
    type: Categorical
    validation:
      dimension: current_dependents_uk
      required: true
  - comments: null
    description: Selection of each option that applies to the participant. To be collected
      once and submitted within 3 months of enrolment.
    dimensions:
      dimensions:
      - description: null
        value: 0-4
      - description: null
        value: 5-11
      - description: null
        value: 11-17
      - description: null
        value: Caring responsibilities for an adult
      id: current_number_of_dependents_uk
    foreign_keys: null
    id: current_number_of_dependents_uk
    latest_comments: tbc with Ecorys, Palladium and HO
    name: Current dependents in UK
    primary_key: false
    sample_generator: null
    status: Pending consideration
    type: List
    validation:
      dimension: current_number_of_dependents_uk
      required: true
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
    type: Date
    validation:
      date_after: date_of_birth
      required: true
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
    type: Date
    validation:
      date_after: date_arrived_in_uk
      required: true
  - comments: https://esol.britishcouncil.org/sites/default/files/attachments/informational-page/ESOL%20level%20descriptors.pdf
    description: The language level of participant when entering RTOF. Selection of
      one of the specified category, further information on these levels can be found
      here [https://esol.britishcouncil.org/sites/default/files/attachments/informational-page/ESOL%20level%20descriptors.pdf].
      To be collected once and submitted within 3 months of enrolment.
    dimensions:
      dimensions:
      - description: null
        value: Below formal levels
      - description: null
        value: Pre-entry
      - description: null
        value: Entry level 1
      - description: null
        value: Entry level 2
      - description: null
        value: Entry level 3
      - description: null
        value: Level 1
      - description: null
        value: Level 2
      - description: null
        value: Beyond Level 2
      id: language_level_on_entry
    foreign_keys: null
    id: language_level_on_entry
    latest_comments: null
    name: Language level on entry
    primary_key: false
    sample_generator: null
    status: Decided
    type: Categorical
    validation:
      dimension: language_level_on_entry
      required: true
  - comments: To provide a relevant link to equivalent qualification levels around
      the world (https://www.gov.uk/what-different-qualification-levels-mean/list-of-qualification-levels)
    description: The highest level of qualification of participant when entering RTOF.
      Selection of one of the specified category, these refer to [https://www.gov.uk/what-different-qualification-levels-mean/list-of-qualification-levels#:~:text=Level%205%20qualifications%20are%3A,higher%20national%20diploma%20(%20HND%20)].
      To be collected once and submitted within 3 months of enrolment.
    dimensions:
      dimensions:
      - description: null
        value: Below formal levels
      - description: null
        value: Entry level
      - description: null
        value: Level 1-2
      - description: null
        value: Level 3-4
      - description: null
        value: Level 5+
      - description: null
        value: Unknown
      id: highest_qualification_achieved
    foreign_keys: null
    id: highest_qualification_achieved
    latest_comments: null
    name: Highest qualification  level achieved
    primary_key: false
    sample_generator: null
    status: Decided
    type: Categorical
    validation:
      dimension: highest_qualification_achieved
      required: true
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
    type: integer
    validation: {}
  - comments: Simple yes / no selection. To confirm whether this refers to 'ever employed
      in home country' or 'within a given time period before arriving in the UK' [explain
      use case of question - understanding if work in UK is comparable to prior experience]
    description: When participant left home country were they in any form of employment
      - yes / no response. To be collected once and submitted within 3 months of enrolment.
    dimensions:
      dimensions:
      - description: null
        value: 'Yes'
      - description: null
        value: 'No'
      id: employed_in_home_country
    foreign_keys: null
    id: employed_in_home_country
    latest_comments: null
    name: Employed in home country
    primary_key: false
    sample_generator: null
    status: Decided
    type: Categorical
    validation:
      dimension: employed_in_home_country
      required: true
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
    type: Free Text (short)
    validation:
      character_limit: 255
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
    type: Free Text (short)
    validation:
      character_limit: 255
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
    type: Free Text (short)
    validation:
      character_limit: 255
  - comments: 'JF: Why not capture <8 hrs/week? Does this Q relate to status in home
      country? Suggest change ''unpaid work...'' to voluntary work (to include either
      for family or not) Clarify that sick/disabled relates to reason for unemployment
      (if this is the case) These comments also apply to other references to emplyment
      type'
    description: Selection of a single category describing the employment status of
      the participant prior to entering RTOF. To be collected once and submitted within
      3 months of enrolment.
    dimensions:
      dimensions:
      - description: null
        value: PT 0-15 hours per week
      - description: null
        value: PT 16-30 hours per week
      - description: null
        value: FT 31 hours +
      - description: null
        value: Self employed
      - description: null
        value: Government employment & training programme
      - description: null
        value: Unpaid work for relatives business
      - description: null
        value: Unemployed (but looking/available for work)
      - description: null
        value: Looking after family/home
      - description: null
        value: Temporarily sick/injured
      - description: null
        value: Long term sick or disabled
      - description: null
        value: Retired
      id: economic_status
    foreign_keys: null
    id: economic_status
    latest_comments: tbc with James W (Ecorys) to confirm requirements of the VfM
      assessment
    name: Main economic status at baseline
    primary_key: false
    sample_generator: null
    status: Work in progress
    type: Categorical
    validation:
      dimension: economic_status
      required: true
  - comments: Ecorys to provide details. To be collected once and submitted within
      3 months of enrolment.
    description: tbc
    dimensions:
      dimensions:
      - description: null
        value: tbc
      id: housing_baseline_accommodation
    foreign_keys: null
    id: housing_baseline_accommodation
    latest_comments: tbc by Ecorys re. Value for Money assessment
    name: Accommodation type
    primary_key: false
    sample_generator: null
    status: Work in progress
    type: Categorical
    validation:
      dimension: housing_baseline_accommodation
      required: true
  id: baseline
---
