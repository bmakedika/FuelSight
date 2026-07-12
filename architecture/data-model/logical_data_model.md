# Logical Data Model

## Tables de référence

### assets

- asset_id
- asset_code
- asset_type
- location_id

### fuel_operators

- fuel_operator_id
- fuel_operator_name

### receivers

- receiver_id
- receiver_name

### locations

- location_id
- location_name

### movement_types

- movement_type_id
- movement_type_name

---

## Tables opérationnelles

### fuel_transactions

- transaction_id
- transaction_date
- asset_id
- fuel_operator_id
- receiver_id
- movement_type_id
- quantity_liters
- odometer
- hourmeter
- remark

### tank_measurements

- measurement_id
- measurement_date
- location_id
- tank_level_cm
- physical_stock_l
- index_start
- index_end