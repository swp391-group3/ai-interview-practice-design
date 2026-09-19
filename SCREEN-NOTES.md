# RoleCue Batch 1 screen notes

## Marketing / Landing / Desktop / 1440

Path:
screens/shared/marketing/landing-desktop-1440.png

Classification:
MARKETING SCREEN

Purpose:
Introduce RoleCue as a calm, role-specific technical interview preparation product and make the first practice path legible.

Primary action:
Start a practice.

Important information:
The reviewed-role premise, structured practice value, and a framed sample blueprint proof object.

Navigation:
Public entry point with sign-in, approach, pricing, and practice entry routes.

UX constraints:
The visual uses source-system construction geometry and scarce lime markers; the blueprint is illustrative role context, not live candidate data.

## Marketing / Landing / Mobile / 390

Path:
screens/shared/marketing/landing-mobile-390.png

Classification:
MARKETING SCREEN

Purpose:
Preserve the public story and single practice conversion on a narrow mobile composition.

Primary action:
Start a practice.

Important information:
The reviewed-role premise, compact evidence tags, and a readable blueprint stage.

Navigation:
Mobile public entry with direct practice and sign-in routes.

UX constraints:
Content remains single-column with no horizontal dependency; the proof object is simplified without losing its framed role-context meaning.

## Marketing / Pricing / Desktop

Path:
screens/shared/marketing/pricing-desktop.png

Classification:
MARKETING SCREEN

Purpose:
Explain credits without presenting unapproved package values as live pricing.

Primary action:
Start practicing.

Important information:
Credit use visibility, account usage history, and package options explicitly marked as price-pending design placeholders.

Navigation:
Public pricing route with return to sign-in or practice entry.

UX constraints:
No invented price, package amount, gateway, or payment promise is shown.

## Marketing / Pricing / Mobile

Path:
screens/shared/marketing/pricing-mobile.png

Classification:
MARKETING SCREEN

Purpose:
Provide a compact credits explanation for the mobile public route.

Primary action:
Start practicing.

Important information:
Pending package options and the promise that balance is visible before an interview begins.

Navigation:
Mobile public pricing route with sign-in access.

UX constraints:
The design does not imply approved pricing or payments on mobile.

## Auth / Login / Desktop

Path:
screens/shared/auth/login-desktop.png

Classification:
TOP-LEVEL SCREEN

Purpose:
Let a returning candidate access their preparation space.

Primary action:
Sign in.

Important information:
Email and password controls, focused input, visible validation treatment, password recovery, and account creation route.

Navigation:
Entry from public navigation; successful authentication resolves to the appropriate role workspace.

UX constraints:
No social login is introduced. Inputs remain technical rectangles and validation is explicit rather than color-only.

## Auth / Login / Mobile

Path:
screens/shared/auth/login-mobile.png

Classification:
SUPPORTING UX STATE

Purpose:
Provide the responsive 390 px login composition.

Primary action:
Sign in.

Important information:
Focused email input, password validation, recovery, and registration route.

Navigation:
Mobile public entry to authentication, then role-aware workspace routing after success.

UX constraints:
The form remains single-column and complete without a desktop narrative rail.

## Auth / Register / Desktop

Path:
screens/shared/auth/register-desktop.png

Classification:
TOP-LEVEL SCREEN

Purpose:
Create a candidate account before the job description journey starts.

Primary action:
Create account.

Important information:
Identity fields, email, password, and existing-account sign-in route.

Navigation:
Entry from public landing or login; continues to verification when required by the authentication process.

UX constraints:
No social provider or unsupported account choice is implied.

## Auth / Register / Mobile

Path:
screens/shared/auth/register-mobile.png

Classification:
SUPPORTING UX STATE

Purpose:
Provide a narrow responsive registration path.

Primary action:
Create account.

Important information:
Candidate name, email, password, and return to sign-in.

Navigation:
Mobile public entry to registration, then email verification if required.

UX constraints:
Fields are vertically ordered and retain direct labels and 44 px or greater action sizing.

## Auth / Forgot Password

Path:
screens/shared/auth/forgot-password.png

Classification:
TOP-LEVEL SCREEN

Purpose:
Request a password reset link without distracting from the candidate’s practice task.

Primary action:
Send reset link.

Important information:
Email input, recovery explanation, and return to sign-in.

Navigation:
Entered from login; progresses to the reset-password route after the account email receives the link.

UX constraints:
The screen never reveals whether an account exists for a submitted address.

## Auth / Reset Password

Path:
screens/shared/auth/reset-password.png

Classification:
TOP-LEVEL SCREEN

Purpose:
Let a verified recovery link set a new password.

Primary action:
Save new password.

Important information:
New password, confirmation input, and visible mismatch validation.

Navigation:
Entered from the password-reset link; returns to sign-in after successful completion.

UX constraints:
Validation states are explicit and the screen does not expose token or implementation details.

## Auth / Verify Email

Path:
screens/shared/auth/verify-email.png

Classification:
PROCESS STATE

Purpose:
Explain the awaiting-verification state and provide a controlled resend action.

Primary action:
Resend verification link.

Important information:
Verification is pending, the account email is the target, and a resend is available.

Navigation:
Entered after registration; progresses to the confirmed state when verification succeeds.

UX constraints:
The process state is calm and does not make unsupported delivery guarantees.

## Auth / Email Verified

Path:
screens/shared/auth/email-verified.png

Classification:
PROCESS STATE

Purpose:
Confirm that account verification is complete and route the candidate into their workspace.

Primary action:
Continue to dashboard.

Important information:
Clear successful verification status and the next safe route.

Navigation:
Entered from verification completion; exits to the Candidate Dashboard for candidate accounts.

UX constraints:
Success combines an icon, label, and copy rather than relying on lime alone.

## Candidate Shell / Desktop 1440

Path:
screens/candidate/shell-desktop-1440.png

Classification:
TOP-LEVEL SCREEN

Purpose:
Establish the persistent desktop Candidate Workspace frame for later candidate routes.

Primary action:
Navigate to the current preparation task.

Important information:
Stable primary navigation, page-title location, credit context, and account route.

Navigation:
Applies across Candidate Dashboard, new-practice, history, billing, and profile routes.

UX constraints:
Candidate navigation is spacious and low-noise; credit context is present without fabricating a balance.

## Candidate Shell / Laptop 1280

Path:
screens/candidate/shell-laptop-1280.png

Classification:
SUPPORTING UX STATE

Purpose:
Show the compact laptop form of the Candidate Workspace frame.

Primary action:
Navigate using the same candidate route order.

Important information:
Collapsed navigation rail and unchanged page/title/credit hierarchy.

Navigation:
Responsive variation of the Candidate Shell desktop route group.

UX constraints:
The rail condenses without changing navigation order or hiding the active location.

## Candidate / Dashboard

Path:
screens/candidate/dashboard.png

Classification:
TOP-LEVEL SCREEN

Purpose:
Orient a candidate around the next allowed preparation action.

Primary action:
Continue setup.

Important information:
Reviewed sample role context, skill summary, next setup step, and return routes to history, reports, repeat practice, billing, and profile.

Navigation:
Entered after candidate authentication or return from a candidate flow; continues to interview setup.

UX constraints:
The highlighted role data is sample context, not live candidate metrics or scores.

## Dashboard / Empty New User

Path:
screens/candidate/dashboard-empty-new-user.png

Classification:
SUPPORTING UX STATE

Purpose:
Give a new candidate a calm first action when no job description or session exists.

Primary action:
Add a job description.

Important information:
No saved role context, the starting requirement, and the human-review premise.

Navigation:
Entered on the Dashboard for a candidate with no role context; exits to job description entry.

UX constraints:
Absence is not framed as an error and the next action remains singular.

## Dashboard / Returning User

Path:
screens/candidate/dashboard-returning-user.png

Classification:
SUPPORTING UX STATE

Purpose:
Help a returning candidate resume the current preparation route or take a permitted return action.

Primary action:
Resume setup.

Important information:
Reviewed role, current position in the route, report reopening, and repeat-practice availability.

Navigation:
Entered from Candidate Dashboard when a reviewed role is available; exits to setup or eligible history/report routes.

UX constraints:
Secondary return actions never bypass reviewed-role, configuration, or preflight requirements.

## JD / Empty State

Path:
screens/candidate/jd-empty-state.png

Classification:
SUPPORTING UX STATE

Purpose:
Explain why a job description is required before an interview plan can exist.

Primary action:
Add a job description.

Important information:
No role context exists and nothing is generated before it does.

Navigation:
Entered from new-practice when no saved job description is selected; exits to job description entry.

UX constraints:
The state is supportive and does not imply a failed analysis or missing-data error.

## JD / Add Job Description

Path:
screens/candidate/jd-add-job-description.png

Classification:
TOP-LEVEL SCREEN

Purpose:
Collect the source role text or document for analysis.

Primary action:
Analyze role.

Important information:
Labelled job-description text area, document upload option, and explicit pre-analysis expectations.

Navigation:
Entered from Dashboard or JD empty state; exits to the analysis process state.

UX constraints:
The candidate sees that the text is reviewed before it becomes interview input; no score is inferred.

## JD / Analyzing

Path:
screens/candidate/jd-analyzing.png

Classification:
PROCESS STATE

Purpose:
Communicate that the submitted role is being extracted into reviewable context.

Primary action:
Wait for analysis to complete.

Important information:
Analysis is in progress, no fabricated percentage is shown, and no changes are saved yet.

Navigation:
Entered after job-description submission; exits to the analysis result.

UX constraints:
The process state remains quiet and does not imply completion before review.

## JD / Analysis Result

Path:
screens/candidate/jd-analysis-result.png

Classification:
PROCESS STATE

Purpose:
Present extracted role context as a transition into human review.

Primary action:
Review extraction.

Important information:
Sample title, seniority, technical skills, and domain knowledge with a clear human-review requirement.

Navigation:
Entered after analysis; exits to Reviewed Job Description.

UX constraints:
The screen does not invent confidence, relevance, priority, or interview-focus metadata.

## JD / Reviewed Job Description

Path:
screens/candidate/jd-review-and-edit-skills.png

Classification:
SUPPORTING UX STATE

Purpose:
Let the candidate verify and edit extracted role data before it is saved for interview setup.

Primary action:
Save reviewed JD.

Important information:
Title, seniority, technical skills, skill category, required/preferred requirement, technologies, and domain knowledge.

Navigation:
Entered from analysis result; saving exits to Interview Setup / General.

UX constraints:
AI extraction is visibly non-final until review is saved. No unsupported competency metadata is present.

## Interview Setup / General

Path:
screens/candidate/setup-general.png

Classification:
TOP-LEVEL SCREEN

Purpose:
Collect general interview configuration after the reviewed job description is saved.

Primary action:
Generate blueprint.

Important information:
Reviewed role reference, difficulty, duration choice, focus areas, and return to the reviewed JD.

Navigation:
Entered from saved JD review; proceeds to Blueprint Generation or returns to reviewed JD.

UX constraints:
Configuration follows review. Difficulty, duration, and focus remain product-scale choices without fabricated scoring or time claims.

## Interview Setup / Interviewer

Path:
screens/candidate/setup-interviewer.png

Classification:
TOP-LEVEL SCREEN

Purpose:
Choose an interviewer approach as part of the configuration lifecycle.

Primary action:
Continue to blueprint.

Important information:
Curated interviewer selection, selected approach, and voice-selection relationship.

Navigation:
Entered from Interview Setup / General; can open Voice selection before continuing to Blueprint Generation.

UX constraints:
Interviewer choices are role-based practice approaches, not named real people or unsupported avatar promises.

## Interview Setup / Voice

Path:
screens/candidate/setup-voice.png

Classification:
SUPPORTING UX STATE

Purpose:
Allow voice choice within the chosen interviewer decision.

Primary action:
Continue to blueprint.

Important information:
Voice delivery choices, selected preview context, and the associated interviewer approach.

Navigation:
Opened from Interview Setup / Interviewer; returns to the same configuration path before blueprint generation.

UX constraints:
Voice choice is scoped to delivery style and does not imply an unsupported voice catalog or preview guarantee.

## Interview Setup / Credits Gate

Path:
screens/candidate/setup-credits-gate.png

Classification:
SUPPORTING UX STATE

Purpose:
Explain that a practice cannot begin without sufficient credits and route transparently to billing options.

Primary action:
View credit options.

Important information:
No credits available, the impact on starting practice, and a return to dashboard.

Navigation:
Appears during setup when credit availability blocks the next allowed transition; exits to billing or dashboard.

UX constraints:
No package price, balance amount, payment gateway, or blame-oriented copy is invented.

## Blueprint / Generation

Path:
screens/candidate/blueprint-generation.png

Classification:
PROCESS STATE

Purpose:
Show the system structuring a practice plan from reviewed role, configuration, and interviewer choices.

Primary action:
Wait for generation to complete.

Important information:
Role-to-blueprint inputs and a clear no-percentage process state.

Navigation:
Entered after valid configuration; exits to Blueprint Preview & Confirmation.

UX constraints:
The process does not imply a countdown, a fabricated question count, or a live interview state.

## Blueprint / Preview & Confirmation

Path:
screens/candidate/blueprint-preview-confirmation.png

Classification:
SUPPORTING UX STATE

Purpose:
Let the candidate confirm the generated interview structure before preflight.

Primary action:
Confirm blueprint.

Important information:
Interview stages, technical domains, question focus, and return to configuration.

Navigation:
Entered after Blueprint Generation; confirmation exits to Preflight.

UX constraints:
This screen occurs after configuration and generation, never as part of JD review. It does not invent unsupported interview functions.

## Preflight / Checking

Path:
screens/candidate/preflight-checking.png

Classification:
PROCESS STATE

Purpose:
Show required capability checks before a candidate enters practice.

Primary action:
Wait for checks to complete.

Important information:
Microphone, audio output, and browser support checks with no false percentage.

Navigation:
Entered after confirmed blueprint; exits to Preflight Ready, Permission Required, or Failed Check.

UX constraints:
The process remains calm and never resembles surveillance or proctoring.

## Preflight / Ready

Path:
screens/candidate/preflight-ready.png

Classification:
TOP-LEVEL SCREEN

Purpose:
Confirm required capabilities before the candidate begins the live practice route.

Primary action:
Begin practice.

Important information:
Required clear checks, optional-status guidance, and confirmed reviewed role and blueprint.

Navigation:
Entered from Preflight Checking; the primary action leads to the Interview Runtime, which is intentionally not produced in Batch 1.

UX constraints:
The visual stops before the live Interview Runtime and does not depict it.

## Preflight / Permission Required

Path:
screens/candidate/preflight-permission-required.png

Classification:
SUPPORTING UX STATE

Purpose:
Guide a candidate through a user-triggered device permission request.

Primary action:
Request permission.

Important information:
Microphone permission requirement, browser Allow guidance, and return to the current check.

Navigation:
Entered from Preflight Checking when permission has not been granted; exits back to checking or ready state.

UX constraints:
Guidance is supportive and never contains proctoring or punitive language.

## Preflight / Failed Check

Path:
screens/candidate/preflight-failed-check.png

Classification:
SUPPORTING UX STATE

Purpose:
Provide clear recovery choices when a required device check cannot complete.

Primary action:
Try check again.

Important information:
The affected microphone check, practical recovery paths, and alternate browser/device suggestion.

Navigation:
Entered from Preflight Checking; retry returns to checking after a candidate changes their device or browser condition.

UX constraints:
No engineering jargon, false session-preservation claim, or blame-oriented language is shown.
