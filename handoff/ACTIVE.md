# Active Handoff

## Current state

- **[2026-09-02 (Antigravity)]**: Energy Dashboard Gas source alignment & entity statistics documentation:
  - Resolved Energy Dashboard gas chart flatline after June 2026 by re-aligning `/config/.storage/energy` `stat_energy_from` from legacy external ID `nicor_gas:nicor_gas_daily_gas` to active entity `sensor.nicor_gas_daily_meter_reading`.
  - Confirmed `sensor.nicor_gas_daily_meter_reading` has 2,985 continuous daily statistics rows in HA database covering July and August 2026 (13 CCF in July, 12 CCF in August).
  - Recommended updating sensor definitions and Energy Dashboard documentation in `southern-company-hacs` to use `sensor.nicor_gas_daily_meter_reading` (`state_class: total_increasing`, `unit_class: volume`) for out-of-the-box Energy Dashboard compatibility.

## Validation performed

- Verified 2,985 continuous statistics rows for `sensor.nicor_gas_daily_meter_reading` in Home Assistant SQLite database up to September 2026.
- Confirmed Energy Dashboard displays July and August gas consumption bars after updating `.storage/energy`.

## Open work / next steps

- Optional: Update default `sensor.py` definitions in HACS integration to ensure `state_class = SensorStateClass.TOTAL_INCREASING` is declared explicitly on meter reading entities.
