# [Defect] <Short, specific title>

> Fields marked **\*** are mandatory. A defect must not be filed until every mandatory field is filled in.
> Leave optional fields as `N/A` rather than deleting them, so every report has the same shape.

---

## 1. Summary

| Field | Value |
|---|---|
| **Title \*** | <One line: what is broken, where. e.g. "Checkout button unresponsive after applying promo code"> |
| **Severity \*** | <Blocker / Critical / Major / Minor / Trivial> |
| **Priority** | <P1 / P2 / P3 / P4> |
| **Defect type** | <UI / Backend / UI + Backend / Unknown> |
| **Feature / Module** | <e.g. Checkout, Login, Profile> |
| **Date & time found** | <YYYY-MM-DD HH:MM, with timezone> |
| **Reported by** | <Name> |

### Description \*

<Two or three sentences: what is wrong and what impact it has on the user or the business.>

---

## 2. Environment

| Field | Value |
|---|---|
| **Environment \*** | <Dev / QA / Staging / UAT / Production> |
| **Build \*** | <Build or version number, e.g. 4.12.0 (1532)> |
| **Platform & device** | <e.g. iOS 18.1, iPhone 15 Pro / Android 14, Pixel 8 / Chrome 130, macOS> |
| **Account** | <Test account username or user ID. Never include a password.> |
| **Reproducible in production** | <Yes / No / Not checked> |
| **Reproducible on other platforms** | <Web: Yes/No/Not checked · iOS: Yes/No/Not checked · Android: Yes/No/Not checked> |

---

## 3. Reproduction

### Preconditions

<State required before step 1: logged in, feature flag on, cart has items, specific test data, etc. Write N/A if none.>

### Steps to reproduce \*

1. <Step>
2. <Step>
3. <Step>

### Expected result \*

<What should happen.>

### Actual result \*

<What actually happens. Quote exact error messages.>

### Reproducibility \*

<Successful reproductions / attempts, e.g. 5/5, 3/5, 1/5>

---

## 4. Evidence

| Field | Value |
|---|---|
| **Video / screenshot attached** | <Yes / No; list file names> |
| **Reference links** | <Related tickets, designs, specs, requirement docs> |

### API logs

```
<Request URL, method, status code, request/response body, correlation or trace ID. Mask tokens and personal data.>
```

### Device logs

```
<Console, logcat, or Xcode logs around the time of failure. Mask tokens and personal data.>
```

---

## 5. Additional notes

| Field | Value |
|---|---|
| **Workaround** | <Is there a way for the user to get around it? N/A if none.> |
| **Regression** | <Yes, worked in build X / No / Unknown> |
