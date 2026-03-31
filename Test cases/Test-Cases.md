## Testing Considerations
* Functional testing scenarios defined
* Edge cases identified early
* Reduced ambiguity improved QA coverage
* Supports automation readiness


## Impact
* Reduced developer clarification cycles
* Improved requirement clarity
* Lower risk of defects
* Smoother sprint execution
* Better alignment across team

# Test Cases — Profile Update Feature

## Test Suite Overview
- **Feature:** Profile Update  
- **Precondition:** User is logged in  
- **Environment:** Web Application  

---

## TC_001 — Successful Profile Update

| Field | Details |
|------|--------|
| Test Case ID | TC_001 |
| Scenario | Successful profile update |
| Description | Verify that a user can successfully update profile details with valid input |
| Preconditions | User is logged in |
| Test Steps | 1. Navigate to profile page<br>2. Enter valid name, email, phone<br>3. Click “Save” |
| Test Data | Name: John Doe<br>Email: john@email.com<br>Phone: 0821234567 |
| Expected Result | Profile updates successfully and confirmation message is displayed |
| Priority | High |

---

## TC_002 — Invalid Email Format

| Field | Details |
|------|--------|
| Test Case ID | TC_002 |
| Scenario | Invalid email format |
| Description | Verify system rejects invalid email input |
| Preconditions | User is logged in |
| Test Steps | 1. Navigate to profile page<br>2. Enter invalid email (e.g. "johnemail.com")<br>3. Click “Save” |
| Test Data | Email: johnemail.com |
| Expected Result | Error message displayed: “Invalid email format” and update is prevented |
| Priority | High |

---

## TC_003 — Required Fields Missing

| Field | Details |
|------|--------|
| Test Case ID | TC_003 |
| Scenario | Required fields missing |
| Description | Verify system prevents submission when required fields are empty |
| Preconditions | User is logged in |
| Test Steps | 1. Navigate to profile page<br>2. Clear required fields<br>3. Click “Save” |
| Test Data | Name: "" (empty)<br>Email: "" |
| Expected Result | Validation errors displayed and submission is blocked |
| Priority | High |

---

## TC_004 — System Error Handling

| Field | Details |
|------|--------|
| Test Case ID | TC_004 |
| Scenario | System error |
| Description | Verify system handles backend failure gracefully |
| Preconditions | User is logged in |
| Test Steps | 1. Navigate to profile page<br>2. Enter valid details<br>3. Simulate system failure (e.g. API down)<br>4. Click “Save” |
| Test Data | Valid inputs |
| Expected Result | System displays error message and does not save data |
| Priority | High |

---

## TC_005 — Retry After Validation Error

| Field | Details |
|------|--------|
| Test Case ID | TC_005 |
| Scenario | Retry after validation error |
| Description | Ensure user can correct errors and resubmit successfully |
| Preconditions | User is logged in |
| Test Steps | 1. Enter invalid email<br>2. Click “Save” → error shown<br>3. Correct email<br>4. Click “Save” again |
| Expected Result | Profile updates successfully after correction |
| Priority | Medium |

---

## TC_006 — Field-Level Validation (Phone Number)

| Field | Details |
|------|--------|
| Test Case ID | TC_006 |
| Scenario | Phone number validation |
| Description | Verify phone number format validation |
| Preconditions | User is logged in |
| Test Steps | 1. Enter invalid phone (e.g. letters)<br>2. Click “Save” |
| Test Data | Phone: "abc123" |
| Expected Result | Error message displayed and submission blocked |
| Priority | Medium |

---

## TC_007 — Data Persistence Verification

| Field | Details |
|------|--------|
| Test Case ID | TC_007 |
| Scenario | Data persistence |
| Description | Ensure saved data is retained after refresh |
| Preconditions | User is logged in |
| Test Steps | 1. Update profile successfully<br>2. Refresh page |
| Expected Result | Updated details remain saved |
| Priority | High |

---

## Notes **

Test cases were derived directly from acceptance criteria and BPMN process flows 
to ensure full coverage of validation logic, system behaviour, and error handling scenarios.