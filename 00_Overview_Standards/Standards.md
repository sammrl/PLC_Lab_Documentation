# Drawing & Tagging Standards (v0.1)

## Units & Sheets
- Units: inches (mechanical), AWG (wiring), VDC/VAC (electrical)
- Title block: Project, Volume, Sheet, Rev, Date, Author

## Tag Naming Convention
`{Area}_{DeviceType}_{Function}_{Index}`  
Examples: `PANEL_PB_START_01`, `CELL1_MTR_CONVEYOR_01`, `PANEL_LMP_RUN_01`, `SYS_ESTP_01`

DeviceType hints: `PB` pushbutton, `SW` switch, `MTR` motor, `LMP` pilot light, `SV` solenoid valve, `AI/DI/DO/AO` I/O points.

## Wire & Conductor (placeholder – confirm with lab)
- AC Ungrounded (120 VAC): **Black**  
- AC Neutral: **White**  
- Protective Earth: **Green/Green-Yellow**  
- 24 VDC +: **Blue**   
- 24 VDC – / 0V: **Blue/White** or **Black** (confirmn)

## Layer/Color (schematics)
- Power thick line, control thin line; terminals numbered; wire numbers nearest destination.

## File Conventions
- Drawings: `PLCLAB-02-SCH-###_Title_RevA.pdf`
- CSVs: lowercase headers, commas, UTF-8
