# naerm_heat_wave_loads
This repository houses the raw data and processing scripts to create the hourly load time series by 
Balancing Authority based on the 2018 weather year loads. Data are be scaled to match the 2021 total loads data shared 
by Jason Hou on 19-April. The 2018 weather year loads are based on the Total ELectricity Loads (TELL) model.

## Output File
The output of this process is stored in the [data](data/) directory with the filename 
"TELL_Loads_2021_Based_on_2018_Weather.csv".

## Notes
1) Loads in CISO, IPCO, NEVP, and PACE are modeled as a whole in TELL but are separated in GridView. To create the data
for these BAs I used the whole load simulated by TELL and distributed it to the subregions within the BA using the 
annual total load in each subregion to distribute the TELL loads.
2) Three BAs in GridView have zero loads for the year: "TH_Malin", "TH_Mead", and "TH_PV". They are not 
simulated by TELL. I left these in as zero values in the output file.
3) Three BAs in GridView are outside the CONUS and are thus not represented in TELL: AESO, BCHA, and CFE. I left in 
their original 8760-hr load profiles from the 2021 data.

## BAs in the WECC 
>
🟢 = Matched with no issue  
🟡 = Attention needed  
🔴 = No match
>
| GV BA | TELL BA | Matched? | Notes |
| :-: | :-: | :-: | :-: |
| AESO | - | 🔴 | BA is in Canada |
| AVA | AVA | 🟢 | - |
| AZPS | AZPS | 🟢 | - |
| BANC | BANC | 🟢 | - |
| BCHA | - | 🔴 | BA is in Canada |
| BPAT | BPAT | 🟢 | - |
| CFE | - | 🔴 | BA is in Mexico |
| CHPD| CHPD| 🟢 | - |
| CIPB | CISO | 🟡 | Subregion of CISO |
| CIPV | CISO | 🟡 | Subregion of CISO |
| CISC | CISO | 🟡 | Subregion of CISO |
| CISD | CISO | 🟡 | Subregion of CISO |
| DOPD | DOPD | 🟢 | - |
| EPE | EPE | 🟢 | - |
| GCPD | GCPD | 🟢 | - |
| IID | IID | 🟢 | - |
| IPFE | IPCO | 🟡 | Subregion of IPCO |
| IPMV | IPCO | 🟡 | Subregion of IPCO |
| IPTV | IPCO | 🟡 | Subregion of IPCO |
| LDWP | LDWP | 🟢 | - |
| NEVP | NEVP | 🟡 | Subregion of NEVP |
| NWMT | MWMT | 🟢 | - |
| PACW | PACW | 🟢 | - |
| PAID | PACE | 🟡 | Subregion of PACE |
| PAUT | PACE | 🟡 | Subregion of PACE |
| PAWY | PACE | 🟡 | Subregion of PACE |
| PGE | PGE | 🟢 | - |
| PNM | PNM | 🟢 | - |
| PSCO | PSCO | 🟢 | - |
| PSEI | PSEI | 🟢 | - |
| SCL | SCL | 🟢 | - |
| SPCC | NEVP | 🟡 | Subregion of NEVP |
| SRP | SRP | 🟢 | - |
| TEPC | TEPC | 🟢 | - |
| TH Malin | - | 🔴 | No loads |
| TH Mead | - | 🔴 | No loads |
| TH PV | - | 🔴 | No loads |
| TIDC | TIDC | 🟢 | - |
| TPWR | TPWR | 🟢 | - |
| VEA | CISO | 🟡 | Subregion of CISO |
| WACM | WACM | 🟢 | - |
| WALC | WALC | 🟢 | - |
| WAUW | WAUW | 🟢 | - |
