# Postman Collection Runner Result

Latest local automated run during project setup:

- Environment: `Restful Booker`
- Iterations: `1`
- Duration: `12.811 s`
- Average response time: `300 ms`
- Tests: `21`
- Passed: `21`
- Failed: `0`
- Errors: `0`
- Skipped: `0`

## Successful flow

| Step | Request | Status | Result |
|---:|---|---:|---|
| 1 | GET Ping | 201 | PASS |
| 2 | POST Create Token | 200 | PASS |
| 3 | GET Get Booking IDs | 200 | PASS |
| 4 | POST Create Booking | 200 | PASS |
| 5 | GET Get Booking by ID | 200 | PASS |
| 6 | PUT Update Booking | 200 | PASS |
| 7 | GET Get Booking by ID | 200 | PASS |
| 8 | PATCH Partial Update Booking | 200 | PASS |
| 9 | GET Get Booking by ID | 200 | PASS |
| 10 | DELETE Delete Booking | 201 | PASS |
| 11 | GET Get Booking by ID | 404 | PASS — deletion verified |

The final `404 Not Found` is an expected assertion confirming that the created booking was successfully deleted.
