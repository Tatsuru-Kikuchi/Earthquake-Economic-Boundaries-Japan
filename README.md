# Economic Boundaries of Earthquake Impacts in Japan

Analyzing spatial and temporal propagation of economic shocks from earthquakes using boundary detection framework from [Regime-Switch-Dynamics](https://github.com/Tatsuru-Kikuchi/Regime-Swithch-Dynamics).

## Research Questions

1. How far do economic effects extend beyond zones of physical damage?
2. How long does economic recovery take as a function of distance from epicenter?
3. Do supply chain networks amplify spatial propagation?
4. Can we predict economic boundaries from seismic parameters?

## Advantages of Earthquake Natural Experiment

- **Exogenous timing**: Unpredictable occurrence
- **Exogenous location**: Geophysically determined
- **Intensity gradient**: Natural treatment variation with distance
- **Multiple events**: Sufficient variation across time and space
- **Rich data**: JMA seismic data + firm-level economic outcomes

## Data Sources

### Primary Data
1. **Japan Meteorological Agency (気象庁)**
   - Earthquake catalog: magnitude, epicenter, depth, timing
   - Seismic intensity by municipality
   - URL: https://www.data.jma.go.jp/svd/eqdb/data/shindo/

2. **Tokyo Shoko Research (TSR)**
   - Firm bankruptcies by location and date
   - Need to assess data access/cost

3. **EDINET (金融庁)**
   - Listed company financial statements
   - Supplier network disclosures

4. **Statistics Bureau**
   - Regional economic indicators
   - Employment, production data

### Target Earthquakes (2011-2024)

| Date | Location | Magnitude | Max Intensity |
|------|----------|-----------|---------------|
| 2011-03-11 | Tōhoku | 9.0 | 7 |
| 2016-04-14/16 | Kumamoto | 7.3 | 7 |
| 2018-09-06 | Hokkaido | 6.7 | 7 |
| 2024-01-01 | Noto | 7.6 | 7 |

## Methodology

Three-stage boundary detection:
1. **Direct effects**: DiD comparing affected vs unaffected regions
2. **Spatial decay**: Estimate decay rate with distance from epicenter
3. **Temporal recovery**: Estimate recovery half-life

Test theoretical prediction: $d^*/\tau^* \approx \lambda^2/\sqrt{\delta}$

## Project Status

- [x] Repository created
- [ ] Earthquake data downloaded
- [ ] Firm outcome data collected
- [ ] Distance calculations
- [ ] Pilot analysis (Kumamoto 2016)
- [ ] Full estimation
- [ ] Paper draft

## Installation
```bash
git clone https://github.com/Tatsuru-Kikuchi/Earthquake-Economic-Boundaries-Japan.git
cd Earthquake-Economic-Boundaries-Japan
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```
