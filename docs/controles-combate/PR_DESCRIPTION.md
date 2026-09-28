## What changed?
- Read the saved control scale through `SettingsRepository` in the Android combat entry point and pass it to `StreetFighterScreenCommon`.
- Scale the joystick, action buttons, L/R buttons, spacing, and joystick tutorial hint position.
- Clamp the control scale to 0.6–1.4 and keep 1.0 as the default for callers that do not provide it.

## Why?
The control size setting affected Open World mode, but combat controls used fixed dimensions. This change makes “Titulación por combate” on Android respect the same saved preference.

## QA evidence
Manual testing reported by the contributor on a Samsung Galaxy S22 Ultra (Android version not recorded):
- Compared combat controls at 60% and 100%.
- Confirmed joystick and button responsiveness at both sizes.
- Confirmed the saved size persists after restarting the app.
- No overlapping or clipped buttons were observed in these scenarios.

Both screenshots show the modified version with different settings, not before/after versions.

### 60% control size
![Combat controls at 60%](https://raw.githubusercontent.com/Alexis177/PolitecnicoOpenWorld/fix/tamano-controles-combate/docs/controles-combate/capturas/02-combate-60.png)

### 100% control size
![Combat controls at 100%](https://raw.githubusercontent.com/Alexis177/PolitecnicoOpenWorld/fix/tamano-controles-combate/docs/controles-combate/capturas/04-combate-100.png)

No automated tests were added. Testing at 140%, other screen sizes, the P button, tutorial hint placement, and Open World regression testing are not documented.

## Risk/rollback
Scaling controls changes their layout and touch target sizes. Untested screen sizes or larger scales may cause overlap or clipping; smaller scales reduce touch target sizes. Non-Android callers retain the default scale unless they provide a value.

To roll back the implementation, revert commit `5cd5883e864f95c61156a3fd5ea497218b1c9a56`. The existing saved preference does not require a migration.
