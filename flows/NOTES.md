# RoleCue Batch 1 flow notes

## System overview

Path:
`flows/00-system-overview.png`

Purpose:
Maps the public entry path through authentication and role resolution, then separates Candidate and Admin workspaces without blending their product responsibilities.

Key relationships:
- Visitor → Login / Register → Authenticate / Resolve Role → Candidate Dashboard or Admin Dashboard.
- Candidate return routes include Dashboard, History, report reopening, repeat practice, Profile, and Subscription / Credits.
- Admin domains are limited to Dashboard, Users, Sessions, Technical Domains, Question Content, Avatars, Voices, Billing, and Settings.

## Candidate lifecycle

Path:
`flows/01-candidate-flow.png`

Purpose:
Establishes the required reviewed-role progression before a live practice can begin.

Primary lifecycle:
Candidate Dashboard → JD Input → AI Analysis → Human Review / Edit → Reviewed JD → Interview Configuration → Blueprint Generation → Blueprint Preview / Confirmation → Preflight → AI Interview → Evaluation → Performance Report.

UX constraints:
- AI extraction is visibly intermediate until human review is complete.
- Blueprint preview and confirmation occur after configuration and generation.
- Entry from repeat practice or a reopened report cannot bypass the reviewed-role, configuration, or preflight requirements.
- The live Interview Runtime is mapped as an endpoint only; it is not a Batch 1 visual deliverable.

## Admin operations

Path:
`flows/02-admin-flow.png`

Purpose:
Defines the bounded operational navigation model from the Admin Dashboard to only the inventory-approved domains.

UX constraints:
- Admin density is operational and text-first, not a copy of Candidate navigation.
- User/session detail, content edit, avatar/voice management, billing transactions, and settings remain scoped to their named inventory domains.
- No extra administration areas, applicant grading workflows, or fabricated operational modules are implied.
