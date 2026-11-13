---
name: log-service
description: Log maintenance in the user's Lisense garage from invoices, receipts or a description of work done. Use when the user shares a service invoice or asks to record a repair, service or MOT for their car.
---

# Log service

1. Find the vehicle with `garage-vehicles`. If it is missing, offer to add it: resolve it with `garage-vehicle-lookup`, then call `garage-add-vehicle` only after the user agrees.
2. For attached files, call `garage-parse-documents` with the actual file bytes. It stores the documents and returns draft jobs. Do not upload the same files again with `garage-upload-document`.
3. For a typed description, draft jobs yourself. Call `garage-categories` to pick valid category names.
4. Show the drafts with dates, mileage, categories and GBP costs. Keep prices, dates and mileage exactly as documented, and use null for unknown costs.
5. Save with `garage-add-jobs` only after the user confirms, preserving each `sourceDocumentId`.
