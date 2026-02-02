# AIRMAN Evaluation Report

## Level 1 metadata
```json
{
  "pdfs": [
    "10-General-Navigation-2014 (1).pdf",
    "11-radio-navigation-2014.pdf",
    "6-mass-and-balance-and-performance-2014.pdf",
    "7-Flight-Planning-and-Monitoring-2014.pdf",
    "Air-Regulation-RK-BALI (1).pdf",
    "Instruments.pdf",
    "Meteorology full book.pdf"
  ],
  "chunk_size": 1000,
  "chunk_overlap": 150,
  "embed_model": "sentence-transformers/all-MiniLM-L6-v2",
  "num_chunks": 6266
}
```

## Level 2 metadata
```json
{}
```

## Baseline vs Hybrid Metrics
```json
{
  "n_questions": 50,
  "level1_refusal_rate": 0.0,
  "level2_refusal_rate": 0.64,
  "level1_answer_rate": 1.0,
  "level2_answer_rate": 0.36,
  "level1_retrieval_hit_rate": 0.1,
  "level2_retrieval_hit_rate": 0.02,
  "level1_faithfulness_avg": 0.157,
  "level2_faithfulness_avg": 0.7,
  "level1_hallucination_avg": 0.843,
  "level2_hallucination_avg": 0.3
}
```

## Qualitative Analysis — 5 Best (Level 1)
```json
[
  {
    "question": "Why might chunk overlap reduce retrieval misses in dense technical text?",
    "answer": "It has the following disadvantages: Garbling This is caused by overlapping replies from two or more transponders on nearly the same bearing from the ground station and within a distance of 1.7 NM from each other measured on a line from the antenna.",
    "faithfulness": 1.0,
    "top_chunk_citations": [
      "6-mass-and-balance-and-performance-2014.pdf | page 69",
      "11-radio-navigation-2014.pdf | page 196",
      "11-radio-navigation-2014.pdf | page 239"
    ],
    "explanation": "Answer sentences are mostly present in retrieved text."
  },
  {
    "question": "If a user asks for a multi-step explanation, how can you keep it grounded in retrieved text?",
    "answer": "Which statement with respect to the step climb is correct? Which statement with respect to the step climb is correct? Performing a step climb based on economy can be limited by the 1.3g altitude c.",
    "faithfulness": 1.0,
    "top_chunk_citations": [
      "6-mass-and-balance-and-performance-2014.pdf | page 466",
      "6-mass-and-balance-and-performance-2014.pdf | page 485",
      "7-Flight-Planning-and-Monitoring-2014.pdf | page 277"
    ],
    "explanation": "Answer sentences are mostly present in retrieved text."
  },
  {
    "question": "What are the two ADC system types mentioned and how do they differ at a high level?",
    "answer": "A number of different aircraft types may use the same basic Air Data Computer and this device will need to be integrated into the aircraft systems and this is achieved by a “Configuration Module”. The two types of ADC system found are described as either Analogue or Digital from the method of assessment and transmission of information used. the left or right Air Data Computer ( ADC), the Flight Management Computers ( FMC), the Flight Control Computers ( FCC), and the Standby Inertial Reference Systems (IRS).",
    "faithfulness": 0.667,
    "top_chunk_citations": [
      "Instruments.pdf | page 103",
      "Instruments.pdf | page 104",
      "Instruments.pdf | page 104"
    ],
    "explanation": "Answer is weakly supported by retrieved text; likely missing exact sentence match."
  },
  {
    "question": "Describe a failure mode where BM25 helps but reranking is still necessary.",
    "answer": "Where can the pilot look to see the thrust limit mode? Where can the pilot look to see the autothrottle mode? If there is a failure of an FMC, the second system can be expected to operate the aircraft successfully on its own - this is known as Single Mode.",
    "faithfulness": 0.667,
    "top_chunk_citations": [
      "Instruments.pdf | page 278",
      "Instruments.pdf | page 620",
      "Instruments.pdf | page 593"
    ],
    "explanation": "Answer is weakly supported by retrieved text; likely missing exact sentence match."
  },
  {
    "question": "If vector similarity is high but the chunk is off-topic, how does a cross-encoder reranker help?",
    "answer": "What does a CVR record? 4 identifications with the DME at a higher tone",
    "faithfulness": 0.5,
    "top_chunk_citations": [
      "7-Flight-Planning-and-Monitoring-2014.pdf | page 239",
      "Instruments.pdf | page 602",
      "Meteorology full book.pdf | page 477"
    ],
    "explanation": "Answer is weakly supported by retrieved text; likely missing exact sentence match."
  }
]
```

## Qualitative Analysis — 5 Worst (Level 1)
```json
[
  {
    "question": "Explain how you would generate and curate a 50-question set to cover factual, applied, and reasoning skills.",
    "answer": "30 615 30 Questions Questions 13 235 Questions 13 Questions Appendix A to Questions 16 17 18 19 20 21 30 643 30 Questions Questions 18 327 Questions 18 Questions Questions 30 550 Questions30 34 475 Questions 34 Questions",
    "faithfulness": 0.0,
    "top_chunk_citations": [
      "Meteorology full book.pdf | page 621",
      "10-General-Navigation-2014 (1).pdf | page 241",
      "Meteorology full book.pdf | page 649"
    ],
    "explanation": "Answer is weakly supported by retrieved text; likely missing exact sentence match."
  },
  {
    "question": "Explain why showing retrieved chunks in debug mode helps prevent hallucinations during development.",
    "answer": "The errors are usually more significant during changes of pitch attitude than during yawing or rolling movements so that the worst effects are at the start of the climb or descent and on levelling out.",
    "faithfulness": 0.0,
    "top_chunk_citations": [
      "Instruments.pdf | page 551",
      "Instruments.pdf | page 106",
      "6-mass-and-balance-and-performance-2014.pdf | page 101"
    ],
    "explanation": "Answer is weakly supported by retrieved text; likely missing exact sentence match."
  },
  {
    "question": "How would you extend the system to handle follow-up questions while keeping grounding strict?",
    "answer": "He must esta blish a system to check that amendments of his input data are incorporated properly in the system and that the system i s operating correctly on a continuous basis 18 339 Questions18 Questions Questions 32 548 32Questions Appendix A to Revision Questions 16 17 18 19 20 21 13 235 Questions 13 Questions Appendix A to Questions 16 17 18 19 20 21 30 615 30 Questions Questions 18 337 Questions18 Questions Appendix A (ii) Subject to the approval of the Authority, an operator may omit some of t his Data from the mass and balance documentation. (b) Computerised systems.",
    "faithfulness": 0.0,
    "top_chunk_citations": [
      "10-General-Navigation-2014 (1).pdf | page 241",
      "Meteorology full book.pdf | page 621",
      "Meteorology full book.pdf | page 343"
    ],
    "explanation": "Answer is weakly supported by retrieved text; likely missing exact sentence match."
  },
  {
    "question": "Explain how chunk size affects citations quality and answer completeness in a textbook PDF.",
    "answer": "97 Answers . 631 Answers to Specimen Examination Paper. 398 Explanations to Answers – Specimen Exam Paper .",
    "faithfulness": 0.0,
    "top_chunk_citations": [
      "6-mass-and-balance-and-performance-2014.pdf | page 485",
      "Instruments.pdf | page 563",
      "11-radio-navigation-2014.pdf | page 335"
    ],
    "explanation": "Answer is weakly supported by retrieved text; likely missing exact sentence match."
  },
  {
    "question": "Propose a confidence thresholding approach using reranker scores and how it triggers refusal.",
    "answer": "• Maximum landing weight The more limiting of the landing climb and the approach gradient requirements will determine the maximum mass for altitude and temperature at the landing aerodrome. Discontinued Approach Instrument Climb. 188 DISCONTINUED APPROACH CLIMB (One engine inoperative CS-25.121 (d)) A climb gradient not less than: • 2.1% for 2 engine aircraft • 2.4% for 3 engine aircraft • 2.7% for 4 engine aircraft With: • The critical engine inoperative and the remaining engines at go-around thrust • Landing gear retracted • Flaps in the approach configuration, provided that the approach flap V SR does not exceed 110% of landing flap VSR • Aerodrome altitude • Ambient temperature • Speed: Normal approach speed but not greater than 1.4VSR.",
    "faithfulness": 0.0,
    "top_chunk_citations": [
      "10-General-Navigation-2014 (1).pdf | page 338",
      "6-mass-and-balance-and-performance-2014.pdf | page 313",
      "10-General-Navigation-2014 (1).pdf | page 337"
    ],
    "explanation": "Answer is weakly supported by retrieved text; likely missing exact sentence match."
  }
]
```

## Qualitative Analysis — 5 Best (Level 2)
```json
[
  {
    "question": "If an outside air temperature of -30°C is measured at FL200, what is the ISA temperature deviation?",
    "answer": "An outside air temperature of -30°C is measured whilst cruising at FL200. What is the temperature deviation, in degrees Celsius, from the International Standard Atmosphere overhead Frankfurt (50N 08E) at FL180? What is the temperature deviation from the ISA at this level?",
    "faithfulness": 0.667,
    "top_chunk_citations": [
      "Meteorology full book.pdf | page 17",
      "Meteorology full book.pdf | page 18",
      "Meteorology full book.pdf | page 149"
    ],
    "explanation": "Answer is weakly supported by retrieved text; likely missing exact sentence match."
  },
  {
    "question": "What is the definition of meteorology?",
    "answer": "1 3 The Atmosphere1 The Atmosphere A Definition of Meteorology “The branch of science dealing with the earth’s atmosphere and the physical processes occurring in it.” Reasons for Studying Meteorology • To understand the physical processes in the atmosphere • To understand the meteorological hazards, their effect on aircraft and how to minimize the risks posed by those hazards • To identify the weather information that is required for each flight • To interpret actual and forecast weather conditions from the documentation provided • To analyse and evaluate weather information before flight and in-flight • To devise solutions to problems presented by weather conditions Weather is the one factor in modern aviation over which man has no control; a knowledge of meteorology will at least enable the aviator to anticipate some of the difficulties which weather may cause. 1 1 Chapter The Atmosphere A Definition of Meteorology . The study of temperature variation, both horizontally and vertically has considerable significance in the study of meteorology.",
    "faithfulness": 0.333,
    "top_chunk_citations": [
      "Meteorology full book.pdf | page 9",
      "Meteorology full book.pdf | page 7",
      "Meteorology full book.pdf | page 23"
    ],
    "explanation": "Answer is weakly supported by retrieved text; likely missing exact sentence match."
  },
  {
    "question": "What is the approximate composition of dry air by volume in the troposphere?",
    "answer": "What is the approximate composition of the dry air by volume in the troposphere? isobars far apart, temperature decreasing Temperature 5 60 5Temperature There are four processes which heat the troposphere: • Terrestrial Radiation. What happens to the temperature of a saturated air mass when descending?",
    "faithfulness": 0.333,
    "top_chunk_citations": [
      "Meteorology full book.pdf | page 17",
      "Meteorology full book.pdf | page 84",
      "Meteorology full book.pdf | page 637"
    ],
    "explanation": "Answer is weakly supported by retrieved text; likely missing exact sentence match."
  },
  {
    "question": "What does the tropopause mark in terms of temperature change with height?",
    "answer": "• The Tropopause: • This marks the boundary between the troposphere and the stratosphere and is where temperature ceases to fall with an increase in height. The average height of the tropopause at the Equator is 16-18 km with an average temperature of -75°C to -80°C, and at the poles 8 km with an average temperature of The Atmosphere 1 6 1The Atmosphere The Significance of Tropopause Height The significance of the tropopause height is that it usually marks: • the maximum height of significant cloud. decrease at 0.65 deg C per 100 m 5 63 Temperature 5 Temperature Inversions Where the temperature increases with an increase in height, then we have what is called an inversion.",
    "faithfulness": 0.333,
    "top_chunk_citations": [
      "Meteorology full book.pdf | page 11",
      "Meteorology full book.pdf | page 12",
      "Meteorology full book.pdf | page 16"
    ],
    "explanation": "Answer is weakly supported by retrieved text; likely missing exact sentence match."
  },
  {
    "question": "What are two reasons for studying meteorology for aviation?",
    "answer": "1 3 The Atmosphere1 The Atmosphere A Definition of Meteorology “The branch of science dealing with the earth’s atmosphere and the physical processes occurring in it.” Reasons for Studying Meteorology • To understand the physical processes in the atmosphere • To understand the meteorological hazards, their effect on aircraft and how to minimize the risks posed by those hazards • To identify the weather information that is required for each flight • To interpret actual and forecast weather conditions from the documentation provided • To analyse and evaluate weather information before flight and in-flight • To devise solutions to problems presented by weather conditions Weather is the one factor in modern aviation over which man has no control; a knowledge of meteorology will at least enable the aviator to anticipate some of the difficulties which weather may cause. 3 Reasons for Studying Meteorology . The Handbook of Aviation Meteorology makes the statement: “The study of atmospheric pressure may be said to form the foundations of the science of meteorology.” Atmospheric Pressure Atmospheric pressure is the force per unit area exerted by the atmosphere on any surface in contact with it.",
    "faithfulness": 0.333,
    "top_chunk_citations": [
      "Meteorology full book.pdf | page 9",
      "Meteorology full book.pdf | page 23",
      "Meteorology full book.pdf | page 7"
    ],
    "explanation": "Answer is weakly supported by retrieved text; likely missing exact sentence match."
  }
]
```

## Qualitative Analysis — 5 Worst (Level 2)
```json
[
  {
    "question": "In decision point procedure planning, what does contingency fuel between departure and decision point enable?",
    "answer": "The normal non-consumption of contingency fuel, which can be a considerable amount (usually 3% at least of the fuel between departure and Decision Point), permits Decision Point Procedure to be feasible and safe. Departure Airport Decision Point Destination Airport En route Alternate Destination Alternate Figure 2.7 Decision point procedure Comparing the Decision Point Procedure fuel requirement with the normal fuel requirements, the maximum fuel reduction available is the contingency fuel (3% or 5% of trip fuel) between Departure and Decision Point. The success of a Decision Point Procedure will depend on whether unforeseen events, such as not being cleared to the optimum cruise level or avoidance of weather, have caused the contingency fuel allowance to be used.",
    "faithfulness": 0.0,
    "top_chunk_citations": [
      "7-Flight-Planning-and-Monitoring-2014.pdf | page 42",
      "7-Flight-Planning-and-Monitoring-2014.pdf | page 42",
      "7-Flight-Planning-and-Monitoring-2014.pdf | page 286"
    ],
    "explanation": "Answer is weakly supported by retrieved text; likely missing exact sentence match."
  },
  {
    "question": "Given a flight to an isolated aerodrome, what additional fuel requirement is described for turbine aircraft?",
    "answer": "If an engine fails or the pressurization is lost at the most critical point, the aircraft to descend as necessary and proceed to an adequate alternate aerodrome and hold at 1500 ft for 15 minutes above the aerodrome elevation in ISA conditions except that this additional fuel is not required if adequate basic trip, contingency, alternate specifies that the fuel must include: • Taxi fuel • Trip fuel • Contingency fuel • Additional fuel if required but not less than: • For aeroplanes with reciprocating engines, fuel to fly for 45 minutes plus 15% of the flight time planned to be spent at cruising level, or two hours, whichever is less. ETOPS - Fuel Policy Pre-flight An operator shall ensure that the pre-flight calculation of usable fuel required for a flight includes: • Taxi fuel • Trip fuel • Reserve fuel consisting of: • Contingency • Alternate fuel, if a destination alternate is required • Final reserve fuel (for aeroplanes with turbine power units, fuel to fly for 30 minutes at holding speed at 1500 ft (450 m) above aerodrome elevation in standard conditions), and, • Additional fuel, if required by the type of operation (e.g. • Final reserve fuel (for aeroplanes with turbine power units, fuel to fly for 30 minutes at holding speed at 1500 ft (450 m) above aerodrome elevation in standard conditions), and • Additional fuel, if required by the type of operation (e.g.",
    "faithfulness": 0.0,
    "top_chunk_citations": [
      "7-Flight-Planning-and-Monitoring-2014.pdf | page 43",
      "7-Flight-Planning-and-Monitoring-2014.pdf | page 32",
      "7-Flight-Planning-and-Monitoring-2014.pdf | page 43"
    ],
    "explanation": "Answer is weakly supported by retrieved text; likely missing exact sentence match."
  },
  {
    "question": "If the ADC on one side fails, what arrangements can allow the captain's instruments to be fed from the other side?",
    "answer": "In some aircraft the ADS is designed so that the outputs from each computer are not directed exclusively to instruments on one side of the panel. When the pressure acting on one side of a paddle is greater than the pressure on the other side, the paddle and probe rotate until the pressures are equal. Two sets of slots in the probe allow pressure variations, caused by changes in airstream direction, to be transmitted through separate air passages to opposite sides of a paddle chamber.",
    "faithfulness": 0.0,
    "top_chunk_citations": [
      "Instruments.pdf | page 105",
      "Instruments.pdf | page 104",
      "Instruments.pdf | page 451"
    ],
    "explanation": "Answer is weakly supported by retrieved text; likely missing exact sentence match."
  },
  {
    "question": "In the ISA deviation calculation, how is deviation computed from actual and ISA temperature?",
    "answer": "To simplify the calculation use the formula: true altitude = indicated altitude + (indicated altitude/1000 × ISA deviation × 4) + 27(actual pressure - pressure setting) correct QNH is set, the indicated error differs from the true altitude by temperature error. Now to find the deviation from ISA we subtract the ISA temperature from the actual temperature: ISA Deviation = actual temperature - ISA temperature So if the actual temperature at 18 000 ft is -27°C, then the deviation is: ISA Deviation = -27 - (-21) = -6° So if the actual temperature at 18 000 ft is -27°C, then the deviation is: ISA Deviation = -27 - (-21) = -6° For the temperatures below, calculate the ISA deviations: Height (ft) Temperature (°C) ISA Temperature ISA Deviation 1500 +28 17 500 -18 24 000 -35 37 000 -45 9500 -5 5000 +15 31 000 -50 57 000 -67 If the limiting deviation for your aircraft at an airfield 5000 ft AMSL is ISA +10, what is the maximum temp at which you can operate? To do this we firstly need to determine what the ISA temperature is at a specified altitude, then calculate the deviation from the ISA.",
    "faithfulness": 0.0,
    "top_chunk_citations": [
      "Meteorology full book.pdf | page 14",
      "Meteorology full book.pdf | page 14",
      "Meteorology full book.pdf | page 138"
    ],
    "explanation": "Answer is weakly supported by retrieved text; likely missing exact sentence match."
  },
  {
    "question": "What does RNAV stand for in the context of navigation systems?",
    "answer": "• Indicator in the form of a: ◦ Course Deviation Indicator (CDI) or ◦ Horizontal Situation Indicator (HSI) RTN RAD CHK DATA Figure 13.1 VOR/DME RNAV Integrated Nav SystemFigure 16.1 VOR/DME RNAV Integrated Nav System 16 263 Area Navigation Systems (RNAV) 16 Area Navigation Systems (RNAV) Operation of a Simple 2D RNAV System A simple RNAV system uses rho/theta (range/bearing) to define position, which is derived from range and bearing information from VOR/DME stations. one which enables the aircraft to navigate on any desired flight path within the coverage of appropriate ground based navigation aids only Area Navigation Systems (RNAV) 16 268 16Area Navigation Systems (RNAV) The 737-800 FMS The 737-800 FMS comprises: • Flight Management Computer System (FMCS) • Autopilot/Flight Director System (AFDS) • Autothrottle (A/T) • 2 Inertial Reference Systems (IRS) Each component is an independent system which may be used individually or in various combinations. Benefits of RNAV RNAV allows aircraft to take a more direct flight path appropriate to the route they are Area Navigation Systems (RNAV) 16 260 16Area Navigation Systems (RNAV) Area Navigation Systems (RNAV) 16 262 16Area Navigation Systems (RNAV) There are three levels of RNAV capability: • 2D RNAV which relates to the capabilities in the horizontal plane only.",
    "faithfulness": 0.0,
    "top_chunk_citations": [
      "11-radio-navigation-2014.pdf | page 267",
      "11-radio-navigation-2014.pdf | page 266",
      "11-radio-navigation-2014.pdf | page 268"
    ],
    "explanation": "Answer is weakly supported by retrieved text; likely missing exact sentence match."
  }
]
```

## Per-question comparison
| # | Question | L1 refused | L1 hit | L1 faith | L1 halluc | L2 refused | L2 hit | L2 faith | L2 halluc |
|---:|---|---:|---:|---:|---:|---:|---:|---:|---:|
| 1 | What is the definition of meteorology? | False | False | 0.0 | 1.0 | False | False | 0.333 | 0.667 |
| 2 | What is the definition of the atmosphere? | False | False | 0.0 | 1.0 | True | False | 1.0 | 0.0 |
| 3 | What is the approximate composition of dry air by volume in the troposphere? | False | False | 0.333 | 0.667 | False | False | 0.333 | 0.667 |
| 4 | In the ISA, what is the sea level standard temperature? | False | False | 0.0 | 1.0 | False | False | 0.0 | 1.0 |
| 5 | In the ISA, what is the sea level standard pressure in hPa? | False | False | 0.333 | 0.667 | False | False | 0.0 | 1.0 |
| 6 | In the ISA, what is the standard lapse rate below 11 km? | False | False | 0.333 | 0.667 | True | False | 1.0 | 0.0 |
| 7 | What does the tropopause mark in terms of temperature change with height? | False | False | 0.333 | 0.667 | False | False | 0.333 | 0.667 |
| 8 | What are two reasons for studying meteorology for aviation? | False | False | 0.333 | 0.667 | False | False | 0.333 | 0.667 |
| 9 | What is the role of the Air Data Computer (ADC) in an aircraft? | False | False | 0.0 | 1.0 | False | False | 0.0 | 1.0 |
| 10 | What are the two ADC system types mentioned and how do they differ at a high level? | False | True | 0.667 | 0.333 | True | False | 1.0 | 0.0 |
| 11 | In FMC initialization, what is checked or input on the IDENT and POS INIT pages? | False | False | 0.0 | 1.0 | False | False | 0.0 | 1.0 |
| 12 | What is the purpose of the CDU scratchpad in an FMC? | False | False | 0.0 | 1.0 | False | False | 0.0 | 1.0 |
| 13 | What does the term 'Decision Point Procedure' relate to in fuel policy? | False | False | 0.0 | 1.0 | False | False | 0.333 | 0.667 |
| 14 | How is an 'Isolated aerodrome' defined in fuel planning context? | False | False | 0.333 | 0.667 | False | False | 0.333 | 0.667 |
| 15 | What is the difference between a QDR and a QDM in VOR terminology? | False | False | 0.333 | 0.667 | False | False | 0.333 | 0.667 |
| 16 | What does RNAV stand for in the context of navigation systems? | False | False | 0.0 | 1.0 | False | False | 0.0 | 1.0 |
| 17 | In the ISA deviation calculation, how is deviation computed from actual and ISA temperature? | False | False | 0.333 | 0.667 | False | False | 0.0 | 1.0 |
| 18 | What does the document say about ozone hazards at high altitude? | False | False | 0.0 | 1.0 | True | False | 1.0 | 0.0 |
| 19 | What does system redundancy mean in the air data system context? | False | False | 0.0 | 1.0 | True | False | 1.0 | 0.0 |
| 20 | What does the document describe as the main purpose of flight planning? | False | False | 0.333 | 0.667 | True | False | 1.0 | 0.0 |
| 21 | If an outside air temperature of -30°C is measured at FL200, what is the ISA temperature deviation? | False | False | 0.0 | 1.0 | False | True | 0.667 | 0.333 |
| 22 | If the tropopause is reported at FL330, what can you infer about significant cloud tops relative to it? | False | False | 0.333 | 0.667 | True | False | 1.0 | 0.0 |
| 23 | If the ADC on one side fails, what arrangements can allow the captain's instruments to be fed from the other side? | False | False | 0.0 | 1.0 | False | False | 0.0 | 1.0 |
| 24 | During FMC pre-flight initialization, what sequence of pages would you expect to use after IDENT? | False | False | 0.0 | 1.0 | True | False | 1.0 | 0.0 |
| 25 | If the navigation database is out of date, what action is described to activate the next cycle? | False | False | 0.0 | 1.0 | True | False | 1.0 | 0.0 |
| 26 | Given a flight to an isolated aerodrome, what additional fuel requirement is described for turbine aircraft? | False | False | 0.0 | 1.0 | False | False | 0.0 | 1.0 |
| 27 | In decision point procedure planning, what does contingency fuel between departure and decision point enable? | False | False | 0.0 | 1.0 | False | False | 0.0 | 1.0 |
| 28 | If asked for the common emergency VHF frequency, how would you answer using only the document text? | False | False | 0.333 | 0.667 | True | False | 1.0 | 0.0 |
| 29 | If a question is not supported by any retrieved chunk, what exact refusal must your system return? | False | False | 0.0 | 1.0 | True | False | 1.0 | 0.0 |
| 30 | If BM25 returns many candidates but vector retrieval returns few, how can hybrid retrieval help? | False | False | 0.0 | 1.0 | True | False | 1.0 | 0.0 |
| 31 | Why might chunk overlap reduce retrieval misses in dense technical text? | False | True | 1.0 | 0.0 | True | False | 1.0 | 0.0 |
| 32 | How would you cite an answer when you only have chunk metadata for source and page? | False | False | 0.0 | 1.0 | True | False | 1.0 | 0.0 |
| 33 | How would you decide to refuse answering when retrieval confidence is low? | False | False | 0.0 | 1.0 | True | False | 1.0 | 0.0 |
| 34 | If a user asks about something outside aviation docs, how should the assistant respond? | False | False | 0.0 | 1.0 | True | False | 1.0 | 0.0 |
| 35 | How would you debug a wrong answer: what retrieved chunks would you inspect first? | False | False | 0.0 | 1.0 | True | False | 1.0 | 0.0 |
| 36 | If vector similarity is high but the chunk is off-topic, how does a cross-encoder reranker help? | False | True | 0.5 | 0.5 | True | False | 1.0 | 0.0 |
| 37 | If you must show top 3 chunks in debug mode, what fields would you include in the response? | False | False | 0.0 | 1.0 | True | False | 1.0 | 0.0 |
| 38 | If a user asks for a multi-step explanation, how can you keep it grounded in retrieved text? | False | True | 1.0 | 0.0 | True | False | 1.0 | 0.0 |
| 39 | If you use FAISS with normalized embeddings and inner product, what similarity measure does it approximate? | False | False | 0.0 | 1.0 | True | False | 1.0 | 0.0 |
| 40 | If pages are 0-indexed by the loader, how do you show human-friendly page numbers in citations? | False | False | 0.0 | 1.0 | True | False | 1.0 | 0.0 |
| 41 | Compare vector-only retrieval vs hybrid retrieval: why can hybrid improve recall for rare acronyms and numbers? | False | False | 0.0 | 1.0 | True | False | 1.0 | 0.0 |
| 42 | Describe a failure mode where BM25 helps but reranking is still necessary. | False | True | 0.667 | 0.333 | True | False | 1.0 | 0.0 |
| 43 | When could a high rerank score still lead to a wrong answer, and how would you mitigate it? | False | False | 0.0 | 1.0 | True | False | 1.0 | 0.0 |
| 44 | Explain how you would measure retrieval hit-rate without manual labeling, and what are its limitations. | False | False | 0.0 | 1.0 | True | False | 1.0 | 0.0 |
| 45 | Propose a confidence thresholding approach using reranker scores and how it triggers refusal. | False | False | 0.0 | 1.0 | True | False | 1.0 | 0.0 |
| 46 | Explain how chunk size affects citations quality and answer completeness in a textbook PDF. | False | False | 0.0 | 1.0 | True | False | 1.0 | 0.0 |
| 47 | If two chunks disagree, how would you craft an answer that stays faithful and notes the condition? | False | False | 0.333 | 0.667 | True | False | 1.0 | 0.0 |
| 48 | How would you extend the system to handle follow-up questions while keeping grounding strict? | False | False | 0.0 | 1.0 | True | False | 1.0 | 0.0 |
| 49 | Explain why showing retrieved chunks in debug mode helps prevent hallucinations during development. | False | False | 0.0 | 1.0 | True | False | 1.0 | 0.0 |
| 50 | Explain how you would generate and curate a 50-question set to cover factual, applied, and reasoning skills. | False | False | 0.0 | 1.0 | True | False | 1.0 | 0.0 |