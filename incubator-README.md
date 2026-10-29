# Smart Infant Incubator Parameter Monitoring System (SIIMPS)

Second-year subject project, B.Tech Biomedical Engineering, Thapar Institute of Engineering & Technology (TIET), Department of Electrical & Instrumentation Engineering. Team of 5. Session Jul-Dec 2024. Supervisors: Dr. Deepti Mittal and Dr. Debasmita Mondal.

**Status: student prototype, documentation only.** The physical prototype is held by the college. The Arduino source code is not included in this repository.
**Not a medical device. Not calibrated, not clinically tested, and not tested on infants.**

## What it is

A low-cost cardboard-enclosure prototype that reads environmental and physiological parameters with an Arduino UNO, shows them on an I2C LCD, and sounds a buzzer alert. It was demonstrated with a doll in a test run. It monitors and alerts. It does not control temperature or humidity.

## Hardware

| Part | Used for |
|---|---|
| Arduino UNO, breadboard | controller and prototyping |
| DHT11 | temperature and humidity |
| DS18B20 | temperature |
| MQ135 | air quality |
| HX711 with 10 kg load cell | weight |
| Pulse Sensor Amped | pulse |
| MAX30102 | heart rate and SpO2 |
| LCD with I2C | display |
| Buzzer | alerts |

## Design targets (from the project poster)

These were design targets, not verified performance.

| Parameter | Target range | Sensor |
|---|---|---|
| Temperature | 35-37.5 C | DS18B20 |
| Humidity | 40-60% RH | DHT11 |
| Air quality | detect CO2 and VOCs | MQ135 |
| Heart rate / SpO2 | 120-160 bpm / above 95% | MAX30102 |

## Recorded test readings

One reading per sensor, taken at the bench. These show the sensors were wired and reading. They are not calibration or validation results.

| Sensor | Reading |
|---|---|
| DHT11 | 82% humidity, 26.2 C |
| DS18B20 | 22.94 C |
| MQ135 | 711.32 (raw, uncalibrated) |
| HX711 | 306.55 (raw, uncalibrated) |
| MAX30102 | 120.68 bpm, SpO2 96% |

Room conditions were outside the incubator design ranges, so these readings do not represent an operating incubator.

## My role

Sensor integration and Arduino programming for most of the sensors. The whole team shared soldering, sensor placement, and building the enclosure (window cut-outs, sliding opening, and a side panel housing the electronics). The team also spoke informally with parents and doctors and made a rough cost estimate (under 1 lakh INR if ever commercialized, an estimate only).
<!-- TODO: add one specific debugging story, e.g. which sensor gave trouble and how you fixed it -->

## Limitations

- Prototype uses breadboard wiring and a cardboard enclosure.
- No calibration against reference instruments.
- Some readings (for example the pulse sensor value) were not valid heart-rate measurements.
- No heater, fan, or feedback control. No remote monitoring module.
- Reference standards considered during design: ISO 13485 and IEEE 2700-2017. The prototype is not certified or compliant with either.

## Files

- `images/`: hardware photos
<!-- TODO: add docs/report.pdf only if the college allows sharing -->
