# Automated Test Scenarios

## TC-API-001 — Health check

**Request:** `GET /ping`  
**Expected:** HTTP `201`.

## TC-API-002 — Create authentication token

**Request:** `POST /auth` with valid demo credentials.  
**Expected:** HTTP `200`; response contains `token`; token is saved to the environment.

## TC-API-003 — Get booking IDs

**Request:** `GET /booking`  
**Expected:** HTTP `200`; response is an array; array contains booking IDs.

## TC-API-004 — Create booking

**Request:** `POST /booking`  
**Expected:** HTTP `200`; response contains `bookingid`; created booking values match request data; `bookingId` is saved to the environment.

## TC-API-005 — Verify created booking

**Request:** `GET /booking/{{bookingId}}`  
**Expected:** HTTP `200`; booking data matches the initial create request.

## TC-API-006 — Full booking update

**Request:** `PUT /booking/{{bookingId}}`  
**Expected:** HTTP `200`; full booking response contains updated price, dates, and additional needs.

## TC-API-007 — Verify full update

**Request:** `GET /booking/{{bookingId}}`  
**Expected:** HTTP `200`; persisted booking data matches the PUT request.

## TC-API-008 — Partial booking update

**Request:** `PATCH /booking/{{bookingId}}`  
**Expected:** HTTP `200`; only selected fields are changed (`lastname`, `totalprice`).

## TC-API-009 — Verify partial update

**Request:** `GET /booking/{{bookingId}}`  
**Expected:** HTTP `200`; patched fields contain new values.

## TC-API-010 — Delete booking

**Request:** `DELETE /booking/{{bookingId}}`  
**Expected:** HTTP `201`.

## TC-API-011 — Verify booking deletion

**Request:** `GET /booking/{{bookingId}}`  
**Expected:** HTTP `404`; the deleted booking is no longer available.
