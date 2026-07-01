# Feature Mapping v9

## PIN Recovery

- Forgot PIN button added on the lock screen.
- Recovery code is current 24-hour time in HHmm format.
- User sets a new PIN after recovery code is accepted.

## Activity Pagination

- Activity page now loads a paginated subset instead of rendering all rows.
- Page sizes: 10, 15, 20, 50.
- Prev/Next buttons navigate pages.
- Selected page size persists in settings table.

## Exports

- PDF export uses Android document picker.
- Excel export added as SpreadsheetML `.xls` file.
- User chooses file name and storage location for both.

## Performance

- Screenshot previews are not rendered inline.
- A screenshot button opens the screenshot dialog only when needed.


## v10 fixes

- Removed the aggressive idle-stop condition from the foreground service.
- Screenshot capture delay changed to 3000 ms.
- Added package-to-friendly-name mapping for common apps.
- Timeline now draws all visible segments across multiple lanes.
