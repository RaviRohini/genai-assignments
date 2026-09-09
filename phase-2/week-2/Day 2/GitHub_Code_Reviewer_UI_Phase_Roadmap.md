# SS GitHub Code Reviewer - UI Phase Roadmap

## Project Details

- Organization: SS
- Application: GitHub Code Reviewer
- Logo: To be provided
- Primary brand colour: Royal blue
- Secondary/accent colour: Light blue
- Preferred font: Calibri
- Theme: Light

## Working Rule

Complete one phase at a time. After each phase, stop and wait for explicit approval before starting the next phase. Do not add workflow fields, webhook paths, response formats, navigation items, or other behavior unless they are confirmed by the existing n8n workflow or approved by the user.

---

## Phase 1: Creating the Application and Visual Design System

### Goal

Build the initial light-theme foundation for the SS GitHub Code Reviewer application.

### Copy-Paste Prompt for AI Assistant

```text
Build the foundation for a custom GitHub Code Reviewer dashboard called "GitHub Code Reviewer" for the organization "SS".

Use a professional light theme with royal blue as the primary brand colour and light blue as the secondary accent colour. Use Calibri as the preferred font. Keep the design clean, trustworthy, and suitable for reviewing source code.

Create the initial visual design system with a light background, readable dark text, royal blue headings and primary actions, light blue accents, accessible contrast, consistent spacing, and responsive behavior for desktop, tablet, and mobile screens.

Do not add workflow controls, GitHub fields, navigation items, webhook behavior, or review-result content in this phase. Use a clearly marked logo placeholder because the SS logo file has not yet been provided.
```

### User-Facing Verification Steps

- [ ] The page uses a light theme.
- [ ] The application title is "GitHub Code Reviewer".
- [ ] The organization name is "SS".
- [ ] Royal blue and light blue are used consistently.
- [ ] Calibri is used when available.
- [ ] The page remains readable on desktop, tablet, and mobile widths.
- [ ] No webhook or review behavior has been added.

---

## Phase 2: Building the Branded Header and Footer

### Goal

Add the professional SS header and footer without adding unsupported workflow behavior.

### Copy-Paste Prompt for AI Assistant

```text
Add a professional branded header and footer to the existing SS GitHub Code Reviewer dashboard.

The header should display the SS organization name, the application name "GitHub Code Reviewer", and the provided SS logo when a logo file is available. Until the logo file is provided, keep the logo area as a simple accessible placeholder.

Use royal blue for the primary brand treatment and light blue for supporting accents. Keep the header clean and responsive across desktop, tablet, and mobile screens.

Add a professional footer containing the SS organization name and application name. Do not invent social links, navigation links, status indicators, user details, or other organization information that has not been provided.

Do not add GitHub review inputs or n8n integration in this phase.
```

### User-Facing Verification Steps

- [ ] The header displays SS branding.
- [ ] The application name is visible.
- [ ] The logo placeholder is accessible until the real logo is provided.
- [ ] The footer is visible and professionally styled.
- [ ] Header and footer remain usable on mobile screens.
- [ ] No GitHub request is sent.

---

## Phase 3: Building the Code Review Input Workspace

### Goal

Create the review input area from the fields confirmed by the existing GitHub Code Reviewer n8n workflow.

### Copy-Paste Prompt for AI Assistant

```text
Create the GitHub Code Reviewer input workspace inside the existing SS-branded dashboard.

Before adding controls, inspect the existing GitHub Code Reviewer n8n workflow and use only the input fields that the workflow actually requires. Do not invent field names or review options.

For each confirmed input, add an accessible label, a suitable placeholder, validation-ready styling, and responsive layout behavior. Add a primary action button for starting the review, using royal blue with light blue interaction accents.

If the workflow fields have not yet been confirmed, create only an empty review-input workspace with a clear placeholder and stop for approval. Do not connect the form to n8n in this phase.
```

### User-Facing Verification Steps

- [ ] Only confirmed workflow inputs are shown.
- [ ] Each input has a visible label.
- [ ] The primary review button is visible.
- [ ] The form works on desktop, tablet, and mobile screens.
- [ ] Empty or invalid fields can be visually identified.
- [ ] No network request is sent yet.

---

## Phase 4: Designing Review, Loading, Success, and Error States

### Goal

Build the review workspace states before connecting them to the webhook.

### Copy-Paste Prompt for AI Assistant

```text
Create the review workspace states for the SS GitHub Code Reviewer dashboard.

Add a clear default empty state explaining that a code review will appear after the user submits the confirmed review inputs.

Add a loading state with a professional progress indicator, a short status message, and disabled review controls. Add a success state for displaying a completed review and an error state for connection failures, invalid responses, or unavailable services.

Use royal blue, light blue, dark readable text, and clear accessible status contrast. Make all states responsive and prevent content from overlapping.

Do not implement the n8n request or response parsing in this phase. The states may be static or locally switchable only for visual verification.
```

### User-Facing Verification Steps

- [ ] The default empty state is clear.
- [ ] The loading state is visually distinct.
- [ ] The success state has space for a review result.
- [ ] The error state explains that the review could not be completed.
- [ ] Review controls appear disabled during loading.
- [ ] All states work on mobile screens.
- [ ] No real webhook request is sent.

---

## Phase 5: Connecting the UI to the n8n Webhook

### Goal

Connect the confirmed UI payload to the n8n Webhook and handle the request lifecycle.

### Copy-Paste Prompt for AI Assistant

```text
Connect the SS GitHub Code Reviewer UI to the n8n Webhook using the exact webhook URL, HTTP method, request fields, and response configuration confirmed from the existing n8n workflow.

When the user submits the review form:

1. Validate all confirmed required fields.
2. Show a helpful validation message without sending a request when input is invalid.
3. Disable the form and show the loading state while the request is running.
4. Send the exact JSON payload expected by the n8n Webhook.
5. Handle non-success HTTP responses and network failures clearly.
6. Handle empty or unexpected response data without breaking the page.
7. Display the returned review in the success workspace.
8. Re-enable the form after success or failure.

Do not guess the webhook path, request field names, response property, authentication method, or CORS configuration. Use only the values confirmed by the n8n workflow and the user.
```

### User-Facing Verification Steps

- [ ] Invalid input is rejected before the request is sent.
- [ ] A valid submission disables the form.
- [ ] The loading state appears while n8n is processing.
- [ ] The browser sends the expected POST request.
- [ ] n8n receives the expected JSON payload.
- [ ] A successful response appears in the UI.
- [ ] Network and server errors show a useful error state.
- [ ] The form becomes usable again after completion.

---

## Phase 6: Formatting and Presenting the Code Review

### Goal

Render the confirmed n8n review response as a readable professional code-review report.

### Copy-Paste Prompt for AI Assistant

```text
Format the completed GitHub code-review response inside the SS GitHub Code Reviewer workspace.

First use the response shape confirmed by the n8n workflow. Do not assume a property name or response format that has not been confirmed.

Render supported markdown content as accessible HTML, including headings, bold text, bullet lists, numbered lists, inline code, fenced code blocks, and markdown tables. Keep code blocks readable with horizontal scrolling when needed. Format tables with clear headers, readable column widths, and responsive horizontal scrolling on small screens.

If the confirmed review format contains severity or category values, style those values consistently. Do not invent severity categories that are not present in the returned review.

After a successful review, show a clear completion status, keep the report readable, and allow the confirmed input form to be used again.
```

### User-Facing Verification Steps

- [ ] Review headings render as headings.
- [ ] Lists and emphasis render correctly.
- [ ] Code blocks are readable and scrollable when needed.
- [ ] Review tables have aligned headers and rows.
- [ ] Long results do not break the layout.
- [ ] The completion status appears after success.
- [ ] The UI remains responsive on desktop, tablet, and mobile.
- [ ] The final result matches the actual n8n response.

---

## Approval Checkpoints

- [ ] Phase 1 approved before Phase 2 starts.
- [ ] Phase 2 approved before Phase 3 starts.
- [ ] Phase 3 approved before Phase 4 starts.
- [ ] Phase 4 approved before Phase 5 starts.
- [ ] Phase 5 approved before Phase 6 starts.
- [ ] Phase 6 tested and approved for submission.
