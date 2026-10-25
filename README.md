# ISMNdashboard
An interactive dashboard to view the soil moisture data from the International Soil Moisture Network 

## Branch `screened`: ismn_ref product (sm_qc `s4_export.R`)

```bash
python ismn_dashboard.py --ismn-dir products/ismn_ref_v1 --output ismn_ref_v1_dashboard.html
```

| Panel | Default | Switch "Show raw, removed and filled data" |
|---|---|---|
| Surface (5 cm) | final SM (`sm_qaqc`, black) + soil T 5 cm (`st_qaqc`, right axis) | + raw SM (grey, all exported years), removed days coloured by `sm_flag`, gap-filled days (▲) |
| Root zone | final SM, 0.1·(5\|10) + 0.3·(20\|10\|15) + 0.6·(50\|30\|20 cm) | no change |

x axis 2001-01-01 to 2025-12-31 (`--start-date`, `--end-date`), a line at every 1 January.
Station list: `meta_final.csv` (period, depths, expert review).
